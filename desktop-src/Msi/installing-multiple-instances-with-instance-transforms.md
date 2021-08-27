---
description: Dieses Thema enthält Richtlinien für die Installation oder Neuinstallation einer Installation mit mehreren Instanzen, die Instanztransformationen verwendet.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installieren mehrerer Instanzen mit Instanztransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a25b2cba8fd91316d62692d278345e0f7d9751f018e1c33239412988bfe118a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074900"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Installieren mehrerer Instanzen mit Instanztransformationen

Dieses Thema enthält Richtlinien für die Installation oder Neuinstallation einer Installation mit mehreren Instanzen, die Instanztransformationen verwendet.

-   Wenn Sie eine neue Instanz mit einer Instanztransformation installieren, schließen Sie die **MSINEWINSTANCE-Eigenschaft** ein, und legen **Sie MSINEWINSTANCE**=1 fest.
-   Wenn Sie eine neue Instanz mit einer Instanztransformation installieren, schließen Sie die TRANSFORMS-Eigenschaft ein, und legen Sie die erste Transformation in der Liste der Transformationen auf die Instanztransformation fest, die den Produktcode ändert. Alle Anpassungstransformationen sollten der Instanztransformation am Anfang dieser Liste folgen.
-   Die einfachste Möglichkeit, eine Wartungsinstallation zu initiieren und eine Instanz neu zu installieren, besteht im Verweisen auf den Produktcode der Instanz. Wenn Sie die Wartungsinstallation mithilfe des Paketpfads initiieren, müssen Sie auch den Produktcode der Instanz angeben. Verwenden Sie in der Befehlszeile die Option /n {Product Code}. Verwenden Sie im Code oder Skript die **MSIINSTANCEGUID-Eigenschaft.**

Das folgende Beispiel zeigt die Installation einer neuen -Instanz über eine Befehlszeile, bei der der Instanztransformation ein Doppelpunkt vorangestellt ist, der angibt, dass die Transformation in das Paket eingebettet ist.

**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**

Im folgenden Beispiel wird die Installation einer neuen -Instanz mit [**msiInstallProduct veranschaulicht.**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

Das folgende Beispiel zeigt die Installation der neuen -Instanz aus dem Skript.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

Im folgenden Beispiel wird eine -Instanz neu installiert, ohne das Paket erneut zwischenspeichern zu müssen. Auf die -Instanz wird durch ihren Produktcode {00000001-0002-0000-0000-624474736554} verwiesen.

**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**

Im folgenden Beispiel wird eine -Instanz neu installiert und das Paket über die Befehlszeile neu zwischengespeichert. Auf die -Instanz wird durch den Paketpfad verwiesen. Sie müssen nur dann die Option /n {Product Code} verwenden, wenn das Produkt ursprünglich mit einer Instanztransformation installiert wurde.

**msiexec /I c: \\ newpath \\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**

Im folgenden Beispiel wird eine -Instanz neu installiert und das Paket mit **msiInstallProduct zwischengespeichert.** Auf die -Instanz wird durch den Paketpfad verwiesen. Verwenden Sie **die MSIINSTANCEGUID-Eigenschaft,** um den Produktcode der -Instanz zur Verfügung zu stellen.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

Im folgenden Beispiel wird eine -Instanz neu installiert und das Paket mithilfe des Skripts zwischengespeichert. Verwenden Sie **die MSIINSTANCEGUID-Eigenschaft,** um den Produktcode der -Instanz zur Verfügung zu stellen.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

Das folgende Beispiel zeigt, wie Sie eine -Instanz über die Befehlszeile ankn geben.

**msiexec /jm mypackage.msi /t :instance.mst /c /qb**

Das folgende Beispiel zeigt, wie Sie installieren, um eine -Instanz mit **msiAdvertiseProductEx an angekündigt.**

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

Das folgende Beispiel zeigt, wie ein Patch über eine Befehlszeile auf eine -Instanz angewendet wird. Sie müssen nur dann die Option /n {Product Code} verwenden, wenn das Produkt ursprünglich mit einer Instanztransformation installiert wurde.

**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**

Im folgenden Beispiel wird gezeigt, wie Sie mit [**msiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)einen Patch auf eine Instanzinstallation anwenden.

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Weitere Informationen finden Sie unter Installieren mehrerer Instanzen von Produkten und [Patches](installing-multiple-instances-of-products-and-patches.md) und Erstellen mehrerer Instanzen [mit Instanztransformationen.](authoring-multiple-instances-with-instance-transforms.md)

 

 



