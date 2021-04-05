---
title: Serialisierungsdienste
description: Microsoft RPC unterstützt zwei Methoden zum Codieren und Decodieren von Daten, kollektiv als Serialisieren von Daten bezeichnet.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Serialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fc5b877e29f7a7f6cd102663017f64bebfdff04
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713542"
---
# <a name="serialization-services"></a>Serialisierungsdienste

Microsoft RPC unterstützt zwei Methoden zum Codieren und Decodieren von Daten, kollektiv als *Serialisieren von Daten* bezeichnet. Serialisierung bedeutet, dass die Daten von den von Ihnen kontrollierten Puffern gemarshallt und aus diesen entfernt werden. Dies unterscheidet sich von der herkömmlichen Verwendung von RPC, bei der die stubvorgänge und die RPC-Lauf Zeit Bibliothek die vollständige Kontrolle über die marshallingpuffer haben und der Prozess transparent ist. Sie können den Puffer für die Speicherung auf permanenten Medien, Verschlüsselung usw. verwenden. Beim Codieren von Daten werden die Daten in einen Puffer gemarshallt, und der Puffer wird an Sie übergeben. Beim Decodieren von Daten geben Sie einen marshallingpuffer mit darin befindlichen Daten an, und die Daten werden aus dem Puffer in den Arbeitsspeicher gemarshallt. Sie können auf einer Prozedur oder einem Typ serialisieren.

> [!Note]  
> Der Begriff *Pickeln* wird häufig von Entwicklern verwendet, um die Serialisierung zu beschreiben. Die Windows SDK Beispiele enthalten ein Verzeichnis namens "pickle", das die Beispiel Programme für die RPC-Serialisierung *beibehält* .

 

Die Serialisierung nutzt die RPC-Mechanismen für das Mars Hallen und das Marshalling von Daten zu anderen Zwecken. Anstatt mehrere e/a-Vorgänge zum Serialisieren einer Gruppe von Objekten in einen Stream zu verwenden, kann eine Anwendung z. b. die Leistung optimieren, indem mehrere Objekte verschiedener Typen in einen Puffer serialisiert und anschließend der gesamte Puffer in einem einzigen Vorgang geschrieben wird. Die Funktionen, die serialisierungshandles manipulieren, sind unabhängig vom Typ der verwendeten Serialisierung.

Ein weiteres Beispiel: Wenn Sie einen Netzwerk Transportmechanismus außer RPC verwenden müssen, z. b. Microsoft Windows Sockets (Winsock). Mit der RPC-Serialisierung kann das Programmaufrufe an Funktionen ausführen, die Ihre Daten in Puffer Mars Hallen, und diese Daten dann mithilfe von Winsock übertragen. Wenn Ihre Anwendung Daten empfängt, kann Sie den RPC-Serialisierungsmechanismus verwenden, um Daten aus Puffern zu entsperren, die von den Winsock-Routinen gefüllt werden. Dies bietet Ihnen viele Vorteile von Anwendungen im RPC-Stil und ermöglicht gleichzeitig die Verwendung von nicht-RPC-Transportmechanismen.

Sie können die Serialisierung auch für Zwecke verwenden, die nicht mit der Netzwerkkommunikation verknüpft sind. Nachdem Sie z. b. die RPC-Codierungs Funktionen zum Mars Hallen von Daten in einen Puffer verwendet haben, können Sie Sie in einer Datei speichern, die von einer anderen Anwendung verwendet werden kann. Sie können Sie auch verschlüsseln. Sie können damit sogar eine Hardware-und betriebssystemunabhängige Darstellung von Daten in einer-Datenbank speichern.

Die folgenden Themen enthalten eine Erläuterung der Serialisierungsdienste, die von Microsoft RPC unterstützt werden:

-   [Verwenden von Serialisierungsdiensten](using-serialization-services.md)
-   [Prozessserialisierung](procedure-serialization.md)
-   [Typserialisierung](type-serialization.md)
-   [Serialisierungshandles](serialization-handles.md)

 

 




