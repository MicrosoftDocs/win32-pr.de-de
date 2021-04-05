---
title: Fixierte Arrays
description: Wenn die Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet. Bei der Verwendung von "Mittel l" definieren Sie fixierte Arrays auf die gleiche Weise, wie Sie Sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.
ms.assetid: b9a2fa0b-1386-43e1-ab55-0a57cd8d1f18
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bb3a620e86bff47e04afb5078dff50faee9fef0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711430"
---
# <a name="fixed-arrays"></a>Fixierte Arrays

Wenn die Schnittstelle ein Array mit einer bestimmten Anzahl von Elementen als Parameter angibt, wird ein festes Array verwendet. Bei der Verwendung von "Mittel l" definieren Sie fixierte Arrays auf die gleiche Weise, wie Sie Sie in C definieren. Sie geben den Typ, den Namen und die Größe des Arrays an.

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

Wenn ein Client Programm ein festes Array an ein Serverprogramm übergibt, sendet der Clientstub das gesamte Array an den Serverstub. Der Serverstub ordnet Speicher für das Array zu und speichert die Array Daten, die er über das Netzwerk empfängt, in den zugeordneten Arbeitsspeicher. Anschließend wird das Array an die Remote Prozedur auf dem Server weitergeleitet. Der Server kann die Daten im Array ändern.

Wenn die Remote Prozedur beendet wird, sendet der Server-Stub den Inhalt des Arrays an den Client zurück. Der Client-Stub kopiert die Daten, die er aus dem Serverstub empfangen hat, in das ursprüngliche Array. Das Client Programm kann dann die Daten wie beim Empfang der Daten von einem lokalen Prozedur aufrufsvorgang verwenden.

 

 




