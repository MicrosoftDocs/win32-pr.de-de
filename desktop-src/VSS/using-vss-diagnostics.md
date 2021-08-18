---
description: Vsdiagview und Vssagent sind Tools, die Sie zur Problembehandlung von VSS-Anwendungen verwenden können. Hinweis Diese Tools sind im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Verwenden der VSS-Diagnose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7742bf706da0bb8fdd377960a597a61b6592b772df98982cec500434f66c7579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118590803"
---
# <a name="using-vss-diagnostics"></a>Verwenden der VSS-Diagnose

Vsdiagview und Vssagent sind Tools, die Sie zur Problembehandlung von VSS-Anwendungen verwenden können.

> [!Note]  
> Diese Tools sind im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Sie können das Windows SDK von [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) herunterladen.

 

In der Windows SDK-Installation finden Sie diese Tools unter `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

## <a name="gathering-data"></a>Sammeln von Daten

Sie können Daten mithilfe des Vssagent-Befehls sammeln.

**So sammeln Sie Daten mit vssagent**

1.  Um Daten über die Befehlszeile zu sammeln, verwenden Sie den Vssagent-Befehl wie folgt:

    **vssagent -gather** *XmlFileName .xml**

2.  Informationen zum Anzeigen der Ausgabedatei finden Sie im folgenden Abschnitt Anzeigen von Daten.

## <a name="viewing-data"></a>Anzeigen von Daten

Die Vsdiagview-Anwendung kann zum Anzeigen von Daten verwendet werden, die mit dem Vssagent-Befehl erfasst wurden. Vsdiagview zeigt die folgenden Informationen zum Computer an:

-   Informationen zum Computer, z. B. Betriebssystemversion, verfügbarer Gesamtspeicher und CPU-Geschwindigkeit
-   Die Namen und Versionsnummern der VSS-Binärdateien
-   Die Namen und Eigenschaften der Datenträger- und Volumegeräte
-   Die Namen und Eigenschaften von COM+-Anwendungen
-   Die Namen von Ereignisprotokollen, die zum Diagnostizieren von VSS-Problemen verwendet werden können
-   Die Namen von VSS-Writern und die von ihnen behandelten Ereignisse
-   Informationen zu anderen Betriebssystemdateien

**So zeigen Sie Daten mit vsdiagview an**

1.  Wählen Sie im Menü Datei die Option **Öffnen** aus, um nach einer Datei zu suchen. (Der Standardspeicherort ist C: \\ vssdiag.)
2.  Klicken Sie auf **Öffnen,** um die Daten anzuzeigen.

 

 



