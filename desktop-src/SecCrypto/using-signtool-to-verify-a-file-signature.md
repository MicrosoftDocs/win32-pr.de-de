---
description: Erläutert die Verwendung von SignTool zum Überprüfen einer Dateisignatur.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Verwenden von SignTool zum Überprüfen einer Dateisignatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e91df7a64a8db48d04ceba9df5fbc3fd358058
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107954923"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Verwenden von SignTool zum Überprüfen einer Dateisignatur

Der folgende Befehl überprüft die Signatur einer Datei mit dem Namen *MyControl.exe*:

**SignTool verify** *MyControl.exe*

Wenn im vorherigen Beispiel ein Fehler auftritt, könnte es sein, dass die Signatur ein Codesignaturzertifikat verwendet hat. [SignTool](signtool.md) verwendet zur Überprüfung standardmäßig die Windows-Treiberrichtlinie.

Der folgende Befehl überprüft die Signatur mithilfe der Standardauthentifizierungsüberprüfungsrichtlinie:

**SignTool verify /pa** *MyControl.exe*

Der folgende Befehl überprüft eine Systemdatei, die möglicherweise in einem Katalog signiert ist:

**SignTool verify /a** *SysFile.dll*

Der folgende Befehl überprüft eine Systemdatei, die in einem Katalog mit dem Namen *MyCat.cat* signiert ist:

**SignTool verify /c** *MyCat.cat* *MyFile.ini*

Für jede [SignTool-Überprüfung](signtool.md) können Sie den Signierer des Zertifikats abrufen. Der folgende Befehl überprüft eine Systemdatei und zeigt das Signaturgeberzertifikat an:

**SignTool verify /v** *MyControl.exe*

[SignTool](signtool.md) gibt Befehlszeilentext zurück, der das Ergebnis der Signaturüberprüfung angibt. Darüber hinaus gibt SignTool für eine erfolgreiche Ausführung den Exitcode 0 (null) zurück, einen für eine fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurde.

Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).

 

 



