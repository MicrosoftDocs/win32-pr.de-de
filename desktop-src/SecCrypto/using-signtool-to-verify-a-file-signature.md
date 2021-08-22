---
description: Erläutert die Verwendung von SignTool zum Überprüfen einer Dateisignatur.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Verwenden von SignTool zum Überprüfen einer Dateisignatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 137a4117b64ca5d62ee2ffe5fb80a7e0751d91f840ce1270482d9e114f4dd61b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118896693"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Verwenden von SignTool zum Überprüfen einer Dateisignatur

Der folgende Befehl überprüft die Signatur einer Datei namens *MyControl.exe*:

**SignTool verify** *MyControl.exe*

Wenn im vorherigen Beispiel ein Fehler auftritt, könnte es sein, dass die Signatur ein Codesignaturzertifikat verwendet hat. [SignTool](signtool.md) verwendet standardmäßig die Windows Treiberrichtlinie für die Überprüfung.

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

 

 



