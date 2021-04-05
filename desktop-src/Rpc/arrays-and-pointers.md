---
title: Arrays und Zeiger
description: Der Remote Prozedur Aufruf (RPC) ist so konzipiert, dass er für Entwickler größtenteils transparent ist.
ms.assetid: 5ad5a51d-a821-44a5-bbc3-14409cb42cb4
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Arrays und Zeiger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4cb6bc3f4a2ec4af85156bf15160b0ce7d1efc33
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103711334"
---
# <a name="arrays-and-pointers"></a>Arrays und Zeiger

Der Remote Prozedur Aufruf (RPC) ist so konzipiert, dass er für Entwickler größtenteils transparent ist. Um diese Transparenz zu erreichen, überträgt der Clientstub sowohl den Zeiger als auch das Datenobjekt, auf das er verweist, an den Server. Wenn die Daten von der Remote Prozedur geändert werden, muss der Server die neuen Daten an den Client zurücksenden, damit der Client die neuen Daten über die ursprünglichen Daten kopieren kann.

Im allgemeinen verhält sich ein Remote Prozedur aufrufsverhalten wie ein lokaler Prozedur Aufrufe. Das heißt, wenn ein Zeiger ein Parameter ist, kann die Remote Prozedur auf das Datenobjekt zugreifen, auf das der Zeiger auf die gleiche Weise wie eine lokale Prozedur verweist.

Da Client-und Serverprogramme in unterschiedlichen Adressbereichen ausgeführt werden, müssen Entwickler Microsoft Interface Definition Language-Attribute (Mittelwert) verwenden, um zu beschreiben, wie Array-und Zeiger Daten zwischen dem Client und dem Server übertragen werden. Dieser Abschnitt enthält eine Übersicht über die Verwendung von Arrays und Zeigern in verteilten Anwendungen in den folgenden Themen:

-   [Arrays und RPC](arrays-and-rpc.md)
-   [Zeiger und RPC](pointers-and-rpc.md)
-   [Verwenden von Arrays, Zeichen folgen und Zeigern](using-arrays-strings-and-pointers.md)

 

 




