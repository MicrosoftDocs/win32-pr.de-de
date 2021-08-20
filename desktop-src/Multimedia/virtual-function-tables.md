---
title: Tabellen virtueller Funktionen
description: Tabellen virtueller Funktionen
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b403debddeecbbfe099224943ac6cdf0a1875dff9c19ea08a96e9cb029875a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118135497"
---
# <a name="virtual-function-tables"></a>Tabellen virtueller Funktionen

Eine virtuelle Funktionstabelle ist ein Array von Zeigern auf die Methoden, die ein Objekt unterstützt. Wenn Sie C verwenden, wird ein Objekt als Struktur angezeigt, deren erster Member ein Zeiger auf die virtuelle Funktionstabelle (**lpVtbl**) ist. Das heißt, der erste Member zeigt auf ein Array mit Funktionsze zeigern. Alle Methoden verwenden einen Zeiger auf die Funktionstabelle als ersten Parameter. Daher ruft das folgende Beispiel die **Read-Methode** eines **pStream-Objekts** auf:


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



In C+ + ist der Zeiger auf  die virtuelle Funktionstabelle, der this-Zeiger, implizit. Folgendes entspricht dem vorherigen Beispiel bei Verwendung von C+ +:


```C++
pStream->Read(parameters) 
 
```



 

 




