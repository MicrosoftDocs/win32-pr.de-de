---
title: Pipes (RPC)
description: Der Pipetypkonstruktor ist ein äußerst effizienter Mechanismus zum Übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Remoteprozeduraufruf RPC , beschrieben, Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c477dc249e400022efda21fef4055840c5095e74500f4ae0bea375310b1903f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927522"
---
# <a name="pipes-rpc"></a>Pipes (RPC)

Der Pipetypkonstruktor ist ein äußerst effizienter Mechanismus zum Übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind. Durch die Verwendung einer Pipe verarbeitet die RPC-Laufzeit die tatsächliche Datenübertragung, wodurch der Aufwand für wiederholte Remoteprozeduraufrufe entbiert wird.

Nachdem ein Client eine Remoteprozedur aufgerufen hat, die über einen Pipeparameter verfügt, werden der Client und der Server eine Eingabeschleife zum Übertragen von Daten ausgeführt. Die Daten können auf dem Client oder dem Server erstellt werden. In beiden Richtungen muss die Datenmenge (in Bytes) nicht im Voraus bekannt sein. Die Daten können inkrementell erstellt oder verwendet werden. Während der Datenübertragungsschleife ruft der Server Stubroutinen auf, die einen Datenpuffer laden oder entladen. Der Client ruft vom Programmierer definierte Prozeduren auf, um Puffer zu reservieren, Daten in die Puffer zu laden und Daten aus den Puffern zu entladen.

Dieser Abschnitt bietet eine Übersicht über die Verwendung von Pipes für Remoteprozeduraufrufe. Die Übersicht wird in den folgenden Themen angezeigt:

-   [Grundlegende Pipeterminologie](essential-pipe-terminology.md)
-   [Der Pipezustand](the-pipe-state.md)
-   [Definieren von Pipes in IDL-Dateien](defining-pipes-in-idl-files.md)
-   [Clientseitige Pipeimplementierung](client-side-pipe-implementation.md)
-   [Serverseitige Pipeimplementierung](server-side-pipe-implementation.md)
-   [Regeln für mehrere Pipes](rules-for-multiple-pipes.md)
-   [Kombinieren von Pipe- und Nonpipe-Parametern](combining-pipe-and-nonpipe-parameters.md)

Weitere Informationen zur Pipesyntax und zu Einschränkungen finden Sie unter [pipe](/windows/desktop/Midl/pipe) in der MIDL-Sprachreferenz. Das PIPES-Beispielprogramm im RPC-Beispielverzeichnis (Platform Software Development Kit) veranschaulicht, wie \\ **\[ \] In-Out-Pipes** verwendet werden, um Daten zwischen einem Client und einem Server zu übertragen.

 

 
