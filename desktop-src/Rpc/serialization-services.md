---
title: Serialisierungsdienste
description: Microsoft RPC unterstützt zwei Methoden zum Codieren und Decodieren von Daten, die zusammen als Serialisieren von Daten bezeichnet werden.
ms.assetid: 36d6ea16-7d01-436e-ac32-610c3ddb8b8d
keywords:
- Rpc-Aufruf einer Remoteprozedur , beschrieben, Serialisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc54e6daf4ace5ffb3ee5d22886a570ae1e9ab1ae834cfac12a91d234c331e20
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035530"
---
# <a name="serialization-services"></a>Serialisierungsdienste

Microsoft RPC unterstützt zwei Methoden zum Codieren und Decodieren von Daten, die zusammen als *Serialisieren von Daten bezeichnet werden.* Serialisierung bedeutet, dass die Daten in Puffer gemarshallt und aus Puffern, die Sie steuern, nicht gemarshallt werden. Dies unterscheidet sich von der herkömmlichen Verwendung von RPC, bei der die Stubs und die RPC-Laufzeitbibliothek die vollständige Kontrolle über die Marshallingpuffer haben und der Prozess transparent ist. Sie können den Puffer für die Speicherung auf permanenten Medien, Verschlüsselung und so weiter verwenden. Wenn Sie Daten codieren, marshallen die RPC-Stubs die Daten in einen Puffer und übergeben den Puffer an Sie. Wenn Sie Daten decodieren, geben Sie einen Marshallingpuffer mit Daten an, und die Daten werden aus dem Puffer in den Arbeitsspeicher entmarshaliert. Sie können auf Prozedur- oder Typbasis serialisieren.

> [!Note]  
> Der Begriff *Pickling* wird häufig von Entwicklern verwendet, um die Serialisierung zu beschreiben. Tatsächlich enthalten die Windows SDK-Beispiele ein Verzeichnis namens *pickle,* das die RPC-Serialisierungsbeispielprogramme beibwahrt.

 

Die Serialisierung nutzt die RPC-Mechanismen zum Marshallen und Unmarshaling von Daten für andere Zwecke. Anstatt beispielsweise mehrere E/A-Vorgänge zum Serialisieren einer Gruppe von Objekten in einen Stream zu verwenden, kann eine Anwendung die Leistung optimieren, indem mehrere Objekte verschiedener Typen in einen Puffer serialisiert und dann der gesamte Puffer in einem einzigen Vorgang geschrieben wird. Die Funktionen, die Serialisierungshandles bearbeiten, sind unabhängig vom Serialisierungstyp, den Sie verwenden.

Ein weiteres Beispiel ist die Verwendung eines Netzwerktransportmechanismus neben RPC, z. B. Microsoft Windows Sockets (Winsock). Mit der RPC-Serialisierung kann Ihr Programm Funktionen aufrufen, die Ihre Daten in Puffer marshallen und diese Daten dann mit Winsock übertragen. Wenn Ihre Anwendung Daten empfängt, kann sie den RPC-Serialisierungsmechanismus verwenden, um Daten aus Puffern, die von den Winsock-Routinen gefüllt werden, zu entmarshalieren. Dadurch erhalten Sie viele Vorteile von ANWENDUNGEN im RPC-Stil und ermöglichen gleichzeitig die Verwendung von Nicht-RPC-Transportmechanismen.

Sie können die Serialisierung auch für Zwecke verwenden, die nicht mit der Netzwerkkommunikation in Zusammenhang stehen. Wenn Sie beispielsweise die RPC-Codierungsfunktionen zum Marshallen von Daten in einen Puffer verwenden, können Sie sie in einer Datei zur Verwendung durch eine andere Anwendung speichern. Sie können sie auch verschlüsseln. Sie können sie sogar verwenden, um eine hardware- und betriebssystemunabhängige Darstellung von Daten in einer Datenbank zu speichern.

In den folgenden Themen werden die Serialisierungsdienste behandelt, die von Microsoft RPC unterstützt werden:

-   [Verwenden von Serialisierungsdiensten](using-serialization-services.md)
-   [Prozedurserialisierung](procedure-serialization.md)
-   [Typserialisierung](type-serialization.md)
-   [Serialisierungshandles](serialization-handles.md)

 

 




