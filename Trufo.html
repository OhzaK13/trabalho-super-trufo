#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <ctime>
#include <cstdlib>

struct City {
    std::string name;
    int population;       // habitantes em milhares
    int area;             // km²
    double gdp;           // PIB em bilhões BRL
    double hdi;           // IDH (0.0 - 1.0)
    int tourist_score;    // 0-100
    int altitude;         // metros
};

// Protótipos
void init_deck(std::vector<City>& deck);
void shuffle_deck(std::vector<City>& deck);
void distribute(const std::vector<City>& deck, std::vector<City>& player, std::vector<City>& computer);
void show_card(const City& c);
int choose_attribute();
int compare_attribute(const City& a, const City& b, int attr);
void press_enter_to_continue();

int main() {
    std::vector<City> deck;
    init_deck(deck);
    shuffle_deck(deck);

    std::vector<City> player, computer;
    distribute(deck, player, computer);

    std::cout << "=== Super Trunfo: Cidades do Brasil ===\n";
    std::cout << "Voce vs Computador\n\n";

    int round = 1;
    std::vector<City> pile;
    bool player_turn = true; // jogador começa

    std::srand((unsigned)time(nullptr));

    while (!player.empty() && !computer.empty()) {
        std::cout << "---- Rodada " << round++ << " ----\n";
        std::cout << "Cartas: Voce = " << player.size() << " | Computador = " << computer.size() << "\n";

        City pc = player.front(); player.erase(player.begin());
        City cc = computer.front(); computer.erase(computer.begin());

        std::cout << "\nSua carta:\n";
        show_card(pc);

        int attr;
        if (player_turn) {
            attr = choose_attribute();
        }
        else {
            // IA simples: escolhe atributo onde sua carta é relativamente mais forte
            double scores[6] = {
                double(cc.population - pc.population),
                double(cc.area - pc.area),
                cc.gdp - pc.gdp,
                cc.hdi - pc.hdi,
                double(cc.tourist_score - pc.tourist_score),
                double(cc.altitude - pc.altitude)
            };
            int best = 0;
            double bestv = scores[0];
            for (int i = 1; i < 6; ++i)
                if (scores[i] > bestv) { bestv = scores[i]; best = i; }
            attr = best + 1;
            std::cout << "Computador escolhe o atributo " << attr << ".\n";
        }

        std::cout << "\nCarta do computador:\n";
        show_card(cc);

        pile.push_back(pc);
        pile.push_back(cc);

        int cmp = compare_attribute(pc, cc, attr);

        if (cmp > 0) {
            std::cout << "\n-> Voce venceu a rodada!\n";
            player.insert(player.end(), pile.begin(), pile.end());
            pile.clear();
            player_turn = true;
        }
        else if (cmp < 0) {
            std::cout << "\n-> Computador venceu a rodada!\n";
            computer.insert(computer.end(), pile.begin(), pile.end());
            pile.clear();
            player_turn = false;
        }
        else {
            std::cout << "\n== Empate! Cartas vao para o monte e proxima rodada desempata ==\n";
            player_turn = !player_turn;
            // cartas permanecem no monte
        }

        press_enter_to_continue();
    }

    if (player.empty()) {
        std::cout << "\n### Voce perdeu! O computador ganhou o jogo. ###\n";
    }
    else {
        std::cout << "\n### Parabens! Voce ganhou o jogo. ###\n";
    }

    return 0;
}

// Inicializa deck com cidades e atributos
void init_deck(std::vector<City>& deck) {
    deck.clear();

    City c;

    c = { "São Paulo", 1233000, 1521, 700.0, 0.805, 85, 760 };
    deck.push_back(c);
    c = { "Rio de Janeiro", 671890, 1182, 300.0, 0.799, 95, 2 };
    deck.push_back(c);
    c = { "Brasília", 305514, 5802, 120.0, 0.824, 70, 1172 };
    deck.push_back(c);
    c = { "Salvador", 288669, 693, 80.0, 0.759, 88, 8 };
    deck.push_back(c);
    c = { "Fortaleza", 266934, 313, 60.0, 0.754, 82, 21 };
    deck.push_back(c);
    c = { "Belo Horizonte", 252156, 331, 90.0, 0.797, 68, 852 };
    deck.push_back(c);
    c = { "Manaus", 221958, 1141, 55.0, 0.737, 60, 92 };
    deck.push_back(c);
    c = { "Curitiba", 194862, 432, 75.0, 0.823, 66, 900 };
    deck.push_back(c);
    c = { "Recife", 164572, 218, 48.0, 0.772, 74, 4 };
    deck.push_back(c);
    c = { "Porto Alegre", 148494, 496, 65.0, 0.805, 64, 10 };
    deck.push_back(c);
}

// Embaralha deck usando std::random_shuffle
void shuffle_deck(std::vector<City>& deck) {
    std::srand((unsigned)time(nullptr));
    std::random_shuffle(deck.begin(), deck.end());
}

// Distribui alternadamente cartas entre jogador e computador
void distribute(const std::vector<City>& deck, std::vector<City>& player, std::vector<City>& computer) {
    player.clear();
    computer.clear();
    for (size_t i = 0; i < deck.size(); ++i) {
        if (i % 2 == 0) player.push_back(deck[i]);
        else computer.push_back(deck[i]);
    }
}

void show_card(const City& c) {
    std::cout << "Nome: " << c.name << "\n";
    std::cout << "1) Populacao (hab, em milhares): " << c.population << "\n";
    std::cout << "2) Area (km²): " << c.area << "\n";
    std::cout << "3) PIB (bilhoes BRL): " << c.gdp << "\n";
    std::cout << "4) IDH: " << c.hdi << "\n";
    std::cout << "5) Turismo (score): " << c.tourist_score << "\n";
    std::cout << "6) Altitude (m): " << c.altitude << "\n";
}

int choose_attribute() {
    int a = 0;
    while (true) {
        std::cout << "\nEscolha o atributo para comparar (digite 1-6): ";
        std::cin >> a;
        if (std::cin.fail() || a < 1 || a > 6) {
            std::cin.clear();
            std::cin.ignore(10000, '\n');
            std::cout << "Entrada invalida. Tente novamente.\n";
            continue;
        }
        std::cin.ignore(10000, '\n');
        break;
    }
    return a;
}

int compare_attribute(const City& a, const City& b, int attr) {
    switch (attr) {
    case 1: return (a.population > b.population) ? 1 : (a.population < b.population ? -1 : 0);
    case 2: return (a.area > b.area) ? 1 : (a.area < b.area ? -1 : 0);
    case 3: return (a.gdp > b.gdp) ? 1 : (a.gdp < b.gdp ? -1 : 0);
    case 4: return (a.hdi > b.hdi) ? 1 : (a.hdi < b.hdi ? -1 : 0);
    case 5: return (a.tourist_score > b.tourist_score) ? 1 : (a.tourist_score < b.tourist_score ? -1 : 0);
    case 6: return (a.altitude > b.altitude) ? 1 : (a.altitude < b.altitude ? -1 : 0);
    default: return 0;
    }
}

void press_enter_to_continue() {
    std::cout << "\nPressione Enter para continuar...";
    std::cin.ignore(std::numeric_limits<std::streamsize>::max(), '\n');
}
