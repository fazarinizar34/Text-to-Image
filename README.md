# Text to Image Generation (Pokemon) 🧬🎨

## Deskripsi Proyek

Proyek ini merupakan **tugas eksperimen Text-to-Image** yang mensimulasikan alur kerja *Text-to-Image Generation* menggunakan dataset caption Pokémon. Fokus utama proyek adalah **alur pemrosesan data, vektorisasi teks, pipeline training, dan simulasi model Transformer**, bukan menghasilkan gambar realistis seperti Stable Diffusion.

Notebook ini cocok untuk **pembelajaran konsep dasar** bagaimana teks dapat dipetakan menjadi representasi visual dalam sistem AI generatif.

---

## Struktur File

```
📦 Text-to-Image-Pokemon
 ┣ 📜 Nizar_Fazari_Hidayat_Tugas_5_Text_to_Image.ipynb
 ┗ 📜 README.md
```

---

## Penjelasan File

### 1️⃣ `Nizar_Fazari_Hidayat_Tugas_5_Text_to_Image.ipynb`

Notebook utama yang berisi seluruh tahapan eksperimen, meliputi:

#### 🔹 1. Install & Import Library

Menggunakan beberapa library utama:

* `tensorflow` & `keras` → membangun dan melatih model
* `datasets (HuggingFace)` → memuat dataset caption Pokémon
* `numpy` & `matplotlib` → pengolahan data dan visualisasi
* `PIL` → pemrosesan citra

#### 🔹 2. Load Dataset Caption

Dataset yang digunakan:

* **`reach-vb/pokemon-blip-captions`**
* Dataset berisi pasangan **gambar Pokémon dan caption teks**

Dataset ini hanya digunakan sebagai **sumber teks dan contoh visual**, bukan untuk training model difusi sesungguhnya.

#### 🔹 3. Text Vectorization

* Menggunakan `TextVectorization`
* Maksimum kosakata: **5000 token**
* Panjang sequence: **20 token**

Tahap ini mengubah teks deskripsi Pokémon menjadi representasi numerik.

#### 🔹 4. Preprocessing Dataset

* Resize gambar ke **64×64 piksel**
* Normalisasi nilai piksel ke rentang **0–1**
* Caption diubah menjadi token numerik
* Dataset diproses menggunakan `tf.data.Dataset`

#### 🔹 5. Model Dummy (Simulasi Transfor
