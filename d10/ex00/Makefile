# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: viwade <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/08/06 16:05:46 by viwade            #+#    #+#              #
#    Updated: 2018/08/06 23:58:40 by viwade           ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

NAME = ./libft.a
AR = ar
FILES = ft_putchar.c ft_putstr.c ft_strcmp.c ft_strlen.c ft_swap.c
GCC = gcc
CFLAGS ?= -Wall -Werror -Wextra
CFLAGS += -I includes
SOURCE = $(addprefix ./srcs/, $(FILES))
OBJECTS = $(addprefix ./includes/, $(FILES:.c=.o))

all: $(NAME)

clean:
	rm -rf ./build/

fclean: clean
	rm -f $(NAME)

re: fclean all

build:
	mkdir ./build/

$(NAME): $(OBJECTS)
	$(AR) rcs $@ $(OBJECTS)

build/%.o : srcs/%.c | build
	$(CC) $(CFLAGS) -c %< -o $@
