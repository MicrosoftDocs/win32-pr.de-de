---
description: Die VBScript-Datei WiToAnsi.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie ein Skript zum Umschreiben einer Unicode-Textdatei als ANSI-Textdatei verwendet wird.
ms.assetid: cb22495f-968c-470a-a2f1-d0e068133956
title: Kopieren einer Unicode-Datei in eine ANSI-Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde68c60eaa5a007aee7d2ca2d79159c9b7fce20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866092"
---
# <a name="copy-a-unicode-file-to-an-ansi-file"></a>Kopieren einer Unicode-Datei in eine ANSI-Datei

Die VBScript-Datei WiToAnsi.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie ein Skript zum Umschreiben einer Unicode-Textdatei als ANSI-Textdatei verwendet wird.

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie mithilfe der folgenden Syntax eine Befehlszeile an der Eingabeaufforderung ein. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiToAnsi.vbs \[ Pfad zum Unicode- \] \[ Dateipfad zur ANSI-Datei\]**

Geben Sie die Unicode-Textdatei an, die konvertiert wird. Geben Sie die ANSI-Textdatei an, die erstellt wird. Wenn keine ANSI-Datei angegeben ist, wird die Unicode-Datei ersetzt.

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



