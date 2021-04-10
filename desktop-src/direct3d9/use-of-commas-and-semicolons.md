---
description: Die Verwendung von Kommas und Semikolons kann das komplexeste Syntax Problem im Dateiformat sein, und diese Verwendung ist sehr streng. Kommas werden verwendet, um Array Elemente voneinander zu trennen. die einzelnen Datenelemente werden durch Semikolons beendet.
ms.assetid: 82582213-907c-4760-a849-e6cf5f6d60bc
title: Verwendung von Kommas und Semikolons
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba238d50ff5d0dace017f16b75547df6b016e14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125570"
---
# <a name="use-of-commas-and-semicolons"></a>Verwendung von Kommas und Semikolons

Die Verwendung von Kommas und Semikolons kann das komplexeste Syntax Problem im Dateiformat sein, und diese Verwendung ist sehr streng. Kommas werden verwendet, um Array Elemente voneinander zu trennen. die einzelnen Datenelemente werden durch Semikolons beendet.

Wenn eine Vorlage beispielsweise folgendermaßen definiert wird:


```
template mytemp {
DWORD myvar;
}
```



Eine Instanz dieser Vorlage sieht dann wie folgt aus:


```
mytemp dataTemp {
1;
}
```



Wenn eine Vorlage, die eine andere Vorlage enthält, folgendermaßen definiert ist:


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



Eine Instanz dieser Vorlage sieht dann wie folgt aus:


```
container dataContainer {
1.1;
2; 
3;;
}
```



Beachten Sie, dass die zweite Zeile, die den Wert von mytemp innerhalb des Containers darstellt, zwei Semikolons am Ende der Zeile enthält. Das erste Semikolon gibt das Ende des Datenelements an, aTemp (innerhalb des Containers) und das zweite Semikolon das Ende des Containers.

Wenn ein Array wie folgt definiert wird:


```
Template mytemp {

array DWORD myvar[3];

}
```



Dann sieht eine Instanz von wie folgt aus:


```
mytemp aTemp {
1, 2, 3;
}
```



Im Array Beispiel ist es nicht erforderlich, dass die Datenelemente durch Semikolons getrennt werden, da Sie durch Kommas getrennt sind. Das Semikolon am Ende markiert das Ende des Arrays.

Stellen Sie sich eine Vorlage vor, die ein Array von Datenelementen enthält, die durch eine Vorlage definiert werden.


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



Eine Instanz dieses Beispiels würde wie im folgenden Beispiel aussehen.


```
container aContainer {
3;
1;2;,3;4;,5;6;;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Text Codierung](text-encoding.md)
</dt> </dl>

 

 



