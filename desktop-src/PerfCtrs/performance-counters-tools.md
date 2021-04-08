---
description: In der folgenden Tabelle sind die
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Tools für Leistungsindikatoren
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959748"
---
# <a name="performance-counters-tools"></a>Tools für Leistungsindikatoren

## <a name="data-collection-tools"></a>Tools für die Datensammlung

Die folgenden Tools sind hilfreich beim Verarbeiten oder Bearbeiten von Windows-Leistungsdaten.

|Tool|BESCHREIBUNG
|----|-----------
| [Systemmonitor](/windows-server/administration/windows-commands/perfmon) | GUI-Tool zum Erfassen und Anzeigen von Leistungsdaten. `perfmon.exe` Hiermit wird die MMC mit dem System Monitor-Snap-in gestartet, das Zugriff auf die Tools "System Monitor", "Datensammler Sätze" und "Berichte" bietet.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Befehlszeilen Tool zum Erfassen und Drucken von Leistungsdaten. Kann verwendet werden, um verfügbare Gegensätze aufzulisten, Verfügbare Leistungsindikatoren aufzulisten, Indikator Daten in der Konsole auszugeben oder Leistungsindikator Daten in einer Protokolldatei (CSV, TDF, BLG) zu erfassen.
| [Relog](/windows-server/administration/windows-commands/relog) |Befehlszeilen Tool zum Transformieren und Zusammenführen von Protokolldateien (CSV, TDF, BLG), `typeperf.exe` die über oder über die APIs aufgezeichnet wurden `PDH.dll` .
| [LogMan](/windows-server/administration/windows-commands/logman) |Befehlszeilen Tool zum Steuern von Datensammler Sätzen.

## <a name="data-provider-tools"></a>Datenanbieter Tools

Die folgenden Tools sind hilfreich beim Veröffentlichen von Windows-Leistungsdaten.

|Tool|BESCHREIBUNG
|----|-----------
| [Ctrpp](ctrpp.md) | Das Befehlszeilen-Buildtool aus dem Windows SDK, das das Leistungsindikator-v2-Anbieter Manifest überprüft und kompiliert. Dieses Tool generiert die `.h` Header und `.rc` Ressourcen Skripts, die zum Erstellen eines v2-Anbieters benötigt werden.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Ein Befehlszeilen Tool, mit dem der Anbieter auf einem System installiert wird.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Ein Befehlszeilen Tool, mit dem der Anbieter von einem System deinstalliert wird.
