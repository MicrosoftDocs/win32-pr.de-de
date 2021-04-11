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
# <a name="installing-multiple-instances-with-instance-transforms"></a><span data-ttu-id="9296d-103">Installieren mehrerer Instanzen mit instanztransformationen</span><span class="sxs-lookup"><span data-stu-id="9296d-103">Installing Multiple Instances with Instance Transforms</span></span>

<span data-ttu-id="9296d-104">Dieses Thema enthält Richtlinien für die Installation oder Neuinstallation einer Installation mit mehreren Instanzen, bei der instanztransformationen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9296d-104">This topic provides guidelines for installing or reinstalling a multiple instance installation that uses instance transforms.</span></span>

-   <span data-ttu-id="9296d-105">Wenn Sie eine neue Instanz mit einer instanztransformation installieren, schließen Sie die **msinewinstance** -Eigenschaft ein, und legen Sie **msinewinstance**= 1 fest.</span><span class="sxs-lookup"><span data-stu-id="9296d-105">When installing a new instance with an instance transform, include the **MSINEWINSTANCE** property and set **MSINEWINSTANCE**=1.</span></span>
-   <span data-ttu-id="9296d-106">Wenn Sie eine neue Instanz mit einer instanztransformation installieren, schließen Sie die Transformationen-Eigenschaft ein, und legen Sie die erste Transformation in der Liste der Transformationen auf die instanztransformation fest, die den Produktcode ändert.</span><span class="sxs-lookup"><span data-stu-id="9296d-106">When installing a new instance with an instance transform, include the TRANSFORMS property and set the first transform in the list of transforms to the instance transform that changes the product code.</span></span> <span data-ttu-id="9296d-107">Alle Anpassungs Transformationen sollten der instanztransformation am Anfang dieser Liste folgen.</span><span class="sxs-lookup"><span data-stu-id="9296d-107">Any customization transforms should follow the instance transform at the beginning of this list.</span></span>
-   <span data-ttu-id="9296d-108">Am einfachsten können Sie eine Wartungs Installation initiieren und eine Instanz neu installieren, indem Sie auf den Produktcode der Instanz verweisen.</span><span class="sxs-lookup"><span data-stu-id="9296d-108">The easiest way to initiate a maintenance installation, and reinstall an instance, is to reference the product code of the instance.</span></span> <span data-ttu-id="9296d-109">Wenn Sie die Wartungs Installation mit dem Paketpfad initiieren, müssen Sie auch den Produktcode der Instanz angeben.</span><span class="sxs-lookup"><span data-stu-id="9296d-109">If you initiate the maintenance installation by using the package path, you must also specify the product code of the instance.</span></span> <span data-ttu-id="9296d-110">Verwenden Sie in der Befehlszeile die Option/n {Product Code}.</span><span class="sxs-lookup"><span data-stu-id="9296d-110">From the command line, use the /n {Product Code} option.</span></span> <span data-ttu-id="9296d-111">Verwenden Sie im Code oder Skript die **msiinstanceguid** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="9296d-111">From code or script, use the **MSIINSTANCEGUID** property.</span></span>

<span data-ttu-id="9296d-112">Im folgenden Beispiel wird gezeigt, wie eine neue Instanz von einer Befehlszeile aus installiert wird, wobei der instanztransformation ein Doppelpunkt vorangestellt wird, der angibt, dass die Transformation in das Paket eingebettet ist.</span><span class="sxs-lookup"><span data-stu-id="9296d-112">The following example shows installing a new instance from a command line where the instance transform is prefixed by a colon which specifies that the transform is embedded in the package.</span></span>

<span data-ttu-id="9296d-113">**msiexec/I mypackage.msi Transformationen =: instance. MST msinewinstance = 1/QB**</span><span class="sxs-lookup"><span data-stu-id="9296d-113">**msiexec /I mypackage.msi TRANSFORMS=:instance.mst MSINEWINSTANCE=1 /qb**</span></span>

<span data-ttu-id="9296d-114">Das folgende Beispiel zeigt die Installation einer neuen Instanz mit [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span><span class="sxs-lookup"><span data-stu-id="9296d-114">The following example shows installing a new instance using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta).</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("TRANSFORMS=:instance.mst MSINEWINSTANCE=1"));
```

<span data-ttu-id="9296d-115">Das folgende Beispiel zeigt die Installation der neuen Instanz aus dem Skript.</span><span class="sxs-lookup"><span data-stu-id="9296d-115">The following example shows installing the new instance from script.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "TRANSFORMS=:instance.mst MSINEWINSTANCE=1"
```

<span data-ttu-id="9296d-116">Im folgenden Beispiel wird eine-Instanz neu installiert, ohne dass das Paket erneut zwischengespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="9296d-116">The following example reinstalls an instance without re-caching the package.</span></span> <span data-ttu-id="9296d-117">Der Produktcode verweist auf die Instanz {00000001-0002-0000-0000-624474736554} .</span><span class="sxs-lookup"><span data-stu-id="9296d-117">The instance is referred to by its product code {00000001-0002-0000-0000-624474736554}.</span></span>

<span data-ttu-id="9296d-118">**msiexec/I {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = omus/QB**</span><span class="sxs-lookup"><span data-stu-id="9296d-118">**msiexec /I {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=omus /qb**</span></span>

<span data-ttu-id="9296d-119">Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket über die Befehlszeile erneut zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9296d-119">The following example reinstalls an instance and re-caches the package from the command line.</span></span> <span data-ttu-id="9296d-120">Der Paketpfad verweist auf die Instanz.</span><span class="sxs-lookup"><span data-stu-id="9296d-120">The instance is referred to by the package path.</span></span> <span data-ttu-id="9296d-121">Sie müssen nur die Option/n {Product Code} einschließen, wenn das Produkt ursprünglich mit einer instanztransformation installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9296d-121">You are only required to include the /n {Product Code} option if the product is originally installed with an instance transform.</span></span>

<span data-ttu-id="9296d-122">**msiexec/I c: \\ NewPath \\mypackage.msi/n {00000001-0002-0000-0000-624474736554} REINSTALL = ALL REINSTALLMODE = vomus/QB**</span><span class="sxs-lookup"><span data-stu-id="9296d-122">**msiexec /I c:\\newpath\\mypackage.msi /n {00000001-0002-0000-0000-624474736554} REINSTALL=ALL REINSTALLMODE=vomus /qb**</span></span>

<span data-ttu-id="9296d-123">Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket mit **msiinstallproduct** zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9296d-123">The following example reinstalls an instance and caches the package using **MsiInstallProduct**.</span></span> <span data-ttu-id="9296d-124">Der Paketpfad verweist auf die Instanz.</span><span class="sxs-lookup"><span data-stu-id="9296d-124">The instance is referred to by the package path.</span></span> <span data-ttu-id="9296d-125">Verwenden Sie die **msiinstanceguid** -Eigenschaft, um den Produktcode der-Instanz bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9296d-125">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
UINT uiStat = MsiInstallProduct(_T("path to mypackage.msi"), _T("MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"));
```

<span data-ttu-id="9296d-126">Im folgenden Beispiel wird eine-Instanz neu installiert und das Paket mithilfe des-Skripts zwischengespeichert.</span><span class="sxs-lookup"><span data-stu-id="9296d-126">The following example reinstalls an instance and caches the package using script.</span></span> <span data-ttu-id="9296d-127">Verwenden Sie die **msiinstanceguid** -Eigenschaft, um den Produktcode der-Instanz bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9296d-127">Use the **MSIINSTANCEGUID** property to provide the product code of the instance.</span></span>

``` syntax
Dim Installer As Object
Set Installer = CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "path to mypackage.msi", "MSIINSTANCEGUID={00000001-0002-0000-0000-624474736554}  REINSTALL=ALL REINSTALLMODE=vomus"
```

<span data-ttu-id="9296d-128">Im folgenden Beispiel wird gezeigt, wie eine Instanz über die Befehlszeile angekündigt wird.</span><span class="sxs-lookup"><span data-stu-id="9296d-128">The following example shows how to advertise an instance using the command line.</span></span>

<span data-ttu-id="9296d-129">**msiexec/JM mypackage.msi/t: instance. MST/c/QB**</span><span class="sxs-lookup"><span data-stu-id="9296d-129">**msiexec /jm mypackage.msi /t :instance.mst /c /qb**</span></span>

<span data-ttu-id="9296d-130">Im folgenden Beispiel wird gezeigt, wie installiert wird, um eine Instanz mit **msiankünabproductex** ankündigen zu können.</span><span class="sxs-lookup"><span data-stu-id="9296d-130">The following example shows how to install to advertise an instance using **MsiAdvertiseProductEx**.</span></span>

``` syntax
UINT uiStat = MsiAdvertiseProductEx(_T("path to mypackage.msi"), NULL, _T(":instance.mst"), 0, 0, MSIADVERTISEOPTIONS_INSTANCE);
```

<span data-ttu-id="9296d-131">Im folgenden Beispiel wird gezeigt, wie ein Patch von einer Befehlszeile auf eine-Instanz angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9296d-131">The following example shows how to apply a patch to an instance from a command line.</span></span> <span data-ttu-id="9296d-132">Sie müssen nur die Option/n {Product Code} einschließen, wenn das Produkt ursprünglich mit einer instanztransformation installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9296d-132">You are only required to include the /n {Product Code} option if the product was originally installed with an instance transform.</span></span>

<span data-ttu-id="9296d-133">**msiexec/p mypatch. msp/n {00000001-0002-0000-0000-624474736554} /qb**</span><span class="sxs-lookup"><span data-stu-id="9296d-133">**msiexec /p mypatch.msp /n {00000001-0002-0000-0000-624474736554} /qb**</span></span>

<span data-ttu-id="9296d-134">Im folgenden Beispiel wird gezeigt, wie Sie mithilfe von [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha)einen Patch auf eine instanzinstallation anwenden.</span><span class="sxs-lookup"><span data-stu-id="9296d-134">The following example shows how to apply a patch to an instance installation using [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha).</span></span>

``` syntax
UINT uiStat = MsiApplyPatch(_T("path to mypatch.msp"), _T("{00000001-0002-0000-0000-624474736554}"), INSTALLTYPE_SINGLE_INSTANCE, _T("REINSTALL=ALL REINSTALLMODE=omus"));
```

<span data-ttu-id="9296d-135">Weitere Informationen finden Sie unter [Installieren mehrerer Instanzen von Produkten und Patches](installing-multiple-instances-of-products-and-patches.md) und [Erstellen mehrerer Instanzen mit instanztransformationen](authoring-multiple-instances-with-instance-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="9296d-135">For more information, see [Installing Multiple Instances of Products and Patches](installing-multiple-instances-of-products-and-patches.md) and [Authoring Multiple Instances with Instance Transforms](authoring-multiple-instances-with-instance-transforms.md).</span></span>

 

 



