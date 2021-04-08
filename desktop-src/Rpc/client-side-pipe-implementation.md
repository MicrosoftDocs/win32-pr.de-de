---
title: Client-Side Pipe-Implementierung
description: Client seitige Pipe-Implementierung in Remote Prozedur Aufruf (RPC).
ms.assetid: d790f859-47a9-4b6c-a218-8cbe05db21b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5666656f1f7296c252395255c17902a91cb32a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856684"
---
# <a name="client-side-pipe-implementation"></a>Client-Side Pipe-Implementierung

Die Client Anwendung muss die folgenden Prozeduren implementieren, die vom Clientstub während der Datenübertragung aufgerufen werden:

-   Eine Pull-Prozedur (für eine Eingabe Pipe)
-   Eine pushprozedur (für eine ausgabepipe)
-   Eine Zuordnungs Prozedur, um einen Puffer für die Übertragungsdaten zuzuordnen.

Alle diese Prozeduren müssen die Argumente verwenden, die von der von der Mittel l generierten Header Datei angegeben werden. Außerdem muss die Client Anwendung über eine Status Variable verfügen, um zu bestimmen, wo Daten gesucht oder platziert werden sollen.

Die zuordnungsprozedur kann auch so einfach oder so komplex sein, wie Sie benötigt wird. Sie kann z. b. jedes Mal, wenn der Stub die Funktion aufruft, einen Zeiger auf denselben Puffer zurückgeben, oder es kann jeweils eine andere Arbeitsspeicher Menge zuordnen. Wenn Ihre Daten bereits in der richtigen Form vorhanden sind (z. b. ein Array von Pipe-Elementen), können Sie die Zuordnungs Prozedur mit der Pull-Prozedur koordinieren, um einen Puffer zuzuordnen, der die Daten bereits enthält. In diesem Fall kann die Pull-Prozedur eine leere Routine sein.

Die Puffer Zuordnung muss in Bytes erfolgen. Die Push-und Pull-Prozeduren hingegen manipulieren Elemente, deren Größe in Bytes davon abhängt, wie Sie definiert wurden.

In diesem Abschnitt wird die Client Implementierung von Eingabe-und ausgabepipes in den folgenden Abschnitten erläutert:

-   [Implementieren von Eingabe Pipes auf dem Client](implementing-input-pipes-on-the-client.md)
-   [Implementieren von Ausgabe Pipes auf dem Client](implementing-output-pipes-on-the-client.md)

 

 




