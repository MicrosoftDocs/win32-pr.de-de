---
title: Verweis Zeiger
description: Verweis Zeiger sind die einfachsten Zeiger und erfordern die geringste Menge an Verarbeitung durch den Clientstub.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 427605f330b1a73c541c95019f8ca4bdd6cc8ef4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039490"
---
# <a name="reference-pointers"></a>Verweis Zeiger

Verweis Zeiger sind die einfachsten Zeiger und erfordern die geringste Menge an Verarbeitung durch den Clientstub. Wenn ein Client Programm einen Verweis Zeiger an eine Remote Prozedur übergibt, enthält der Verweis Zeiger immer die Adresse eines gültigen Speicherblocks. Es wird immer noch auf denselben Speicherblock verwiesen, wenn die Remote Prozedur abgeschlossen ist. Diese Zeiger werden hauptsächlich verwendet, um Verweis Semantik zu implementieren und \[ [**out**](/windows/desktop/Midl/out-idl) - \] Parameter in C zuzulassen.

Im folgenden Beispiel ändert sich der Wert des-Zeigers während des-Aufrufes nicht, obwohl sich der Inhalt der Daten an der durch den Zeiger gekennzeichneten Adresse ändern kann.

![Daten, die sich an einer statischen Verweis Zeiger Adresse ändern](images/prog-a07.png)

Ein Verweis Zeiger hat die folgenden Eigenschaften:

-   Er verweist immer auf einen gültigen Speicher und hat nie den Wert **null**.
-   Sie ändert sich nie während eines Aufrufes und zeigt immer auf denselben Speicher vor und nach dem-Befehl.
-   Daten, die von der Remote Prozedur zurückgegeben werden, werden in den vorhandenen Speicher geschrieben.
-   Auf den Speicher, auf den von einem Verweis Zeiger verwiesen wird, kann nicht von einem anderen Zeiger oder einem anderen Namen in der Funktion zugegriffen werden.

Verwenden Sie das \[ [**ref**](/windows/desktop/Midl/ref) - \] Attribut, um Verweis Zeiger in Schnittstellendefinitionen anzugeben, wie im folgenden Beispiel gezeigt.

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface RefPtrInterface
{
  void RemoteFn([in, out, ref] char *pChar);
}
```

In diesem Beispiel wird der Parameter *PChar* als Zeiger auf ein einzelnes Zeichen, nicht auf ein Array von Zeichen definiert. Dabei handelt es sich um einen \[ **out** \] -Parameter und einen Verweis Zeiger, der auf den Arbeitsspeicher verweist, der von der Server Routine remotefn mit Daten aufgefüllt wird.

 

 