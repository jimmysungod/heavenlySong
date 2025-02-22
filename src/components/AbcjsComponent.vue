<template>
  <main>
    <div class="container">
      <div class="row">
        <p>
          <label for="song-picker">
            Select song:
            <select id="song-picker" v-model="selectedTrack">
              <option value="-1">Select a tune</option>
              <option value="0">天堂咫尺眼前</option>
              <option value="1">聖靈之火</option>
              <option value="2">我神可敬可畏</option>
            </select>
          </label>
        </p>
        <p>
          <label for="instrument-picker">
            Select instrument:
            <select
              id="instrument-picker"
              v-model="instrument"
              @change="setInstrument"
            >
              <option value="0">Acoustic Grand Piano</option>
              <option value="1">Bright Acoustic Piano</option>
              <option value="2">Electric Grand Piano</option>
              <option value="3">Honky-tonk Piano</option>
              <option value="4">Electric Piano 1</option>
              <option value="5">Electric Piano 2</option>
              <option value="6">Harpsichord</option>
              <option value="7">Clavi</option>
              <option value="8">Celesta</option>
              <option value="9">Glockenspiel</option>
              <option value="10">Music Box</option>
              <option value="11">Vibraphone</option>
              <option value="12">Marimba</option>
              <option value="13">Xylophone</option>
              <option value="14">Tubular Bells</option>
              <option value="15">Dulcimer</option>
              <option value="16">Drawbar Organ</option>
              <option value="17">Percussive Organ</option>
              <option value="18">Rock Organ</option>
              <option value="19">Church Organ</option>
              <option value="20">Reed Organ</option>
              <option value="21">Accordion</option>
              <option value="22">Harmonica</option>
              <option value="23">Tango Accordion</option>
              <option value="24">Acoustic Guitar (nylon)</option>
              <option value="25">Acoustic Guitar (steel)</option>
              <option value="26">Electric Guitar (jazz)</option>
              <option value="27">Electric Guitar (clean)</option>
              <option value="28">Electric Guitar (muted)</option>
              <option value="29">Overdriven Guitar</option>
              <option value="30">Distortion Guitar</option>
              <option value="31">Guitar harmonics</option>
              <option value="32">Acoustic Bass</option>
              <option value="33">Electric Bass (finger)</option>
              <option value="34">Electric Bass (pick)</option>
              <option value="35">Fretless Bass</option>
              <option value="36">Slap Bass 1</option>
              <option value="37">Slap Bass 2</option>
              <option value="38">Synth Bass 1</option>
              <option value="39">Synth Bass 2</option>
              <option value="40">Violin</option>
              <option value="41">Viola</option>
              <option value="42">Cello</option>
              <option value="43">Contrabass</option>
              <option value="44">Tremolo Strings</option>
              <option value="45">Pizzicato Strings</option>
              <option value="46">Orchestral Harp</option>
              <option value="47">Timpani</option>
              <option value="48">String Ensemble 1</option>
              <option value="49">String Ensemble 2</option>
              <option value="50">SynthStrings 1</option>
              <option value="51">SynthStrings 2</option>
              <option value="52">Choir Aahs</option>
              <option value="53">Voice Oohs</option>
              <option value="54">Synth Voice</option>
              <option value="55">Orchestra Hit</option>
              <option value="56">Trumpet</option>
              <option value="57">Trombone</option>
              <option value="58">Tuba</option>
              <option value="59">Muted Trumpet</option>
              <option value="60">French Horn</option>
              <option value="61">Brass Section</option>
              <option value="62">SynthBrass 1</option>
              <option value="63">SynthBrass 2</option>
              <option value="64">Soprano Sax</option>
              <option value="65">Alto Sax</option>
              <option value="66">Tenor Sax</option>
              <option value="67">Baritone Sax</option>
              <option value="68">Oboe</option>
              <option value="69">English Horn</option>
              <option value="70">Bassoon</option>
              <option value="71">Clarinet</option>
              <option value="72">Piccolo</option>
              <option value="73">Flute</option>
              <option value="74">Recorder</option>
              <option value="75">Pan Flute</option>
              <option value="76">Blown Bottle</option>
              <option value="77">Shakuhachi</option>
              <option value="78">Whistle</option>
              <option value="79">Ocarina</option>
              <option value="80">Lead 1 (square)</option>
              <option value="81">Lead 2 (sawtooth)</option>
              <option value="82">Lead 3 (calliope)</option>
              <option value="83">Lead 4 (chiff)</option>
              <option value="84">Lead 5 (charang)</option>
              <option value="85">Lead 6 (voice)</option>
              <option value="86">Lead 7 (fifths)</option>
              <option value="87">Lead 8 (bass + lead)</option>
              <option value="88">Pad 1 (new age)</option>
              <option value="89">Pad 2 (warm)</option>
              <option value="90">Pad 3 (polysynth)</option>
              <option value="91">Pad 4 (choir)</option>
              <option value="92">Pad 5 (bowed)</option>
              <option value="93">Pad 6 (metallic)</option>
              <option value="94">Pad 7 (halo)</option>
              <option value="95">Pad 8 (sweep)</option>
              <option value="96">FX 1 (rain)</option>
              <option value="97">FX 2 (soundtrack)</option>
              <option value="98">FX 3 (crystal)</option>
              <option value="99">FX 4 (atmosphere)</option>
              <option value="100">FX 5 (brightness)</option>
              <option value="101">FX 6 (goblins)</option>
              <option value="102">FX 7 (echoes)</option>
              <option value="103">FX 8 (sci-fi)</option>
              <option value="104">Sitar</option>
              <option value="105">Banjo</option>
              <option value="106">Shamisen</option>
              <option value="107">Koto</option>
              <option value="108">Kalimba</option>
              <option value="109">Bag pipe</option>
              <option value="110">Fiddle</option>
              <option value="111">Shanai</option>
              <option value="112">Tinkle Bell</option>
              <option value="113">Agogo</option>
              <option value="114">Steel Drums</option>
              <option value="115">Woodblock</option>
              <option value="116">Taiko Drum</option>
              <option value="117">Melodic Tom</option>
              <option value="118">Synth Drum</option>
              <option value="119">Reverse Cymbal</option>
              <option value="120">Guitar Fret Noise</option>
              <option value="121">Breath Noise</option>
              <option value="122">Seashore</option>
              <option value="123">Bird Tweet</option>
              <option value="124">Telephone Ring</option>
              <option value="125">Helicopter</option>
              <option value="126">Applause</option>
              <option value="127">Gunshot</option>
            </select>
          </label>
        </p>
        <p>
          <button @click="play" :class="{ hidden: playing, 'floating-button': showBackToTop }">Play</button>
          <button @click="stop" :class="{ hidden: !playing, 'floating-button': showBackToTop }">Stop</button>
        </p>
      </div>
      <div class="row">
        <p>
          <input
            type="checkbox"
            id="soprano"
            name="soprano"
            v-model="voiceParts.soprano"
            @change="setInstrument"
          />
          <label for="soprano">第一聲部 (Soprano)</label>
          <input
            type="checkbox"
            id="alto"
            name="alto"
            v-model="voiceParts.alto"
            @change="setInstrument"
          />
          <label for="alto">第二聲部 (Alto)</label>
          <input
            type="checkbox"
            id="tenor"
            name="tenor"
            v-model="voiceParts.tenor"
            @change="setInstrument"
          />
          <label for="tenor">第三聲部 (Tenor)</label>
          <input
            type="checkbox"
            id="bass"
            name="bass"
            v-model="voiceParts.bass"
            @change="setInstrument"
          />
          <label for="bass">第四聲部 (Bass)</label>
        </p>
      </div>
      <div id="paper1" :class="{ hidden: selectedTrack !== '0' }"></div>
      <div id="paper2" :class="{ hidden: selectedTrack !== '1' }"></div>
      <div id="paper3" :class="{ hidden: selectedTrack !== '2' }"></div>
      <div id="audio"></div>
    </div>
  </main>
</template>

<script setup>
import { ref, reactive, computed, onMounted } from "vue";
import ABCJS from "abcjs";
import "abcjs/abcjs-audio.css";

const scores = [
  // Tune 0
  `
X:1
T:天堂咫尺眼前
%%score ( 1 2 ) ( 3 4 )
L:1/4
Q:1/4=93
M:3/4
K:F
%%stretchlast true
V:1 treble nm="Soprano" snm="Soprano" 
V:2 treble nm="Alto" snm="Alto"
V:3 bass nm="Tenor" snm="Tenor"
V:4 bass nm="Bass" snm="Bass"
V:1
|: F A3/2 F/ | c2 z | F A3/2 F/ | E2 z |  D3 | C3 |
w: 1 3 1 | 5 | 1 3 1 | .7 | .6 | .5 |
w: 1     |   |       |   |   |   |
w: 國 度 呈 | 現 | 榮 光 無 | 限 | 生 | 命
w: 榮 耀 寶 | 座 | 君 王 復 | 活 | 聖 | 潔
D F A | G2 z |  F A3/2 F/ | c2 z | F A3/2 F/ | E2 z |
w: .6 1 3 | 2 | 1 3 1 | 5 | 1 3 1 | .7 |
w: .4     |   |        |   |       |   |
w: 湧 流 活 | 泉 | 聖 山 綿 | 延 | 微 風 拂 | 面
w: 永 恆 居 | 所 | 基 督 國 | 度 | 永 永 遠 | 遠
D F A | G2 F | F3 |1,2,3. z E F |  G3 | G F G | A3 |
w: .6 1 3 | 2 1 | 1 | .7 1 | 2 | 2 1 2 | 3 |
w: .4     |     |   |     |   |       |   |
w: 天 堂 咫 | 尺 眼 | 前 | v1:生 命 | 樹 | 果 實 纍 | 纍
w: 耶 穌 咫 | 尺 眼 | 前 | v2:眾 聖 | 徒 | 雲 彩 圍 | 繞
w: -  -  - | -  - | -  | v3:慈 愛 | 主 | 輕 聲 呼 | 喚
V:2
|: F A3/2 F/ | A2 z | F A3/2 F/ | C2 z |  B,3 | A,3 |
w: 1 3 1 | 3 | 1 3 1 | .5 | .4 | .3 |
B, D F | E2 z |  F A3/2 F/ | A2 z | F A3/2 F/ | C2 z |
w: .4 .6 1 | .7 | 1 3 1 | 3 | 1 3 1 | .5 |
B, D F | E2 C | C3 |1,2,3. z C C |  B,3 | B, D B, | C3 |
w: .4 .6 1 | .7 .5 | .5 | .5 .5 | .4 | .4 .6 .4 | .5 |
V:3
|: F, F,3/2 F,/ | C2 z | F, F,3/2 F,/ | C2 z |  D3 | C3 |
w: 1 1 1 | 5 | 1 1 1 | 5 | 6 | 5 |
w: 1     |   |       |   |   |   |
B, D F | E2 z |  F, F,3/2 F,/ | A,2 z | F, F,3/2 F,/ | A,2 z |
w: 4 6 1' | 7 | 1 1 1 | 3 | 1 1 1 | 3 |
w: 2     |   |        |   |       |   |
B, B, B, | C2 B, | A,3 |1,2,3. z G, F, |  _E,3 | D, D, G, | F,3 |
w: 4 4 4 | 5 4 | 3 | 2 1 | .7 | .6 .6 2 | 1 |
w: 1     |     |   |     |   |       |   |
V:4
|: F, F,3/2 F,/ | A,2 z | F, F,3/2 F,/ | A,2 z |  B,3 | A,3 |
w: 1 1 1 | 3 | 1 1 1 | 3 | 4 | 3 |
G, B, D | C2 z |  F, F,3/2 F,/ | A,2 z | F, F,3/2 F,/ | A,2 z |
w: 2 4 6 | 5 | 1 1 1 | 3 | 1 1 1 | 3 |
F, F, B, | C2 B, | A,3 |1,2,3. z G, F, |  _E,3 | D, D, G, | F,3 |
w: 1 1 4 | 5 4 | 3 | 2 1 | .7 | .6 .6 2 | 1 |
V:1
z G A | B3 | B A B | c3 |  z A B | c3- | c A G |
w: 2 3 | 4 | 4 3 4 | 5 | 3 4 | 5 | 5 3 2 |
w: .7   |   |       |   |     |   |       |
w:  永 生 | 河 | 涓 流 蜿 | 蜒 | 天 上 | 美 | - 麗 世 
w:  神 家 | 人 | 親 密 擁 | 抱 | 口 唱 | 心 | - 和 歡
w:  彩 虹 | 約 | 跨 過 雲 | 端 | 基 督 | 馨 | - 香 充
F3 |  z G A | B3- | B A F | G3- |  G z z :| z4 
w: 1 | 2 3 | 4 | 4 3 1 | 2 | 2 |
w: 1 |     |   |       |   |   |
w:  界 | 基 督 | 為 | - 我 | 預 備 
w:  笑 | 歌 聲 | 餘 | - 音 | 繚 繞
w:  滿 | 恩 典 | 滋 | - 潤 | 溫 暖
|: D F A | G2 F |  F3- | F z z :|
w: .6 1 3 | 2 1 | 1 | 1 |
w: .4     |     |   |   |
w:  天 堂 咫 | 尺 眼 | 前
V:2
z E F | G3 | G F G | A3 |  z A B | A3- | A A G |
w: .7 1 | 2 | 2 1 2 | 3 | 3 4 | 3 | 3 3 2 |
F3 |  z G A | G3- | G A F | E3- |  E z z :| z4
w: 1 | 2 3 | 2 | 2 3 1 | .7 | .7 | 
|: B, D F | E2 C |  C3- | C z z :|
w: .4 .6 1 | .7 .5 | .5 | .5 |
V:3
z G, F, | _E,3 | D, D, G, | F,3 |  z F, G, | A,3- | A, A, A, |
w: 2 1 | .7 | .6 .6 2 | 1 | 1 2 | 3 | 3 3 3 |
w: 2   |   |       |   |     |   |       |
D,3 |  z D, D, | _E,3- | E, _E, E, | C,3- |  C, z z :| z4
w: .6 | .6 .6 | .7 | .7 .7 .7 | .5 | .5 |
w: .6 |     |   |       |   |   |
|: F, F, B, | C2 B, |  A,3- | A, z z :|
w: 1 1 4 | 5 4 | 3 | 3 |
w: 1     |     |   |   |
V:4
z G, F, | _E,3 | D, D, G, | F,3 |  z F, G, | A,3- | A, A, A, |
w: 2 1 | .7 | .6 .6 2 | 1 | 1 2 | 3 | 3 3 3 |
D,3 |  z D, D, | _E,3- | E, _E, E, | C,3- |  C, z z :| z4 
w: .6 | .6 .6 | .7 | .7 .7 .7 | .5 | .5 | 
|: F, F, B, | C2 B, |  A,3- | A, z z :|
w: 1 1 4 | 5 4 | 3 | 3 |
  `,
  // Tune 1
  `
X:1
T:聖靈之火
%%score ( 1 2 ) ( 3 4 )
L:1/4
Q:1/4=78
M:4/4
K:D
%%stretchlast true
%%staffsep 80
V:1 treble nm="Soprano" snm="Soprano" 
V:2 treble nm="Alto" snm="Alto"
V:3 bass nm="Tenor" snm="Tenor"
V:4 bass nm="Bass" snm="Bass"
V:1
D/F/ A/ | B3/2 B/ A/A/ A/G/ | A2 z/ D/ F/A/ | B3/2 B/ A/A/ A/G/ |
w: 1 3 5| 6 6 5 5 5 4| 5 1 3 5| 6 6 5 5 5 4
w: 1    |            |        |            |
w: 期 待 此|刻 祢 點 燃 我 心|火, 渴 望 祢|愛 祢 待 我 如 朋
w: 奇 妙 大|能 創 造 浩 瀚 宇|宙, 奇 妙 大|能 拯 救 我 得 自
w: 給 我 火|種 讓 我 堅 定 不|怠, 給 我 渴|望 建 立 國 度 萬
F2 z/ D/ F/A/ | B3/2 A/ c/c/ c/d/ | B2 z/ D/ F/A/ | B2 z/ D/ F/A/ |
w: 3 1 3 5| 6 5 7 7 7 1'| 6 1 3 5| 6 1 3 5|
w: 1      |            |        |        |
w:友, 期 待 祢|光 照 亮 前 行 天|路, 我 們 需|要 祢 在 左
w:由, 同 聲 高|唱 主 祢 就 在 其|中, 主 祢 是|我 唯 一 所
w:載, 給 我 夢|想 當 夢 想 終 實|現, 我 們 將|會 與 祢 同
A2 z/ D/ F/A/ | B2 z/ A/ A/G/ | A2 z/ D/ F/A/ | B B z/ A/ A/G/ |
w: 5 1 3 5| 6 5 5 4| 5 1 3 5| 6 6 5 5 4|
w: 2      |        |        |          |
w:右. 聖 靈 之|火 全 能 烈|火  天 命 呼|召 我 更 新 除
w:求. 聖 靈 之|火 全 能 烈|火  天 命 呼|召 我 更 新 除
w:在.     |
F2 z/ A/ d/c/ | B2 z/ A/ F/A/ | B2 z/ D/ F/A/ | B2 z/ D/ F/E/ |  D3 z |]
w: 3 5 1' 7| 6 5 3 5| 6 1 3 5| 6 1 3 2| 1|
w: 3      |        |        |        |  |
w:舊 燃 燒 心|頭 流 貫 血|中 聖 靈 之|火 聖 靈 之|火
w:舊 燃 燒 心|頭 流 貫 血|中 聖 靈 之|火 聖 靈 之|火
V:2
D/D/ F/ | G3/2 G/ E/E/ E/E/ | F2 z/ D/ D/F/ | G3/2 G/ E/E/ E/D/ |
w: 1 1 3| 5 5 2 2 2 2| 3 1 1 3| 5 5 2 2 2 1|
D2 z/ D/ D/F/ | G3/2 G/ A/A/ A/B/ | F2 z/ D/ D/F/ | G2 z/ D/ D/F/ |
w: 1 1 1 3| 5 5 6 6 6 7| 3 1 1 3| 5 1 1 3|
E2 z/ D/ D/F/ | G2 z/ E/ E/D/ | F2 z/ D/ D/F/ | G G z/ E/ E/D/ |
w: 2 1 1 3| 5 2 2 1| 3 1 1 3| 5 5 2 2 1|
F2 z/ F/ A/A/ | G2 z/ F/ F/F/ | F2 z/ D/ D/F/ | G2 z/ D/ D/C/ |  D3 x |]
w: 3 3 5 5| 4 3 3 3| 3 1 1 3| 4 1 1 7| 1|
V:3
A,/D/ D/ | D3/2 D/ D/D/ D/C/ | D2 z/ A,/ D/D/ | D3/2 D/ D/D/ C/B,/ |
w: 5 1' 1'| 1' 1' 1' 1' 1' 7| 1' 5 1' 1'| 1' 1' 1' 1' 7 6|
w: 1    |            |        |            |
A,2 z/ A,/ D/D/ | D3/2 D/ C/E/ E/F/ | D2 z/ D/ D/D/ | D2 z/ A,/ D/D/ |
w: 5 5 1' 1'| 1' 1' 7 2 2 3| 1' 1' 1' 1'| 1' 5 1' 1'|
w: 1      |            |        |        |
(D2 C/) x3/2 | D D D C | D D A, x | D D D C |
w: 1' 7| 1' 1' 1' 7| 1' 1' 5| 1' 1' 1' 7|
w: 5  |        |      |        |
w:     |聖 靈 火  全  |能 烈 火   |呼 召 我  更
D D A, x | D E E C | D D D x | D D C B, |  A,3 x |]
w: 1' 1' 5 | 1' 2' 2' 7 | 1' 1' 1' | 1' 1' 7 6 | 5|
w: 1    |        |      |        |  |
w:新 除 舊 |在 心 頭 流 |貫 血 中 |喔 聖 靈 之|火
V:4
D,/D,/ D,/ | G,3/2 G,/ A,/A,/ A,/A,/ | D,2 z/ D,/ D,/D,/ | G,3/2 G,/ A,/A,/ A,/A,/ |
w: 1 1 1| 5 5 6 6 6 6| 1 1 1 1| 5 5 6 6 6 6|
D,2 z/ D,/ D,/D,/ | G,3/2 G,/ A,/A,/ A,/A,/ | B,2 z/ B,/ B,/A,/ | G,2 z/ D,/ D,/D,/ |
w: 1 1 1 1| 5 5 6 6 6 6| 6 6 6 5| 4 1 1 1|
A,2- A,/ z/ z | G, G, A, A, | D, D, D, z | G, G, A, A, |
w: 5 5| 4 4 5 5| 1 1 1| 4 4 5 5|
D, D, D, z | G, G, A, A, | B, B, B, z | G, G, A, A, |  D,3 z |]
w: 1 1 1| 5 5 6 6| 6 6 6| 5 5 6 6| 1|
`,
// Tune 2
`
X:1
T:我神可敬可畏
%%score ( 1 2 ) ( 3 4 )
L:1/4
Q:1/4=110
M:4/4
K:G
%%stretchlast true
V:1 treble nm="Soprano" snm="Soprano" 
V:2 treble nm="Alto" snm="Alto"
V:3 bass nm="Tenor" snm="Tenor"
V:4 bass nm="Bass" snm="Bass"
V:1
E |: E3 E/F/ | G D B (G/A/) | A3 (G/F/) |
w: 6 | 6 6 7 | 1' 5 3' 1' 2' | 2' 1' 7 |
w: 6 |       |           |       |
w: 我 | 神 是 可 | 敬 可 畏, 祂 | 以 大 能 |
G/G/ (F/E/) E (D/E/) | E3 (E/F/) | G D B (G/A/) |
w: 1' 1' 7 6 6 5 6 | 6 6 7 | 1' 5 3' 1' 2' |
w: 6             |       |           |
w: 仁 愛, 智 - 慧 從 | 天 主 | 宰 全 地 我 |
A B/A/ G F |1  E3 E :| E2 z E | E F/G/ F D | E3 E |
w: 2' 3' 2' 1' 7 | 6 6 | 6 6 | 6 7 1' 7 5 | 6 6 |
w: 6         |     |     |           |     |
w: 神 是 可 敬 可 | 畏. 我 | 畏. 我 | 神 是 可 敬 可 | 畏! 我 |
E F/G/ F D | E3 E | E2 F G | F2 d2 |  !fermata!e3 |]
w: 6 7 1' 7 5 | 6 6 | 6 7 1' | 7 5 | 6 |
w: 4         |     |       |     |   |
w: 神 是 可 敬 可 | 畏! 我 | 神 是 可 | 敬 可 畏!
V:2
E |: C3 C/D/ | D D D D | F3 E/D/ |
w: 6 | 4 4 5 | 5 5 5 5 | 7 6 5
E/E/ D B, B, | C3 C/D/ | D D D D |
w: 6 6 5 3 3 | 4 4 5 | 5 5 5 5 |
E E/E/ E ^D |1  B,3 E :| B,2 B, x | C C/C/ D B, | B,3 B, |
w: 6 6 6 6 5 | 3 6 | 3 3 | 4 4 4 5 3 | 3 3 |
C C/C/ D B, | B,3 B, | C2 D C | D2 F2 |  G3 |]
w: 4 4 4 5 3 | 3 3 | 4 5 4 | 5 7 | 1
V:3
E, |: G,3 G,/A,/ | G, G, G, B, | D3 A, |
w: 6 | 1' 1' 2' | 1' 1' 1' 3' | 5' 2' |
w: 6 |       |         |     |
B,/B,/ A, G, G, | G,3 (G,/A,/) | G, G, G, B, |
w: 3' 3' 2' 1' 1' | 1' 1' 2' | 1' 1' 1' 3' |
w: 6         |       |         |
C D/C/ B, A, |1  G,3 E, :| G,2 G, x | G, F,/E,/ F, A, | G,3 G, |
w: 4' 5' 4' 3' 2' | 1' 6 | 1' 1' | 1' 7 6 7 2' | 1' 1' |
w: 2         |     |     |           |     |
G, F,/E,/ F, A, | G,3 G, | G,2 A, G, | A,2 A,2 |  !fermata!B,3 |]
w: 1' 7 6 7 2' | 1' 1' | 1' 2' 1' | 2' 2' | 3'
w: 2         |     |       |     |  
V:4
E, |: C,3 C,/C,/ | B,, B,, G,, G,, | D,3 D, |
w: 6 | 4 4 4 | 3 3 1 1 | 5 5 |
E,/E,/ E, E, D, | C,3 C, | B,, B,, E, E, |
w: 6 6 6 6 5 | 4 4 | 3 3 6 6 |
A,, A,,/A,,/ B,, B,, |1  E,3 E, :| E,2 z E, | A,, A,,/A,,/ B,, B,, | E,3 E, |
w: 2 2 2 3 3 | 6 6 | 6 6 | 2 2 2 3 3 | 6 6 |
A,, A,,/A,,/ B,, B,, | E,3 D, | C,2 B,, A,, | B,,2 B,,2 |  [E,,E,]3 |]
w: 2 2 2 3 3 | 6 5 | 4 3 2 | 3 3 | 6
`
];
const voiceParts = reactive({
  soprano: true,
  alto: true,
  tenor: true,
  bass: true,
});
const selectedTrack = ref(-1);
const instrument = ref("0");
const playing = ref(false);
// 狀態：是否顯示回到頂部按鈕
const showBackToTop = ref(false);
let tunes = [];
let buffers = [];

const voiceArray = computed(() => {
  const result = [];
  if (!voiceParts.soprano) result.push(0);
  if (!voiceParts.alto) result.push(1);
  if (!voiceParts.tenor) result.push(2);
  if (!voiceParts.bass) result.push(3);
  return result;
});

const renderTune = (abc, i) => {
  return ABCJS.renderAbc(`paper${i + 1}`, abc, { add_classes: true })[0];
};

const primeTune = (visualObj) => {
  const midi = new ABCJS.synth.CreateSynth();
  return midi
    .init({
      visualObj: visualObj,
      options: {
        program: instrument.value,
        chordsOff: true,
        voicesOff: voiceArray.value,
        drumOff: true,
        channel: 0,
      },
    })
    .then(() => {
      return midi.prime();
    })
    .then(() => {
      return midi;
    });
};

const stop = () => {
  playing.value = false;
  return Promise.all(
    buffers.map((buff) => {
      return buff.then((synth) => {
        synth.stop();
        return synth;
      });
    })
  );
};

const play = () => {
  setInstrument();
  stop();
  const buff = buffers[selectedTrack.value];
  if (buff) {
    buff.then((synth) => {
      synth.start();
      playing.value = true;
    });
  } else {
    alert("Please select a song first");
  }
};

const setInstrument = () => {
  stop();
  buffers = tunes.map(primeTune);
};

// 監聽滾動事件的函式
const handleScroll = () => {
  const scrollTop = window.scrollY || document.documentElement.scrollTop;
  showBackToTop.value = scrollTop > 100; // 滾動超過100px才顯示按鈕
};

onMounted(() => {
  window.addEventListener('scroll', handleScroll);
  tunes = scores.map(renderTune);
  buffers = tunes.map(primeTune);
  var voice1Lyrics = document.querySelectorAll(".abcjs-v0 .abcjs-lyric");
  voice1Lyrics.forEach(function (lyric) {
    lyric.classList.add("voice-1");
  });
  var voice2Lyrics = document.querySelectorAll(".abcjs-v1 .abcjs-lyric");
  voice2Lyrics.forEach(function (lyric) {
    lyric.classList.add("voice-2");
  });
  var voice3Lyrics = document.querySelectorAll(".abcjs-v2 .abcjs-lyric");
  voice3Lyrics.forEach(function (lyric) {
    lyric.classList.add("voice-3");
  });
  var voice4Lyrics = document.querySelectorAll(".abcjs-v3 .abcjs-lyric");
  voice4Lyrics.forEach(function (lyric) {
    lyric.classList.add("voice-4");
  });
});
</script>

<style scoped>
main {
  max-width: 770px;
  margin: 0 auto;
}

.hidden {
  display: none;
}

.row {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
}

.status {
  padding: 2px 10px 10px 10px;
  background-color: #f0f0f0;
  width: 250px;
}

@media (prefers-color-scheme: dark) {
  .status {
    background-color: #000000;
  }
}
</style>
<style>
.abcjs-lyric.voice-1 {
  fill: blue; /* 聲部1的歌詞設置為藍色 */
}
.abcjs-lyric.voice-2 {
  fill: red; /* 聲部2的歌詞設置為紅色 */
  transform: translateY(1.2em); /* 將聲部2的歌詞向下移動 */
}
.abcjs-lyric.voice-3 {
  fill: purple; /* 聲部3的歌詞設置為紫色 */
}
.abcjs-lyric.voice-4 {
  fill: green; /* 聲部4的歌詞設置為綠色 */
  transform: translateY(1.2em); /* 將聲部4的歌詞向下移動 */
}

/* 設定浮動按鈕的樣式 */
.floating-button {
  position: fixed; /* 固定位置 */
  right: 20px;     /* 距離畫面右邊20px */
  top: 50%;        /* 垂直置中 */
  transform: translateY(-50%); /* 精準垂直置中 */
}
</style>
