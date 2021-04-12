---
description: Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen Patch.
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: Herunterladen und Installieren eines Patches aus dem Internet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31b5fe4ca51b08759bc178b89bfe71c89418e26d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129976"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>Herunterladen und Installieren eines Patches aus dem Internet

Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen [Patch](patch-packages.md). https://MyWeb/MyPatch.mspVerwenden Sie die folgende Befehlszeile, um einen Patch zu installieren, der sich auf einem Webserver unter befindet:

**msiexec/p https://MyWeb/MyPatch.msp**

Um unerwartete Ergebnisse zu vermeiden, starten Sie keinen Patch, indem Sie auf den Link auf der Webseite klicken, auf dem die URL der Patchdatei angezeigt wird. Sie können auch einen Patch installieren, indem Sie ein Skript wie das folgende verwenden:


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



Beachten Sie Folgendes: da das [**Installer**](installer-object.md) -Objekt auf dem Computer des Benutzers nicht als " [safeforscripting](safeforscripting.md) " gekennzeichnet ist, müssen die Benutzer die Sicherheitseinstellungen des Browsers anpassen, damit das Beispiel ordnungsgemäß funktioniert.

Weitere Informationen finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Patch-Pakete](patch-packages.md)
</dt> <dt>

[Erstellen eines Patchpakets](creating-a-patch-package.md)
</dt> <dt>

[Patchen von angepassten Anwendungen](patching-customized-applications.md)
</dt> <dt>

[Herunterladen einer Installation aus dem Internet](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



