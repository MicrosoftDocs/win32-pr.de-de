---
title: Arrayattribute
description: Es besteht eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C.
ms.assetid: 0d65c993-63e4-42ae-ae24-6c19a71386a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ba7bdaa08352a96987066313d4db074872f28b71ec0be0856a32522a849029c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073520"
---
# <a name="array-attributes"></a>Arrayattribute

Es besteht eine enge Beziehung zwischen Arrays und Zeigern in der Programmiersprache C. Wenn ein Arrayname als Parameter an eine Funktion übergeben wird, wird er wie im folgenden Beispiel gezeigt als Zeiger auf das erste Element des Arrays behandelt:


```C++
/* fragment */
extern void f1(char * p1);

void main(void)
{
    char chArray[MAXSIZE];

    fLocal1(chArray);
}
```



In einem lokalen Aufruf können Sie den Zeigerparameter verwenden, um durch den Arbeitsspeicher zu märzen und den Inhalt anderer Adressen zu untersuchen:


```C++
/* dump memory (fragment) */
void fLocal1(char * pch1)
{
    int i;

    for (i = 0; i < MAXSIZE; i++)
       printf("%c ", *pch1++);
}
```



Wenn ein Client einen Zeiger auf eine Remoteprozedur übergibt, überträgt der Clientstub sowohl den Zeiger als auch die Daten, auf die er zeigt. Sofern der Zeiger nicht auf die entsprechenden Daten beschränkt ist, muss bei jedem Remoteaufruf der clientseitige Arbeitsspeicher übertragen werden. Durch erzwingen der starken Eingabe in der Schnittstellendefinition schränkt MIDL die Clientstubverarbeitung auf die Daten ein, die dem angegebenen Zeiger entsprechen.

Die Größe des Arrays und der Bereich von Arrayelementen, die an den Remotecomputer übertragen werden, können konstant oder variabel sein. Wenn diese Werte variabel sind und daher zur Laufzeit bestimmt werden, müssen Sie Attribute in der IDL-Datei verwenden, um anzugeben, wie viele Arrayelemente übertragen werden sollen. Die folgenden MIDL-Attribute unterstützen Array-Begrenzungen.



| attribute                             | BESCHREIBUNG                                             | Standard |
|---------------------------------------|---------------------------------------------------------|---------|
| \[[ **first \_ is**](/windows/desktop/Midl/first-is)\]   | Index des ersten übertragenen Arrayelements.           | 0       |
| \[[ **last \_ is**](/windows/desktop/Midl/last-is)\]     | Index des letzten übertragenen Arrayelements.            | \-      |
| \[[ **length \_ ist**](/windows/desktop/Midl/length-is)\] | Gesamtanzahl der übertragenen Arrayelemente.             | \-      |
| \[[ **max \_ is**](/windows/desktop/Midl/max-is)\]       | Der höchste gültige Arrayindexwert.                        | \-      |
| \[[ **min \_ is**](/windows/desktop/Midl/min-is)\]       | Niedrigster gültiger Arrayindexwert.                         | 0       |
| \[[ **size \_ ist**](/windows/desktop/Midl/size-is)\]     | Gesamtanzahl der Arrayelemente, die dem Array zugeordnet sind. | \-      |



 

> [!Note]  
> Das **min \_ is-Attribut** ist in RPC nicht implementiert. Der minimale Arrayindex wird immer als 0 (null) behandelt.

 

 

 