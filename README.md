# class-work
import logging
logger = logging.getLogger(__name__)

def write_to_db(userid, name, surname, birthday):
    logger.info(f'{userid=} вызвал функцию write_to_db: {name=} {surname=} {birthday=}')
    with open('database.txt', 'a', encoding='UTF-8') as file:
        file.write(str(userid))
    file.write('\t')
    file.write(name)
    file.write('\t')
    file.write(surname)
    file.write('\t')
    file.write(birthday)
    file.write('\n')
if __name__ == '__main__':
    write_to_db()
