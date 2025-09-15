.PHONY: all debug release clean

# Компилятор
CXX = g++

# Флаги компиляции
RELEASE_FLAGS = -O2 -Wall -DNDEBUG
DEBUG_FLAGS   = -g -O0 -Wall

# Имена исполняемых файлов
RELEASE_EXEC = kazino-royal
DEBUG_EXEC   = kazino-royal-dbg

# Исходный файл
SOURCE = Kazino-Royal.cpp

# --- Цели по умолчанию ---
all: debug release

# --- Сборка debug версии ---
debug: $(DEBUG_EXEC)

$(DEBUG_EXEC): $(SOURCE)
	$(CXX) $(DEBUG_FLAGS) $(SOURCE) -o $(DEBUG_EXEC)

# --- Сборка release версии ---
release: $(RELEASE_EXEC)

$(RELEASE_EXEC): $(SOURCE)
	$(CXX) $(RELEASE_FLAGS) $(SOURCE) -o $(RELEASE_EXEC)

# --- Очистка ---
clean:
	rm -f $(RELEASE_EXEC) $(DEBUG_EXEC)
