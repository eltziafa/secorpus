# secorpus · Greek Stock Exchange Corpus

**[Ελληνικά](#ελληνικά) · [English](#english)**

Διεύθυνση / Address: **https://secorpus.gr**

---

## Ελληνικά

Το **secorpus** είναι σώμα κειμένων του ενωσιακού χρηματιστηριακού δικαίου (ελληνικά, με παράλληλο γαλλικό σκέλος) και το συνοδευτικό εργαλείο διερεύνησής του στον φυλλομετρητή. Αναπτύσσεται από την Ελένη Τζιάφα (Τμήμα Γαλλικής Γλώσσας και Φιλολογίας, Εθνικό και Καποδιστριακό Πανεπιστήμιο Αθηνών).

### Το σώμα (data/v1)

| | |
|---|---|
| Έγγραφα | 819 |
| Τμήματα | 294.750 |
| Λέξεις (EL) | 6.651.009 |
| Γλώσσες | Ελληνικά, με γαλλικό παράλληλο σκέλος στο ~95% των τμημάτων |
| Χρονικό εύρος | 2001–2021 |
| Επισημείωση | Μορφή, λήμμα και μέρος του λόγου (spaCy, el_core_news_lg / fr_core_news_md) |

**Πηγές:** DGT-TM (Ευρωπαϊκή Επιτροπή· επαναχρησιμοποίηση βάσει της απόφασης 2011/833/ΕΕ) και EUR-Lex. Η θεματική οριοθέτηση έγινε με περιγραφείς EuroVoc (χρηματιστήριο αξιών, κεφαλαιαγορά, κινητές αξίες, χρηματοδοτικό μέσο, εποπτεία της αγοράς, εταιρεία επενδύσεων, αθέμιτη χρηματιστηριακή εκμετάλλευση εμπιστευτικών πληροφοριών, κατάταξη πιστοληπτικής ικανότητας), μέσω του SPARQL endpoint του Cellar.

### Το εργαλείο (index.html)

Αυτόνομο αρχείο HTML, χωρίς διακομιστή, χωρίς εξωτερικές εξαρτήσεις και χωρίς δικτυακά αιτήματα πέραν των δεδομένων του σώματος. Λειτουργίες: συμφραστικοί πίνακες (KWIC) με αναζήτηση λέξης, λήμματος και κανονικών εκφράσεων· ταξινόμηση ως προς το αριστερό ή δεξί συμφραζόμενο· κατανομή ανά έτος (ανά εκατομμύριο λέξεις)· συνάψεις (MI και logDice, παράθυρο ±5)· πίνακας συχνοτήτων· εξαγωγή CSV· φόρτωση τοπικών υποσωμάτων που δεν αποστέλλονται πουθενά. Διεπαφή σε ελληνικά, γαλλικά και αγγλικά.

### Μεθοδολογικές σημειώσεις και γνωστά όρια

1. Το DGT-TM δεν περιέχει όλες τις πράξεις: οι MiFID II (2014/65/ΕΕ) και MiFIR (600/2014) απουσιάζουν από όλες τις εκδόσεις του και ενσωματώθηκαν απευθείας από το EUR-Lex, με δομική ευθυγράμμιση σε επίπεδο παραγράφου (πεδία `unit`, `source` στα δεδομένα).
2. Η κάλυψη μετά το 2021 εκκρεμεί, καθώς οι διαθέσιμες εκδόσεις του DGT-TM φθάνουν έως τα δεδομένα του 2020 (με μερική κάλυψη του 2021).
3. Η λημματοποίηση του el_core_news_lg έχει μετρήσιμα όρια: ενδεικτικά, για το λήμμα «κεφαλαιαγορά» ανακτά 390 από 477 επιφανειακές εμφανίσεις (ανάκληση ~82%). Για εξαντλητικές μετρήσεις συνιστάται η αναζήτηση με κανονικές εκφράσεις.
4. Η άντληση CELEX από το Cellar έγινε τμηματικά ανά περιγραφέα και έτος, λόγω του ορίου ~10.000 γραμμών ανά ερώτημα του endpoint.
5. Οι εγγραφές του τομέα E (ΕΖΕΣ) δεν φέρουν έτος και εμφανίζονται ως «χ.χ.».

Η γραμμή προεπεξεργασίας (Python) περιλαμβάνεται στον φάκελο `pipeline/` για λόγους αναπαραγωγιμότητας.

### Αναφορά

> Τζιάφα, Ε. (2026). *secorpus: Greek Stock Exchange Corpus* [Σώμα κειμένων και εργαλείο]. Εθνικό και Καποδιστριακό Πανεπιστήμιο Αθηνών. https://secorpus.gr

### Άδειες

Το εργαλείο διατίθεται με άδεια [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/deed.el). Τα δεδομένα προέρχονται από το DGT-TM και το EUR-Lex και διέπονται από τους όρους επαναχρησιμοποίησης της Ευρωπαϊκής Επιτροπής (απόφαση 2011/833/ΕΕ), με υποχρέωση αναφοράς της πηγής. Ο σχεδιασμός και η υλοποίηση έγιναν σε συνεργασία με το Claude Fable 5 (Anthropic).

---

## English

**secorpus** is a corpus of EU capital-market law texts (Greek, with a parallel French layer) together with a browser-based exploration tool. It is developed by Eleni Tziafa (Department of French Language and Literature, National and Kapodistrian University of Athens).

### The corpus (data/v1)

819 documents · 294,750 segments · 6,651,009 Greek tokens · ~95% with parallel French · time span 2001–2021 · annotated for form, lemma and part of speech (spaCy, el_core_news_lg / fr_core_news_md).

**Sources:** DGT-TM (European Commission; reuse under Decision 2011/833/EU) and EUR-Lex. Thematic delimitation via EuroVoc descriptors (stock exchange, capital market, securities, financial instrument, market supervision, investment company, insider trading, credit rating) through the Cellar SPARQL endpoint.

### The tool (index.html)

A single self-contained HTML file: no server, no external dependencies, no network requests beyond the corpus data. Features: KWIC concordances with word, lemma and regular-expression search; sorting by left/right context; distribution by year (per million words); collocations (MI and logDice, ±5 window); frequency table; CSV export; loading of local subcorpora that never leave the browser. Interface in Greek, French and English.

### Methodological notes and known limits

1. DGT-TM is incomplete: MiFID II (2014/65/EU) and MiFIR (600/2014) are absent from all its releases and were added directly from EUR-Lex with structural paragraph-level alignment (`unit`, `source` fields).
2. Coverage after 2021 is pending; available DGT-TM releases extend to 2020 data (partial 2021).
3. el_core_news_lg lemmatisation has measurable limits: for the lemma «κεφαλαιαγορά» it retrieves 390 of 477 surface occurrences (~82% recall). Regular-expression search is recommended for exhaustive counts.
4. CELEX retrieval from Cellar was partitioned per descriptor and year due to the endpoint's ~10,000-row result limit.
5. Sector-E (EFTA) records carry no year and appear as "n.d.".

The preprocessing pipeline (Python) is included in `pipeline/` for reproducibility.

### Citation

> Tziafa, E. (2026). *secorpus: Greek Stock Exchange Corpus* [Corpus and tool]. National and Kapodistrian University of Athens. https://secorpus.gr

### Licences

The tool is released under [CC BY-NC-ND 4.0](https://creativecommons.org/licenses/by-nc-nd/4.0/). The data originate from DGT-TM and EUR-Lex and are governed by the European Commission's reuse terms (Decision 2011/833/EU), with source attribution required. Designed and implemented in collaboration with Claude Fable 5 (Anthropic).
