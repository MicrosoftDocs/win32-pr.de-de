---
title: Arrayattribute
description: Es gibt eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed669a2a81528afa84b41a1be25a0c84f70fbe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729433"
---
# <a name="array-attributes"></a>Arrayattribute

Es gibt eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C. Wenn ein Array Name als Parameter an eine Funktion übergeben wird, wird er als Zeiger auf das erste Element des Arrays behandelt, wie im folgenden Beispiel gezeigt:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



In einem lokalen-Befehl können Sie den Zeiger Parameter verwenden, um den Arbeitsspeicher zu durchsuchen und den Inhalt anderer Adressen zu untersuchen:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Wenn ein Client einen Zeiger an eine Remote Prozedur übergibt, überträgt der Clientstub den Zeiger und die Daten, auf die er verweist. Wenn der Zeiger nicht auf seine entsprechenden Daten beschränkt ist, muss der gesamte Arbeitsspeicher des Clients mit jedem Remote-Befehl übertragen werden. Durch erzwingen der starken Typisierung in der Schnittstellen Definition schränkt die Client-Stub-Verarbeitung von der Mittell auf die Daten ein, die dem angegebenen Zeiger entsprechen.

Die Größe des Arrays und der Bereich der Array Elemente, die an den Remote Computer übertragen werden, können konstant oder variabel sein. Wenn diese Werte variabel sind und daher zur Laufzeit bestimmt werden, müssen Sie Attribute in der IDL-Datei verwenden, um anzugeben, wie viele Array Elemente übertragen werden sollen. Die folgenden Mittell-Attribute unterstützen Array Begrenzungen.



| Attribut                             | BESCHREIBUNG                                             | Standard |
|---------------------------------------|---------------------------------------------------------|---------|
| \[der [ **erste \_ ist**](/windows/desktop/Midl/first-is)\]   | Der Index des ersten übertragenen Array Elements.           | 0       |
| \[[ **Letzter \_ ist**](/windows/desktop/Midl/last-is)\]     | Der Index des letzten übertragenen Array Elements.            | \-      |
| \[[ **Länge \_ ist**](/windows/desktop/Midl/length-is)\] | Gesamtanzahl der übertragenen Array Elemente.             | \-      |
| \[[ **Max \_ ist**](/windows/desktop/Midl/max-is)\]       | Höchster gültiger Array Indexwert.                        | \-      |
| \[[ **Min \_ ist**](/windows/desktop/Midl/min-is)\]       | Niedrigster gültiger Array Indexwert.                         | 0       |
| \[[ **Größe \_** :](/windows/desktop/Midl/size-is)\]     | Die Gesamtanzahl der für das Array zugeordneten Array Elemente. | \-      |



 

> [!Note]  
> Das **Min \_ is** -Attribut ist in RPC nicht implementiert. Der minimale Array Index wird immer als 0 (null) behandelt.

 

 

 