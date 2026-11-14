
import streamlit as st

# ==============================
# KONFIGURASI HALAMAN
# ==============================
st.set_page_config(
    page_title="MathClass 12",
    page_icon="📐",
    layout="wide"
)

# ==============================
# DESAIN CSS
# ==============================
st.markdown("""
<style>
.stApp {
    background-color: #f4f7fb;
}

.main-title {
    font-size: 38px;
    font-weight: 800;
    color: #173b67;
}

.subtitle {
    color: #64748b;
    font-size: 16px;
}

.question-box {
    background: white;
    padding: 25px;
    border-radius: 15px;
    border: 1px solid #e2e8f0;
    margin-bottom: 15px;
}

.answer-box {
    background: #e8f5e9;
    padding: 20px;
    border-radius: 12px;
    border-left: 5px solid #2e9d50;
}

.stButton button {
    border-radius: 10px;
    font-weight: bold;
    min-height: 42px;
}
</style>
""", unsafe_allow_html=True)

# ==============================
# DATABASE SOAL
# ==============================
soal = {
    "Limit Fungsi": [
        {
            "pertanyaan": "Nilai dari lim x→2 (x² - 4)/(x - 2) adalah ...",
            "pilihan": ["A. 2", "B. 4", "C. 6", "D. 8", "E. 10"],
            "jawaban": "B. 4",
            "pembahasan": """
            Faktorkan pembilang:

            x² - 4 = (x - 2)(x + 2)

            Maka:

            (x² - 4)/(x - 2) = x + 2

            Substitusi x = 2:

            2 + 2 = 4
            """
        },
        {
            "pertanyaan": "Nilai dari lim x→3 (x² - 9)/(x - 3) adalah ...",
            "pilihan": ["A. 3", "B. 6", "C. 9", "D. 12", "E. 15"],
            "jawaban": "B. 6",
            "pembahasan": """
            Faktorkan:

            x² - 9 = (x - 3)(x + 3)

            Sederhanakan menjadi x + 3.

            Substitusi x = 3:

            3 + 3 = 6
            """
        }
    ],

    "Turunan Fungsi": [
        {
            "pertanyaan": "Turunan pertama dari f(x) = 3x² + 5x - 7 adalah ...",
            "pilihan": [
                "A. 3x + 5",
                "B. 6x + 5",
                "C. 6x - 5",
                "D. 3x² + 5",
                "E. 6x + 7"
            ],
            "jawaban": "B. 6x + 5",
            "pembahasan": """
            Gunakan aturan turunan:

            Jika f(x) = axⁿ, maka f'(x) = anxⁿ⁻¹.

            Turunkan setiap suku:

            3x² → 6x
            5x → 5
            -7 → 0

            Jadi f'(x) = 6x + 5.
            """
        },
        {
            "pertanyaan": "Jika f(x) = x³ - 4x² + 2x, maka f'(x) adalah ...",
            "pilihan": [
                "A. 3x² - 8x + 2",
                "B. 3x² - 4x + 2",
                "C. x² - 8x + 2",
                "D. 3x² + 8x + 2",
                "E. 3x - 8"
            ],
            "jawaban": "A. 3x² - 8x + 2",
            "pembahasan": """
            Turunkan setiap suku:

            x³ → 3x²
            -4x² → -8x
            2x → 2

            Jadi:

            f'(x) = 3x² - 8x + 2
            """
        }
    ],

    "Integral": [
        {
            "pertanyaan": "Hasil integral ∫ 2x dx adalah ...",
            "pilihan": [
                "A. x + C",
                "B. x² + C",
                "C. 2x² + C",
                "D. x³ + C",
                "E. 2 + C"
            ],
            "jawaban": "B. x² + C",
            "pembahasan": """
            Gunakan rumus integral:

            ∫ axⁿ dx = (a/(n+1))xⁿ⁺¹ + C

            Maka:

            ∫ 2x dx = 2 × x²/2 + C

            Hasilnya adalah x² + C.
            """
        },
        {
            "pertanyaan": "Hasil dari ∫ 3x² dx adalah ...",
            "pilihan": [
                "A. x³ + C",
                "B. 3x³ + C",
                "C. 6x + C",
                "D. x² + C",
                "E. 3x + C"
            ],
            "jawaban": "A. x³ + C",
            "pembahasan": """
            ∫ 3x² dx

            = 3 × (x³/3) + C

            = x³ + C
            """
        }
    ],

    "Peluang": [
        {
            "pertanyaan": "Sebuah dadu dilempar sekali. Peluang muncul angka genap adalah ...",
            "pilihan": [
                "A. 1/6",
                "B. 1/3",
                "C. 1/2",
                "D. 2/3",
                "E. 5/6"
            ],
            "jawaban": "C. 1/2",
            "pembahasan": """
            Ruang sampel dadu:

            {1, 2, 3, 4, 5, 6}

            Angka genap:

            {2, 4, 6}

            Banyak kejadian = 3
            Banyak ruang sampel = 6

            P(A) = 3/6 = 1/2
            """
        },
        {
            "pertanyaan": "Dalam sebuah kantong terdapat 3 bola merah dan 2 bola biru. Peluang mengambil bola biru adalah ...",
            "pilihan": [
                "A. 1/5",
                "B. 2/5",
                "C. 3/5",
                "D. 4/5",
                "E. 1/2"
            ],
            "jawaban": "B. 2/5",
            "pembahasan": """
            Jumlah seluruh bola = 3 + 2 = 5

            Jumlah bola biru = 2

            P(biru) = 2/5
            """
        }
    ]
}

# ==============================
# HEADER
# ==============================
st.markdown('<div class="main-title">📐 MathClass 12</div>',
            unsafe_allow_html=True)

st.markdown(
    '<div class="subtitle">Platform belajar dan latihan matematika SMA kelas XII</div>',
    unsafe_allow_html=True
)

st.divider()

# ==============================
# SIDEBAR
# ==============================
st.sidebar.title("📚 Menu Belajar")

menu = st.sidebar.radio(
    "Pilih Materi",
    ["Beranda"] + list(soal.keys())
)

st.sidebar.divider()
st.sidebar.info("Belajar matematika sedikit demi sedikit setiap hari!")

# ==============================
# BERANDA
# ==============================
if menu == "Beranda":

    st.subheader("Selamat Datang! 👋")

    st.write("""
    Selamat datang di MathClass 12.

    Website ini membantu kamu mempelajari matematika kelas 12
    melalui latihan soal, jawaban, dan pembahasan.
    """)

    col1, col2, col3 = st.columns(3)

    with col1:
        st.metric("Materi", len(soal))

    with col2:
        total = sum(len(x) for x in soal.values())
        st.metric("Total Soal", total)

    with col3:
        st.metric("Jenjang", "Kelas XII")

    st.divider()

    st.subheader("📖 Daftar Materi")

    for materi, daftar in soal.items():
        with st.expander(materi):
            st.write(f"Jumlah latihan: {len(daftar)} soal")
            st.write("Pilih materi melalui menu di sebelah kiri.")

# ==============================
# HALAMAN QUIZ
# ==============================
else:

    st.subheader(f"📘 Materi: {menu}")

    daftar_soal = soal[menu]

    # Session state
    key = f"nomor_{menu}"
    answer_key = f"jawaban_{menu}"
    checked_key = f"checked_{menu}"
    score_key = f"score_{menu}"

    if key not in st.session_state:
        st.session_state[key] = 0

    if answer_key not in st.session_state:
        st.session_state[answer_key] = {}

    if checked_key not in st.session_state:
        st.session_state[checked_key] = {}

    if score_key not in st.session_state:
        st.session_state[score_key] = 0

    nomor = st.session_state[key]
    current = daftar_soal[nomor]

    st.progress((nomor + 1) / len(daftar_soal))

    st.caption(
        f"Soal {nomor + 1} dari {len(daftar_soal)}"
    )

    st.markdown(
        f"""
        <div class="question-box">
            <h3>📝 Pertanyaan</h3>
            <p style="font-size:19px;color:#173b67;">
                {current['pertanyaan']}
            </p>
        </div>
        """,
        unsafe_allow_html=True
    )

    # Pilihan jawaban
    selected = st.radio(
        "Pilih jawaban yang menurutmu benar:",
        current["pilihan"],
        index=(
            current["pilihan"].index(
                st.session_state[answer_key][nomor]
            )
            if nomor in st.session_state[answer_key]
            else None
        ),
        key=f"radio_{menu}_{nomor}"
    )

    st.session_state[answer_key][nomor] = selected

    # Periksa jawaban
    if st.button("🔍 Periksa Jawaban", type="primary",
                 use_container_width=True):

        st.session_state[checked_key][nomor] = True

        if selected == current["jawaban"]:
            st.session_state[score_key] += 1

    # Tampilkan pembahasan
    if st.session_state[checked_key].get(nomor, False):

        if selected == current["jawaban"]:
            st.success("🎉 Benar! Jawaban kamu tepat.")
        else:
            st.error("Belum tepat. Yuk, pelajari pembahasannya!")

        st.markdown(
            f"""
            <div class="answer-box">
                <h3>✅ Jawaban Benar</h3>
                <h2>{current['jawaban']}</h2>
            </div>
            """,
            unsafe_allow_html=True
        )

        st.subheader("💡 Pembahasan")

        st.markdown(current["pembahasan"])

    st.divider()

    # Navigasi
    col1, col2 = st.columns(2)

    with col1:
        if nomor > 0:
            if st.button("⬅️ Soal Sebelumnya",
                         use_container_width=True):
                st.session_state[key] -= 1
                st.rerun()

    with col2:
        if nomor < len(daftar_soal) - 1:
            if st.button("Soal Berikutnya ➡️",
                         use_container_width=True):
                st.session_state[key] += 1
                st.rerun()
        else:
            st.success("Kamu sudah menyelesaikan semua soal!")

    st.divider()

    st.metric(
        "🏆 Jawaban Benar",
        f"{st.session_state[score_key]} / {len(daftar_soal)}"
    )

    if st.button("🔄 Ulangi Materi", use_container_width=True):
        st.session_state[key] = 0
        st.session_state[answer_key] = {}
        st.session_state[checked_key] = {}
        st.session_state[score_key] = 0
        st.rerun()

# ==============================
# FOOTER
# ==============================
st.divider()

st.markdown(
    "<center>© 2026 MathClass 12 | Belajar Matematika Lebih Mudah 📐</center>",
    unsafe_allow_html=True
)
