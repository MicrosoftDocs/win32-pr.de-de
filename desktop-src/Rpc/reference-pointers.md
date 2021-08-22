---
title: Verweiszeiger
description: Verweiszeiger sind die einfachsten Zeiger und erfordern die geringste Verarbeitung durch den Clientstub.
ms.assetid: 393aec84-8e8f-41b9-956f-d28a80d3a8c4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6338b1017f05bdf004fee2b288c4eae1ee9775eaa2ad225d5f4b6afa3e74d8ea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927035"
---
# <a name="reference-pointers"></a>Verweiszeiger

Verweiszeiger sind die einfachsten Zeiger und erfordern die geringste Verarbeitung durch den Clientstub. Wenn ein Clientprogramm einen Verweiszeiger an eine Remoteprozedur übergibt, enthält der Verweiszeiger immer die Adresse eines gültigen Speicherblocks. Sie verweist nach Abschluss der Remoteprozedur weiterhin auf denselben Speicherblock. Diese Zeiger werden hauptsächlich verwendet, um Verweissemantik zu implementieren und \[ [**out-Parameter**](/windows/desktop/Midl/out-idl) \] in C zuzulassen.

Im folgenden Beispiel ändert sich der Wert des Zeigers während des Aufrufs nicht, obwohl sich der Inhalt der Daten an der vom Zeiger angegebenen Adresse ändern kann.

![Daten, die an einer statischen Verweiszeigeradresse geändert werden](images/prog-a07.png)

Ein Verweiszeiger weist die folgenden Merkmale auf:

-   Sie verweist immer auf gültigen Speicher und hat nie den Wert **NULL**.
-   Sie ändert sich nie während eines Aufrufs und verweist vor und nach dem Aufruf immer auf denselben Speicher.
-   Von der Remoteprozedur zurückgegebene Daten werden in den vorhandenen Speicher geschrieben.
-   Auf den Speicher, auf den ein Verweiszeiger zeigt, kann von keinem anderen Zeiger oder einem anderen Namen in der Funktion zugegriffen werden.

Verwenden Sie das \[ [](/windows/desktop/Midl/ref) \] ref-Attribut, um Verweiszeiger in Schnittstellendefinitionen anzugeben, wie im folgenden Beispiel gezeigt.

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

In diesem Beispiel wird der *Parameter pChar* als Zeiger auf ein einzelnes Zeichen und nicht als Array von Zeichen definiert. Es handelt sich um einen \[ **out-Parameter** \] und einen Verweiszeiger, der auf den Arbeitsspeicher verweist, den die Serverroutine RemoteFn mit Daten auffüllt.

 

 