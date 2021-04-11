---
description: Dieses Thema enthält Richtlinien für die Installation oder Neuinstallation einer Installation mit mehreren Instanzen, bei der instanztransformationen verwendet werden.
ms.assetid: cf9076b1-5674-4ba8-9890-e981221d7b03
title: Installieren mehrerer Instanzen mit instanztransformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bae8d73ad60567e1557257c1207558290ba29db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041891"
---
# <a name="installing-multiple-instances-with-instance-transforms"></a>Installieren mehrerer Instanzen mit instanztransformationen

Dieses Thema enthält Richtlinien für die Installation oder Neuinstallation einer Installation mit mehreren Instanzen, bei der instanztransformationen verwendet werden.

-   Wenn Sie eine neue Instanz mit einer instanztransformation installieren, schließen Sie die **msinewinstance** -Eigenschaft ein, und legen Sie **msinewinstance**= 1 fest.
-   Wenn Sie eine neue Instanz mit einer instanztransformation installieren, schließen Sie die Transformationen-Eigenschaft ein, und legen Sie die erste Transformation in der Liste der Transformationen auf die instanztransformation fest, die den Produktcode ändert. Alle Anpassungs Transformationen sollten der instanztransformation am Anfang dieser Liste folgen.
-   Am einfachsten können Sie eine Wartungs Installation initiieren und eine Instanz neu installieren, indem Sie auf den Produktcode der Instanz verweisen. Wenn Sie die Wartungs Installation mit dem Paketpfad initiieren, müssen Sie auch den Produktcode der Instanz angeben. Verwenden Sie in der Befehlszeile die Option/n {Product Code}. Verwenden Sie im Code oder Skript die **msiinstanceguid** -Eigenschaft.

Im folgenden Beispiel wird gezeigt, wie eine neue Instanz von einer Befehlszeile aus installiert wird, wobei der instanztransformation ein Doppelpunkt vorangestellt wird, der angibt, dass die Transformation in das Paket eingebettet ist.

**msiexec/I mypackage.msi Transformationen =: instance. MST msinewinstance = 1/QB**

Das folgende Beispiel zeigt die Installation einer neuen Instanz mit [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

Das folgende Beispiel zeigt die Installation der neuen Instanz aus dem Skript.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

Im folgenden Beispiel wird eine-Instanz neu installiert, ohne dass das Paket erneut zwischengespeichert wird. Der Produktcode verweist auf die Instanz {00000001-0002-0000-0000-624474736554} .

**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**

Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket über die Befehlszeile erneut zwischengespeichert. Der Paketpfad verweist auf die Instanz. Sie müssen nur die Option/n {Product Code} einschließen, wenn das Produkt ursprünglich mit einer instanztransformation installiert wurde.

**msiexec/I c: \\ NewPath \\mypackage.msi/n {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**

Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket mit **msiinstallproduct** zwischengespeichert. Der Paketpfad verweist auf die Instanz. Verwenden Sie die **msiinstanceguid** -Eigenschaft, um den Produktcode der-Instanz bereitzustellen.

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket mithilfe des-Skripts zwischengespeichert. Verwenden Sie die **msiinstanceguid** -Eigenschaft, um den Produktcode der-Instanz bereitzustellen.

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

Im folgenden Beispiel wird gezeigt, wie eine Instanz über die Befehlszeile angekündigt wird.

**msiexec/JM mypackage.msi/t: instance. MST/c/QB**

Im folgenden Beispiel wird gezeigt, wie installiert wird, um eine Instanz mit **msiankünabproductex** ankündigen zu können.

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

Im folgenden Beispiel wird gezeigt, wie ein Patch von einer Befehlszeile auf eine-Instanz angewendet wird. Sie müssen nur die Option/n {Product Code} einschließen, wenn das Produkt ursprünglich mit einer instanztransformation installiert wurde.

**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /qb**

Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)einen Patch auf eine instanzinstallation anwenden.

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md) und [Erstellen mehrerer Instanzen mit instanztransformationen](authoring-multiple-instances-with-instance-transforms.md).

 

 



