---
description: Vsdiagview und vssagent sind Tools, die Sie verwenden können, um Probleme mit VSS-Anwendungen zu beheben. Beachten Sie, dass diese Tools im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten sind.
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: Verwenden der VSS-Diagnose
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343683"
---
# <a name="using-vss-diagnostics"></a>Verwenden der VSS-Diagnose

Vsdiagview und vssagent sind Tools, die Sie verwenden können, um Probleme mit VSS-Anwendungen zu beheben.

> [!Note]  
> Diese Tools sind im Microsoft Windows Software Development Kit (SDK) für Windows Vista und höher enthalten. Sie können die Windows SDK von herunterladen [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) .

 

In der Windows SDK-Installation finden Sie diese Tools in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (für 64-Bit-Windows) und `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (für 32-Bit-Windows).

## <a name="gathering-data"></a>Sammeln von Daten

Sie können Daten mit dem Befehl vssagent sammeln.

**So erfassen Sie Daten mithilfe von vssagent**

1.  Verwenden Sie zum Erfassen von Daten über die Befehlszeile den vssagent-Befehl wie folgt:

    **vssagent-** " *xmlFileName * * *. XML* " erfassen*

2.  Informationen zum Anzeigen der Ausgabedatei finden Sie im folgenden Abschnitt zum Anzeigen von Daten.

## <a name="viewing-data"></a>Anzeigen von Daten

Die vsdiagview-Anwendung kann verwendet werden, um Daten anzuzeigen, die mit dem vssagent-Befehl erfasst wurden. Vsdiagview zeigt die folgenden Informationen zum Computer an:

-   Informationen zum Computer, z. b. Betriebssystemversion, gesamter Arbeitsspeicher und CPU-Geschwindigkeit
-   Die Namen und Versionsnummern der VSS-Binärdateien
-   Die Namen und Eigenschaften der Datenträger-und Volumegeräte
-   Die Namen und Eigenschaften der com+-Anwendungen
-   Die Namen der Ereignisprotokolle, die für die Diagnose von VSS-Problemen verwendet werden können.
-   Die Namen aller VSS-Writer und der Ereignisse, die Sie behandeln
-   Informationen zu anderen Betriebssystemdateien

**So zeigen Sie Daten mithilfe von vsdiagview an**

1.  Wählen Sie im Menü Datei die Option **Öffnen** aus, um nach einer Datei zu suchen. (Der Standard Speicherort ist C: \\ vssdiag.)
2.  Klicken Sie auf **Öffnen** , um die Daten anzuzeigen.

 

 



