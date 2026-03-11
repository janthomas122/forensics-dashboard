import { useState, useEffect } from "react";

const CASES = [
  {
    id: "ZD-2026-0041",
    device: "iPhone 15 Pro",
    imei: "352099001761481",
    seized: "02-03-2026",
    officer: "Rechercheur van Dijk",
    status: "EXTRACTIE_COMPLEET",
    progress: 100,
    tags: ["Fraude", "Witwassen"],
    findings: [
      { type: "Berichten", icon: "💬", count: 4821, flagged: 34 },
      { type: "Foto's", icon: "🖼️", count: 1203, flagged: 12 },
      { type: "Locatiedata", icon: "📍", count: 9821, flagged: 88 },
      { type: "Contacten", icon: "👤", count: 312, flagged: 7 },
      { type: "Verwijderde bestanden", icon: "🗑️", count: 441, flagged: 22 },
    ],
    timeline: [
      { date: "02-03-2026 14:22", event: "In beslag genomen", type: "intake" },
      { date: "03-03-2026 09:05", event: "UFED extractie gestart", type: "process" },
      { date: "03-03-2026 11:43", event: "Extractie voltooid", type: "success" },
      { date: "04-03-2026 08:30", event: "Analyse begonnen", type: "process" },
      { date: "07-03-2026 16:00", event: "Rapport gegenereerd", type: "success" },
    ],
    integrity: "a3f2c1b9d4e78f0a1b2c3d4e5f6789abc012345",
    riskScore: 87,
  },
  {
    id: "ZD-2026-0038",
    device: "Samsung Galaxy S24",
    imei: "490154203237518",
    seized: "28-02-2026",
    officer: "Rechercheur Bakker",
    status: "ANALYSE_LOPEND",
    progress: 62,
    tags: ["Drugshandel"],
    findings: [
      { type: "Berichten", icon: "💬", count: 2103, flagged: 91 },
      { type: "Foto's", icon: "🖼️", count: 887, flagged: 5 },
      { type: "Locatiedata", icon: "📍", count: 5302, flagged: 44 },
      { type: "Contacten", icon: "👤", count: 198, flagged: 18 },
      { type: "Verwijderde bestanden", icon: "🗑️", count: 203, flagged: 31 },
    ],
    timeline: [
      { date: "28-02-2026 19:55", event: "In beslag genomen", type: "intake" },
      { date: "01-03-2026 07:00", event: "Faraday-zak geplaatst", type: "process" },
      { date: "01-03-2026 13:12", event: "UFED extractie gestart", type: "process" },
      { date: "01-03-2026 15:30", event: "Extractie voltooid", type: "success" },
      { date: "02-03-2026 10:00", event: "Analyse lopend...", type: "active" },
    ],
    integrity: "b7e3a2c1d9f0e1b4c5d6e7f890abcdef123456",
    riskScore: 73,
  },
  {
    id: "ZD-2026-0029",
    device: "Google Pixel 8",
    imei: "359876043210987",
    seized: "18-02-2026",
    officer: "Rechercheur Smit",
    status: "WACHT_OP_ONTGRENDELING",
    progress: 15,
    tags: ["Cybercrime", "Identiteitsfraude"],
    findings: [],
    timeline: [
      { date: "18-02-2026 11:30", event: "In beslag genomen", type: "intake" },
      { date: "18-02-2026 12:00", event: "Faraday-zak geplaatst", type: "process" },
      { date: "19-02-2026 09:00", event: "Pincode-aanvraag rechtbank ingediend", type: "process" },
      { date: "25-02-2026 14:00", event: "Wacht op rechterlijk bevel", type: "warning" },
    ],
    integrity: "—",
    riskScore: 51,
  },
  {
    id: "ZD-2026-0055",
    device: "iPhone 13",
    imei: "356789012345678",
    seized: "09-03-2026",
    officer: "Rechercheur van Dijk",
    status: "NIEUW_INTAKE",
    progress: 5,
    tags: ["Bedreiging", "Stalking"],
    findings: [],
    timeline: [
      { date: "09-03-2026 22:14", event: "In beslag genomen", type: "intake" },
      { date: "10-03-2026 08:00", event: "Ingecheckt bij digitaal lab", type: "process" },
    ],
    integrity: "—",
    riskScore: 38,
  },
];

const STATUS = {
  EXTRACTIE_COMPLEET:     { label: "Extractie compleet",     color: "#22c55e", bg: "#22c55e18", border: "#22c55e44" },
  ANALYSE_LOPEND:         { label: "Analyse lopend",         color: "#eab308", bg: "#eab30818", border: "#eab30844" },
  WACHT_OP_ONTGRENDELING: { label: "Wacht op ontgrendeling", color: "#f97316", bg: "#f9731618", border: "#f9731644" },
  NIEUW_INTAKE:           { label: "Nieuw — intake",         color: "#60a5fa", bg: "#60a5fa18", border: "#60a5fa44" },
};

const TIMELINE_COLORS = {
  intake: "#60a5fa", process: "#64748b", success: "#22c55e", warning: "#f97316", active: "#eab308",
};

function Badge({ status }) {
  const s = STATUS[status];
  return (
    <span style={{
      display: "inline-flex", alignItems: "center", gap: 5,
      background: s.bg, border: `1px solid ${s.border}`,
      color: s.color, fontSize: 11, fontWeight: 600,
      padding: "3px 9px", borderRadius: 20, whiteSpace: "nowrap",
    }}>
      <span style={{
        width: 6, height: 6, borderRadius: "50%", background: s.color, flexShrink: 0,
        animation: status === "ANALYSE_LOPEND" ? "blink 1.4s infinite" : "none",
      }} />
      {s.label}
    </span>
  );
}

function Tag({ label }) {
  return (
    <span style={{
      fontSize: 11, padding: "2px 8px", borderRadius: 4,
      background: "#1e293b", color: "#94a3b8", border: "1px solid #334155",
    }}>{label}</span>
  );
}

function ProgressBar({ value, status }) {
  const color = STATUS[status].color;
  return (
    <div style={{ background: "#1e293b", borderRadius: 99, height: 6, width: "100%", overflow: "hidden" }}>
      <div style={{ height: "100%", width: `${value}%`, background: color, borderRadius: 99, transition: "width 1s ease", boxShadow: `0 0 8px ${color}55` }} />
    </div>
  );
}

function RiskCircle({ score }) {
  const color = score >= 75 ? "#ef4444" : score >= 50 ? "#eab308" : "#22c55e";
  const label = score >= 75 ? "Hoog" : score >= 50 ? "Gemiddeld" : "Laag";
  const r = 24, circ = 2 * Math.PI * r;
  return (
    <div style={{ display: "flex", flexDirection: "column", alignItems: "center", gap: 4 }}>
      <svg width="64" height="64" viewBox="0 0 64 64">
        <circle cx="32" cy="32" r={r} fill="none" stroke="#1e293b" strokeWidth="5" />
        <circle cx="32" cy="32" r={r} fill="none" stroke={color} strokeWidth="5"
          strokeDasharray={circ} strokeDashoffset={circ - (score / 100) * circ}
          strokeLinecap="round" transform="rotate(-90 32 32)"
          style={{ transition: "stroke-dashoffset 1s ease" }} />
        <text x="32" y="37" textAnchor="middle" fill={color} fontSize="14" fontFamily="monospace" fontWeight="700">{score}</text>
      </svg>
      <span style={{ fontSize: 10, color: "#64748b", fontWeight: 600, textTransform: "uppercase", letterSpacing: 0.5 }}>{label} risico</span>
    </div>
  );
}

function Section({ title, children }) {
  return (
    <div style={{ background: "#0f172a", border: "1px solid #1e293b", borderRadius: 12, overflow: "hidden" }}>
      {title && (
        <div style={{ padding: "12px 20px", borderBottom: "1px solid #1e293b", background: "#0b1525" }}>
          <span style={{ fontSize: 11, fontWeight: 700, color: "#475569", textTransform: "uppercase", letterSpacing: 1 }}>{title}</span>
        </div>
      )}
      {children}
    </div>
  );
}

export default function App() {
  const [selected, setSelected] = useState(CASES[0]);
  const [tab, setTab] = useState("bevindingen");
  const [clock, setClock] = useState(new Date());

  useEffect(() => {
    const t = setInterval(() => setClock(new Date()), 1000);
    return () => clearInterval(t);
  }, []);

  const totalFlagged = CASES.flatMap(c => c.findings).reduce((s, f) => s + (f?.flagged || 0), 0);

  const stats = [
    { label: "Actieve zaken", value: CASES.length, color: "#f1f5f9" },
    { label: "In analyse", value: CASES.filter(c => c.status === "ANALYSE_LOPEND").length, color: "#eab308" },
    { label: "Wacht op toegang", value: CASES.filter(c => c.status === "WACHT_OP_ONTGRENDELING").length, color: "#f97316" },
    { label: "Extractie klaar", value: CASES.filter(c => c.status === "EXTRACTIE_COMPLEET").length, color: "#22c55e" },
    { label: "Items gemarkeerd", value: totalFlagged, color: "#ef4444" },
  ];

  return (
    <div style={{ fontFamily: "'Inter', -apple-system, sans-serif", background: "#060c18", minHeight: "100vh", color: "#e2e8f0", display: "flex", flexDirection: "column", fontSize: 14 }}>
      <style>{`
        @import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&family=JetBrains+Mono:wght@400;600&display=swap');
        * { box-sizing: border-box; margin: 0; padding: 0; }
        @keyframes blink { 0%,100%{opacity:1} 50%{opacity:0.2} }
        ::-webkit-scrollbar { width: 4px; }
        ::-webkit-scrollbar-track { background: #0b1220; }
        ::-webkit-scrollbar-thumb { background: #1e293b; border-radius: 99px; }
        .case-row { cursor: pointer; padding: 16px; border-bottom: 1px solid #1e293b; transition: background 0.12s; }
        .case-row:hover { background: #0c1526; }
        .case-row.sel { background: #0d1e36; border-left: 3px solid #3b82f6; padding-left: 13px; }
        .tab { background: none; border: none; cursor: pointer; padding: 12px 20px; font-size: 13px; font-family: inherit; font-weight: 500; color: #475569; border-bottom: 2px solid transparent; transition: all 0.12s; }
        .tab.on { color: #60a5fa; border-bottom-color: #60a5fa; }
        .tab:hover:not(.on) { color: #94a3b8; }
      `}</style>

      {/* ── TOP BAR ── */}
      <div style={{ background: "#0b1220", borderBottom: "1px solid #1e293b", padding: "0 24px", height: 54, display: "flex", alignItems: "center", justifyContent: "space-between", flexShrink: 0 }}>
        <div style={{ display: "flex", alignItems: "center", gap: 12 }}>
          <div style={{ width: 34, height: 34, borderRadius: 8, background: "linear-gradient(135deg,#1d4ed8,#1e40af)", display: "flex", alignItems: "center", justifyContent: "center", fontSize: 17 }}>🔍</div>
          <div>
            <div style={{ fontSize: 14, fontWeight: 700, color: "#f1f5f9" }}>Digitaal Forensisch Onderzoek</div>
            <div style={{ fontSize: 11, color: "#475569" }}>Politie Nederland · Beveiligd systeem</div>
          </div>
        </div>
        <div style={{ display: "flex", alignItems: "center", gap: 14 }}>
          <span style={{ fontSize: 12, color: "#475569", fontFamily: "'JetBrains Mono', monospace" }}>
            {clock.toLocaleDateString("nl-NL")} · {clock.toLocaleTimeString("nl-NL")}
          </span>
          <span style={{ background: "#450a0a", border: "1px solid #7f1d1d", padding: "4px 12px", borderRadius: 6, fontSize: 11, color: "#fca5a5", fontWeight: 600 }}>
            🔒 VERTROUWELIJK
          </span>
        </div>
      </div>

      {/* ── STATS ROW ── */}
      <div style={{ background: "#0b1220", borderBottom: "1px solid #1e293b", padding: "12px 24px", display: "flex", gap: 8, flexShrink: 0 }}>
        {stats.map((s, i) => (
          <div key={i} style={{ flex: 1, background: "#0f172a", border: "1px solid #1e293b", borderRadius: 10, padding: "12px 16px" }}>
            <div style={{ fontSize: 24, fontWeight: 700, color: s.color, fontFamily: "'JetBrains Mono', monospace", lineHeight: 1 }}>{s.value}</div>
            <div style={{ fontSize: 11, color: "#64748b", marginTop: 4 }}>{s.label}</div>
          </div>
        ))}
      </div>

      {/* ── MAIN ── */}
      <div style={{ display: "flex", flex: 1, overflow: "hidden" }}>

        {/* ── SIDEBAR ── */}
        <div style={{ width: 300, background: "#0b1220", borderRight: "1px solid #1e293b", display: "flex", flexDirection: "column", flexShrink: 0 }}>
          <div style={{ padding: "12px 16px", borderBottom: "1px solid #1e293b" }}>
            <div style={{ fontSize: 11, fontWeight: 700, color: "#475569", textTransform: "uppercase", letterSpacing: 1 }}>
              {CASES.length} apparaten in beheer
            </div>
          </div>
          <div style={{ overflowY: "auto", flex: 1 }}>
            {CASES.map(c => (
              <div key={c.id} className={`case-row ${selected?.id === c.id ? "sel" : ""}`} onClick={() => { setSelected(c); setTab("bevindingen"); }}>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start", marginBottom: 8 }}>
                  <div>
                    <div style={{ fontSize: 14, fontWeight: 600, color: "#f1f5f9", marginBottom: 2 }}>{c.device}</div>
                    <div style={{ fontSize: 11, color: "#475569", fontFamily: "'JetBrains Mono', monospace" }}>{c.id}</div>
                  </div>
                </div>
                <div style={{ marginBottom: 8 }}>
                  <Badge status={c.status} />
                </div>
                <div style={{ marginBottom: 8 }}>
                  <ProgressBar value={c.progress} status={c.status} />
                </div>
                <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center" }}>
                  <div style={{ display: "flex", gap: 4 }}>{c.tags.map(t => <Tag key={t} label={t} />)}</div>
                  <span style={{ fontSize: 12, fontWeight: 700, color: STATUS[c.status].color, fontFamily: "monospace" }}>{c.progress}%</span>
                </div>
              </div>
            ))}
          </div>
        </div>

        {/* ── DETAIL ── */}
        {selected && (
          <div style={{ flex: 1, display: "flex", flexDirection: "column", overflow: "hidden" }}>

            {/* Case header */}
            <div style={{ background: "#0b1220", borderBottom: "1px solid #1e293b", padding: "18px 24px", flexShrink: 0 }}>
              <div style={{ display: "flex", justifyContent: "space-between", alignItems: "flex-start" }}>
                <div>
                  <div style={{ display: "flex", alignItems: "center", gap: 10, marginBottom: 10, flexWrap: "wrap" }}>
                    <span style={{ fontSize: 20, fontWeight: 700, color: "#f1f5f9", fontFamily: "'JetBrains Mono', monospace" }}>{selected.id}</span>
                    <Badge status={selected.status} />
                    <div style={{ display: "flex", gap: 5 }}>{selected.tags.map(t => <Tag key={t} label={t} />)}</div>
                  </div>
                  <div style={{ display: "flex", gap: 28, flexWrap: "wrap" }}>
                    {[["Apparaat", selected.device], ["IMEI", selected.imei], ["In beslag", selected.seized], ["Rechercheur", selected.officer]].map(([k, v]) => (
                      <div key={k}>
                        <div style={{ fontSize: 10, color: "#475569", textTransform: "uppercase", letterSpacing: 0.8, fontWeight: 700, marginBottom: 3 }}>{k}</div>
                        <div style={{ fontSize: 13, color: "#cbd5e1", fontWeight: 500, fontFamily: k === "IMEI" ? "'JetBrains Mono', monospace" : "inherit" }}>{v}</div>
                      </div>
                    ))}
                  </div>
                  <div style={{ marginTop: 12, display: "inline-flex", alignItems: "center", gap: 8, background: "#0f172a", border: "1px solid #1e293b", borderRadius: 6, padding: "5px 12px" }}>
                    <span style={{ fontSize: 10, color: "#475569", fontWeight: 700, textTransform: "uppercase", letterSpacing: 0.8 }}>SHA-256</span>
                    <span style={{ fontSize: 11, color: "#60a5fa", fontFamily: "'JetBrains Mono', monospace" }}>{selected.integrity}</span>
                  </div>
                </div>
                <RiskCircle score={selected.riskScore} />
              </div>
            </div>

            {/* Tabs */}
            <div style={{ background: "#0b1220", borderBottom: "1px solid #1e293b", display: "flex", padding: "0 24px", flexShrink: 0 }}>
              {[["bevindingen", "📊 Bevindingen"], ["tijdlijn", "🕐 Tijdlijn"], ["details", "ℹ️ Apparaatdetails"]].map(([key, lbl]) => (
                <button key={key} className={`tab ${tab === key ? "on" : ""}`} onClick={() => setTab(key)}>{lbl}</button>
              ))}
            </div>

            {/* Content */}
            <div style={{ flex: 1, overflowY: "auto", padding: "20px 24px", display: "flex", flexDirection: "column", gap: 16 }}>

              {tab === "bevindingen" && <>
                {/* Progress card */}
                <Section title="Extractiestatus">
                  <div style={{ padding: "16px 20px" }}>
                    <div style={{ display: "flex", justifyContent: "space-between", alignItems: "center", marginBottom: 10 }}>
                      <Badge status={selected.status} />
                      <span style={{ fontSize: 16, fontWeight: 700, color: STATUS[selected.status].color, fontFamily: "monospace" }}>{selected.progress}%</span>
                    </div>
                    <ProgressBar value={selected.progress} status={selected.status} />
                  </div>
                </Section>

                {/* Findings */}
                {selected.findings.length > 0 ? (
                  <Section title="Geëxtraheerde data">
                    {/* Totals */}
                    <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", borderBottom: "1px solid #1e293b" }}>
                      <div style={{ padding: "16px 20px", borderRight: "1px solid #1e293b" }}>
                        <div style={{ fontSize: 26, fontWeight: 700, color: "#f1f5f9", fontFamily: "monospace" }}>
                          {selected.findings.reduce((s, f) => s + f.count, 0).toLocaleString("nl")}
                        </div>
                        <div style={{ fontSize: 12, color: "#64748b", marginTop: 3 }}>Totaal geëxtraheerde items</div>
                      </div>
                      <div style={{ padding: "16px 20px" }}>
                        <div style={{ fontSize: 26, fontWeight: 700, color: "#ef4444", fontFamily: "monospace" }}>
                          {selected.findings.reduce((s, f) => s + f.flagged, 0)}
                        </div>
                        <div style={{ fontSize: 12, color: "#64748b", marginTop: 3 }}>Gemarkeerd voor review</div>
                      </div>
                    </div>
                    {/* Table header */}
                    <div style={{ display: "grid", gridTemplateColumns: "2fr 1fr 1fr 140px", padding: "8px 20px", borderBottom: "1px solid #1e293b", background: "#0b1525" }}>
                      {["Categorie", "Totaal", "Gemarkeerd", "% Gemarkeerd"].map(h => (
                        <span key={h} style={{ fontSize: 10, fontWeight: 700, color: "#475569", textTransform: "uppercase", letterSpacing: 0.8 }}>{h}</span>
                      ))}
                    </div>
                    {/* Rows */}
                    {selected.findings.map((f, i) => {
                      const pct = Math.round((f.flagged / f.count) * 100);
                      const fc = f.flagged > 50 ? "#ef4444" : f.flagged > 15 ? "#eab308" : "#22c55e";
                      return (
                        <div key={f.type} style={{ display: "grid", gridTemplateColumns: "2fr 1fr 1fr 140px", alignItems: "center", padding: "13px 20px", borderBottom: i < selected.findings.length - 1 ? "1px solid #1e293b" : "none" }}>
                          <div style={{ display: "flex", alignItems: "center", gap: 9 }}>
                            <span style={{ fontSize: 17 }}>{f.icon}</span>
                            <span style={{ fontWeight: 500, color: "#e2e8f0" }}>{f.type}</span>
                          </div>
                          <span style={{ fontFamily: "monospace", fontWeight: 600, color: "#94a3b8" }}>{f.count.toLocaleString("nl")}</span>
                          <span style={{ fontFamily: "monospace", fontWeight: 700, color: fc }}>⚑ {f.flagged}</span>
                          <div>
                            <div style={{ display: "flex", justifyContent: "space-between", marginBottom: 4 }}>
                              <span style={{ fontSize: 10, color: "#475569" }}>{pct}%</span>
                            </div>
                            <div style={{ background: "#1e293b", borderRadius: 99, height: 5 }}>
                              <div style={{ height: "100%", width: `${pct}%`, background: fc, borderRadius: 99 }} />
                            </div>
                          </div>
                        </div>
                      );
                    })}
                  </Section>
                ) : (
                  <Section>
                    <div style={{ padding: "48px 24px", textAlign: "center" }}>
                      <div style={{ fontSize: 36, marginBottom: 12 }}>📱</div>
                      <div style={{ fontSize: 15, fontWeight: 600, color: "#475569", marginBottom: 6 }}>Geen data beschikbaar</div>
                      <div style={{ fontSize: 13, color: "#334155" }}>Extractie is nog niet gestart of wacht op toegang tot het apparaat.</div>
                    </div>
                  </Section>
                )}
              </>}

              {tab === "tijdlijn" && (
                <Section title="Keten van bewaring — Chain of Custody">
                  <div style={{ padding: "20px 24px", position: "relative", paddingLeft: 52 }}>
                    <div style={{ position: "absolute", left: 32, top: 24, bottom: 24, width: 2, background: "#1e293b", borderRadius: 99 }} />
                    {selected.timeline.map((e, i) => (
                      <div key={i} style={{ position: "relative", marginBottom: 24 }}>
                        <div style={{
                          position: "absolute", left: -20, top: 3,
                          width: 12, height: 12, borderRadius: "50%",
                          background: TIMELINE_COLORS[e.type],
                          boxShadow: `0 0 8px ${TIMELINE_COLORS[e.type]}88`,
                          border: "2px solid #0f172a",
                        }} />
                        <div style={{ fontSize: 11, color: "#475569", fontFamily: "'JetBrains Mono', monospace", marginBottom: 4 }}>{e.date}</div>
                        <div style={{ fontSize: 14, fontWeight: 500, color: "#e2e8f0" }}>{e.event}</div>
                      </div>
                    ))}
                  </div>
                </Section>
              )}

              {tab === "details" && <>
                <div style={{ display: "grid", gridTemplateColumns: "1fr 1fr", gap: 10 }}>
                  {[
                    ["Model", selected.device],
                    ["IMEI", selected.imei],
                    ["Zaakcode", selected.id],
                    ["Inbeslagnamedatum", selected.seized],
                    ["Rechercheur", selected.officer],
                    ["Status", STATUS[selected.status].label],
                    ["Delicten", selected.tags.join(", ")],
                    ["Risicoscore", `${selected.riskScore} / 100`],
                  ].map(([k, v]) => (
                    <div key={k} style={{ background: "#0f172a", border: "1px solid #1e293b", borderRadius: 10, padding: "14px 18px" }}>
                      <div style={{ fontSize: 10, color: "#475569", fontWeight: 700, textTransform: "uppercase", letterSpacing: 0.8, marginBottom: 5 }}>{k}</div>
                      <div style={{ fontSize: 14, color: "#e2e8f0", fontWeight: 500, fontFamily: ["IMEI", "Zaakcode"].includes(k) ? "'JetBrains Mono', monospace" : "inherit" }}>{v}</div>
                    </div>
                  ))}
                </div>
                <Section title="Forensische integriteitswaarde (SHA-256)">
                  <div style={{ padding: "16px 20px" }}>
                    <div style={{ fontSize: 12, color: "#60a5fa", fontFamily: "'JetBrains Mono', monospace", wordBreak: "break-all", background: "#060c18", padding: "10px 14px", borderRadius: 6, border: "1px solid #1e293b", marginBottom: 10 }}>
                      {selected.integrity}
                    </div>
                    <div style={{ fontSize: 12, color: "#64748b", lineHeight: 1.6 }}>
                      Berekend bij eerste extractie en geverifieerd bij elke volgende toegang. Een afwijking duidt op compromittering van het bewijsmateriaal.
                    </div>
                  </div>
                </Section>
              </>}
            </div>
          </div>
        )}
      </div>
    </div>
  );
}
