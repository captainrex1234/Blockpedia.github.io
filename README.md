# Blockpedia.github.io
The Minecraft blockpedia for you and you friends to use


<!doctype html>
<html lang="en">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width,initial-scale=1">
<title>Blockpedia — Minecraft Block Encyclopedia</title>
<style>
:root{
 --bg:#0e0e0e;--panel:#202020;--panel2:#292929;--panel3:#353535;
 --green:#55a83d;--green2:#78cf53;--text:#f3f3f3;--muted:#aaa;
 --line:#484848;--gold:#e5c65a;--blue:#77bce9;--red:#d95845
}
*{box-sizing:border-box}
html{scroll-behavior:smooth}
body{margin:0;background:linear-gradient(#121212,#0b0b0b);color:var(--text);font-family:Arial,Helvetica,sans-serif}
button,input,select{font:inherit}
a{color:var(--blue)}
.top{
 position:sticky;top:0;z-index:20;display:flex;gap:11px;align-items:center;
 padding:10px 17px;background:#1d1d1d;border-bottom:4px solid #090909;
 box-shadow:0 3px 0 #060606
}
.logo{font-weight:900;font-size:22px;white-space:nowrap;text-shadow:2px 2px #000;cursor:pointer}
.logo span{color:var(--green2)}
.search{flex:1;min-width:170px;background:#101010;color:#fff;border:2px solid #555;border-radius:3px;padding:10px 12px}
.btn,.navbtn{
 border:2px solid #111;border-radius:3px;background:var(--green);color:white;
 padding:9px 13px;font-weight:800;cursor:pointer;box-shadow:inset 0 -3px rgba(0,0,0,.25)
}
.btn:hover,.navbtn:hover{background:var(--green2)}
.navbtn.secondary{background:#383838}
.wrap{max-width:1450px;margin:auto;padding:18px;display:grid;grid-template-columns:220px minmax(0,1fr) 345px;gap:18px}
.panel{background:var(--panel);border:2px solid var(--line);box-shadow:0 3px 0 #080808}
.side{padding:14px;height:max-content;position:sticky;top:76px}
.side h3{font-size:12px;color:#8fd45e;margin:3px 0 8px;letter-spacing:.7px}
.side button{display:block;width:100%;text-align:left;border:0;background:transparent;color:#ddd;padding:8px;border-radius:2px;cursor:pointer}
.side button:hover,.side button.active{background:#3b552f}
.count{float:right;color:#888;font-size:12px}
.main{min-width:0}
.hero{
 padding:21px;margin-bottom:14px;background:
 linear-gradient(rgba(54,54,54,.94),rgba(24,24,24,.96)),
 repeating-linear-gradient(45deg,#333 0 14px,#2d2d2d 14px 28px)
}
.hero h1{margin:0 0 6px;font-size:34px}.hero p{margin:0;color:#bdbdbd;line-height:1.5}
.toolbar{display:flex;gap:8px;align-items:center;flex-wrap:wrap;margin-bottom:12px}
.toolbar select{background:#151515;color:#eee;border:2px solid #555;border-radius:3px;padding:9px}
.status{margin-left:auto;color:#999;font-size:13px}
.notice{background:#24361d;border-left:5px solid var(--green2);padding:11px;margin:0 0 13px;line-height:1.45}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(180px,1fr));gap:11px}
.card{
 background:var(--panel);border:2px solid #454545;box-shadow:0 2px 0 #090909;
 padding:10px;cursor:pointer;min-height:210px;display:flex;flex-direction:column;
 transition:.08s
}
.card:hover{border-color:var(--green2);transform:translateY(-1px)}
.thumb{height:125px;border:2px solid #555;background:
 repeating-conic-gradient(#373737 0 25%,#2f2f2f 0 50%) 50%/22px 22px;
 display:flex;align-items:center;justify-content:center;overflow:hidden}
.thumb img{image-rendering:pixelated;width:102px;height:102px;object-fit:contain;display:block}
.thumb .emoji{font-size:53px;text-shadow:4px 4px #111}
.name{font-weight:900;margin-top:9px;line-height:1.15}.mini{color:#999;font-size:12px;margin-top:4px}
.card .open{margin-top:auto;color:#86d35f;font-size:11px;text-transform:uppercase;letter-spacing:.5px;padding-top:8px}
.detail{padding:14px;position:sticky;top:76px;height:max-content}
.detail-inner{min-height:140px}
.detail-head{display:flex;gap:12px;align-items:center;border-bottom:2px solid #454545;padding-bottom:12px}
.bigthumb{width:114px;height:114px;flex:none;background:repeating-conic-gradient(#373737 0 25%,#2f2f2f 0 50%) 50%/22px 22px;border:2px solid #555;display:flex;align-items:center;justify-content:center;overflow:hidden}
.bigthumb img{image-rendering:pixelated;width:98px;height:98px;object-fit:contain}
.detail h2{margin:0;font-size:23px;line-height:1.15}.id{color:#888;font:12px monospace;margin-top:4px;word-break:break-all}
.stats{display:grid;grid-template-columns:1fr 1fr;margin-top:12px;border:1px solid #4b4b4b}
.stat{padding:9px;border-right:1px solid #4b4b4b;border-bottom:1px solid #4b4b4b}.stat:nth-child(2n){border-right:0}
.stat b{display:block;color:#aaa;font-size:11px;text-transform:uppercase;margin-bottom:4px}
.section{margin-top:13px}.section h3{font-size:14px;margin:0 0 6px;color:#8ed45d}
.box{background:#181818;border:1px solid #454545;padding:9px;line-height:1.5;font-size:13px}
.tag{display:inline-block;background:#3a3a3a;border:1px solid #555;border-radius:3px;padding:3px 6px;margin:2px 3px 2px 0;font-size:11px}
.back{margin-bottom:12px}
.homeHero{text-align:center;padding:34px 24px}
.homeHero h1{font-size:42px;margin:0 0 7px;text-shadow:3px 3px #000}.homeHero p{color:#bbb;max-width:720px;margin:0 auto;line-height:1.55}
.quick{display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin:15px 0}
.quick .card{min-height:145px}
.quick .card h3{margin:0 0 5px;color:#90d866}
.articleGrid{display:grid;grid-template-columns:repeat(auto-fit,minmax(230px,1fr));gap:12px}
.articleCard{background:var(--panel);border:2px solid var(--line);box-shadow:0 2px 0 #070707;cursor:pointer;overflow:hidden}
.articleCard:hover{border-color:var(--green2)}
.articlePic{height:145px;background:#303030;display:flex;align-items:center;justify-content:center}
.articlePic img{width:120px;height:120px;image-rendering:pixelated;object-fit:contain}
.articleBody{padding:12px}.articleBody h3{margin:0 0 6px}.articleBody p{margin:0;color:#aaa;font-size:13px;line-height:1.45}
.articlePage{padding:18px}.articlePage h1{margin:0 0 7px;font-size:34px}.articleMeta{color:#888;font-size:12px;margin-bottom:15px}
.articleText{line-height:1.65;color:#ddd}.articleText h2{border-bottom:2px solid #454545;padding-bottom:7px}
.articleText ul{padding-left:22px}
.related{display:grid;grid-template-columns:repeat(auto-fill,minmax(140px,1fr));gap:8px}
.related .miniCard{background:#171717;border:1px solid #444;padding:9px;cursor:pointer}.miniCard:hover{border-color:var(--green2)}
.empty,.loading{padding:35px;text-align:center;color:#999;background:var(--panel);border:2px solid var(--line)}
.footer{max-width:1450px;margin:auto;padding:20px;color:#777;font-size:12px;line-height:1.6}
@media(max-width:1160px){.wrap{grid-template-columns:205px minmax(0,1fr)}.detail{grid-column:1/-1;position:static}}
@media(max-width:780px){.wrap{grid-template-columns:1fr}.side{display:none}.top{flex-wrap:wrap}.search{order:3;flex-basis:100%}.status{margin-left:0}.quick{grid-template-columns:1fr}.homeHero h1{font-size:32px}}
</style>
</head>
<body>
<header class="top">
  <div class="logo" onclick="home()">⛏ <span>Block</span>pedia</div>
  <input id="search" class="search" placeholder="Search blocks, articles, or anything..." autocomplete="off">
  <button class="navbtn" onclick="home()">Home</button>
  <button class="navbtn secondary" onclick="showBlocks()">Blocks</button>
</header>

<div class="wrap">
  <aside class="panel side">
    <h3>SITE</h3>
    <button id="homeSide" onclick="home()">Home</button>
    <button id="articlesSide" onclick="home('articles')">Featured Articles</button>
    <button onclick="showBlocks()">All Blocks</button>

    <h3 style="margin-top:18px">BLOCK INDEX</h3>
    <button data-cat="All">All blocks <span id="allCount" class="count">—</span></button>
    <button data-cat="Building">Building <span id="buildingCount" class="count">—</span></button>
    <button data-cat="Natural">Natural <span id="naturalCount" class="count">—</span></button>
    <button data-cat="Ores">Ores & minerals <span id="oreCount" class="count">—</span></button>
    <button data-cat="Wood">Wood & plants <span id="woodCount" class="count">—</span></button>
    <button data-cat="Decorative">Decorative <span id="decorCount" class="count">—</span></button>
    <button data-cat="Utility">Utility & redstone <span id="utilityCount" class="count">—</span></button>
    <button data-cat="Nether">Nether <span id="netherCount" class="count">—</span></button>
    <button data-cat="End">End <span id="endCount" class="count">—</span></button>
  </aside>

  <main class="main">
    <div id="main"></div>
  </main>

  <aside id="detail" class="panel detail">
    <div class="detail-inner loading">Open a block to see its full encyclopedia entry.</div>
  </aside>
</div>

<div class="footer">
  <b>Blockpedia 26.3:</b> fan-made Minecraft reference interface. The live registry and textures are loaded from the Minecraft 26.3 asset/data ecosystem. Always verify version-specific recipes and mechanics on the linked Minecraft Wiki page.
</div>

<script>
const SOURCES = {
  blocks:'https://raw.githubusercontent.com/RosegoldMC/minecraft-data.cr/main/data/26.3/blocks.json',
  items:'https://raw.githubusercontent.com/RosegoldMC/minecraft-data.cr/main/data/26.3/items.json',
  blockImg:'https://mcasset.cloud/26.3/assets/minecraft/textures/block/',
  itemImg:'https://mcasset.cloud/26.3/assets/minecraft/textures/item/',
  wiki:'https://minecraft.wiki/w/'
};

let blocks=[], items=[], itemMap={}, currentCat='All', includeTechnical=false;
let currentView='home';

const fallback=[
{name:'stone',hardness:1.5,material:'mineable/pickaxe'},{name:'dirt',hardness:.5,material:'mineable/shovel'},
{name:'grass_block',hardness:.6,material:'mineable/shovel'},{name:'cobblestone',hardness:2,material:'mineable/pickaxe'},
{name:'oak_planks',hardness:2,material:'mineable/axe'},{name:'oak_log',hardness:2,material:'mineable/axe'},
{name:'glass',hardness:.3,material:'default'},{name:'sand',hardness:.5,material:'mineable/shovel'},
{name:'gravel',hardness:.6,material:'mineable/shovel'},{name:'coal_ore',hardness:3,material:'mineable/pickaxe'},
{name:'iron_ore',hardness:3,material:'mineable/pickaxe'},{name:'diamond_ore',hardness:3,material:'mineable/pickaxe'},
{name:'obsidian',hardness:50,material:'mineable/pickaxe'},{name:'netherrack',hardness:.4,material:'mineable/pickaxe'},
{name:'end_stone',hardness:3,material:'mineable/pickaxe'},{name:'red_wool',hardness:.8,material:'wool'}
];

const $=id=>document.getElementById(id);
const pretty=s=>s.split('_').map(w=>w.charAt(0).toUpperCase()+w.slice(1)).join(' ');
const esc=s=>String(s??'').replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]));
const cleanName=n=>encodeURIComponent(pretty(n).replaceAll(' ','_'));

function cat(b){
 const n=b.name;
 if(/ore|raw_|diamond|emerald|lapis|coal|redstone|copper|gold|iron|quartz|ancient_debris|netherite|amethyst|heavy_core|sulfur/.test(n))return 'Ores';
 if(/log|wood|planks|stem|hyphae|leaves|sapling|propagule|mangrove|bamboo|mushroom|flower|grass|fern|vine|roots|crop|cactus|sugar_cane|melon|pumpkin|wheat|beetroot|carrots|potatoes|chorus/.test(n))return 'Wood';
 if(/brick|stone|deepslate|tuff|granite|diorite|andesite|sandstone|prismarine|concrete|terracotta|mud|resin|cobblestone|basalt|blackstone|purpur|end_stone|nylium|netherrack/.test(n))return 'Building';
 if(/nether|soul_|crimson|warped|basalt|magma|glowstone|quartz/.test(n))return 'Nether';
 if(/end_|purpur|chorus/.test(n))return 'End';
 if(/door|trapdoor|button|lever|pressure_plate|rail|piston|observer|hopper|dispenser|dropper|redstone|comparator|repeater|tripwire|note_block|target|crafter|crafting_table|furnace|blast_furnace|smoker|anvil|chest|barrel|shulker|beacon|brewing|enchant|smithing|loom|cartography|grindstone|stonecutter|lectern|shelf|campfire|lantern|torch|bed|sign|bell|beehive|jukebox/.test(n))return 'Utility';
 if(/glass|pane|wool|carpet|candle|banner|painting|sculk|coral|sea_lantern|bookshelf|pot|decorated|head|skull|fence|wall|stairs|slab/.test(n))return 'Decorative';
 if(/air|water|lava|void|moving_piston|bubble_column/.test(n))return 'Technical';
 return 'Natural';
}

function guide(b){
 const n=b.name;
 let craft='Not craftable as a simple recipe, or the recipe depends on the block set.';
 let find='World generation or a structure/biome; open the linked Minecraft Wiki entry for exact locations.';
 let renewable='See the full linked entry';
 if(/_planks$/.test(n)){craft='1 matching log or wood → 4 planks';find='Crafted from the matching tree wood';renewable='Usually renewable'}
 else if(/_log$|_wood$|_stem$|_hyphae$/.test(n)){craft='Usually obtained from a matching tree or fungus';find=/crimson|warped/.test(n)?'Nether forests':'The matching tree biome';renewable='Renewable'}
 else if(/_leaves$/.test(n)){craft='Obtained from trees; not normally crafted';find='Attached to the corresponding tree';renewable='Renewable'}
 else if(/_sapling$|propagule$/.test(n)){craft='Not normally crafted';find='Dropped/generated by the corresponding tree leaves';renewable='Renewable'}
 else if(/_ore$/.test(n)){craft='Not normally crafted';find=/nether_/.test(n)?'Nether underground':'Overworld underground';renewable='Usually non-renewable'}
 else if(/_stairs$/.test(n)){craft='Common pattern: 6 matching blocks → 4 stairs; some sets also use the stonecutter';find='Crafted or stonecut from the matching block';renewable='Depends on the base block'}
 else if(/_slab$/.test(n)){craft='Common pattern: 3 matching blocks → 6 slabs; some sets also use the stonecutter';find='Crafted or stonecut from the matching block';renewable='Depends on the base block'}
 else if(/_wall$/.test(n)){craft='Common pattern: 6 matching blocks → 6 walls; some sets also use the stonecutter';find='Crafted or stonecut from the matching block';renewable='Depends on the base block'}
 else if(n==='glass'){craft='Smelt sand → glass';find='Smelt sand or obtain from generated structures';renewable='Renewable'}
 else if(/wool$/.test(n)){craft='Use 4 matching wool items to make a block';find='Sheep; dye white wool for colored variants';renewable='Renewable'}
 else if(n==='stone'){craft='Smelt cobblestone → stone';find='Underground in the Overworld';renewable='Renewable'}
 else if(n==='cobblestone'){craft='Mined from stone or generated by lava + water';find='Underground and in generated structures';renewable='Renewable'}
 else if(n==='sand'||n==='red_sand'){craft='Not normally crafted';find='Deserts, beaches and related terrain';renewable='Limited; check version-specific renewable mechanics'}
 else if(n==='gravel'){craft='Not normally crafted';find='Underground, rivers, beaches and some Nether terrain';renewable='Renewable through some mechanics'}
 else if(/^(bedrock|reinforced_deepslate)$/.test(n)){craft='Cannot be crafted in Survival';find='Special world/structure generation';renewable='Non-renewable'}
 else if(/^(water|lava)$/.test(n)){craft='Placed with a bucket; source mechanics can make renewable supplies';find='Natural world generation';renewable='Renewable'}
 else if(/^(diamond_block|gold_block|iron_block|copper_block|coal_block|lapis_block|redstone_block)$/.test(n)){craft='Usually 9 matching resource items → 1 block';find='Crafted from the matching resource';renewable='Depends on the resource'}
 return {craft,find,renewable};
}

function toolName(b){
 const m=b.material||'';
 if(m.includes('axe'))return 'Axe';
 if(m.includes('shovel'))return 'Shovel';
 if(m.includes('hoe'))return 'Hoe';
 if(m.includes('pickaxe'))return 'Pickaxe';
 if(m==='wool')return 'Shears / hand';
 return 'Any / special';
}

function picture(name,cls=''){
 const bid='img_'+Math.random().toString(36).slice(2);
 setTimeout(()=>{
   const img=document.getElementById(bid); if(!img)return;
   img.onerror=function(){if(this.dataset.fallback!=='1'){this.dataset.fallback='1';this.src=SOURCES.itemImg+name+'.png'}else{this.style.display='none';const e=this.nextElementSibling;if(e)e.style.display='block'}};
   img.src=SOURCES.blockImg+name+'.png';
 },0);
 return `<img id="${bid}" class="${cls}" alt="${esc(pretty(name))} texture"><div class="emoji" style="display:none">▧</div>`;
}

const articles=[
 {id:'mining-basics',title:'Mining Basics',tag:'Guide',image:'stone',desc:'A starter guide to hardness, tools, and choosing the right block to mine.'},
 {id:'ore-hunting',title:'Ore Hunting Guide',tag:'Guide',image:'diamond_ore',desc:'Learn where the major ores generate and what tools you need.'},
 {id:'wood-sets',title:'Wood Sets',tag:'Building',image:'oak_log',desc:'A quick tour of logs, planks, leaves, slabs, stairs, fences, doors and more.'},
 {id:'nether-building',title:'Building in the Nether',tag:'Nether',image:'netherrack',desc:'Key Nether building blocks and where to get them.'},
 {id:'redstone-101',title:'Redstone 101',tag:'Technical',image:'redstone_block',desc:'Start exploring redstone components and useful block properties.'},
 {id:'new-in-263',title:'What’s New in 26.3',tag:'Update',image:'poplar_leaves',desc:'New Wilderness Bound content, including Poplar wood and colorful leaves.'}
];

function articleView(a){
 const related={
  'mining-basics':['stone','deepslate','cobblestone','obsidian'],
  'ore-hunting':['coal_ore','iron_ore','gold_ore','diamond_ore','emerald_ore','redstone_ore'],
  'wood-sets':['oak_log','oak_planks','oak_leaves','oak_stairs','oak_slab'],
  'nether-building':['netherrack','basalt','blackstone','nether_bricks','soul_sand'],
  'redstone-101':['redstone_block','redstone_torch','piston','observer','hopper'],
  'new-in-263':['poplar_log','poplar_planks','red_poplar_leaves','orange_poplar_leaves','yellow_poplar_leaves','wool_stairs','white_concrete_stairs']
 }[a.id]||[];
 return `<div class="panel articlePage">
   <button class="btn back" onclick="home('articles')">← Back to articles</button>
   <h1>${esc(a.title)}</h1>
   <div class="articleMeta">${esc(a.tag)} · Blockpedia guide</div>
   <div class="articleText">${articleCopy(a.id)}</div>
   <h2>Related blocks</h2>
   <div class="related">${related.map(n=>blocks.find(b=>b.name===n)).filter(Boolean).map(b=>`<div class="miniCard" onclick="showBlocks('${esc(b.name)}')"><b>${esc(pretty(b.name))}</b><div style="color:#888;font-size:11px;margin-top:4px">Open block entry →</div></div>`).join('')}</div>
 </div>`;
}

function articleCopy(id){
 const copy={
  'mining-basics':`<p>Mining is one of the core loops of Minecraft. <b>Hardness</b> measures how long a block takes to break by hand or with the appropriate tool; the fastest tool also depends on the block's mining material.</p>
   <h2>Picking a tool</h2><p>Pickaxes are used for many stone and ore blocks, axes for wood, and shovels for dirt-like terrain. The block page on this site shows the material/tool family whenever the registry exposes it.</p>
   <h2>Why hardness matters</h2><p>Higher hardness generally means a longer break time. Some blocks such as bedrock are effectively unbreakable in normal Survival play.</p>`,
  'ore-hunting':`<p>Ores are mineral blocks that generate in the world and can usually be mined with a pickaxe of an appropriate tier. The exact generation rules vary by version and ore.</p>
   <h2>Useful habits</h2><ul><li>Bring the correct pickaxe tier before mining valuable ores.</li><li>Check the block entry for the ore's hardness and linked Wiki details.</li><li>Use the search bar to jump directly to a specific ore.</li></ul>`,
  'wood-sets':`<p>Wood sets are some of the most versatile building materials. A typical set includes logs, planks, leaves, stairs, slabs, fences, gates, doors and more.</p>
   <h2>Renewability</h2><p>Most normal tree wood is renewable because saplings can grow into new trees. The exact availability of each newer wood family is shown on its block page and linked Wiki entry.</p>`,
  'nether-building':`<p>The Nether has its own collection of building materials, including netherrack, basalt, blackstone, Nether bricks and wood from Crimson and Warped forests.</p>
   <h2>Where to look</h2><p>Use the site's Nether category to browse related blocks, then open a block to see its source and a link to its complete Wiki article.</p>`,
  'redstone-101':`<p>Redstone components let blocks respond to power, signals and player interactions. This encyclopedia includes common redstone-related blocks in the Utility category.</p>
   <h2>Start simple</h2><p>Learn one component at a time, then combine components into circuits. The block entries provide the quick reference information, while the linked Wiki pages provide the deeper mechanics.</p>`,
  'new-in-263':`<p>Minecraft Java Edition 26.3 is the <i>Wilderness Bound</i> release. It added the Dappled Forest biome, Poplar trees, fallen Poplar trees, new colored Poplar leaves, a Poplar wood set, Shelf Mushrooms, Red Shrubs, Abandoned Camps, Explorer Maps, Cushions, Straw Beds, Wool stairs/slabs and Concrete stairs/slabs. citeturn960204search0</p>
   <h2>Poplar wood</h2><p>The new Poplar tree has red, orange and yellow leaf variants, while Poplar Leaves can drop Poplar Saplings that may grow into any of the three variants. citeturn960204search0</p>`
 };
 return copy[id]||'<p>Article coming soon.</p>';
}

function home(anchor=''){
 currentView='home'; $('homeSide').classList.add('active'); $('main').innerHTML=`
 <section class="panel hero homeHero">
   <h1>Welcome to Blockpedia</h1>
   <p>A Minecraft-style reference book for blocks, building materials, locations, tools, recipes, renewability and more.</p>
   <div style="margin-top:17px"><button class="btn" onclick="showBlocks()">Browse every block →</button></div>
 </section>
 <div class="quick">
   <div class="card" onclick="showBlocks()"><h3>🧱 Every Block</h3><p class="mini">Search the current Java Edition block registry.</p></div>
   <div class="card" onclick="home('articles')"><h3>📖 Articles</h3><p class="mini">Guides and reference pages appear here on the home page.</p></div>
   <div class="card" onclick="showBlocks('diamond_ore')"><h3>💎 Quick Search</h3><p class="mini">Open a block instantly and inspect its stats.</p></div>
 </div>
 <section id="articlesSection" class="panel" style="padding:15px">
   <h2 style="margin-top:0">Featured & Recent Articles</h2>
   <div class="articleGrid">${articles.map(a=>`<div class="articleCard" onclick="openArticle('${a.id}')">
     <div class="articlePic">${picture(a.image)}</div>
     <div class="articleBody"><div style="color:#87d35c;font-size:11px;text-transform:uppercase">${esc(a.tag)}</div><h3>${esc(a.title)}</h3><p>${esc(a.desc)}</p></div>
   </div>`).join('')}</div>
 </section>`;
 setTimeout(()=>{if(anchor==='articles')document.getElementById('articlesSection')?.scrollIntoView();},50);
 closeDetail();
}

function showBlocks(openName=''){
 currentView='blocks'; $('homeSide').classList.remove('active');
 $('main').innerHTML=`
 <section class="panel hero">
   <h1>Minecraft Block Encyclopedia</h1>
   <p>Click any block picture or card to open the complete quick-reference entry.</p>
 </section>
 <div class="notice"><b>Images:</b> each card loads its 26.3 block texture, with an item-texture fallback for blocks whose icon is stored separately.</div>
 <div class="toolbar">
   <select id="filter"><option value="all">Gameplay blocks</option><option value="technical">Include technical/hidden blocks</option></select>
   <select id="sort"><option value="name">A–Z</option><option value="hardness">Hardness</option><option value="id">Registry order</option></select>
   <div id="status" class="status">Loading…</div>
 </div>
 <div id="grid" class="grid"></div>`;
 $('filter').addEventListener('change',e=>{includeTechnical=e.target.value==='technical';renderGrid()});
 $('sort').addEventListener('change',renderGrid);
 renderGrid();
 if(openName){setTimeout(()=>showDetail(openName),80)}
}

function renderGrid(){
 let q=$('search').value.trim().toLowerCase();
 let arr=blocks.filter(b=>includeTechnical||cat(b)!=='Technical');
 if(currentCat!=='All')arr=arr.filter(b=>cat(b)===currentCat);
 if(q)arr=arr.filter(b=>(b.name+' '+pretty(b.name)).toLowerCase().includes(q));
 const sort=$('sort')?.value||'name';
 arr.sort((a,b)=>sort==='hardness'?(b.hardness??-999)-(a.hardness??-999):sort==='id'?(a.minStateId??0)-(b.minStateId??0):pretty(a.name).localeCompare(pretty(b.name)));
 $('status').textContent=`Showing ${arr.length.toLocaleString()} of ${blocks.length.toLocaleString()} blocks`;
 $('grid').innerHTML=arr.length?arr.map(b=>{
   const h=b.hardness===-1?'Unbreakable':(b.hardness??'—');
   return `<article class="card" onclick="showDetail('${esc(b.name)}')" title="Open ${esc(pretty(b.name))}">
     <div class="thumb">${picture(b.name)}</div>
     <div class="name">${esc(pretty(b.name))}</div>
     <div class="mini">Hardness: ${esc(String(h))}</div>
     <div class="mini">${esc(toolName(b))}</div>
     <div class="open">View full entry →</div>
   </article>`;
 }).join(''):'<div class="empty">No blocks match that search.</div>';
}

function showDetail(name){
 const b=blocks.find(x=>x.name===name);if(!b)return;
 const stack=itemMap[b.name]?.stackSize??64, g=guide(b), h=b.hardness===-1?'Unbreakable':(b.hardness??'—');
 const states=b.states?.length?b.states.map(s=>`${s.name} (${s.num_values})`).join(', '):'None';
 $('detail').innerHTML=`<div class="detail-inner">
  <button class="btn" onclick="closeDetail()" style="margin-bottom:11px">× Close</button>
  <div class="detail-head">
   <div class="bigthumb">${picture(b.name)}</div>
   <div><h2>${esc(pretty(b.name))}</h2><div class="id">minecraft:${esc(b.name)}</div></div>
  </div>
  <div class="stats">
   <div class="stat"><b>Hardness</b>${esc(String(h))}</div>
   <div class="stat"><b>Stack size</b>${esc(String(stack))}</div>
   <div class="stat"><b>Best tool</b>${esc(toolName(b))}</div>
   <div class="stat"><b>Category</b>${esc(cat(b))}</div>
   <div class="stat"><b>State IDs</b>${b.minStateId??'—'}–${b.maxStateId??'—'}</div>
   <div class="stat"><b>States</b>${esc(String(states))}</div>
  </div>
  <div class="section"><h3>How to craft / obtain</h3><div class="box">${esc(g.craft)}</div></div>
  <div class="section"><h3>Where to find it</h3><div class="box">${esc(g.find)}</div></div>
  <div class="section"><h3>Renewability</h3><div class="box">${esc(g.renewable)}</div></div>
  <div class="section"><h3>Full information</h3><div class="box"><a target="_blank" rel="noopener" href="${SOURCES.wiki+cleanName(b.name)}">Open the complete Minecraft Wiki article →</a></div></div>
 </div>`;
}

function closeDetail(){
 $('detail').innerHTML='<div class="detail-inner loading">Open a block to see its full encyclopedia entry.</div>';
}

function openArticle(id){
 const a=articles.find(x=>x.id===id);if(!a)return;
 currentView='article';$('homeSide').classList.remove('active');
 $('main').innerHTML=articleView(a);closeDetail();
 window.scrollTo({top:0,behavior:'smooth'});
}

document.querySelectorAll('.side button[data-cat]').forEach(btn=>btn.onclick=()=>{
 currentCat=btn.dataset.cat;
 document.querySelectorAll('.side button[data-cat]').forEach(x=>x.classList.remove('active'));
 btn.classList.add('active');
 if(currentView!=='blocks')showBlocks();
 else renderGrid();
});

$('search').addEventListener('input',()=>{
 if(!$('grid'))showBlocks();
 else renderGrid();
});

async function load(){
 try{
  const [br,ir]=await Promise.all([fetch(SOURCES.blocks),fetch(SOURCES.items)]);
  if(!br.ok||!ir.ok)throw new Error('fetch failed');
  blocks=await br.json();items=await ir.json();itemMap=Object.fromEntries(items.map(i=>[i.name,i]));
 }catch(e){
  blocks=fallback;items=[];itemMap={};
 }
 const counts={All:0,Building:0,Natural:0,Ores:0,Wood:0,Decorative:0,Utility:0,Nether:0,End:0};
 blocks.forEach(b=>{counts.All++;const c=cat(b);if(counts[c]!==undefined)counts[c]++});
 const ids={All:'allCount',Building:'buildingCount',Natural:'naturalCount',Ores:'oreCount',Wood:'woodCount',Decorative:'decorCount',Utility:'utilityCount',Nether:'netherCount',End:'endCount'};
 Object.entries(ids).forEach(([k,id])=>{const el=$(id);if(el)el.textContent=counts[k]});
 document.querySelectorAll('.side button[data-cat]').forEach(x=>x.classList.remove('active'));
 home();
}

load();
</script>
</body>
</html>
