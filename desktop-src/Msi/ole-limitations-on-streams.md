---
description: Entwickler von Installations Datenbanken müssen zwei Einschränkungen bei der Behandlung von Streams durch die strukturierte Win32 OLE-Speicher Implementierung beachten.
ms.assetid: ebd5fcac-0238-4f30-9fd5-a0c5cf9028ef
title: OLE-Einschränkungen für Streams
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8ccf2a259b004605381792a4eb9da62d329be91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214952"
---
# <a name="ole-limitations-on-streams"></a>OLE-Einschränkungen für Streams

Entwickler von Installations Datenbanken müssen zwei Einschränkungen bei der Behandlung von Streams durch die strukturierte Win32 OLE-Speicher Implementierung beachten. Diese Einschränkungen können sich durch Transformationen und andere Daten, die in der Datenbank als Stream gespeichert werden können, indirekt auf die Installer-Funktionen auswirken.

Es gibt zwei relevante Einschränkungen:

-   Binärdaten werden mit einem Indexnamen gespeichert, der erstellt wird, indem der Tabellenname und die Werte der Primärschlüssel des Datensatzes mithilfe eines Punkte Trennzeichens verkettet werden. OLE schränkt Streamnamen auf 32 Zeichen ein (31 + null-Terminator). Windows Installer verwendet einen Komprimierungs Algorithmus, der das Limit je nach Zeichen auf 62 Zeichen erweitern kann. Beachten Sie, dass Doppelbyte Zeichen als 2 gezählt werden.
-   Obwohl mehrere Streams gleichzeitig geöffnet sein können, können Sie einen Stream nicht ein zweites Mal öffnen, bis der erste Verweis geschlossen wird. Dies bedeutet, dass Sie nicht denselben binären Datenstrom auswählen können, der gleichzeitig in mehreren Datensätzen geöffnet werden soll. Der Versuch, die Binärdaten aus dem zweiten Datensatz zu lesen, schlägt fehl. Außerdem können Sie die Primärschlüssel eines Datensatzes nicht umbenennen, während ein binärer Datenstrom in diesem Datensatz geöffnet ist.

 

 



