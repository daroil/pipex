# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Makefile                                           :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: dhendzel <dhendzel@student.42.fr>          +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2022/11/01 15:26:49 by dhendzel          #+#    #+#              #
#    Updated: 2023/01/07 05:44:55 by dhendzel         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

CC = gcc

SRCS = 	pipex.c children.c free.c msg.c

NAME =  pipex
LIBFT	:= ./libft
OBJ	= $(SRCS:.c=.o)
CFLAGS = -Wall -Werror -Wextra



all: libft $(NAME)

libft:
	@$(MAKE) -C $(LIBFT)

$(NAME): $(OBJ)
	$(CC) $(OBJ) $(LIBFT)/libft.a -o $(NAME)

clean:
	rm -f $(OBJ)
	@$(MAKE) -C $(LIBFT) clean

fclean: clean
	rm -f $(NAME)
	@$(MAKE) -C $(LIBFT) fclean

re: fclean all

norm:
	norminette $(SRCS) 
	@$(MAKE) -C $(LIBFT) norm

# ./pipex infile "ls -l" "wc -l" outfile

.PHONY: all clean fclean re norm libft