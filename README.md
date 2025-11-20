# Thesimpsonsapi
api for thesimpsonsapi.com site about the simpsons
# main
```cpp
#include "Thesimpsonsapi.h"
#include <iostream>

int main() {
   Thesimpsonsapi api;

    auto characters = api.characters_list().then([](json::value result) {
        std::cout << result<< std::endl;
    });
    characters.wait();
    
    return 0;
}
```

# Launch (your script)
```
g++ -std=c++11 -o main main.cpp -lcpprest -lssl -lcrypto -lpthread -lboost_system -lboost_chrono -lboost_thread
./main
```
