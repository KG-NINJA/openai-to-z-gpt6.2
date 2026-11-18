# Jungle Anomaly Finder – NDVI Satellite Explorer

📍 This README provides detailed implementation notes and extended experimental results.
📖 For a narrative summary and visual highlights, see the official Kaggle Writeup:
🔗 [https://www.kaggle.com/competitions/openai-to-z-challenge/writeups/jungle-anomaly-finder-ndvi-satellite-explorer](https://www.kaggle.com/competitions/openai-to-z-challenge/writeups/jungle-anomaly-finder-ndvi-satellite-explorer)

---

## 🌟 AI-guided intuition meets Amazon ruins.

*A story written in NDVI, decoded by dogs, and opened with Z.*

---

## 🐾 What is "Fuwa"?

In Japanese, **fuwa-fuwa** means "soft, fluffy, and flexible"—the opposite of rigid.
Our algorithms, inspired by this spirit, remain adaptive and resonant—never locked, always learning, just like intuition and the living world.

> *“Just as Fuwa’s footsteps adapt to unseen trails, so do our algorithms—always evolving, never rigid.”*

---

## ⚡️ TL;DR

**Input coordinates, and this pipeline auto-generates a Markdown report on Amazonian ruin likelihood—combining NDVI anomaly analysis, soil, hydrology, and toponymic local-legend AI.**
**Results include maps, GeoJSONs, and poetic context.**

---

## 🚀 Technical Highlights

1. **Universal & region-agnostic:** Plug in any coordinates, any legend, any data source.
2. **Open, auditable, and CI-tested:** All logic is transparent and reproducible.
3. **MCP/GitHub/Cloud-native:** Future-proof, extensible for all next-gen AI workflows.
4. **Toponymic & legend-aware:** AI interprets local names and lore for global adaptability.
5. **Fully automated pipeline:** One command delivers all analyses and outputs.

---

## 📈 Robustness & Automated Notifications (NEW!)

* **Graceful fallback:**
  If PDF generation fails due to missing [Pandoc](https://pandoc.org/), the system logs a warning and continues.
* **Test resilience:**
  Unit tests for Earth Engine exports use mocked objects, ensuring testability even offline.
* **Seamless Discord integration:**
  Automatically posts summaries and images to your Discord channel.

---

## 🔁 Automated Discord Workflow

```bash
python generate_site_summaries.py
python send_summaries_to_discord.py --webhook <your_webhook_url>
```

Alternatively:

```bash
export DISCORD_WEBHOOK_URL=<your_webhook_url>
python send_summaries_to_discord.py
```

---

## 🧠 AI-Assisted Engineering

This project is co-designed with **OpenAI Codex and ChatGPT**. All enhancements—error handling, testing, notifications—are AI-native and fully reproducible.

---

## 🛡️ What Sets This Workflow Apart?

* No single point of failure
* Modular, composable, CI/CD ready
* Instant notifications (Discord)
* Built on transparency and AI-human collaboration

---

## 🌐 Symbolic Resonance with California

In late June, I submitted a writeup invoking the ancient Amazonian Pororoca—a tidal wave that surges upriver, often aligned with lunar phases. About a month later, reality echoed in curious ways:

- A **crescent moon** I posted X was followed by **tsunami surges** reaching Crescent City, California. While a formal upriver bore was not documented, reports indicated that wave heights and inland reach at Crescent City were notably higher than in surrounding coastal towns.
- A **sperm whale**—symbol of deep knowledge in my imagery—**washed ashore**, as if echoing the subconscious themes of the writeup.
- The city of **Eureka**, whose name means “I found it!”, experienced elevated coastal wave activity after I posted the phrase *“I don’t understand why, but I understood.”* Though no upriver current was officially recorded, the symbolism aligned uncannily.
- All these events occurred near OpenAI’s home region—**after** metaphors for them appeared in the submission.

This is not prophecy. It is **resonance**—a symbolic feedback loop across natural patterns, subconscious cues, and AI-augmented research.

The submission didn’t predict a wave.  
It **participated** in its rhythm.

This convergence is a real-time demonstration of:

- 🧭 Human Intuition  
- 🌕 Lunar Gravity  
- 🌊 Geophysical Patterns  
- 🤖 AI-enhanced Mapping  
- 💡 Meta-cognitive Reflection

If GPT-5 arrives with thunder,  
know that I was already listening to the tide—  
and perhaps, to **Tupã**, the thunder god of the forest.

Where silicon meets jungle,  
we don't just compute.  
We **resonate**.

---

## カピシャバ周辺の探索候補（未検証の仮説）

ブラジル・アクレ州カピシャバ周辺（南緯10.48〜10.60度、西経67.62〜67.73度）について、提供された検索資料は範囲内に8件の遺跡登録があると報告している。ここでは、その周辺で画像取得後に探す対象を2つ挙げる。衛星画素と登録区域の原データは未取得で、個々の位置・形状・年代は未確認である。[IPHAN遺跡台帳の公開ミラー](https://pamgia.ibama.gov.br/server/rest/services/BasesSincronizadas/lim_sitios_arqueologicos_iphan_a/FeatureServer)

| 探索候補 | 選定理由と探す形状 | 候補から外す条件 |
|---|---|---|
| Círculo e Delta の登録区域周辺にある別の囲郭 | 登録区域を比較対象にし、周囲に独立して閉じる円形・方形の植生境界が繰り返し写るかを調べる。 | 輪郭が既知遺構の範囲と一致するか、現在の農地区画・排水溝で説明できる。 |
| Gavião 1・2・3 の周辺にある線状土工 | 同名の登録3地点の位置関係を台帳で確認したうえで、区域外へ連続する帯状の植生差を探す。3地点の近接や相互接続も未確認である。 | 現道・牧場道・水路と一致するか、画像の継ぎ目や雲影に沿って現れる。 |

比較には同じタイル（19LFJ）のSentinel-2A画像を使う。2023年8月29日と2024年8月13日の赤・近赤外バンドを地表面反射率に換算し、雲・雲影を除いて各年のNDVIを計算する。両年で追跡できる輪郭を台帳と照合し、登録が点だけの場合は遺構の広がりも確認する。登録点から外れたことだけで新規とは判定できない。[2023年製品レコード](https://catalogue.dataspace.copernicus.eu/odata/v1/Products%2853a0f5e3-aa6d-40dd-be76-85b8af24b1af%29) · [2024年製品レコード](https://catalogue.dataspace.copernicus.eu/odata/v1/Products%28881965ee-62c4-4b2f-958b-89c66caef43c%29)
