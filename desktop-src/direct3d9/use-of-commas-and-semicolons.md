---
description: Die Verwendung von Kommas und Semikolons kann das komplexeste Syntaxproblem im Dateiformat sein, und diese Verwendung ist sehr streng. Kommas werden verwendet, um Arraymember zu trennen. Semikolons beenden jedes Datenelement.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Verwenden von Kommas und Semikolons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b44d20d4a8e99a75522fa3703d58d82f3bf4dfe130e530d18141b7f45e572717
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119044058"
---
# <a name="use-of-commas-and-semicolons"></a>Verwenden von Kommas und Semikolons

Die Verwendung von Kommas und Semikolons kann das komplexeste Syntaxproblem im Dateiformat sein, und diese Verwendung ist sehr streng. Kommas werden verwendet, um Arraymember zu trennen. Semikolons beenden jedes Datenelement.

Beispiel: Eine Vorlage wird wie folgt definiert:


```
template mytemp {
DWORD myvar;
}
```



Anschließend sieht eine Instanz dieser Vorlage wie folgt aus:


```
mytemp dataTemp {
1;
}
```



Wenn eine Vorlage, die eine andere Vorlage enthält, wie folgt definiert wird:


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
FLOAT aFloat;
mytemp aTemp;
}
```



Anschließend sieht eine Instanz dieser Vorlage wie folgt aus:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Beachten Sie, dass die zweite Zeile, die den Mytemp innerhalb des Containers darstellt, zwei Semikolons am Ende der Zeile enthält. Das erste Semikolon gibt das Ende des Datenelements, aTemp (innerhalb des Containers) und das zweite Semikolon das Ende des Containers an.

Wenn ein Array wie folgt definiert ist:


```
Template mytemp {

array DWORD myvar[3];

}
```



Anschließend sieht eine Instanz dieser wie folgt aus:


```
mytemp aTemp {
1, 2, 3;
}
```



Im Arraybeispiel müssen die Datenelemente nicht durch Semikolons getrennt werden, da sie durch Kommas voneinander getrennt werden. Das Semikolon am Ende markiert das Ende des Arrays.

Betrachten Sie eine Vorlage, die ein Array von Datenelementen enthält, die von einer Vorlage definiert werden.


```
template mytemp {
DWORD myvar;
DWORD myvar2;
}
template container {
DWORD count;
array mytemp tempArray[count];
}
```



Eine Instanz dieser würde wie im folgenden Beispiel aussehen.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Textcodierung](text-encoding.md)
</dt> </dl>

 

 



