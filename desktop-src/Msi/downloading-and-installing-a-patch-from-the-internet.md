---
description: Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen Patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Herunterladen und Installieren eines Patches aus dem Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f662279ac929d831bb69acc597358c8eddc509738fc71a43df44ec186120c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947354"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Herunterladen und Installieren eines Patches aus dem Internet

Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen [Patch.](patch-packages.md) Verwenden Sie die folgende Befehlszeile, um einen Patch auf einem Webserver unter zu https://MyWeb/MyPatch.msp installieren:

**msiexec /p https://MyWeb/MyPatch.msp**

Um unerwartete Ergebnisse zu vermeiden, starten Sie keinen Patch, indem Sie auf der Webseite auf den Link klicken, auf dem die URL der Patchdatei angezeigt wird. Sie können einen Patch auch mithilfe eines Skripts wie dem folgenden installieren:


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



Da das [**Installer-Objekt**](installer-object.md) auf dem Computer des Benutzers nicht als [SafeForScripting](safeforscripting.md) gekennzeichnet ist, müssen Benutzer ihre Browsersicherheitseinstellungen anpassen, damit das Beispiel ordnungsgemäß funktioniert.

Weitere Informationen finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und digitaler [Signaturen und Windows Installer.](digital-signatures-and-windows-installer.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patchpakete](patch-packages.md)
</dt> <dt>

[Erstellen eines Patchpakets](creating-a-patch-package.md)
</dt> <dt>

[Patchen benutzerdefinierter Anwendungen](patching-customized-applications.md)
</dt> <dt>

[Herunterladen einer Installation aus dem Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



