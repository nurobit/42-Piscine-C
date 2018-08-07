# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: viwade <marvin@42.fr>                      +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2018/08/06 16:05:46 by viwade            #+#    #+#              #
#    Updated: 2018/08/07 00:04:23 by viwade           ###   ########.fr        #
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
	rm -rf ./includes/

fclean: clean
	rm -f $(NAME)

re: fclean all

build:
	mkdir ./includes/

$(NAME): $(OBJECTS)
	$(AR) rcs $@ $(OBJECTS)

includes/%.o: srcs/%.c | build
	$(CC) $(CFLAGS) -c %< -o $@
