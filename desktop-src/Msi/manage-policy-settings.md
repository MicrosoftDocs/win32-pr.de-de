---
description: Die VBScript-Datei WiPolicy.vbs wird in den Windows SDK Komponenten für Windows Installer Entwickler bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Verwalten von Systemrichtlinien verwendet werden kann. Die Richtlinie kann von einem Administrator mithilfe des Gruppenrichtlinie-Editors (gpe) konfiguriert werden.
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Verwalten von Richtlinieneinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86684e75e09fa0a588c2d1d0d999488d6e89fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355520"
---
# <a name="manage-policy-settings"></a>Verwalten von Richtlinieneinstellungen

Die VBScript-Datei WiPolicy.vbs wird in den [Windows SDK Komponenten für Windows Installer Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie das Skript zum Verwalten von [Systemrichtlinien](system-policy.md)verwendet werden kann. Die Richtlinie kann von einem Administrator mithilfe des Gruppenrichtlinie-Editors (gpe) konfiguriert werden.

In diesem Beispiel werden die Windows Installer-Richtlinien veranschaulicht.

Zum Verwenden dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Wenn Sie CScript.exe verwenden möchten, um dieses Beispiel auszuführen, geben Sie einen Befehl an der Eingabeaufforderung ein, indem Sie die folgende Syntax verwenden. Hilfe wird angezeigt, wenn das erste Argument/? oder, wenn zu wenige Argumente angegeben werden. Um die Ausgabe in eine Datei umzuleiten, beenden Sie die Befehlszeile mit VSB > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für Erfolg zurück, 1, wenn Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript-WiPolicy.vbs \[ Richtlinien \] \[ Wert\]**

Wenn keine Argumente in der Befehlszeile angegeben werden, gibt das Beispiel die aktuellen Richtlinien Einstellungen zurück. Legen Sie die Richtlinie fest, die mit den folgenden Bezeichnercodes festgelegt werden soll. Geben Sie den neuen Wert für die Richtlinie an. Um den aktuellen Wert einer Richtlinie zurückzugeben, geben Sie eine leere Zeichenfolge "" als Wert an.



| CODE | BESCHREIBUNG                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Protokollierungs Modi. Weitere Informationen finden Sie unter [Protokollierung](logging.md) .                                                                            |
| DO   | Debug-Modi. Weitere Informationen finden Sie unter [Debuggen](debug.md).                                                                                   |
| DI   | Deaktivieren Sie Windows Installer Modus. Weitere Informationen finden Sie unter [DisableMSI](disablemsi.md).                                                      |
| WT   | Wartezeit in Sekunden, wenn keine Aktivität aufgetreten ist. **HKLM** \\ **Software** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installer** \\ **Timeout** |
| DB   | Deaktivieren Sie das Durchsuchen von Quell Speicherorten. Weitere Informationen finden Sie unter [disablebrowse](disablebrowse.md).                                     |
| Gbar   | Deaktivieren Sie das Patchen. Weitere Informationen finden Sie unter [disablepatch](disablepatch.md).                                                                |
| UC   | Öffentliche Eigenschaften, die an den Installations Dienst gesendet werden. Weitere Informationen finden Sie unter [enableusercontrol](enableusercontrol.md).                             |
| SS   | Installer ist für die Skripterstellung im Browser sicher. Weitere Informationen finden Sie unter [safeforscripting](safeforscripting.md).                               |
| EM   | System Privilegien (HKLM). Weitere Informationen finden Sie unter [alwaysinstallerhöhten](alwaysinstallelevated.md).                                      |
| EU   | System Privilegien (HKCU). Weitere Informationen finden Sie unter [alwaysinstallerhöhten](alwaysinstallelevated.md).                                      |
| DR   | Deaktivieren der Rollback-Richtlinie. Weitere Informationen finden Sie unter [DISABLEROLLBACK](disablerollback.md).                                                   |
| TS   | Suchen Sie im Stammverzeichnis des Quell Bilds nach Transformationen. Weitere Informationen finden Sie unter [transformsatsource-Richtlinie](transformsatsource-policy.md).             |
| TP   | Heften Sie sichere wandelt im Client seitigen Cache an. Weitere Informationen finden Sie unter [transformssecure Policy](transformssecure-policy.md).                 |
| SO   | Such Reihenfolge der Quell Typen. Weitere Informationen finden Sie unter [SearchOrder](searchorder.md).                                                      |



 

Weitere Skript Beispiele finden Sie unter [Windows Installer Skript Beispiele](windows-installer-scripting-examples.md). Beispiel Hilfsprogramme, die keinen Windows Script Host erfordern, finden Sie unter [Windows Installer-Entwicklungs Tools](windows-installer-development-tools.md).

 

 



