NAME		= program
SRCS		= main.cpp \
			Dog.cpp \
			Cat.cpp \
			Animal.cpp \
			WrongAnimal.cpp \
			WrongCat.cpp \
			Brain.cpp

OBJS		= ${SRCS:%.cpp=%.o}
DEPS		= ${SRCS:.cpp=.d}
CC			= c++
CPPFLAGS	= -Wall -Wextra -Werror -std=c++98
RM			= rm -f

all:		${NAME}

${NAME}:	${OBJS}
	${CC} ${CPPFLAGS} ${OBJS} -o ${NAME}

%.o: %.cpp
			$(CC) $(CPPFLAGS) -c $< -o $@

clean:
			${RM} ${OBJS} ${DEPS}

fclean:		clean
			${RM} ${NAME}

re:			fclean all

.PHONY:		all clean fclean re