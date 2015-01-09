<table border="1" cellpadding="2" cellspacing="0" width="100%"><tbody><tr><td valign="top">Индекс</td><td valign="top">key</td><td valign="top">left</td><td valign="top">rigth</td></tr><tr><td valign="top">Tree[0]</td><td valign="top">A</td><td valign="top">1</td><td valign="top">2</td></tr><tr><td valign="top"><div>Tree[1]</div></td><td valign="top">B</td><td valign="top">3</td><td valign="top">-1</td></tr><tr><td valign="top"><div>Tree[2]</div></td><td valign="top">C</td><td valign="top">4</td><td valign="top">5</td></tr><tr><td valign="top">Tree[3]</td><td valign="top">D</td><td valign="top">-1</td><td valign="top">-1</td></tr><tr><td valign="top"><div>Tree[4]</div></td><td valign="top">E</td><td valign="top">-1</td><td valign="top">6</td></tr><tr><td valign="top"><div>Tree[5]</div></td><td valign="top">F</td><td valign="top">7</td><td valign="top">8</td></tr><tr><td valign="top"><div>Tree[6]</div></td><td valign="top">G</td><td valign="top">-1</td><td valign="top">-1</td></tr><tr><td valign="top"><div>Tree[7]</div></td><td valign="top">H</td><td valign="top">-1</td><td valign="top">-1</td></tr><tr><td valign="top"><div>Tree[8]</div></td><td valign="top">I</td><td valign="top">-1</td><td valign="top">-1</td></tr></tbody></table><div><br></div></div>
Идеальное дерево называется **идеально сбалансированным**, если для каждого его узла количество узлов в левом и правом поддеревьев различается не более чем на единицу.

Правило равномерного распределения при известном количестве узлов n:
	1. Взять один узел в качестве корня
	2. Построить левое поддерево с nl=n div 2 узлами тем же способом
	3. Построить правое подддерево с nr=n-nl=1 с узлами тем же способом
Код:

	stuct Node
	{
		int key;
		Node *left, *right;
	};
	///
	Node* Tree(int n)
	{
		Node *tmp;
		int x, nl, nr;
		if (n==0) return NULL;
		else
		{
			nl=nl/2;
			nr =n-nl-1;
		}
		count << "Введите значение";
		cin >> x;
		tmp = new Node;
		tmp -> key = x;
		tmp -> left= Tree(nl);
		m
	}

	int main()
	{
		d;
	}


Бинарные деревья поиска
------
Бинарное дерево называется **бинарным деревом поиска**, если оно организовано таким образом, что у ключей слева.
Места элементов в дереве определяются как значениями ключей, так и последовательностью их поступления.
При случайном распределении ключей в исходной последовательности получается почти сбалансированное дерево. Если исходная последовательность упорядоченна по возрастанию или убыванию ключей, то дерево вырождается в последовательный список.
Создание дерева:
	1. Первый элемент образует корень.
	2. Для последующих элементов осуществляется поиск включения по ветвям дерева до тех пор пока не будет найден подходящий узел с новым указателем, куда и вставляется новый элемент.

Сбалансированное АВЛ - дерево поиска.
-------
АВЛ дерево происходит от фамилий трёх учёных, (вероятно советских) Адельсон-Вельский и Ландис.
**АВЛ дерево** - такое дерево, у которого высота поддеревьев для каждой вершины различается не более чем, на единицу.
Показатель сбалансированности = высота правого поддерева (Hr) - высота левого поддерева (Hl).

	0, если Hr = Hl
	1, если Hr > Hl
	-1, если Hr < Hl

При работе с АВЛ деревьями (при включении) необходимо поддерживать сбалансированность дерева в целом.
**Включение узла в АВЛ дерево.**

<table border="1" cellpadding="2" cellspacing="0" width="100%"><tbody><tr><td valign="top"><br></td><td valign="top"><div><br></div></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr></tbody></table>

Балансировка выполняется с помощью действий, называемых поворотами узлов.
При включении узлов повороты выполняются для ближайшего узла к включённому с нарушенной балансировкой.

Табличные структуры.
-----------
Таблица состоит из строк и столбцов. Строки в таблицах ещё называются записями, кортежами. Столбцы называются полями или атрибутами.

<div style="font-size: 15px;">
<table border="1" cellpadding="2" cellspacing="0" width="100%">
<tbody>
<tr><td valign="top">Имя поле 1</td><td valign="top">Имя поле 2</td><td valign="top">Имя поле 3</td><td valign="top">Имя поле 4</td></tr>
<tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td></tr><tr><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td><td valign="top"><br></td>
</tr>
</tbody>
</table>

