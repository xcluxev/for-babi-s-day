import tkinter as tk
import random

# ==========================================
# SETTINGS
# ==========================================

BG = "#EAF6FF"          # Very light baby blue
BLUE = "#8ECDF4"        # Baby blue
DARK_BLUE = "#4A9FD1"   # Darker blue
WHITE = "#FFFFFF"
TEXT = "#24445A"
LIGHT_BLUE = "#D6EEFF"

FONT = "Georgia"

# ==========================================
# MAIN WINDOW
# ==========================================

root = tk.Tk()
root.title("Birthday Mystery 🩵")
root.geometry("650x700")
root.configure(bg=BG)
root.resizable(False, False)


# ==========================================
# SCREEN SYSTEM
# ==========================================

def clear_screen():
    for widget in root.winfo_children():
        widget.destroy()


def title(text):
    label = tk.Label(
        root,
        text=text,
        font=(FONT, 30, "bold"),
        bg=BG,
        fg=TEXT
    )

    label.pack(pady=20)

    return label


def button(text, command):
    btn = tk.Button(
        root,
        text=text,
        command=command,
        font=(FONT, 14, "bold"),
        bg=BLUE,
        fg=WHITE,
        activebackground=DARK_BLUE,
        activeforeground=WHITE,
        relief="flat",
        padx=20,
        pady=10,
        cursor="hand2"
    )

    btn.pack(pady=8)

    return btn


# ==========================================
# START SCREEN
# ==========================================

def start_screen():

    clear_screen()

    tk.Label(
        root,
        text="🩵",
        font=(FONT, 60),
        bg=BG
    ).pack(pady=20)

    title("Birthday Mystery")

    tk.Label(
        root,
        text=(
            "Hey babi ko!! 🩵\n\n"
            "I made a little game just for you:)).\n"
            "Y=ou have to solve muna ah? HAHAHA"
        ),
        font=(FONT, 15),
        bg=BG,
        fg=TEXT,
        justify="center"
    ).pack(pady=10)

    button(
        "Start the Game 🩵",
        word_search
    )


# ==========================================
# WORD SEARCH
# ==========================================

ROWS = [
    "BIRTHDAY",
    "OEVENLUV",
    "CAXQWZEA",
    "LOVEHART",
    "MZPYOYTS",
    "SMILEABC",
    "QXGIFTND",
    "HAPPYYOU"
]

WORDS = [
    "BIRTHDAY",
    "LOVE",
    "HEART",
    "SMILE",
    "GIFT"
]

POSITIONS = {

    "BIRTHDAY": [
        (0,0),(0,1),(0,2),(0,3),
        (0,4),(0,5),(0,6),(0,7)
    ],

    "LOVE": [
        (3,0),(3,1),(3,2),(3,3)
    ],

    "HEART": [
        (3,3),(2,3),(1,3),(0,3),(0,4)
    ],

    "SMILE": [
        (5,0),(5,1),(5,2),(5,3),(5,4)
    ],

    "GIFT": [
        (6,4),(6,5),(6,6),(6,7)
    ]
}

selected = []
found_words = set()
word_buttons = {}
grid_buttons = []


def word_search():

    clear_screen()

    title("🔎 Word Search")

    tk.Label(
        root,
        text=(
            "Find all 5 hidden words!\n"
            "Click the letters in the correct order."
        ),
        font=(FONT, 13),
        bg=BG,
        fg=TEXT
    ).pack()

    word_frame = tk.Frame(root, bg=BG)
    word_frame.pack(pady=15)

    word_buttons.clear()

    for word in WORDS:

        label = tk.Label(
            word_frame,
            text=word,
            font=(FONT, 11, "bold"),
            bg=LIGHT_BLUE,
            fg=TEXT,
            padx=10,
            pady=5
        )

        label.pack(side="left", padx=4)

        word_buttons[word] = label

    grid_frame = tk.Frame(root, bg=BG)
    grid_frame.pack(pady=10)

    grid_buttons.clear()

    for r in range(8):

        row_buttons = []

        for c in range(8):

            btn = tk.Button(
                grid_frame,
                text=ROWS[r][c],
                font=(FONT, 15, "bold"),
                width=3,
                height=1,
                bg=WHITE,
                fg=TEXT,
                relief="solid",
                command=lambda r=r, c=c:
                    select_letter(r, c)
            )

            btn.grid(
                row=r,
                column=c,
                padx=2,
                pady=2
            )

            row_buttons.append(btn)

        grid_buttons.append(row_buttons)

    global selected, found_words

    selected = []
    found_words = set()

    status = tk.Label(
        root,
        text="",
        font=(FONT, 12, "bold"),
        bg=BG,
        fg=DARK_BLUE
    )

    status.pack(pady=10)

    root.search_status = status


def select_letter(row, col):

    global selected

    position = (row, col)

    if position in selected:

        selected.remove(position)

        grid_buttons[row][col].configure(
            bg=WHITE,
            fg=TEXT
        )

        return

    selected.append(position)

    grid_buttons[row][col].configure(
        bg=BLUE,
        fg=WHITE
    )

    check_word()


def check_word():

    global selected

    for word in WORDS:

        if word in found_words:
            continue

        target = POSITIONS[word]

        if (
            len(selected) == len(target)
            and all(x in selected for x in target)
        ):

            found_words.add(word)

            word_buttons[word].configure(
                bg=BLUE,
                fg=WHITE
            )

            for r, c in selected:

                grid_buttons[r][c].configure(
                    bg=LIGHT_BLUE,
                    fg=DARK_BLUE
                )

            selected = []

            root.search_status.configure(
                text=f"{word} found! ✨"
            )

            if len(found_words) == len(WORDS):

                root.search_status.configure(
                    text="All words found! 🩵"
                )

                root.after(
                    1000,
                    puzzle_pieces
                )

            return

    if len(selected) >= 8:

        selected = []

        for row in grid_buttons:

            for btn in row:

                btn.configure(
                    bg=WHITE,
                    fg=TEXT
                )

        root.search_status.configure(
            text="Not a word! Try again 🔎"
        )


# ==========================================
# PUZZLE PIECES
# ==========================================

CORRECT_ORDER = [
    "H", "A", "P", "P",
    "Y", "B", "I", "R",
    "T", "H", "D", "A",
    "Y", "🩵", "!", "🎂"
]

pieces = []
selected_piece = None
piece_buttons = []


def puzzle_pieces():

    clear_screen()

    title("🧩 Put the Pieces Together")

    tk.Label(
        root,
        text=(
            "Tap two pieces to swap them.\n"
            "Put them in the correct order to reveal the message!"
        ),
        font=(FONT, 13),
        bg=BG,
        fg=TEXT
    ).pack(pady=5)

    global pieces

    pieces = CORRECT_ORDER.copy()

    random.shuffle(pieces)

    create_piece_interface()


def create_piece_interface():

    global piece_buttons

    piece_buttons = []

    piece_frame = tk.Frame(
        root,
        bg=BG
    )

    piece_frame.pack(pady=20)

    for i in range(16):

        btn = tk.Button(
            piece_frame,
            text=pieces[i],
            font=(FONT, 20, "bold"),
            width=4,
            height=2,
            bg=LIGHT_BLUE,
            fg=TEXT,
            relief="solid",
            command=lambda i=i:
                select_piece(i)
        )

        btn.grid(
            row=i // 4,
            column=i % 4,
            padx=4,
            pady=4
        )

        piece_buttons.append(btn)

    tk.Label(
        root,
        text="Current arrangement:",
        font=(FONT, 12, "bold"),
        bg=BG,
        fg=TEXT
    ).pack()

    board = tk.Frame(
        root,
        bg=WHITE,
        padx=10,
        pady=10
    )

    board.pack(pady=10)

    for i, piece in enumerate(pieces):

        tk.Label(
            board,
            text=piece,
            font=(FONT, 18, "bold"),
            width=3,
            height=2,
            bg=WHITE,
            fg=TEXT
        ).grid(
            row=i // 4,
            column=i % 4,
            padx=2,
            pady=2
        )

    global puzzle_status

    puzzle_status = tk.Label(
        root,
        text="",
        font=(FONT, 12, "bold"),
        bg=BG,
        fg=DARK_BLUE
    )

    puzzle_status.pack(pady=5)


def select_piece(index):

    global selected_piece

    if selected_piece is None:

        selected_piece = index

        piece_buttons[index].configure(
            bg=BLUE,
            fg=WHITE
        )

        return

    if selected_piece == index:

        piece_buttons[index].configure(
            bg=LIGHT_BLUE,
            fg=TEXT
        )

        selected_piece = None

        return

    pieces[selected_piece], pieces[index] = (
        pieces[index],
        pieces[selected_piece]
    )

    selected_piece = None

    create_piece_interface()

    check_puzzle()


def check_puzzle():

    if pieces == CORRECT_ORDER:

        puzzle_status.configure(
            text="You solved it! 🩵"
        )

        root.after(
            1000,
            win_screen
        )


# ==========================================
# WIN SCREEN
# ==========================================

def win_screen():

    clear_screen()

    tk.Label(
        root,
        text="🎁",
        font=(FONT, 70),
        bg=BG
    ).pack(pady=20)

    title("You Did It! 🩵")

    tk.Label(
        root,
        text=(
            "You solved every puzzle!\n\n"
            "But there's one last surprise waiting for you..."
        ),
        font=(FONT, 15),
        bg=BG,
        fg=TEXT,
        justify="center"
    ).pack(pady=10)

    button(
        "Open Your Surprise 💌",
        birthday_message
    )


# ==========================================
# BIRTHDAY MESSAGE
# ==========================================

def birthday_message():

    clear_screen()

    tk.Label(
        root,
        text="💐",
        font=(FONT, 60),
        bg=BG
    ).pack(pady=10)

    title("Happy Birthday My Babyyy! 🩵")

    message = (
        "Happy birthday, babi ko! 🩵\n\n"

        "I’m sorry I haven’t been able to make enough time for you because of my busy schedule, and I’m sorry for always falling asleep whenever we’re talking. I know I could do better, and I’ll try my best to make more time for you.\n\n"

        "For your birthday, I just wish that you’ll always have reasons to smile, that you’ll keep believing in yourself even on the hard days, and that all the things you’ve been working and hoping for slowly come your way. You’re stronger than you realize, and I’m genuinely so proud of you for how far you’ve come. "
        "I'm really happy that I get to be part of your life, "
        "and I hope this little game made your birthday "
        "a little more special.\n\n"

        "I love you so much, babi, more than you know. 🩵"
    )

    tk.Label(
        root,
        text=message,
        font=(FONT, 15),
        bg=BG,
        fg=TEXT,
        justify="center",
        wraplength=520
    ).pack(pady=15)

    tk.Label(
        root,
        text="— Made with love, just for you 💌",
        font=(FONT, 13, "italic", "bold"),
        bg=BG,
        fg=DARK_BLUE
    ).pack(pady=10)


# ==========================================
# START
# ==========================================

start_screen()

root.mainloop()
