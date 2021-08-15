---
description: Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der PATCH-Eigenschaft installiert wird.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Patchen von Erstinstallationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddf89c3a83a6000a5716b5317a9fc2965562c217b110b020a2795573f8175235
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118377633"
---
# <a name="patching-initial-installations"></a>Patchen von Erstinstallationen

Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der [**PATCH-Eigenschaft installiert**](patch.md) wird.

Um bei der ersten Installation der Anwendung einen Patch anzuwenden, muss die [**PATCH-Eigenschaft**](patch.md) in der Befehlszeile festgelegt werden. Geben Sie den vollständigen Pfad zum Patch in der Befehlszeile als Eigenschaftswertpaar "PATCH={ pfad *to patch*}" an.

Beachten Sie, dass die Angabe der [**PATCH-Eigenschaft**](patch.md) in der Befehlszeile die Patchanwendbarkeitsprüfungen überschreibt, die bei Verwendung von [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder der Befehlszeilenoption /p [ausgeführt werden.](command-line-options.md)

Wenn ein Patch mit [**msiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder der Befehlszeilenoption [/p](command-line-options.md)angewendet wird, vergleicht das Installationsprogramm die derzeit auf [](template-summary.md) dem Computer installierten Anwendungen mit der Liste der Produktcodes, die zum Empfangen des Patches berechtigt sind, in der Eigenschaft Vorlagenzusammenfassung.

Wenn Sie die [**PATCH-Eigenschaft**](patch.md) in der Befehlszeile so festlegen, dass sie bei der ersten Installation installiert wird, werden die Anwendungen, die zum Empfangen des Patches berechtigt sind, durch Validierungsbedingungen für die in das Patchpaket eingebetteten Transformationen bestimmt. Die empfohlene Methode zum Generieren eines Patchpakets ist die Verwendung eines Tools zum Erstellen von Patches wie [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL. ](patchwiz-dll.md) Die Validierungsbedingungen für Transformationen im Patch stammen aus der ProductValidateFlags -Spalte in der [TargetImages-Tabelle](targetimages-table-patchwiz-dll-.md) der PatchErstellungseigenschaftendatei (PCP- Datei).

Der Patch kann angewendet werden, wenn die Anwendung zum ersten Mal über eine Befehlszeile, eine andere Anwendung oder ein Skript installiert wird.

Das folgende Beispiel zeigt das erstmalige Patchen über die Befehlszeile.

**msiexec /I** *package.msi* **PATCH=**_"c: directory \\ \\ patch.msp"_

Das folgende Beispiel zeigt das erstmalige Patchen aus einer anderen Anwendung.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

Das folgende Beispiel zeigt das erstmalige Patchen aus dem Skript.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



**Windows Installer 3.0 und höher: **

Ab version Windows Installer 3.0 können mehrere Patches angewendet werden, wenn eine Anwendung zum ersten Mal installiert wird. Legen Sie [**die PATCH-Eigenschaft**](patch.md) auf eine durch Semikolons getrennte Liste der vollständigen Pfade der Patches fest. Das folgende Beispiel zeigt das erstmalige Patchen mehrerer Patches über die Befehlszeile.

**msiexec /I** *package.msi* **PATCH=**_"c: directory \\ \\ patch.msp;c: directory \\ \\ patch2.msp;c: directory \\ \\ patch3.msp"_

 

 



