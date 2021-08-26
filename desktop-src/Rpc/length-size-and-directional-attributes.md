---
title: Länge, Größe und direktionale Attribute
description: Bei der Übergabe von Arrays zwischen Client und Server bestimmen die größenbezogenen Attribute \ max is\ und \ size ist\, wie viele Arrayelemente der \_ \_ Serverstub zuteilen.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e91424a93a53fe710c945011d19f8f97dc0f65e4899bc3305be5725d5a08e7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020131"
---
# <a name="length-size-and-directional-attributes"></a>Länge, Größe und direktionale Attribute

Bei der Übergabe von Arrays zwischen client und server wird durch die größenbezogenen Attribute max und size bestimmt, wie viele Arrayelemente vom \[ [**\_**](/windows/desktop/Midl/max-is) \] \[ [**\_**](/windows/desktop/Midl/size-is) \] Serverstub reserviert werden. Die Länge der längenbezogenen Attribute ist , zuerst ist , und zuletzt wird bestimmt, wie viele Elemente sowohl an den Server als auch an den \[ [**\_**](/windows/desktop/Midl/length-is) \] Client übertragen \[ [**\_**](/windows/desktop/Midl/first-is) \] \[ [**\_**](/windows/desktop/Midl/last-is) \] werden.

Auf Parameter können unterschiedliche direktionale Attribute angewendet werden. Einige Kombinationen von direktionalen Attributen können jedoch Fehler verursachen. Angenommen, Sie schreiben eine Schnittstelle, die eine Prozedur mit zwei Parametern, einem Array und der übertragenen Länge des Arrays angibt. Der Begriff *dir \_ attr bezieht* sich auf das direktionale Attribut, das auf den Parameter angewendet wird:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

Das MIDL-Compilerverhalten für jede Kombination von direktionalen Attributen wird in der folgenden Tabelle beschrieben.



| Array                                          | Length-Parameter                               | Stubaktionen während des Aufrufs vom Client zum Server                                                                                                                                                                                                                          | Stubaktionen bei Rückgabe vom Server zum Client                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**In**](/windows/desktop/Midl/in)\]                          | \[[**In**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge und die Anzahl der elemente, die durch den -Parameter angegeben werden.                                                                                                                                                                                              | Es werden keine Daten übertragen.                                                                                                                                                                                                 |
| \[[**In**](/windows/desktop/Midl/in)\]                          | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Nicht legal; MIDL-Compilerfehler.                                                                                                                                                                                                                                         | Nicht legal; MIDL-Compilerfehler.                                                                                                                                                                                      |
| \[[**In**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den length-Parameter angegeben werden.                                                                                                                                                                                       | Übertragen Sie nur die Länge.                                                                                                                                                                                            |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**In**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge.<br/> Wenn die Arraygröße fest ist, ordnen Sie die Arraygröße auf dem Server zu, übertragen aber keine Elemente.<br/> Wenn die Arraygröße nicht gebunden ist, nicht legal: MIDL-Compilerfehler.<br/>                                                              | Übertragen Sie die Anzahl der Elemente, die durch die Länge angegeben werden.<br/> Beachten Sie, dass die Länge geändert werden kann und einen anderen Wert als der Wert auf dem Client haben kann. Übertragen Sie die Länge nicht.<br/>          |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Ordnen Sie Speicherplatz für den Length-Parameter auf dem Server zu, übertragen Sie den Parameter jedoch nicht. Wenn die Arraygröße fest ist, ordnen Sie die Arraygröße auf dem Server zu, übertragen jedoch keine Elemente.<br/> Wenn die Arraygröße nicht festgelegt ist, nicht legal: MIDL-Compilerfehler.<br/> | Übertragen Sie die Länge und die Anzahl der Elemente, die durch die von der Serveranwendung festgelegten Länge angegeben werden.                                                                                                             |
| \[[**out**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie den Length-Parameter. Wenn die Arraygröße gebunden ist, ordnen Sie die Arraygröße auf dem Server zu, übertragen aber keine Elemente.<br/> Wenn die Arraygröße nicht gebunden ist, nicht legal: MIDL-Compilerfehler.<br/>                                                           | Übertragen Sie die Länge. Übertragen Sie die Anzahl der Arrayelemente, die durch die Länge angegeben werden.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**In**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge und die Anzahl der elemente, die durch den -Parameter angegeben werden.                                                                                                                                                                                              | Übertragen Sie die Länge nicht. Übertragen Sie die Anzahl der Elemente, die durch die Länge angegeben werden.<br/> Beachten Sie, dass die Länge geändert werden kann und einen anderen Wert als der ursprüngliche Wert auf dem Client haben kann.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**out**](/windows/desktop/Midl/out-idl)\]                    | Nicht legal; MIDL-Compilerfehler.                                                                                                                                                                                                                                         | Nicht legal; MIDL-Compilerfehler.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie die Länge und die Anzahl der elemente, die durch den -Parameter angegeben werden.                                                                                                                                                                                              | Übertragen Sie die Länge und die Anzahl der elemente, die durch den -Parameter angegeben werden.                                                                                                                                           |



 

Im Allgemeinen sollten Sie die Längen- oder Größenparameter auf serverseitiger Seite nicht ändern. Wenn Sie den Length-Parameter ändern, können Sie verwaisten Arbeitsspeicher verwenden. Weitere Informationen finden Sie unter [Verwaister Arbeitsspeicher.](memory-orphaning.md)

 

