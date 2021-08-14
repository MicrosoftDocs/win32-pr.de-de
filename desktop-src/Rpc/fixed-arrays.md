---
title: Feste Arrays
description: Wenn Ihre Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet. Wenn Sie MIDL verwenden, definieren Sie feste Arrays auf die gleiche Weise, wie Sie sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1040e417cc896b9f4bd2271dc69e23033332354357b2aad32053724d94b79035
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929979"
---
# <a name="fixed-arrays"></a>Feste Arrays

Wenn Ihre Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet. Wenn Sie MIDL verwenden, definieren Sie feste Arrays auf die gleiche Weise, wie Sie sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.

Im folgenden Beispiel wird veranschaulicht, wie ein festes Array definiert wird.

``` syntax
[
    /*Attributes are defined here. */
]
interface MyInterface
{
    const long ARRAY_SIZE = 1000;

    MyRemoteProc(char achArray[ARRAY_SIZE]);

    /* Other interface procedures are defined here. */
}
```

Wenn ein Clientprogramm ein festes Array an ein Serverprogramm übergibt, sendet der Clientstub das gesamte Array an den Serverstub. Der Serverstub belegt Arbeitsspeicher für das Array und speichert die Arraydaten, die er über das Netzwerk empfängt, im zugeordneten Arbeitsspeicher. Anschließend wird das Array an die Remoteprozedur auf dem Server übergeben. Der Server kann die Daten im Array ändern.

Wenn die Remoteprozedur beendet wird, sendet der Serverstub den Inhalt des Arrays zurück an den Client. Der Clientstub kopiert die vom Serverstub empfangenen Daten in das ursprüngliche Array. Das Clientprogramm kann die Daten dann so verwenden, als ob es die Daten von einem lokalen Prozeduraufruf empfangen hätte.

 

 




