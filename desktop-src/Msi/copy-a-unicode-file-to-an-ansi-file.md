---
description: Die VBScript-Datei WiToAnsi.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispiel zeigt, wie skript verwendet wird, um eine Unicode-Textdatei als ANSI-Textdatei neu zu schreiben.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Kopieren einer Unicode-Datei in eine ANSI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 224a9115da67848bd43aaceb7e5d8f529693558191e52a04de2e7645a4e60aeb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143374"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Kopieren einer Unicode-Datei in eine ANSI-Datei

Die VBScript-Datei WiToAnsi.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie skript verwendet wird, um eine Unicode-Textdatei als ANSI-Textdatei neu zu schreiben.

Für die Verwendung dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie eine Befehlszeile an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript WiToAnsi.vbs \[ Pfad zum Unicode-Dateipfad \] \[ zur ANSI-Datei\]**

Geben Sie die Unicode-Textdatei an, die konvertiert wird. Geben Sie die ANSI-Textdatei an, die erstellt wird. Wenn keine ANSI-Datei angegeben ist, wird die Unicode-Datei ersetzt.

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Skripthost nicht benötigen, finden Sie [unter Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



