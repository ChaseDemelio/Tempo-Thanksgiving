<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Thanksgiving: Feast of the Feastbringer - Raid Guide (Classic)</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <style>
    /* Reset / base */
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }
    body {
      font-family: Arial, sans-serif;
      background: #141414 url("https://wow.zamimg.com/images/wow/icons/medium/inv_thanksgiving_turkey.jpg") no-repeat fixed center top;
      color: #e3e3e3;
      line-height: 1.5;
    }
    a {
      color: #ffcc00;
      text-decoration: none;
    }
    a:hover {
      text-decoration: underline;
    }

    /* Header */
    .header {
      background: linear-gradient(90deg, #111 0%, #1f1f1f 50%, #111 100%);
      border-bottom: 2px solid #ff8000;
      padding: 12px 20px;
      display: flex;
      align-items: center;
      gap: 12px;
      position: sticky;
      top: 0;
      z-index: 100;
    }
    .header-logo {
      width: 32px;
      height: 32px;
      border-radius: 4px;
      background: radial-gradient(circle at 30% 30%, #ffcc00 0, #ff8000 45%, #6a2b00 100%);
      display: flex;
      align-items: center;
      justify-content: center;
      font-weight: bold;
      font-size: 18px;
      color: #000;
      text-shadow: 0 0 4px rgba(0,0,0,0.8);
    }
    .header-title {
      font-size: 18px;
      font-weight: bold;
      color: #ffcc00;
    }
    .header-subtitle {
      font-size: 12px;
      color: #aaa;
      margin-left: auto;
    }

    /* Layout */
    .page {
      display: flex;
      max-width: 1200px;
      margin: 16px auto 40px;
      padding: 0 16px;
      gap: 16px;
    }

    /* Sidebar */
    .sidebar {
      width: 250px;
      background: rgba(10,10,10,0.9);
      border: 1px solid #333;
      border-radius: 4px;
      padding: 12px;
      max-height: calc(100vh - 80px);
      overflow-y: auto;
      position: sticky;
      top: 72px;
    }
    .sidebar-title {
      font-size: 14px;
      font-weight: bold;
      color: #ffcc00;
      margin-bottom: 8px;
      border-bottom: 1px solid #333;
      padding-bottom: 4px;
    }
    .sidebar ul {
      list-style: none;
      font-size: 13px;
    }
    .sidebar li {
      margin: 4px 0;
    }
    .sidebar li a {
      color: #ddd;
    }
    .sidebar li a:hover {
      color: #ffcc00;
    }

    /* Main content */
    .content {
      flex: 1;
      background: rgba(15,15,15,0.95);
      border: 1px solid #333;
      border-radius: 4px;
      padding: 16px 20px 24px;
    }

    .tagline {
      font-size: 13px;
      color: #bbb;
      margin-bottom: 12px;
    }

    h1 {
      font-size: 24px;
      color: #ffcc00;
      margin-bottom: 4px;
      text-shadow: 0 0 6px rgba(0,0,0,0.8);
    }
    h2 {
      font-size: 18px;
      color: #ffb84d;
      margin: 20px 0 4px;
      border-bottom: 1px solid #333;
      padding-bottom: 3px;
    }
    h3 {
      font-size: 16px;
      color: #ffdd88;
      margin: 14px 0 4px;
    }
    h4 {
      font-size: 14px;
      color: #ffd18a;
      margin: 10px 0 3px;
    }

    p {
      margin: 4px 0 8px;
      font-size: 14px;
    }
    ul {
      margin: 4px 0 8px 16px;
    }
    li {
      font-size: 14px;
      margin: 2px 0;
    }

    .pill-row {
      display: flex;
      flex-wrap: wrap;
      gap: 8px;
      margin: 6px 0 10px;
    }
    .pill {
      font-size: 12px;
      padding: 2px 8px;
      border-radius: 999px;
      border: 1px solid #444;
      background: #222;
      color: #ddd;
      white-space: nowrap;
    }

    .meta-box {
      border: 1px solid #444;
      border-radius: 4px;
      background: #1a1a1a;
      padding: 8px 10px;
      margin-bottom: 10px;
      font-size: 13px;
    }
    .meta-box strong {
      color: #ffcc00;
    }

    .callout {
      border-left: 3px solid #ff8000;
      background: #1c1308;
      padding: 8px 10px;
      font-size: 13px;
      margin: 10px 0 14px;
    }
    .callout strong {
      color: #ffcc00;
    }

    .table-like {
      border: 1px solid #333;
      border-radius: 4px;
      background: #1a1a1a;
      margin: 8px 0 12px;
      overflow: hidden;
    }
    .table-row {
      display: flex;
      border-bottom: 1px solid #262626;
    }
    .table-row:last-child {
      border-bottom: none;
    }
    .table-cell {
      padding: 6px 8px;
      font-size: 13px;
    }
    .table-cell.header {
      background: #262626;
      font-weight: bold;
      color: #ffcc00;
    }
    .table-cell.w-30 {
      width: 30%;
    }
    .table-cell.w-70 {
      width: 70%;
    }

    .footer-note {
      font-size: 12px;
      color: #888;
      margin-top: 16px;
      border-top: 1px solid #333;
      padding-top: 6px;
    }

    @media (max-width: 900px) {
      .page {
        flex-direction: column;
      }
      .sidebar {
        position: static;
        width: 100%;
        max-height: none;
        order: -1;
      }
    }
  </style>
</head>
<body>
  <header class="header">
    <div class="header-logo">T</div>
    <div class="header-title">Thanksgiving: Feast of the Feastbringer</div>
    <div class="header-subtitle">WoW Classic – Holiday Raid Guide</div>
  </header>

  <div class="page">
    <aside class="sidebar">
      <div class="sidebar-title">Quick Navigation</div>
      <ul>
        <li><a href="#overview">Overview</a></li>
        <li><a href="#prep">Raid Preparation</a></li>
        <li><a href="#attunement">Attunement</a></li>
        <li><a href="#consumables">Consumables & World Buffs</a></li>
        <li><a href="#trash">Greeting Trash Gauntlet</a></li>
        <li><a href="#boss">Boss: The Feastbringer</a></li>
        <li><a href="#phases">Phase Breakdown</a></li>
        <li><a href="#loot">Loot & Rewards</a></li>
        <li><a href="#achievements">Achievements</a></li>
        <li><a href="#lockout">Lockout</a></li>
      </ul>
    </aside>

    <main class="content">
      <section id="overview">
        <h1>Thanksgiving: Feast of the Feastbringer</h1>
        <p class="tagline">
          A once-per-year, 40-player social raid tuned for maximum emotional damage and Well Fed uptime.
        </p>

        <div class="meta-box">
          <p><strong>Instance Type:</strong> Holiday Raid (Family)</p>
          <p><strong>Difficulty:</strong> High – mechanically simple, socially lethal</p>
          <p><strong>Recommended Size:</strong> 10–40 players (extended family scaling)</p>
          <p><strong>Primary Rewards:</strong> Well Fed, Leftovers, Parental Approval</p>
        </div>

        <p>
          Thanksgiving is a single-boss raid centered around <strong>The Feastbringer (Mom)</strong>. Once
          <em>Dinner Phase</em> begins, the instance cannot be reset. Expect long phases, unskippable RP, and
          wipe conditions tied to poor plate management, arguments, or refusing seconds.
        </p>
      </section>

      <section id="prep">
        <h2>Raid Preparation</h2>

        <h3>Recommended Raid Composition</h3>
        <div class="table-like">
          <div class="table-row">
            <div class="table-cell header w-30">Role</div>
            <div class="table-cell header w-70">Recommended</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Main Tank</div>
            <div class="table-cell w-70">Dad (handles Turkey Carve frontal cleave)</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Off-Tank</div>
            <div class="table-cell w-70">Oldest sibling / cousin, assigned to kid-aggro and stray NPCs</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Healers</div>
            <div class="table-cell w-70">Anyone doing dishes, emotional support, or conflict resolution</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Melee DPS</div>
            <div class="table-cell w-70">Carvers, table-setters, food runners</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Ranged DPS</div>
            <div class="table-cell w-70">Couch crew, commentary specialists, “supervisors”</div>
          </div>
          <div class="table-row">
            <div class="table-cell w-30">Utility Hybrids</div>
            <div class="table-cell w-70">People who can “check the rolls,” “grab drinks,” and kite conversations</div>
          </div>
        </div>

        <div class="callout">
          <strong>Tip:</strong> Bring at least one raid member with high IRL Charisma to off-tank awkward conversations
          and interrupt near-wipe scenarios.
        </div>
      </section>

      <section id="attunement">
        <h2>Attunement</h2>
        <p>
          Entry to the instance requires completion of the questline
          <strong>“What Are You Bringing?”</strong>
        </p>
        <ul>
          <li>Bring one dish, dessert, or drink.</li>
          <li>Equip at least one polite greeting.</li>
          <li>Acknowledge The Feastbringer (Mom) on arrival.</li>
        </ul>
        <p>
          Failing attunement applies the debuff <strong>Showed Up Empty-Handed</strong>, increasing Disappointment damage
          taken for the entire lockout.
        </p>
      </section>

      <section id="consumables">
        <h2>Consumables & World Buffs</h2>

        <h3>Recommended Consumables</h3>
        <div class="pill-row">
          <div class="pill">Elixir of Social Fortitude</div>
          <div class="pill">Dark Gravy Protection Potion</div>
          <div class="pill">Rumsey Rum (Any)</div>
          <div class="pill">Cranberry Crit Elixir</div>
          <div class="pill">Emergency AFK Macro</div>
        </div>
        <ul>
          <li><strong>Elixir of Social Fortitude:</strong> Increases patience and tolerance to repeat questions.</li>
          <li><strong>Dark Gravy Protection Potion (DGPP):</strong> Reduces incoming Disappointment damage.</li>
          <li><strong>Rumsey Rum:</strong> Grants stamina for Dessert Enrage phase.</li>
          <li><strong>Cranberry Crit Elixir:</strong> Increases crit chance on compliments and small talk.</li>
          <li><strong>Emergency AFK Macro:</strong> “Bathroom break” or “need to check something” escape tool.</li>
        </ul>

        <h3>World Buffs</h3>
        <ul>
          <li><strong>Grandma’s Meal:</strong> Strongest Well Fed buff. Cannot be dispelled, only consumed.</li>
          <li><strong>Cozy Home (Fireplace Aura):</strong> +40 stamina, reduces emotional damage taken.</li>
          <li><strong>Sibling Coordination:</strong> Pre-raid coordination buff; improves interrupt coverage.</li>
          <li><strong>Good Night’s Sleep:</strong> Mandatory for progression pulls.</li>
        </ul>
      </section>

      <section id="trash">
        <h2>Greeting Trash Gauntlet</h2>
        <p>
          Before reaching the boss, the raid must clear the unskippable <strong>Greeting Gauntlet</strong>, a corridor
          filled with high-HP NPCs linked by social tethers.
        </p>

        <h3>Key Trash NPCs</h3>

        <h4>Aunt Cluster</h4>
        <ul>
          <li><strong>Hug Spam:</strong> Harmless but roots targets briefly.</li>
          <li><strong>How’s Work?</strong> Roots target for 30+ seconds with forced dialogue.</li>
        </ul>

        <h4>Uncle of Infinite Stories</h4>
        <ul>
          <li><strong>Story From ’78:</strong> 90-second uninterruptible channeled monologue.</li>
          <li><strong>Misremembered Anecdote:</strong> Confuses target, lowering mental clarity.</li>
        </ul>

        <h4>Cousin Level 12</h4>
        <ul>
          <li>Casts <strong>Look What I Can Do</strong> on a short cooldown, demanding constant attention.</li>
        </ul>

        <h4>Neighbor Nobody Knows</h4>
        <ul>
          <li>Stealthed add that opens with <strong>I Don’t Believe We’ve Met</strong>.</li>
          <li>Applies raid-wide awkwardness debuff.</li>
        </ul>

        <div class="callout">
          <strong>Trash Tip:</strong> Absolutely avoid triggering the hidden
          <strong>Family Politics</strong> mechanic. This is effectively an instant wipe.
        </div>
      </section>

      <section id="boss">
        <h2>Boss: The Feastbringer (Mom)</h2>
        <p><em>“She Who Must Be Obeyed” – Family, Humanoid</em></p>

        <div class="meta-box">
          <p><strong>Health:</strong> Very High</p>
          <p><strong>Enrage Timer:</strong> Variable (based on raid behavior)</p>
          <p><strong>Wipe Conditions:</strong> Arguing, insufficient eating, refusing seconds, ignoring mechanics</p>
          <p><strong>Immunities:</strong> Silence, hard CC, weak excuses</p>
        </div>

        <h3>Global Abilities</h3>
        <ul>
          <li><strong>Guilt Aura:</strong> Passive aura that stacks on players who skip mechanics or avoid food.</li>
          <li><strong>Overcooked Disappointment:</strong> Raid-wide emotional damage if effort isn’t acknowledged.</li>
          <li><strong>Plate Check:</strong> Random inspection; can trigger <strong>Guilt Bomb</strong> follow-up.</li>
        </ul>

        <h3>Active Abilities</h3>
        <ul>
          <li><strong>Turkey Carve (Frontal Cleave):</strong> MT only. Any melee in front arc risk Dryness stacks.</li>
          <li><strong>Seconds Call (Raid Check):</strong> If under 50% of raid accepts seconds, casts
              <strong>Disappointment Volley</strong>.</li>
          <li><strong>Gravy Slick:</strong> Ground effect slowing movement, causing plate mishaps.</li>
          <li><strong>Dessert Enrage:</strong> At high raid fullness, casts <strong>Try My Pie</strong> repeatedly.</li>
        </ul>
      </section>

      <section id="phases">
        <h2>Phase Breakdown</h2>

        <h3>Phase 1: Table Setup</h3>
        <p>
          Soft RP phase. Minimal damage but high risk of early pulls.
        </p>
        <ul>
          <li>Do not pull Mom’s aggro by hovering in the kitchen.</li>
          <li>Assign utility players to assist with placing dishes and drinks.</li>
          <li>Ranged should position near exits to kite early conversation adds.</li>
        </ul>

        <h3>Phase 2: Main Course</h3>
        <p>
          Primary progression check; longest and most demanding phase.
        </p>
        <ul>
          <li>Maintain even food consumption to avoid <strong>You Didn’t Try My Dish</strong> stacks.</li>
          <li>Healers manage both physical and emotional damage from small talk and criticism mechanics.</li>
          <li>Tanks rotate cooldowns when <strong>Turkey Carve</strong> overlaps with <strong>Seconds Call</strong>.</li>
        </ul>

        <h3>Phase 3: Dessert (Soft Enrage)</h3>
        <ul>
          <li><strong>Pie Beam:</strong> Chain-dessert effect; multiple bounces possible.</li>
          <li><strong>Sweetness Overload:</strong> Severe movement speed reduction.</li>
          <li><strong>Food Coma:</strong> Ticking debuff that eventually incapacitates the raid.</li>
        </ul>
        <p>
          Execute phase begins when raid reaches ~85% fullness. Manage intake carefully to avoid early coma.
        </p>

        <h3>Hard Enrage: Political Discussion</h3>
        <p>
          Triggered by any NPC mentioning politics, controversial news, or “kids these days.”
        </p>
        <ul>
          <li>Only counter is <strong>Immediate Subject Change</strong>, with low success rate.</li>
          <li>If it lands, the cast is delayed. If it fails, prepare for a full emotional wipe.</li>
        </ul>

        <h3>Phase 4: Cleanup (Hidden Final Boss)</h3>
        <p>
          On defeat, The Feastbringer summons <strong>The Sink</strong>, a high-armor stationary add.
        </p>
        <ul>
          <li>Requires 5–7 cleaners for efficient kill.</li>
          <li>Ignoring The Sink applies <strong>Reputation Loss</strong> until next holiday.</li>
          <li>Completing Cleanup grants <strong>Parental Approval</strong> until Christmas reset.</li>
        </ul>
      </section>

      <section id="loot">
        <h2>Loot & Rewards</h2>

        <h3>Common Drops</h3>
        <ul>
          <li><strong>Leftovers:</strong> In multiple containers; quality scales with early participation.</li>
          <li><strong>Well Fed Buff:</strong> Long-duration stat increase, stacks with Rested XP IRL.</li>
          <li><strong>Ziplock Containers of Unknown Origin:</strong> BoE, can be reused.</li>
        </ul>

        <h3>Rare Drops</h3>
        <ul>
          <li><strong>Home Baked Rolls:</strong> High-value comfort food item.</li>
          <li><strong>Pie Slice of Unusual Size:</strong> Cosmetic + morale boost.</li>
          <li><strong>Unattainable Warmth of Family:</strong> Non-tradable, nostalgia-type trinket.</li>
        </ul>

        <h3>Legendary Rewards</h3>
        <ul>
          <li><strong>Take Some With You:</strong> Legendary-level insistence; guarantees Leftover drop.</li>
          <li><strong>Mom’s Good Graces:</strong> Reputation buff lasting until Christmas instance.</li>
        </ul>
      </section>

      <section id="achievements">
        <h2>Achievements</h2>
        <ul>
          <li><strong>[No Wipes]:</strong> Complete the raid without any arguments.</li>
          <li><strong>[Seconds Heroic]:</strong> Accept seconds for all major dishes.</li>
          <li><strong>[The Pie-tanical]:</strong> Survive Dessert Phase without entering Food Coma.</li>
          <li><strong>[Uncle Interruptor]:</strong> Successfully stop <em>Story From ’78</em> before full channel.</li>
          <li><strong>[Full Clear]:</strong> Participate in Cleanup Phase without being asked.</li>
        </ul>
      </section>

      <section id="lockout">
        <h2>Lockout</h2>
        <p>
          Thanksgiving has a strict <strong>annual lockout</strong> (~365 days). The instance cannot be extended, reset,
          or pugged after the fact. All progress and reputation carry into future years.
        </p>
      </section>

      <div class="footer-note">
        Share this page with your guild, assign roles, pop your world buffs, and good luck on progression. May your RNG
        be blessed and your wipes minimal.
      </div>
    </main>
  </div>
</body>
</html>
