---
description: Entwickler von Installationsdatenbanken müssen zwei Einschränkungen bei der Verarbeitung von Datenströmen durch die Win32 OLE Structured Storage-Implementierung beachten.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: OLE-Einschränkungen Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69a3a1c606a4446129d9e6592c9b352dd0b3e06ae5c77bb378c2430a32cbc568
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119754250"
---
# <a name="ole-limitations-on-streams"></a>OLE-Einschränkungen Streams

Entwickler von Installationsdatenbanken müssen zwei Einschränkungen bei der Verarbeitung von Datenströmen durch die Win32 OLE Structured Storage-Implementierung beachten. Diese Einschränkungen können sich indirekt durch Transformationen und andere Daten, die in der Datenbank als Stream gespeichert werden können, auf Installerfunktionen auswirken.

Es gibt zwei relevante Einschränkungen:

-   Binärdaten werden mit einem Indexnamen gespeichert, der durch Verkettung des Tabellennamens und der Werte der Primärschlüssel des Datensatzes mithilfe eines Zeitraumtrennzeichens erstellt wird. OLE beschränkt Streamnamen auf 32 Zeichen (31 + NULL-Abschlusszeichen). Windows Das Installationsprogramm verwendet einen Komprimierungsalgorithmus, der den Grenzwert je nach Zeichen auf 62 Zeichen erweitern kann. Beachten Sie, dass Doppel bytezeichen als 2 gezählt werden.
-   Obwohl mehrere Streams gleichzeitig geöffnet sein können, können Sie einen Stream erst ein zweites Mal öffnen, wenn der erste Verweis geschlossen wird. Dies bedeutet, dass Sie nicht denselben binären Datenstrom auswählen können, um in mehreren Datensätzen gleichzeitig geöffnet zu sein. Fehler beim Lesen der Binärdaten aus dem zweiten Datensatz. Außerdem können Sie die Primärschlüssel eines Datensatzes nicht umbenennen, solange ein binärer Datenstrom in diesem Datensatz geöffnet ist.

 

 



