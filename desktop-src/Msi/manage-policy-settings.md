---
description: Die VBScript-Datei WiPolicy.vbs wird in den Windows SDK-Komponenten für Windows Installer-Entwickler bereitgestellt. Dieses Beispiel zeigt, wie Skripts zum Verwalten von Systemrichtlinien verwendet werden können. Die Richtlinie kann von einem Administrator mithilfe des Gruppenrichtlinie-Editors (GPE) konfiguriert werden.
ms.assetid: 17cfed46-503f-4124-9f0e-1655fda153d0
title: Verwalten von Richtlinieneinstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1261c48ec7cc7e51a8556b7565075fa9e92bd60481da08f4f311a3de995a91f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118945606"
---
# <a name="manage-policy-settings"></a>Verwalten von Richtlinieneinstellungen

Die VBScript-Datei WiPolicy.vbs wird in den [Windows SDK-Komponenten für Windows Installer-Entwickler](platform-sdk-components-for-windows-installer-developers.md)bereitgestellt. Dieses Beispiel zeigt, wie Skripts zum Verwalten von [Systemrichtlinien](system-policy.md)verwendet werden können. Die Richtlinie kann von einem Administrator mithilfe des Gruppenrichtlinie-Editors (GPE) konfiguriert werden.

In diesem Beispiel werden die Richtlinien für Windows Installer veranschaulicht.

Für die Verwendung dieses Beispiels ist die CScript.exe oder WScript.exe Version von Windows Script Host erforderlich. Um CScript.exe zum Ausführen dieses Beispiels zu verwenden, geben Sie einen Befehl an der Eingabeaufforderung mit der folgenden Syntax ein. Hilfe wird angezeigt, wenn das erste Argument /? ist. oder , wenn zu wenige Argumente angegeben werden. Um die Ausgabe an eine Datei umzuleiten, beenden Sie die Befehlszeile mit VBS > \[ *Pfad zur Datei* \] . Das Beispiel gibt den Wert 0 für den Erfolg zurück, 1, wenn die Hilfe aufgerufen wird, und 2, wenn das Skript fehlschlägt.

**cscript \[ WiPolicy.vbs-Richtlinienwert \] \[\]**

Wenn in der Befehlszeile keine Argumente angegeben werden, gibt das Beispiel die aktuellen Richtlinieneinstellungen zurück. Geben Sie die festzulegende Richtlinie mithilfe der folgenden Bezeichnercodes an. Geben Sie den neuen Wert für die Richtlinie an. Um den aktuellen Wert einer Richtlinie zurückzugeben, geben Sie eine leere Zeichenfolge "" für den Wert an.



| CODE | BESCHREIBUNG                                                                                                                                  |
|------|----------------------------------------------------------------------------------------------------------------------------------------------|
| LM   | Protokollierungsmodi. Weitere Informationen finden Sie unter [Protokollieren von](logging.md) .                                                                            |
| DO   | Debugmodi. Weitere Informationen finden Sie unter [Debuggen](debug.md)von .                                                                                   |
| DI   | Deaktivieren Sie Windows Installer-Modus. Weitere Informationen finden Sie unter [DisableMsi](disablemsi.md).                                                      |
| Wt   | Wartetimeout in Sekunden, falls keine Aktivität vorhanden ist. **HKLM** \\ **SoftWare** \\ **Richtlinien** \\ **Microsoft** \\ **Windows** \\ **Installationsprogramm** \\ **Timeout** |
| DB   | Deaktivieren Sie das Durchsuchen von Quellspeicherorten durch Benutzer. Weitere Informationen finden Sie unter [DisableBrowse](disablebrowse.md).                                     |
| Dp   | Deaktivieren Sie das Patchen. Weitere Informationen finden Sie unter [DisablePatch](disablepatch.md).                                                                |
| Uc   | Öffentliche Eigenschaften, die an den Installationsdienst gesendet werden. Weitere Informationen finden Sie unter [EnableUserControl.](enableusercontrol.md)                             |
| SS   | Sicheres Installationsprogramm für Skripterstellung über den Browser. Weitere Informationen finden Sie unter [SafeForScripting.](safeforscripting.md)                               |
| EM   | Systemberechtigungen (HKLM). Weitere Informationen finden Sie unter [AlwaysInstallElevated.](alwaysinstallelevated.md)                                      |
| EU   | Systemberechtigungen (HKCU). Weitere Informationen finden Sie unter [AlwaysInstallElevated.](alwaysinstallelevated.md)                                      |
| DR   | Deaktivieren Sie die Rollbackrichtlinie. Weitere Informationen finden Sie unter [DisableRollback.](disablerollback.md)                                                   |
| TS   | Suchen Sie Transformationen im Stammverzeichnis des Quellbilds. Weitere Informationen finden Sie unter [TransformsAtSource-Richtlinie.](transformsatsource-policy.md)             |
| TP   | Heften Sie sichere Tranforms im clientseitigen Cache an. Weitere Informationen finden Sie unter [TransformsSecure policy](transformssecure-policy.md).                 |
| SO   | Suchreihenfolge von Quelltypen. Weitere Informationen finden Sie unter [SearchOrder](searchorder.md).                                                      |



 

Weitere Skriptbeispiele finden Sie unter [Windows Installer Scripting Examples](windows-installer-scripting-examples.md). Beispielhilfsprogramme, die Windows Script Host nicht benötigen, finden Sie unter [Windows Installer Development Tools](windows-installer-development-tools.md).

 

 



