---
title: Pipes (RPC)
description: Der pipetypkonstruktor ist ein sehr effizienter Mechanismus zum übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind.
ms.assetid: 913d5e2a-00ad-4060-9274-a6db23fb2817
keywords:
- Remote Prozedur Aufruf RPC, beschrieben, Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6c670b51dfe634fb5b3318e0a0b8a796cfbf988
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474874"
---
# <a name="pipes-rpc"></a>Pipes (RPC)

Der pipetypkonstruktor ist ein sehr effizienter Mechanismus zum übergeben großer Datenmengen oder einer beliebigen Menge von Daten, die nicht alle gleichzeitig im Arbeitsspeicher verfügbar sind. Durch die Verwendung einer Pipe verarbeitet die RPC-Laufzeit die tatsächliche Datenübertragung und entfällt so den Aufwand, der mit wiederholten Remote Prozedur aufrufen verbunden ist.

Nachdem ein Client eine Remote Prozedur mit einem Pipe-Parameter aufgerufen hat, geben der Client und der Server Schleifen zum Übertragen von Daten ein. Die Daten können auf dem Client oder dem Server erstellt werden. In jedem Fall muss die Datenmenge (in Bytes) nicht im Voraus bekannt sein. Die Daten können inkrementell erzeugt oder genutzt werden. In der Datenübertragungs Schleife ruft der Server Stub-Routinen auf, die einen Datenpuffer laden oder entladen. Der Client ruft vom Programmierer definierte Prozeduren auf, um Puffer zuzuordnen, Daten in Daten zu laden und aus den Puffern zu entladen.

Dieser Abschnitt bietet eine Übersicht über die Verwendung von Pipes für Remote Prozedur Aufrufe. Sie finden die Übersicht in den folgenden Themen:

-   [Wichtige Pipe-Terminologie](essential-pipe-terminology.md)
-   [Der Pipezustand](the-pipe-state.md)
-   [Definieren von Pipes in IDL-Dateien](defining-pipes-in-idl-files.md)
-   [Client seitige Pipe-Implementierung](client-side-pipe-implementation.md)
-   [Server seitige Pipe-Implementierung](server-side-pipe-implementation.md)
-   [Regeln für mehrere Pipes](rules-for-multiple-pipes.md)
-   [Kombinieren von Pipe-und nonpipe-Parametern](combining-pipe-and-nonpipe-parameters.md)

Weitere Informationen zur Pipe-Syntax und zu Einschränkungen finden Sie unter [Pipe](/windows/desktop/Midl/pipe) in der Sprache der Mittel l-Sprache. Das Pipes-Beispielprogramm in der Platform Software Development Kit (SDK)-Beispiele \\ RPC-Verzeichnis veranschaulicht, wie Sie **\[ in, out \]** Pipes zum Übertragen von Daten zwischen einem Client und einem Server verwenden.

 

 
