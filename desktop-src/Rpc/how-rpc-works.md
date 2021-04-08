---
title: Funktionsweise von RPC
description: Die RPC-Tools machen es Benutzern so angezeigt, als ob ein Client eine Prozedur direkt aufruft, die sich in einem Remote Serverprogramm befindet.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12832d0de4eb972bb1d9d51df0c871191d4d079a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711832"
---
# <a name="how-rpc-works"></a>Funktionsweise von RPC

Die RPC-Tools machen es Benutzern so angezeigt, als ob ein Client eine Prozedur direkt aufruft, die sich in einem Remote Serverprogramm befindet. Client und Server verfügen jeweils über eigene Adressräume. Das heißt, jede verfügt über eine eigene Speicher Ressource, die den Daten zugeordnet ist, die von der Prozedur verwendet werden. Die folgende Abbildung veranschaulicht die RPC-Architektur.

![RPC-Architektur](images/prog-a11.png)

Wie die Abbildung zeigt, ruft die Client Anwendung anstelle des eigentlichen Codes, der die Prozedur implementiert, eine lokale Stub-Prozedur auf. Stusb werden kompiliert und mit der Client Anwendung verknüpft. Anstatt den eigentlichen Code zu enthalten, der die Remote Prozedur implementiert, wird der Client-Stub-Code:

-   Ruft die erforderlichen Parameter aus dem Client Adressbereich ab.
-   Übersetzt die Parameter nach Bedarf in ein Standardmäßiges NDR-Format für die Übertragung über das Netzwerk.
-   Ruft Funktionen in der RPC-Client Lauf Zeit Bibliothek auf, um die Anforderung und ihre Parameter an den Server zu senden.

Der Server führt die folgenden Schritte aus, um die Remote Prozedur aufzurufen.

1.  Die Server-RPC-Lauf Zeit Bibliotheksfunktionen akzeptieren die Anforderung und wenden die Stub-Prozedur des Servers an.
2.  Der Serverstub Ruft die Parameter aus dem Netzwerk Puffer ab und konvertiert sie aus dem Netzwerk Übertragungsformat in das Format, das der Server benötigt.
3.  Der Serverstub Ruft das eigentliche Verfahren auf dem Server auf.

Anschließend wird die Remote Prozedur ausgeführt, die möglicherweise Ausgabeparameter und einen Rückgabewert erzeugt. Wenn die Remote Prozedur beendet ist, werden die Daten mit einer ähnlichen Sequenz von Schritten an den Client zurückgegeben.

1.  Die Remote Prozedur gibt die Daten an den Serverstub zurück.
2.  Der Serverstub konvertiert Ausgabeparameter in das Format, das für die Übertragung über das Netzwerk erforderlich ist, und gibt Sie an die RPC-Lauf Zeit Bibliotheksfunktionen zurück.
3.  Die Server-RPC-Lauf Zeit Bibliotheksfunktionen übertragen die Daten im Netzwerk an den Client Computer.

Der Client schließt den Prozess ab, indem er die Daten über das Netzwerk akzeptiert und an die aufrufende Funktion zurückgibt.

1.  Die Client-RPC-Lauf Zeit Bibliothek empfängt die Remote Prozedur Rückgabewerte und gibt Sie an den Client-Stub zurück.
2.  Der Clientstub konvertiert die Daten aus dem Mandanten in das Format, das vom Client Computer verwendet wird. Der Stub schreibt Daten in den Client Speicher und gibt das Ergebnis an das Aufruf Programm auf dem Client zurück.
3.  Die aufrufende Prozedur wird so fortgesetzt, als ob die Prozedur auf dem gleichen Computer aufgerufen wurde.

Die Laufzeitbibliotheken werden in zwei Teilen bereitgestellt: eine Import Bibliothek, die mit der Anwendung verknüpft ist, und die RPC-Lauf Zeit Bibliothek, die als Dynamic Link Library (dll) implementiert wird.

Die Serveranwendung enthält Aufrufe der Server Lauf Zeit Bibliotheksfunktionen, die die-Schnittstelle des Servers registrieren und dem Server das akzeptieren von Remote Prozedur aufrufen erlauben. Die Serveranwendung enthält auch die anwendungsspezifischen Remote Prozeduren, die von den Client Anwendungen aufgerufen werden.

 

 




