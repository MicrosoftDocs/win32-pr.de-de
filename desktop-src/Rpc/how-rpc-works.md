---
title: Funktionsweise von RPC
description: Die RPC-Tools erscheinen Benutzern so, als ob ein Client direkt eine Prozedur aufruft, die sich in einem Remoteserverprogramm befindet.
ms.assetid: 265f31b8-9a41-4255-b070-fd50b00b935b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bd7a3adf59e848d962d4765a0feee16eb1fa84842c2a1ddd34ed82ecf95a8e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020854"
---
# <a name="how-rpc-works"></a>Funktionsweise von RPC

Die RPC-Tools erscheinen Benutzern so, als ob ein Client direkt eine Prozedur aufruft, die sich in einem Remoteserverprogramm befindet. Client und Server verfügen jeweils über eigene Adressräume. Das heißt, jede verfügt über eine eigene Speicherressource, die daten zugeordnet ist, die von der Prozedur verwendet werden. Die folgende Abbildung veranschaulicht die RPC-Architektur.

![RPC-Architektur](images/prog-a11.png)

Wie die Abbildung zeigt, ruft die Clientanwendung eine lokale Stubprozedur auf, anstatt den tatsächlichen Code, der die Prozedur implementieren soll. Stubs werden kompiliert und mit der Clientanwendung verknüpft. Der Clientstubcode enthält nicht den tatsächlichen Code, der die Remoteprozedur implementiert:

-   Ruft die erforderlichen Parameter aus dem Clientadressenraum ab.
-   Übersetzt die Parameter nach Bedarf in ein NDR-Standardformat für die Übertragung über das Netzwerk.
-   Ruft Funktionen in der RPC-Client-Laufzeitbibliothek auf, um die Anforderung und ihre Parameter an den Server zu senden.

Der Server führt die folgenden Schritte aus, um die Remoteprozedur auf aufruft.

1.  Die RPC-Laufzeitbibliotheksfunktionen des Servers akzeptieren die Anforderung und rufen die Serverstubprozedur auf.
2.  Der Serverstub ruft die Parameter aus dem Netzwerkpuffer ab und konvertiert sie aus dem Netzwerkübertragungsformat in das format, das der Server benötigt.
3.  Der Serverstub ruft die tatsächliche Prozedur auf dem Server auf.

Die Remoteprozedur wird dann ausgeführt und generiert möglicherweise Ausgabeparameter und einen Rückgabewert. Wenn die Remoteprozedur abgeschlossen ist, werden die Daten in einer ähnlichen Abfolge von Schritten an den Client zurückgegeben.

1.  Die Remoteprozedur gibt ihre Daten an den Serverstub zurück.
2.  Der Serverstub konvertiert Ausgabeparameter in das format, das für die Übertragung über das Netzwerk erforderlich ist, und gibt sie an die RPC-Laufzeitbibliotheksfunktionen zurück.
3.  Die RPC-Laufzeitbibliotheksfunktionen des Servers übertragen die Daten im Netzwerk an den Clientcomputer.

Der Client schließt den Prozess ab, indem er die Daten über das Netzwerk akzeptiert und an die aufrufende Funktion zurücksendet.

1.  Die RPC-Laufzeitbibliothek des Clients empfängt die Rückgabewerte der Remoteprozedur und gibt sie an den Clientstub zurück.
2.  Der Clientstub konvertiert die Daten aus dem NDR in das vom Clientcomputer verwendete Format. Der Stub schreibt Daten in den Clientspeicher und gibt das Ergebnis an das aufrufende Programm auf dem Client zurück.
3.  Die aufrufende Prozedur wird so fortgesetzt, als wäre die Prozedur auf demselben Computer aufgerufen worden.

Die Laufzeitbibliotheken werden in zwei Teilen bereitgestellt: einer Importbibliothek, die mit der Anwendung verknüpft ist, und der RPC-Laufzeitbibliothek, die als Dll (Dynamic Link Library) implementiert ist.

Die Serveranwendung enthält Aufrufe der Funktionen der Server-Laufzeitbibliothek, die die Schnittstelle des Servers registrieren und es dem Server ermöglichen, Remoteprozeduraufrufe zu akzeptieren. Die Serveranwendung enthält auch die anwendungsspezifischen Remoteverfahren, die von den Clientanwendungen aufgerufen werden.

 

 




