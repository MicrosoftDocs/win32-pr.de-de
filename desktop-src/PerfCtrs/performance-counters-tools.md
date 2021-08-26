---
description: In der folgenden Tabelle sind die
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Leistungsindikatortools
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: a4f1640a269b87cce7452e54a2557dcc9c34fe154ae9e9f95fdd3794e275b59e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033400"
---
# <a name="performance-counters-tools"></a>Leistungsindikatortools

## <a name="data-collection-tools"></a>Tools für die Datensammlung

Die folgenden Tools sind nützlich, wenn Sie Leistungsindikatordaten Windows oder bearbeiten.

|Tool|BESCHREIBUNG
|----|-----------
| [Systemmonitor](/windows-server/administration/windows-commands/perfmon) | GUI-Tool zum Sammeln und Anzeigen von Leistungsindikatordaten. `perfmon.exe` startet MMC mit dem Leistungsmonitor-Snap-In, das Zugriff auf die Tools Leistungsmonitor, Datensammlersätze und Berichte bietet.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Befehlszeilentool zum Sammeln und Drucken von Leistungsindikatordaten. Kann verwendet werden, um verfügbare Leistungsindikatoren auflisten, verfügbare Leistungsindikatoren auflisten, Indikatordaten in der Konsole drucken oder Indikatordaten in einer Protokolldatei (CSV, TDF, BLG) sammeln zu können.
| [Relog](/windows-server/administration/windows-commands/relog) |Befehlszeilentool zum Transformieren und Zusammenführen von Protokolldateien (CSV, TDF, BLG), die über oder über die `typeperf.exe` `PDH.dll` APIs erfasst wurden.
| [Logman](/windows-server/administration/windows-commands/logman) |Befehlszeilentool zum Steuern von Datensammlersätzen.

## <a name="data-provider-tools"></a>Datenanbietertools

Die folgenden Tools sind beim Veröffentlichen von Leistungsindikatordaten Windows nützlich.

|Tool|BESCHREIBUNG
|----|-----------
| [STRPP](ctrpp.md) | Befehlszeilen-Buildtool aus dem Windows SDK, das Ihr Leistungsindikator-V2-Anbietermanifest überprüft und kompiliert. Dieses Tool generiert die Header `.h` und Ressourcenskripts, die `.rc` zum Erstellen eines V2-Anbieters erforderlich sind.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Befehlszeilentool, das zum Installieren Ihres Anbieters auf einem System verwendet wird.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Befehlszeilentool, das zum Deinstallieren Ihres Anbieters von einem System verwendet wird.
