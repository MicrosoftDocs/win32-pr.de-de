---
title: Virtuelle Funktionstabellen
description: Virtuelle Funktionstabellen
ms.assetid: 1b7c6da6-3156-46fe-a9ca-0c1717fe28b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a784a027f7e1120d8e7092aa5dd6c0f5c0e958b3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341841"
---
# <a name="virtual-function-tables"></a>Virtuelle Funktionstabellen

Eine virtuelle Funktions Tabelle ist ein Array von Zeigern auf die Methoden, die von einem Objekt unterstützt werden. Wenn Sie C verwenden, wird ein Objekt als Struktur angezeigt, deren erstes Element ein Zeiger auf die virtuelle Funktions Tabelle (**lpvtbl**) ist. Das heißt, das erste Element verweist auf ein Array mit Funktions Zeigern. Die Methoden übernehmen einen Zeiger auf die Funktions Tabelle als ersten Parameter. Daher wird im folgenden Beispiel die **Read** -Methode eines **pStream** -Objekts aufgerufen:


```C++
pStream->lpVtbl->Read(pStream, parameters) 
 
```



In C + + ist der Zeiger auf die virtuelle Funktions Tabelle, der *this* -Zeiger, implizit. Das folgende Beispiel entspricht dem vorherigen Beispiel bei Verwendung von C + +:


```C++
pStream->Read(parameters) 
 
```



 

 




