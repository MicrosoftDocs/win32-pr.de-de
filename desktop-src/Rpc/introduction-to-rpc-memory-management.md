---
title: Einführung in die RPC-Speicherverwaltung
description: Einführung in die RPC-Speicherverwaltung (Remote Procedure Call).
ms.assetid: 3474d79c-93ef-4221-b9ea-9173978e2929
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a169f87bbd8a9747dd7a4983a26f1122cf575e95434ed0dd3be346bae12b9a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928930"
---
# <a name="introduction-to-rpc-memory-management"></a>Einführung in die RPC-Speicherverwaltung

Im Kontext von RPC umfasst die Speicherverwaltung Folgendes:

-   Zuordnung und Zuordnung des Arbeitsspeichers, der zum Simulieren eines einzelnen konzeptionellen Adressraums zwischen client und server in den verschiedenen Adressräumen der Threads des Clients und Servers erforderlich ist.
-   Bestimmen, welche Softwarekomponente für die Verwaltung des Arbeitsspeichers verantwortlich ist – die Anwendung oder der MIDL-generierte Stub.
-   Auswählen von MIDL-Attributen, die sich auf die Speicherverwaltung auswirken: Richtungsattribute, Zeigerattribute, Arrayattribute und die \[ [ \_ Byteanzahl](/windows/desktop/Midl/byte-count)der ACF-Attribute, \] \[ [Zuordnen](/windows/desktop/Midl/allocate)und Aktivieren von \] \[ [ \_ Zuordnen.](/windows/desktop/Midl/enable-allocate) \]

Wenn ein Programm eine Funktion oder Prozedur im Adressraum aufruft, ist die Speicherverwaltung einfacher als in einer verteilten Anwendung. Zur Veranschaulichung wird im folgenden Diagramm eine binäre Struktur dargestellt. Um diese Datenstruktur an eine Prozedur im Adressraum zu übergeben, übergibt ein Programm einfach einen Zeiger auf den Stamm der Struktur.

![eine binäre Struktur mit Zeigern auf Strukturdaten, die im Stamm der Struktur enthalten sind](images/bintree.png)

Client-/Server-RPC-Anwendungen nutzen Daten über zwei verschiedene Speicherplätze hinweg gemeinsam. Diese Speicherplätze können sich auf demselben Computer befinden oder nicht. In beiden Fällen haben Client und Server keinen direkten Zugriff auf den Arbeitsspeicher des jeweils anderen. RPC hängt von der Fähigkeit ab, den Adressraum des Clientprogramms im Adressraum des Serverprogramms zu simulieren. Außerdem müssen Daten, einschließlich neuer und geänderter Daten, vom Server an den Clientspeicher zurückgegeben werden.

In Fällen wie der im vorherigen Diagramm dargestellten binären Struktur reicht es nicht aus, einen Zeiger auf den Stammknoten an eine Remoteprozedur zu übergeben. Das Programm oder die Stubs müssen die gesamte Struktur an den Adressraum des Servers übergeben, damit die Remoteprozedur darauf zugreifen kann.

 

 