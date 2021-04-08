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
# <a name="generating-a-patch-package"></a>Erstellen eines Patchpakets

Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung eines patcherstellungs Tools, wie z. b. [Msimsp.exe](msimsp-exe.md) , um [uikreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md)aufzurufen. Msimsp.exe und PatchWiz.dll werden im Windows Installer SDK bereitgestellt.

In der folgenden Beispiel Befehlszeile wird Msimsp.exe und die PCP-Datei verwendet, die beim [Erstellen der Eigenschaften Datei für die Patcherstellung](creating-a-patch-creation-properties-file.md) erstellt wurde, um das Beispiel Patch-Paket MNP2000. msp zu generieren.

**Msimsp.exe-s C: \\ Note \_ Installer \\ Patch \\ MNP2000. PCP-p C: \\ Note \_ Installer \\ Patch \\ MNP2000. msp**

Ein erstelltes Tool für die Patcherstellung kann das Patchpaket generieren, indem Sie [uicreatepatchpackage](uicreatepatchpackage-patchwiz-dll-.md) wie folgt aufrufen.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Fortsetzen](applying-a-patch-package-to-a-local-installation.md)

 

 



