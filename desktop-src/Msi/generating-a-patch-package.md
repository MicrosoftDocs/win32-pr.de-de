---
description: Die empfohlene Methode zum Generieren eines Patchpakets besteht darin, ein Patcherstellungstool wie Msimsp.exe zu verwenden, um UiCreatePatchPackage in Patchwiz.dll aufzurufen. Msimsp.exe und PatchWiz.dll werden im Windows Installer SDK bereitgestellt.
ms.assetid: 7fa661aa-d52c-4b08-961f-90ec778f02ff
title: Generieren eines Patchpakets
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0577c678bbb378da425ff438a0e165dcba95d6e1fc1eecc1d9c311fe2c78bca2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119581430"
---
# <a name="generating-a-patch-package"></a>Generieren eines Patchpakets

Die empfohlene Methode zum Generieren eines Patchpakets besteht darin, ein Patcherstellungstool wie [Msimsp.exe](msimsp-exe.md) zu verwenden, um [UiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) in [Patchwiz.dll](patchwiz-dll.md)aufzurufen. Msimsp.exe und PatchWiz.dll werden im Windows Installer SDK bereitgestellt.

In der folgenden Beispielbefehlszeile werden Msimsp.exe und die PCP-Datei verwendet, die unter [Creating a Patch Creation Properties File (Erstellen einer Patcherstellungseigenschaftendatei)](creating-a-patch-creation-properties-file.md) erstellt wurde, um das Beispielpatchpaket MNP2000.msp zu generieren.

**Msimsp.exe -s C: \\ Hinweis \_ Installer Patch \\ \\ MNP2000.pcp -p C: \\ Hinweis Installer Patch \_ \\ \\ MNP2000.msp**

Ein erstelltes Patcherstellungstool kann das Patchpaket generieren, indem [uiCreatePatchPackage](uicreatepatchpackage-patchwiz-dll-.md) wie folgt aufgerufen wird.

``` syntax
UiCreatePatchPackage ("C:\\Note_Installer\\Patch\\MNP2000.pcp", "C:\\Note_Installer\\Patch\\MNP2000.msp", NULL, NULL, "", TRUE)
```

[Fortsetzen](applying-a-patch-package-to-a-local-installation.md)

 

 



