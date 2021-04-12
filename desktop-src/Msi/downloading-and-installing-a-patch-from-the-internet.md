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
# <a name="downloading-and-installing-a-patch-from-the-internet"></a><span data-ttu-id="0b554-103">Herunterladen und Installieren eines Patches aus dem Internet</span><span class="sxs-lookup"><span data-stu-id="0b554-103">Downloading and Installing a Patch From the Internet</span></span>

<span data-ttu-id="0b554-104">Microsoft Windows Installer akzeptiert eine Uniform Resource Locator (URL) als gültige Quelle für einen [Patch](patch-packages.md).</span><span class="sxs-lookup"><span data-stu-id="0b554-104">Microsoft Windows Installer accepts a Uniform Resource Locator (URL) as a valid source for a [patch](patch-packages.md).</span></span> <span data-ttu-id="0b554-105"> https://MyWeb/MyPatch.mspVerwenden Sie die folgende Befehlszeile, um einen Patch zu installieren, der sich auf einem Webserver unter befindet:</span><span class="sxs-lookup"><span data-stu-id="0b554-105">To install a patch located on a web server at https://MyWeb/MyPatch.msp, use the following command line:</span></span>

<span data-ttu-id="0b554-106">**msiexec/p https://MyWeb/MyPatch.msp**</span><span class="sxs-lookup"><span data-stu-id="0b554-106">**msiexec /p https://MyWeb/MyPatch.msp**</span></span>

<span data-ttu-id="0b554-107">Um unerwartete Ergebnisse zu vermeiden, starten Sie keinen Patch, indem Sie auf den Link auf der Webseite klicken, auf dem die URL der Patchdatei angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="0b554-107">To avoid unexpected results, do not launch a patch by clicking the link on the webpage showing the patch file's URL.</span></span> <span data-ttu-id="0b554-108">Sie können auch einen Patch installieren, indem Sie ein Skript wie das folgende verwenden:</span><span class="sxs-lookup"><span data-stu-id="0b554-108">You can also install a patch by using a script like the following:</span></span>


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



<span data-ttu-id="0b554-109">Beachten Sie Folgendes: da das [**Installer**](installer-object.md) -Objekt auf dem Computer des Benutzers nicht als " [safeforscripting](safeforscripting.md) " gekennzeichnet ist, müssen die Benutzer die Sicherheitseinstellungen des Browsers anpassen, damit das Beispiel ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0b554-109">Note that because the [**Installer**](installer-object.md) object is not marked as [SafeForScripting](safeforscripting.md) on the user's computer, users need to adjust their browser security settings for the example to work correctly.</span></span>

<span data-ttu-id="0b554-110">Weitere Informationen finden Sie unter [Richtlinien für die Erstellung sicherer Installationen](guidelines-for-authoring-secure-installations.md) und [digitaler Signaturen und Windows Installer](digital-signatures-and-windows-installer.md).</span><span class="sxs-lookup"><span data-stu-id="0b554-110">For more information, see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b554-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="0b554-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b554-112">Patch-Pakete</span><span class="sxs-lookup"><span data-stu-id="0b554-112">Patch Packages</span></span>](patch-packages.md)
</dt> <dt>

[<span data-ttu-id="0b554-113">Erstellen eines Patchpakets</span><span class="sxs-lookup"><span data-stu-id="0b554-113">Creating a Patch Package</span></span>](creating-a-patch-package.md)
</dt> <dt>

[<span data-ttu-id="0b554-114">Patchen von angepassten Anwendungen</span><span class="sxs-lookup"><span data-stu-id="0b554-114">Patching Customized Applications</span></span>](patching-customized-applications.md)
</dt> <dt>

[<span data-ttu-id="0b554-115">Herunterladen einer Installation aus dem Internet</span><span class="sxs-lookup"><span data-stu-id="0b554-115">Downloading an Installation From the Internet</span></span>](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



