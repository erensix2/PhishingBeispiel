# PhishingBeispiel

<h2 class="sr-only" style="position:absolute;width:1px;height:1px;overflow:hidden;">Phishing-Demo für Bildungszwecke – zeigt wie gefälschte Login-Seiten funktionieren</h2>

<div style="background: var(--color-background-secondary); border-radius: var(--border-radius-lg); padding: 1.5rem;">

  <div style="background: #c0392b; color: white; font-size: 12px; font-weight: 500; text-align: center; padding: 6px 12px; border-radius: var(--border-radius-md); margin-bottom: 1rem; letter-spacing: 0.03em;">
    ⚠️ BILDUNGSZWECKE – Phishing-Demo - Einführung in Computer Systeme
  </div>

  <div style="background: var(--color-background-primary); border: 0.5px solid var(--color-border-tertiary); border-radius: var(--border-radius-lg); padding: 1.5rem; max-width: 400px; margin: 0 auto;">
    
    <div style="text-align: center; margin-bottom: 1.5rem;">
      <div style="width: 48px; height: 48px; background: #1a73e8; border-radius: 50%; display: flex; align-items: center; justify-content: center; margin: 0 auto 0.75rem;">
        <i class="ti ti-lock" style="font-size: 22px; color: white;" aria-hidden="true"></i>
      </div>
      <p style="font-size: 18px; font-weight: 500; margin: 0; color: var(--color-text-primary);">SparkBank Online</p>
      <p style="font-size: 13px; color: var(--color-text-secondary); margin: 4px 0 0;">Bitte melde dich an</p>
    </div>

    <div style="margin-bottom: 1rem;">
      <label style="font-size: 13px; color: var(--color-text-secondary); display: block; margin-bottom: 4px;">Benutzername</label>
      <input type="text" id="username" placeholder="z.B. max.mustermann" style="width: 100%; box-sizing: border-box;" />
    </div>

    <div style="margin-bottom: 1rem;">
      <label style="font-size: 13px; color: var(--color-text-secondary); display: block; margin-bottom: 4px;">Passwort</label>
      <input type="password" id="password" placeholder="Dein Passwort" style="width: 100%; box-sizing: border-box;" />
    </div>

    <div style="margin-bottom: 1rem;">
      <label style="font-size: 13px; color: var(--color-text-secondary); display: block; margin-bottom: 4px;">TAN / Code</label>
      <input type="text" id="tan" placeholder="z.B. 123456" style="width: 100%; box-sizing: border-box;" />
    </div>

    <button onclick="showData()" style="width: 100%; background: #1a73e8; color: white; border: none; padding: 10px; border-radius: var(--border-radius-md); font-size: 15px; cursor: pointer;">
      Anmelden
    </button>

    <p style="font-size: 12px; color: var(--color-text-secondary); text-align: center; margin: 12px 0 0;">
      <i class="ti ti-shield-check" style="font-size:14px; vertical-align:-2px;" aria-hidden="true"></i> Sichere Verbindung
    </p>
  </div>

  <div id="result-box" style="display: none; margin-top: 1.5rem; background: #fff3cd; border: 2px solid #c0392b; border-radius: var(--border-radius-lg); padding: 1.25rem; max-width: 400px; margin-left: auto; margin-right: auto;">
    <p style="font-weight: 500; color: #c0392b; margin: 0 0 0.75rem; font-size: 15px;">
      <i class="ti ti-alert-triangle" style="font-size:18px; vertical-align:-3px; margin-right:6px;" aria-hidden="true"></i>
      So einfach stehlen Betrüger deine Daten!
    </p>
    <div style="background: var(--color-background-primary); border-radius: var(--border-radius-md); padding: 0.75rem; font-size: 14px;">
      <p style="margin: 0 0 6px; color: var(--color-text-secondary); font-size: 12px; font-weight: 500; text-transform: uppercase; letter-spacing: 0.05em;">Abgefangene Daten:</p>
      <div style="display: grid; gap: 6px;">
        <div style="display: flex; justify-content: space-between; align-items: center;">
          <span style="color: var(--color-text-secondary); font-size: 13px;">Benutzername</span>
          <span id="out-user" style="font-weight: 500; color: #c0392b; font-size: 13px;"></span>
        </div>
        <div style="border-top: 0.5px solid var(--color-border-tertiary);"></div>
        <div style="display: flex; justify-content: space-between; align-items: center;">
          <span style="color: var(--color-text-secondary); font-size: 13px;">Passwort</span>
          <span id="out-pass" style="font-weight: 500; color: #c0392b; font-size: 13px;"></span>
        </div>
        <div style="border-top: 0.5px solid var(--color-border-tertiary);"></div>
        <div style="display: flex; justify-content: space-between; align-items: center;">
          <span style="color: var(--color-text-secondary); font-size: 13px;">TAN / Code</span>
          <span id="out-tan" style="font-weight: 500; color: #c0392b; font-size: 13px;"></span>
        </div>
      </div>
    </div>
    <p style="font-size: 13px; color: var(--color-text-secondary); margin: 10px 0 0;">
      Auf einer echten Phishing-Seite würden diese Daten direkt an die Betrüger gesendet – ohne dass du es merkst.
    </p>
  </div>

</div>

<script>
function showData() {
  const u = document.getElementById('username').value || '(leer)';
  const p = document.getElementById('password').value || '(leer)';
  const t = document.getElementById('tan').value || '(leer)';
  document.getElementById('out-user').textContent = u;
  document.getElementById('out-pass').textContent = p;
  document.getElementById('out-tan').textContent = t;
  document.getElementById('result-box').style.display = 'block';
  document.getElementById('result-box').scrollIntoView({behavior: 'smooth', block: 'nearest'});
}
</script>
