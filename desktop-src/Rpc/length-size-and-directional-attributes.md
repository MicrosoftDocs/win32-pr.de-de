---
title: Länge, Größe und direktionale Attribute
description: Bei der Übergabe von Arrays zwischen dem Client und dem Server sind die Größen bezogenen Attribute \ Max \_ \ und \ size \_ \ bestimmt, wie viele Array Elemente der Stub des Servers zuordnet.
ms.assetid: 2c95cf47-6fc0-4ccd-bb4f-acf356596e56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98ffbf1ac75ad82a89e258ab595590fce2190b9e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729305"
---
# <a name="length-size-and-directional-attributes"></a>Länge, Größe und direktionale Attribute

Bei der Übergabe von Arrays zwischen dem Client und dem Server sind die Größen bezogenen Attribute \[ [**\_ Max**](/windows/desktop/Midl/max-is) , \] und die \[ [**Größe \_**](/windows/desktop/Midl/size-is) bestimmt, \] wie viele Array Elemente der Stub des Servers zuordnet. Die Länge der Längen bezogenen Attribute \[ [**\_ beträgt**](/windows/desktop/Midl/length-is) \] , das \[ [**erste \_ ist**](/windows/desktop/Midl/first-is) \] , und der \[ [**Letzte \_**](/windows/desktop/Midl/last-is) Wert \] bestimmt, wie viele Elemente an den Server und den Client übertragen werden.

Auf Parameter können unterschiedliche direktionale Attribute angewendet werden. Einige Kombinationen von direktionalen Attributen können jedoch Fehler verursachen. Angenommen, Sie schreiben eine Schnittstelle, die eine Prozedur mit zwei Parametern, einem Array und der übertragenen Länge des Arrays angibt. Der Begriff *dir \_ attr* bezieht sich auf das auf den Parameter angewendete direktionale Attribut wie folgt:

``` syntax
Proc1(
    [dir_attr] short *plength;
    [dir_attr, length_is(pLength)] short array[MAX_SIZE]);
```

Das Mittelwert-Compilerverhalten für jede Kombination aus direktionalen Attributen wird in der folgenden Tabelle beschrieben.



| Array                                          | Length-Parameter                               | Stub-Aktionen während des Aufrufes vom Client zum Server                                                                                                                                                                                                                          | Stub-Aktionen bei Rückgabe von Server zu Client                                                                                                                                                                         |
|------------------------------------------------|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den-Parameter angegeben werden.                                                                                                                                                                                              | Es wurden keine Daten übertragen.                                                                                                                                                                                                 |
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | Nicht zulässig; Mittlerer l-Compilerfehler.                                                                                                                                                                                                                                         | Nicht zulässig; Mittlerer l-Compilerfehler.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in)\]                          | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den length-Parameter angegeben werden.                                                                                                                                                                                       | Nur die Länge übertragen.                                                                                                                                                                                            |
| \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge.<br/> Wenn die Array Größe korrigiert ist, müssen Sie die Array Größe auf dem Server zuordnen, aber keine Elemente übertragen.<br/> Wenn die Array Größe nicht gebunden ist, ist dies nicht zulässig: mittlerer l-Compilerfehler.<br/>                                                              | Übertragen Sie die Anzahl der Elemente, die durch die Länge angegeben werden.<br/> Beachten Sie, dass die Länge geändert werden kann und einen anderen Wert als der Wert auf dem Client aufweisen kann. Die Länge darf nicht übertragen werden.<br/>          |
| \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | Weisen Sie Speicherplatz für den length-Parameter auf dem Server zu, übertragen Sie den-Parameter jedoch nicht. Wenn die Array Größe korrigiert ist, müssen Sie die Array Größe auf dem Server zuordnen, aber keine Elemente übertragen.<br/> Wenn die Array Größe nicht korrigiert ist, ist dies nicht zulässig: mittlerer l-Compilerfehler.<br/> | Übertragen Sie die Länge und die Anzahl der Elemente, die durch die von der Serveranwendung festgelegte Länge angegeben werden.                                                                                                             |
| \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie den length-Parameter. Wenn die Array Größe gebunden ist, müssen Sie die Array Größe auf dem Server zuordnen, aber keine Elemente übertragen.<br/> Wenn die Array Größe nicht gebunden ist, ist dies nicht zulässig: mittlerer l-Compilerfehler.<br/>                                                           | Übertragen Sie die Länge. Übertragen Sie die Anzahl der Array Elemente, die durch die Länge angegeben werden.<br/>                                                                                                                       |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in)\]                          | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den-Parameter angegeben werden.                                                                                                                                                                                              | Die Länge darf nicht übertragen werden. Übertragen Sie die Anzahl der Elemente, die durch die Länge angegeben werden.<br/> Beachten Sie, dass die Länge geändert werden kann und einen anderen Wert als den ursprünglichen Wert auf dem Client aufweisen kann.<br/> |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**vorgenommen**](/windows/desktop/Midl/out-idl)\]                    | Nicht zulässig; Mittlerer l-Compilerfehler.                                                                                                                                                                                                                                         | Nicht zulässig; Mittlerer l-Compilerfehler.                                                                                                                                                                                      |
| \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | \[[**in**](/windows/desktop/Midl/in), [ **out**](/windows/desktop/Midl/out-idl)\] | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den-Parameter angegeben werden.                                                                                                                                                                                              | Übertragen Sie die Länge und die Anzahl der Elemente, die durch den-Parameter angegeben werden.                                                                                                                                           |



 

Im Allgemeinen sollten Sie die Längen-oder Größen Parameter auf der Serverseite nicht ändern. Wenn Sie den length-Parameter ändern, können Sie Arbeitsspeicher verwaist. Weitere Informationen finden Sie unter Arbeits [Speicher verwaisen](memory-orphaning.md).

 

