Структура и алгоритмы обработки данных. Лекция 3
===========

<div><div style="word-wrap: break-word; -webkit-nbsp-mode: space; -webkit-line-break: after-white-space;"><div>Динамические структуры данных. </div><ul><li>Линейные списки</li><li>Кольцевые списки</li><li>Стек</li><li>Очередь </li><li>Дек</li><li>Мультисписки </li><li>Деревья </li><li>Бинарные деревья </li><li>Графы </li></ul><div><br/>Список (кортеж)  -  конечная последовательность,  допускающая повторения элементов какого-то множества  Ф(Пси) <br/>&lt;х1, х2, .... хn&gt;<br/>Где n&gt;=0 -  количество элементов (длина)  списка, <br/>Хi, I-элемент списка при n=0 список пустой. <br/>Важной структурный особенностью  списка является то,  что элементы линейно упорядоченны в соответствии с их позиции в списке. Элементы множества Ф(пси)  могут иметь сложную структуру,  отражая реальные объекты.... <br/><b><i>Основные операции :</i></b></div><ul><li>Получить значение итого элемента списка или изменить итый элемент. </li><li>Напечатать элементы списка в порядке их расположения. </li><li>Найти в списке элемент с заданным значением </li><li>Определить длину списка</li><li>Вставить новый элемент после или перед иным. </li></ul><div><br/>Реализация списка. <br/>.1.С помощью вектора </div><div>
<img src="img/DSA_l3 (1).png" type="image/png"/></div><div> <br/>//программа <div><br/></div>2. С помощью указателей. <div><br/></div>Элемент <br/><i>Struct  elementtype </i><br/><i>{</i><br/><i> Char El; //поле данных. </i><br/><i> Elementtype *next;</i><br/><i>} ;</i><div><br/></div><i><i> </i></i>Для работы с элементом списка определяют указатель на его начало. </div><div>
<img src="img/DSA_l3 (2).png" type="image/png"/></div><div><br/>Пример<br/>Дано слово,  состоящее из букв,  за которым следует  точка. В слове содержится не более 9 одинаковых  букв,  требуется после каждой группы одинаковых символов ставить,  а повторно вхождение букв удалить. <div><br/></div>Исх. Слово : aaabbbbcceeeee. <br/>Результат: a3b4c2e5<div><br/></div>

  #include <iostream.h>
  #include <conio.h>
  Struct NODE
  {
  Char el;
  NODE *next;
  };
  NODE* iusElem(NODE *_ptr, char _ch); // вставка элемента
  Void printList(NODE *_ pBgn); // начало списка
  Void delElem (NODE *_ptv); //удаление элемента
  Void delList (NODE **_pBgn);//удаление списка освобождение памяти

  Int main ()
  {
  Char ch,k;
  NODE *pBgn, //указатель на начало списка
               *ptr;
               *pgr;
  Cout << "Введите слово" <<endl;
  Ch=getche ();
  pBgn=new NODE;
  pBgn->el=ch;
  pBgn->next=NULL;
  ptr = pBgn;
  // заполнение списка
  While (ch!='.');
  {
  Ch = getche();
  Ptr= insElem (ptr, ch);
  }
  ptr = pBgn;
  While (ptr->el !='.')
  {
  K=1;
  Pgr=ptr;
  Ptr=ptr->next;
  While (pgr -> ==ptr->el)
  {
  K++:
  delElem(pgr);
  Pgr=ptr;
  Ptr=ptr->next;
  }
  InsElem (pgr,k+48);//48ткод нуля 
  }
  Count<<"\n  преобразованное слово: \n";
  PrintList(pBgn);
  delList(&pBgn);
  Return 0;
  }
  NODE* insElem(NODE *_ptr, char_ch)
  {
  NODE *ptmp=new NODE;
  Ptmp->ch;
  Ptmp->next= ptr->next;
  _Ptr->next=ptmp;
  Return ptmp;
  }

<img src="img/DSA_l3 (3).png" type="image/png"/></div><div>Void printList(NODE *_pBgn)<div><br/></div>
</div><div><div><br/></div><div><br/></div>Каждый список содержит указатель на начало и на конец. <br/></div><div>
<img src="img/DSA_lI3 (1).jpeg" type="image/jpeg"/></div><div>
<img src="img/DSA_l3 (4).png" type="image/png"/></div><div>
<img src="img/DSA_lI3 (2).jpeg" type="image/jpeg"/></div><div>Последний элемент такого списка содержит указатель на последующий <br/></div><div>
<img src="img/DSA_l3 (5).png" type="image/png"/></div><div></div></div>
</div>