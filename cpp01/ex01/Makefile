# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: fsariogl <fsariogl@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2023/05/03 17:34:32 by fsariogl          #+#    #+#              #
#    Updated: 2024/04/08 19:35:16 by fsariogl         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = zombie

SRC =	main.cpp		\
		Zombie.cpp		\
		zombieHorde.cpp	\

CC = g++
FLAGS = -Wall -Wextra -Werror --std=c++98
OBJ = $(SRC:.cpp=.o)

all: $(NAME)

%.o: %.cpp Zombie.hpp
	$(CC) $(FLAGS) -c $< -o $@

$(NAME): $(OBJ)
	mkdir -p ./obj/
	$(CC) $(FLAGS) $(OBJ) -o $(NAME)
	mv ./*.o ./obj/.

clean:
	rm -rf $(OBJ) ./obj/

fclean: clean
	rm -rf $(NAME)

re: fclean all

.PHONY: all NAME clean fclean re