---
description: Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung eines patcherstellungs Tools, wie z. b. Msimsp.exe, um uikreatepatchpackage in Patchwiz.dll aufzurufen. Msimsp.exe und PatchWiz.dll werden im Windows Installer SDK bereitgestellt.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Erstellen eines Patchpakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ef64ac66cd0201ae99080ec86e32230bc88407b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960049"
---
# <a name="generating-a-patch-package"></a><span data-ttu-id="07cf6-104">Erstellen eines Patchpakets</span><span class="sxs-lookup"><span data-stu-id="07cf6-104">Generating a Patch Package</span></span>

<span data-ttu-id="07cf6-105">Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung eines patcherstellungs Tools, wie z. b. [Msimsp.exe](msimsp-exe.md) , um [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md)aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="07cf6-105">The recommended method for generating a patch package is to use a patch creation tool such as [Msimsp.exe](msimsp-exe.md) to call [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md).</span></span> <span data-ttu-id="07cf6-106">Msimsp.exe und PatchWiz.dll werden im Windows Installer SDK bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="07cf6-106">Msimsp.exe and PatchWiz.dll are provided in the Windows Installer SDK.</span></span>

<span data-ttu-id="07cf6-107">In der folgenden Beispiel Befehlszeile wird Msimsp.exe und die PCP-Datei verwendet, die beim [Erstellen der Eigenschaften Datei für die Patcherstellung](creating-a-patch-creation-properties-file.md) erstellt wurde, um das Beispiel Patch-Paket MNP2000. msp zu generieren.</span><span class="sxs-lookup"><span data-stu-id="07cf6-107">The following example command line uses Msimsp.exe and the .pcp file created in [Creating a Patch Creation Properties File](creating-a-patch-creation-properties-file.md) to generate the sample patch package MNP2000.msp.</span></span>

<span data-ttu-id="07cf6-108">**Msimsp.exe-s C: \\ Note \_ Installer \\ Patch \\ MNP2000. PCP-p C: \\ Note \_ Installer \\ Patch \\ MNP2000. msp**</span><span class="sxs-lookup"><span data-stu-id="07cf6-108">**Msimsp.exe -s C:\\Note\_Installer\\Patch\\MNP2000.pcp -p C:\\Note\_Installer\\Patch\\MNP2000.msp**</span></span>

<span data-ttu-id="07cf6-109">Ein erstelltes Tool für die Patcherstellung kann das Patchpaket generieren, indem Sie [uicreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) wie folgt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="07cf6-109">An authored patch creation tool may generate the patch package by calling [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) as follows.</span></span>

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[<span data-ttu-id="07cf6-110">Fortsetzen</span><span class="sxs-lookup"><span data-stu-id="07cf6-110">Continue</span></span>](applying-a-patch-package-to-a-local-installation.md)

 

 



