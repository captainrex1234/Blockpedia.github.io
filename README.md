# Blockpedia.github.io
The Minecraft blockpedia for you and you friends to use


<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Blockpedia — Minecraft Block Encyclopedia</title>
<style>
:root{
  --bg:#101010;--panel:#202020;--panel2:#292929;--panel3:#343434;
  --green:#55a83d;--green2:#72c451;--text:#f1f1f1;--muted:#a9a9a9;
  --line:#494949;--gold:#e5c65a;--red:#d85845;--blue:#6fb4e7
}
*{box-sizing:border-box}
body{margin:0;background:linear-gradient(#121212,#0c0c0c);color:var(--text);font-family:Arial,Helvetica,sans-serif}
button,input,select{font:inherit}
.top{
  position:sticky;top:0;z-index:10;display:flex;gap:12px;align-items:center;
  padding:11px 18px;background:#1d1d1d;border-bottom:4px solid #0a0a0a;
  box-shadow:0 3px 0 rgba(0,0,0,.45)
}
.logo{font-weight:900;font-size:22px;white-space:nowrap;text-shadow:2px 2px #000}
.logo span{color:var(--green2)}
.search{flex:1;min-width:160px;background:#101010;color:#fff;border:2px solid #555;border-radius:3px;padding:10px 12px}
.btn{border:2px solid #111;border-radius:3px;background:var(--green);color:#fff;padding:9px 13px;font-weight:700;cursor:pointer;box-shadow:inset 0 -3px rgba(0,0,0,.24)}
.btn:hover{background:var(--green2)}
.wrap{max-width:1400px;margin:auto;padding:18px;display:grid;grid-template-columns:220px minmax(0,1fr) 340px;gap:18px}
.panel{background:var(--panel);border:2px solid var(--line);box-shadow:0 3px 0 #080808}
.side{padding:14px;height:max-content;position:sticky;top:82px}
.side h3{font-size:13px;color:#86d35d;margin:3px 0 9px}
.side button{display:block;width:100%;text-align:left;border:0;background:none;color:#ddd;padding:8px;border-radius:2px;cursor:pointer}
.side button:hover{background:#3a3a3a}.side button.active{background:#3b552f}
.count{color:#8e8e8e;font-size:12px;float:right}
.hero{padding:20px;margin-bottom:14px;background:linear-gradient(#303030,#1e1e1e)}
.hero h1{margin:0 0 6px;font-size:32px}.hero p{color:var(--muted);margin:0;line-height:1.5}
.bar{display:flex;gap:9px;align-items:center;flex-wrap:wrap;margin-bottom:12px}
select{background:#171717;color:#eee;border:2px solid #555;padding:9px;border-radius:3px}
.status{color:#aaa;font-size:13px;margin-left:auto}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(175px,1fr));gap:11px}
.card{
  background:var(--panel);border:2px solid #454545;box-shadow:0 2px 0 #090909;
  padding:10px;cursor:pointer;min-height:195px;display:flex;flex-direction:column
}
.card:hover{border-color:var(--green2);transform:translateY(-1px)}
.thumb{height:116px;border:2px solid #555;background:
 repeating-conic-gradient(#333 0 25%,#2d2d2d 0 50%) 50%/22px 22px;
 display:flex;align-items:center;justify-content:center;overflow:hidden}
.thumb img{image-rendering:pixelated;width:92px;height:92px;object-fit:contain}
.cube{font-size:51px;text-shadow:4px 4px #111}
.name{font-weight:800;margin-top:9px;line-height:1.15}.mini{color:#999;font-size:12px;margin-top:5px}
.detail{padding:14px;position:sticky;top:82px;height:max-content}
.detail-head{display:flex;gap:12px;align-items:center;border-bottom:2px solid #454545;padding-bottom:12px}
.bigthumb{width:110px;height:110px;flex:none;background:repeating-conic-gradient(#333 0 25%,#2d2d2d 0 50%) 50%/22px 22px;border:2px solid #555;display:flex;align-items:center;justify-content:center}
.bigthumb img{image-rendering:pixelated;width:90px;height:90px;object-fit:contain}
.detail h2{margin:0;font-size:22px}.id{color:#8a8a8a;font:12px monospace;margin-top:3px}
.stats{display:grid;grid-template-columns:1fr 1fr;margin-top:12px;border:1px solid #4b4b4b}
.stat{padding:9px;border-right:1px solid #4b4b4b;border-bottom:1px solid #4b4b4b}.stat:nth-child(2n){border-right:0}
.stat b{display:block;color:#aaa;font-size:11px;text-transform:uppercase;margin-bottom:4px}
.section{margin-top:13px}.section h3{font-size:14px;margin:0 0 6px;color:#8ed45d}
.box{background:#181818;border:1px solid #454545;padding:9px;line-height:1.45;font-size:13px}
.tag{display:inline-block;background:#3a3a3a;border:1px solid #555;border-radius:3px;padding:3px 6px;margin:2px 3px 2px 0;font-size:11px}
.source{display:flex;gap:7px;flex-wrap:wrap;margin-top:12px}.source a{color:#8bc6ef}
.notice{background:#24351d;border-left:5px solid var(--green2);padding:10px;margin-bottom:12px;color:#ddd}
.footer{max-width:1400px;margin:auto;padding:20px;color:#777;font-size:12px;line-height:1.5}
.loading{padding:30px;text-align:center;color:#aaa}
.empty{padding:40px;text-align:center;color:#999;background:var(--panel);border:2px solid var(--line)}
@media(max-width:1120px){.wrap{grid-template-columns:200px minmax(0,1fr)}.detail{grid-column:1/-1;position:static}.detail-inner{max-width:900px}}
@media(max-width:760px){.wrap{grid-template-columns:1fr}.side{display:none}.top{flex-wrap:wrap}.search{order:3;flex-basis:100%}.status{margin-left:0}}
</style>
</head>
<body>
<header class="top">
  <div class="logo">⛏ <span>Block</span>pedia</div>
  <input id="search" class="search" placeholder="Search every Minecraft block..." autocomplete="off">
  <select id="sort" title="Sort blocks">
    <option value="name">A–Z</option>
    <option value="hardness">Hardness</option>
    <option value="id">Registry order</option>
  </select>
</header>

<div class="wrap">
  <aside class="panel side">
    <h3>BLOCK INDEX</h3>
    <button data-cat="All" class="active">All blocks <span id="allCount" class="count">—</span></button>
    <button data-cat="Building">Building <span id="buildingCount" class="count">—</span></button>
    <button data-cat="Natural">Natural <span id="naturalCount" class="count">—</span></button>
    <button data-cat="Ores">Ores & minerals <span id="oreCount" class="count">—</span></button>
    <button data-cat="Wood">Wood & plants <span id="woodCount" class="count">—</span></button>
    <button data-cat="Decorative">Decorative <span id="decorCount" class="count">—</span></button>
    <button data-cat="Utility">Utility & redstone <span id="utilityCount" class="count">—</span></button>
    <button data-cat="Nether">Nether <span id="netherCount" class="count">—</span></button>
    <button data-cat="End">End <span id="endCount" class="count">—</span></button>
  </aside>

  <main>
    <section class="panel hero">
      <h1>Minecraft Block Encyclopedia</h1>
      <p>Browse the current Java Edition 26.3 block registry like a giant in-game reference book.</p>
    </section>
    <div class="notice">
      <b>Live data:</b> the block list, hardness, mining material, state data and stack sizes are loaded from a 26.3 data set.
      Recipe, location and renewability notes are presented as a player guide and link to the Minecraft Wiki for the full page.
    </div>
    <div class="bar">
      <select id="filter">
        <option value="all">All gameplay blocks</option>
        <option value="technical">Include technical/hidden blocks</option>
      </select>
      <div id="status" class="status">Loading…</div>
    </div>
    <div id="grid" class="grid"></div>
  </main>

  <aside id="detail" class="panel detail">
    <div class="detail-inner loading">Select a block to see its book page.</div>
  </aside>
</div>

<div class="footer">
  <b>Sources:</b> Minecraft Java Edition 26.3 release notes; RosegoldMC minecraft-data.cr 26.3 registry data; Minecraft Wiki hardness reference.
  This is a fan-made reference site and is not affiliated with Mojang or Microsoft.
</div>

<script>
const SOURCES = {
  blocks:'https://raw.githubusercontent.com/RosegoldMC/minecraft-data.cr/main/data/26.3/blocks.json',
  items:'https://raw.githubusercontent.com/RosegoldMC/minecraft-data.cr/main/data/26.3/items.json',
  wiki:'https://minecraft.wiki/w/'
};

let blocks=[], items=[], itemMap={}, currentCat='All', includeTechnical=false;

const fallback = [
  {name:'stone',hardness:1.5,material:'mineable/pickaxe'},
  {name:'dirt',hardness:.5,material:'mineable/shovel'},
  {name:'grass_block',hardness:.6,material:'mineable/shovel'},
  {name:'cobblestone',hardness:2,material:'mineable/pickaxe'},
  {name:'oak_planks',hardness:2,material:'mineable/axe'},
  {name:'oak_log',hardness:2,material:'mineable/axe'},
  {name:'glass',hardness:.3,material:'default'},
  {name:'sand',hardness:.5,material:'mineable/shovel'},
  {name:'gravel',hardness:.6,material:'mineable/shovel'},
  {name:'coal_ore',hardness:3,material:'mineable/pickaxe'},
  {name:'iron_ore',hardness:3,material:'incorrect_for_wooden_tool'},
  {name:'diamond_ore',hardness:3,material:'incorrect_for_iron_tool'},
  {name:'obsidian',hardness:50,material:'incorrect_for_diamond_tool'},
  {name:'netherrack',hardness:.4,material:'mineable/pickaxe'},
  {name:'end_stone',hardness:3,material:'mineable/pickaxe'},
  {name:'red_wool',hardness:.8,material:'wool'}
];

const $ = id => document.getElementById(id);
function pretty(s){return s.split('_').map(w=>w.charAt(0).toUpperCase()+w.slice(1)).join(' ').replace(/Mc/i,'Mc')}
function esc(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}

function category(b){
  const n=b.name;
  if(/ore|raw_|diamond|emerald|lapis|coal|redstone|copper|gold|iron|quartz|ancient_debris|netherite|amethyst|heavy_core|cinnabar|sulfur/.test(n)) return 'Ores';
  if(/log|wood|planks|stem|hyphae|leaves|sapling|propagule|mangrove|bamboo|mushroom|flower|grass|fern|vine|roots|crop|cactus|sugar_cane|melon|pumpkin|wheat|beetroot|carrots|potatoes|chorus/.test(n)) return 'Wood';
  if(/brick|stone|deepslate|tuff|granite|diorite|andesite|sandstone|prismarine|concrete|terracotta|mud|resin|cobblestone|basalt|blackstone|purpur|end_stone|nylium|netherrack/.test(n)) return 'Building';
  if(/nether|soul_|crimson|warped|basalt|magma|glowstone|quartz/.test(n)) return 'Nether';
  if(/end_|purpur|chorus/.test(n)) return 'End';
  if(/door|trapdoor|button|lever|pressure_plate|rail|piston|observer|hopper|dispenser|dropper|redstone|comparator|repeater|tripwire|note_block|target|crafter|crafting_table|furnace|blast_furnace|smoker|anvil|chest|barrel|shulker|beacon|brewing|enchant|smithing|loom|cartography|grindstone|stonecutter|lectern|shelf|campfire|lantern|torch|bed|sign|bell|beehive|jukebox/.test(n)) return 'Utility';
  if(/glass|pane|wool|carpet|candle|banner|painting|sculk|coral|sea_lantern|lantern|bookshelf|pot|decorated|flower|head|skull|fence|wall|stairs|slab/.test(n)) return 'Decorative';
  if(/air|water|lava|void/.test(n)) return 'Technical';
  return 'Natural';
}

function guide(b){
  const n=b.name;
  let craft='Not craftable as a simple recipe, or recipe varies.';
  let find='World generation or a structure/biome; see the linked wiki page for exact locations.';
  let renewable='See source';
  if(/_planks$/.test(n)){ craft='1 matching log/wood → 4 planks'; find='Crafted from the matching tree/wood; obtain logs from the corresponding biome.'; renewable='Usually renewable';}
  else if(/_log$|_wood$|_stem$|_hyphae$/.test(n)){ craft='Not usually crafted; obtained from a matching tree or fungus.'; find=/crimson|warped/.test(n)?'Nether forests (Crimson/Warped Forests).':'The matching Overworld tree biome.'; renewable='Renewable'}
  else if(/_leaves$/.test(n)){ craft='Usually not crafted; use natural generation or leaf blocks from trees.'; find='Attached to the matching trees; some varieties can be grown.'; renewable='Renewable'}
  else if(/_sapling$|propagule$/.test(n)){ craft='Not crafted; obtained from matching foliage/trees.'; find='Dropped/generated by the corresponding tree type.'; renewable='Renewable'}
  else if(/_ore$/.test(n)){ craft='Not normally crafted.'; find=/nether_/.test(n)?'Nether':'Overworld underground'; renewable='Usually non-renewable'}
  else if(/_stairs$/.test(n)){ craft='Typical recipe: 6 matching blocks → 4 stairs (some sets use stonecutter).'; find='Crafted from the matching block or stonecut in the stonecutter.'; renewable='Depends on base block'}
  else if(/_slab$/.test(n)){ craft='Typical recipe: 3 matching blocks → 6 slabs (or stonecutter).'; find='Crafted from the matching block or stonecut in the stonecutter.'; renewable='Depends on base block'}
  else if(/_wall$/.test(n)){ craft='Typical recipe: 6 matching blocks → 6 walls, or stonecutter.'; find='Crafted from the matching block or stonecut.'; renewable='Depends on base block'}
  else if(n==='glass'){craft='Smelt sand → glass';find='Smelt sand in a furnace, or find naturally in generated structures';renewable='Renewable'}
  else if(/wool$/.test(n)){craft='4 matching wool items → 1 block';find='Sheep and crafted dye variants';renewable='Renewable'}
  else if(n==='stone'){craft='Smelt cobblestone → stone';find='Underground in the Overworld';renewable='Renewable'}
  else if(n==='cobblestone'){craft='Not normally crafted; mined from stone or generated by lava + water';find='Underground / cobblestone generators';renewable='Renewable'}
  else if(n==='sand'||n==='red_sand'){craft='Not normally crafted';find='Deserts, beaches and some badlands terrain';renewable='Limited/renewable by trading in some versions'}
  else if(n==='gravel'){craft='Not normally crafted';find='Underground, beaches, rivers and some Nether terrain';renewable='Renewable via some mechanics'}
  else if(/^(bedrock|reinforced_deepslate)$/.test(n)){craft='Cannot be crafted in Survival';find='Special world/structure generation';renewable='Non-renewable'}
  else if(/^(water|lava)$/.test(n)){craft='Placed using a bucket; infinite sources can be created in certain situations';find='Natural world generation';renewable='Renewable'}
  else if(/^(diamond_block|gold_block|iron_block|copper_block|coal_block|lapis_block)$/.test(n)){craft='9 matching ingots/items → 1 block';find='Crafted from the matching resource';renewable='Depends on resource'}
  return {craft,find,renewable};
}

function toolNames(b){
  const mat=b.material||'default';
  if(mat.includes('axe')) return 'Axe (material dependent)';
  if(mat.includes('shovel')) return 'Shovel';
  if(mat.includes('hoe')) return 'Hoe';
  if(mat.includes('pickaxe')) return 'Pickaxe';
  if(mat==='wool') return 'Shears / hand';
  if(mat==='leaves;mineable/hoe'||mat.includes('leaves')) return 'Hoe / shears';
  return 'Any / special';
}

function imgUrl(n){return 'https://mcasset.cloud/26.3/assets/minecraft/textures/block/'+n+'.png'}

function render(){
  const q=$('search').value.trim().toLowerCase();
  let arr=blocks.filter(b=>includeTechnical || category(b)!=='Technical');
  if(currentCat!=='All') arr=arr.filter(b=>category(b)===currentCat);
  if(q) arr=arr.filter(b=>(b.name+' '+pretty(b.name)).toLowerCase().includes(q));
  const sort=$('sort').value;
  arr.sort((a,b)=>sort==='hardness'?(b.hardness??-999)-(a.hardness??-999):sort==='id'?(a.minStateId??0)-(b.minStateId??0):pretty(a.name).localeCompare(pretty(b.name)));
  $('status').textContent=`Showing ${arr.length.toLocaleString()} of ${blocks.length.toLocaleString()} blocks`;
  const grid=$('grid');
  if(!arr.length){grid.innerHTML='<div class="empty">No blocks match that search.</div>';return}
  grid.innerHTML=arr.map(b=>{
    const hardness=(b.hardness===-1?'∞ / unbreakable':b.hardness);
    return `<article class="card" onclick="showDetail('${esc(b.name)}')">
      <div class="thumb"><img src="${imgUrl(b.name)}" alt="" onerror="this.style.display='none'"><div class="cube">▧</div></div>
      <div class="name">${esc(pretty(b.name))}</div>
      <div class="mini">Hardness: ${esc(String(hardness))}</div>
      <div class="mini">${esc(toolNames(b))}</div>
    </article>`
  }).join('');
  grid.querySelectorAll('.card').forEach(c=>c.querySelector('img')?.addEventListener('load',e=>e.target.nextElementSibling.style.display='none'));
}

function showDetail(name){
  const b=blocks.find(x=>x.name===name); if(!b)return;
  const stack=(itemMap[b.name]?.stackSize) ?? 64;
  const g=guide(b);
  const hardness=b.hardness===-1?'Unbreakable':b.hardness;
  const states=b.states?.length ? b.states.map(s=>`${s.name} (${s.num_values})`).join(', ') : 'None';
  const tags=[category(b),b.material||'default'];
  $('detail').innerHTML=`<div class="detail-inner">
    <div class="detail-head">
      <div class="bigthumb"><img src="${imgUrl(b.name)}" alt="" onerror="this.style.display='none'"><span class="cube">▧</span></div>
      <div><h2>${esc(pretty(b.name))}</h2><div class="id">minecraft:${esc(b.name)}</div></div>
    </div>
    <div class="stats">
      <div class="stat"><b>Hardness</b>${esc(String(hardness))}</div>
      <div class="stat"><b>Stack size</b>${esc(String(stack))}</div>
      <div class="stat"><b>Best tool</b>${esc(toolNames(b))}</div>
      <div class="stat"><b>Category</b>${esc(category(b))}</div>
      <div class="stat"><b>State IDs</b>${b.minStateId??'?'}–${b.maxStateId??'?'}</div>
      <div class="stat"><b>States</b>${esc(String(states))}</div>
    </div>
    <div class="section"><h3>Properties</h3><div class="box">${tags.map(t=>`<span class="tag">${esc(t)}</span>`).join('')}</div></div>
    <div class="section"><h3>How to craft / obtain</h3><div class="box">${esc(g.craft)}</div></div>
    <div class="section"><h3>Where to find it</h3><div class="box">${esc(g.find)}</div></div>
    <div class="section"><h3>Renewability</h3><div class="box">${esc(g.renewable)}</div></div>
    <div class="section"><h3>Wiki page</h3><div class="box"><a class="source" target="_blank" rel="noopener" href="${SOURCES.wiki+encodeURIComponent(pretty(b.name).replaceAll(' ','_'))}">Open the full Minecraft Wiki entry →</a></div></div>
  </div>`;
}

async function load(){
  $('grid').innerHTML='<div class="loading">Loading the 26.3 block registry…</div>';
  try{
    const [br,ir]=await Promise.all([fetch(SOURCES.blocks),fetch(SOURCES.items)]);
    if(!br.ok||!ir.ok) throw new Error('data fetch failed');
    blocks=await br.json(); items=await ir.json(); itemMap=Object.fromEntries(items.map(i=>[i.name,i]));
  }catch(e){
    blocks=fallback; items=[]; itemMap={};
    $('status').textContent='Live registry could not be loaded; showing a small offline fallback.';
  }
  const counts={All:0,Building:0,Natural:0,Ores:0,Wood:0,Decorative:0,Utility:0,Nether:0,End:0};
  blocks.forEach(b=>{counts.All++;const c=category(b);if(c in counts)counts[c]++});
  for(const k of Object.keys(counts)){const el=$(k==='All'?'allCount':k==='Ores'?'oreCount':k==='Wood'?'woodCount':k==='Decorative'?'decorCount':k==='Utility'?'utilityCount':k.toLowerCase()+'Count');if(el)el.textContent=counts[k]}
  render();
  const first=blocks.find(b=>b.name==='stone')||blocks[0]; if(first)showDetail(first.name);
}

document.querySelectorAll('.side button[data-cat]').forEach(btn=>btn.onclick=()=>{
  document.querySelectorAll('.side button[data-cat]').forEach(x=>x.classList.remove('active'));
  btn.classList.add('active'); currentCat=btn.dataset.cat; render();
});
$('search').addEventListener('input',render);
$('sort').addEventListener('change',render);
$('filter').addEventListener('change',e=>{includeTechnical=e.target.value==='technical';render()});
load();
</script>
</body>
</html>
