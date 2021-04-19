---
description: Erläutert, wie SignTool verwendet wird, um eine Datei Signatur zu überprüfen.
ms.assetid: 9c40a397-19ea-4600-97ee-987dd10f4ef8
title: Verwenden von SignTool zum Überprüfen einer Datei Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8161d4c890400f3aa33b415e7ac16a5306aa094
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348470"
---
# <a name="using-signtool-to-verify-a-file-signature"></a>Verwenden von SignTool zum Überprüfen einer Datei Signatur

Mit dem folgenden Befehl wird die Signatur einer Datei mit dem Namen *MyControl.exe* überprüft:

**SignTool-Überprüfung** *MyControl.exe*

Wenn das vorherige Beispiel fehlschlägt, kann die Signatur ein Code Signaturzertifikat verwenden. [SignTool](signtool.md) verwendet standardmäßig die Windows-Treiber Richtlinie für die Überprüfung.

Mit dem folgenden Befehl wird die Signatur mit der Standard Richtlinie für die Authentifizierungs Überprüfung überprüft:

**SignTool Verify/PA** *MyControl.exe*

Mit dem folgenden Befehl wird eine Systemdatei überprüft, die möglicherweise in einem Katalog signiert ist:

**SignTool Verify/a** *SysFile.dll*

Mit dem folgenden Befehl wird eine Systemdatei überprüft, die in einem Katalog mit dem Namen *MyCat.cat* signiert ist:

**SignTool Verify/c** *MyCat.catMyFile.ini*

Für jede [SignTool](signtool.md) -Überprüfung können Sie den Signatur Geber des Zertifikats abrufen. Mit dem folgenden Befehl wird eine Systemdatei überprüft und das Signatur Geber Zertifikat angezeigt:

**SignTool Verify/v** *MyControl.exe*

[SignTool](signtool.md) gibt Befehlszeilen Text zurück, der das Ergebnis der Signatur Überprüfung angibt. Außerdem gibt SignTool den Exitcode 0 (null) für die erfolgreiche Ausführung zurück, einen für die fehlgeschlagene Ausführung und zwei für die Ausführung, die mit Warnungen abgeschlossen wurden.

Weitere Informationen zu [SignTool](signtool.md)finden Sie unter [SignTool](signtool.md).

 

 



