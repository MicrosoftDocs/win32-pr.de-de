---
description: Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der Patch-Eigenschaft installiert wird.
ms.assetid: 2c4b9d5a-34fb-4a0b-b530-30bf238468fd
title: Patchen von erst Installationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa85e15da18f7342f38cf82228bc31b6e3085f09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960829"
---
# <a name="patching-initial-installations"></a>Patchen von erst Installationen

Ein Windows Installer Patch (MSP) kann angewendet werden, wenn eine Anwendung zum ersten Mal mithilfe der [**Patch**](patch.md) -Eigenschaft installiert wird.

Zum Anwenden eines Patches bei der erstmaligen Installation der Anwendung muss die [**Patch**](patch.md) -Eigenschaft in der Befehlszeile festgelegt werden. Geben Sie den vollständigen Pfad zum Patch in der Befehlszeile als "Patch = {*path to Patch*}"-Eigenschaft/Wert-Paar an.

Beachten Sie, dass das Angeben der [**Patch**](patch.md) -Eigenschaft in der Befehlszeile die bei der Verwendung von [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) oder der/p- [Befehlszeilen Option](command-line-options.md)ausgeführten Patch-anwendbarkeits Prüfungen überschreibt.

Wenn ein Patch mithilfe von " [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha) " oder der [Befehlszeilen Option](command-line-options.md)"/p" angewendet wird, vergleicht das Installationsprogramm die aktuell auf dem Computer installierten Anwendungen mit der Liste der Produktcodes, die für den Empfang des Patches in der [**Vorlagen Zusammenfassungs**](template-summary.md) Eigenschaft berechtigt sind.

Wenn Sie die Eigenschaft [**Patch**](patch.md) in der Befehlszeile für die Installation bei der ersten Installation festlegen, werden die Anwendungen, die zum Empfangen des Patches berechtigt sind, durch Überprüfungs Bedingungen für die in das Patchpaket eingebetteten Transformationen bestimmt. Die empfohlene Methode zum Erstellen eines Patchpakets ist die Verwendung eines patcherstellungs Tools wie [Msimsp.exe](msimsp-exe.md) und [PATCHWIZ.DLL](patchwiz-dll.md). Die Überprüfungs Bedingungen für Transformationen im Patch stammen aus der Spalte "productvalidateflags" in der Tabelle " [TargetImages](targetimages-table-patchwiz-dll-.md) " der patcherstellungs-Eigenschaften Datei (. PCP).

Der Patch kann angewendet werden, wenn die Anwendung zum ersten Mal von einer Befehlszeile, einer anderen Anwendung oder einem Skript installiert wird.

Im folgenden wird das erste Patchen von der Befehlszeile gezeigt.

**msiexec/I** *package.msi* **Patch =**_"c: \\ Directory \\ Patch. msp"_

Das folgende Beispiel zeigt das erste Patchen aus einer anderen Anwendung.

``` syntax
UINT uiStat = MsiInstallProduct(_T("package.msi"), _T("PATCH=c:\directory\patch.msp"));
```

Das folgende Beispiel zeigt das erste Patchen aus dem Skript.


```VB
Dim Installer as Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "package.msi", "PATCH=c:\directory\patch.msp"
```



* * Windows Installer 3,0 und höher: * *

Ab Windows Installer Version 3,0 können bei der erstmaligen Installation einer Anwendung mehrere Patches angewendet werden. Legen Sie die Eigenschaft [**Patch**](patch.md) auf eine durch Semikolons getrennte Liste der vollständigen Pfade der Patches fest. Das folgende Beispiel zeigt das erste Patchen mehrerer Patches von der Befehlszeile aus.

**msiexec/I** *package.msi* **Patch =**_"c: \\ Directory \\ Patch. msp; c: \\ Directory \\ Patch2. msp; c: \\ Directory \\ Patch3. msp"_

 

 



