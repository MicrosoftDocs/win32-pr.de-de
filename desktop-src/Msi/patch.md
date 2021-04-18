---
description: Der Installer legt die Patch-Eigenschaft auf eine Liste der angewendeten Patches fest, indem msiapplypatch, msiapplymultiplepatches oder die Befehlszeilen Option/p aufgerufen wird.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Patch-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358685"
---
# <a name="patch-property"></a><span data-ttu-id="bcfd3-103">Patch-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bcfd3-103">PATCH property</span></span>

<span data-ttu-id="bcfd3-104">Der Installer legt die **Patch** -Eigenschaft auf eine Liste der angewendeten Patches fest, indem [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) oder die [Befehlszeilen Option](command-line-options.md)/p aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-104">The installer sets the **PATCH** property to a list of patches being applied by calling [**MsiApplyPatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**MsiApplyMultiplePatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) or the /p [Command Line Option](command-line-options.md).</span></span> <span data-ttu-id="bcfd3-105">Sie können die **Patch** -Eigenschaft auch in der Befehlszeile festlegen, wenn Sie ein Paket mit [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) oder der/i-Befehlszeilen Option installieren.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-105">You can also set the **PATCH** property on the command line while installing a package using [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) or the /i Command Line Option.</span></span>

<span data-ttu-id="bcfd3-106">Der Wert der **Patch** -Eigenschaft ist eine Liste der Patches, die installiert werden.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-106">The value of the **PATCH** property is a list of the patches that are being installed.</span></span> <span data-ttu-id="bcfd3-107">Jeder Patch in der Liste wird durch den vollständigen Pfad zum Paket des Patches (MSP-Datei) repräsentiert. Die vollständigen Pfade in der Liste werden durch Semikolons getrennt.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-107">Each patch in the list is represented by the full path to the patch's package (.msp file.) The full paths in the list are separated by semicolons.</span></span>

<span data-ttu-id="bcfd3-108">**Windows Installer 2,0:** Mehrere Patches werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-108">**Windows Installer 2.0:** Multiple patches are not supported.</span></span> <span data-ttu-id="bcfd3-109">Windows Installer 3,0 ist zum Anwenden mehrerer Patches erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-109">Windows Installer 3.0 is required to apply multiple patches.</span></span>

## <a name="remarks"></a><span data-ttu-id="bcfd3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcfd3-110">Remarks</span></span>

<span data-ttu-id="bcfd3-111">Wenn Sie mit [Msimsp.exe](msimsp-exe.md) ein Patchpaket erstellen und [Patchwiz.dll](patchwiz-dll.md) können Sie angeben, dass eine Aktion oder ein Dialogfeld nur ausgeführt wird, wenn ein bestimmter Patch angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-111">If you create a patch package using [Msimsp.exe](msimsp-exe.md) and [Patchwiz.dll](patchwiz-dll.md) you can specify that an action or a dialog box only run when a particular patch is being applied.</span></span> <span data-ttu-id="bcfd3-112">Wenn Sie das Patchpaket erstellen, z. b. "Test. msp", erstellen Sie ein aktualisiertes Image des Produkts und eine Eigenschaften Datei für die Patcherstellung.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-112">When you create the patch package, for example test.msp, you author an upgraded image of the product and a patch creation properties file.</span></span> <span data-ttu-id="bcfd3-113">Wenn Sie die Eigenschaften Datei für die Patcherstellung erstellen, können Sie einen Eigenschaftsnamen (z. b. patchfortest) in das Feld "mediasrcpropname" der Tabelle " [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) " eingeben.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-113">When authoring the patch creation properties file you can enter a property name, for example PATCHFORTEST, in the MediaSrcPropName field of the [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) table.</span></span> <span data-ttu-id="bcfd3-114">Wenn Sie die Sequenz Tabellen des aktualisierten Abbilds des Produkts erstellen, können Sie in die Spalte Bedingung der Sequenz Tabelle eine Bedingungs Anweisung für die Aktion oder das Dialogfeld einschließen, die Sie bedingen möchten.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-114">When you author the sequence tables of the upgraded image of the product, you can include in the Condition column of the sequence table a conditional statement for the action or dialog box you want to make conditional.</span></span>

<span data-ttu-id="bcfd3-115">Beispielsweise können Sie die folgende Bedingungs Anweisung verwenden, um eine Aktion oder ein Dialogfeld nur dann auszuführen, wenn "Test. msp" angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-115">For example, you can use the following conditional statement to run an action or dialog box only when test.msp is being applied.</span></span>

<dl> <span data-ttu-id="bcfd3-116">Patch und patchfortest und Patch >< patchfortest</span><span class="sxs-lookup"><span data-stu-id="bcfd3-116">PATCH AND PATCHFORTEST AND PATCH >< PATCHFORTEST</span></span>  
</dl>

> [!Note]  
> <span data-ttu-id="bcfd3-117">Da die **patcheigenschaft** mehrere Patches enthalten kann, verwenden Sie den Teil Zeichenfolge-Operator "><", um zu prüfen, ob ein bestimmter Patch statt der Gleichheits Operator "=" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-117">Because the **PATCH** property can contain multiple patches, use the substring operator "><" to test for the presence of a particular patch rather than the equals operator "=".</span></span> <span data-ttu-id="bcfd3-118">Weitere Informationen zu bedingten Anweisungen finden Sie im Abschnitt [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfd3-118">For more information about conditional statements see the [Conditional Statement Syntax](conditional-statement-syntax.md) section.</span></span>

 

<span data-ttu-id="bcfd3-119">Der Installer legt beide Eigenschaften fest, wenn Sie eine Liste von Patches, die "Test. msp" enthalten, anwenden.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-119">The installer sets both properties if you apply a list of patches that includes test.msp.</span></span> <span data-ttu-id="bcfd3-120">Beispielsweise können Sie die [Befehlszeilen Option](command-line-options.md) /p verwenden, um eine Liste mit zwei Patches anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-120">For example, you can use the /p [Command Line Option](command-line-options.md) to apply a list of two patches.</span></span>

<span data-ttu-id="bcfd3-121">**msiexec/qb/p \\ \\ Scratch \\ , Scratch- \\ \\ Patches \\ , Test. msp; \\ \\ Scratch \\ - \\ \\ Balken. msp Scratch**</span><span class="sxs-lookup"><span data-stu-id="bcfd3-121">**msiexec /qb /p \\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp**</span></span>

<span data-ttu-id="bcfd3-122">Der Installer legt die **Patch** -und patchfortest-Eigenschaften wie folgt fest.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-122">The installer sets the **PATCH** and PATCHFORTEST properties as follows.</span></span>

<dl> <span data-ttu-id="bcfd3-123">Patch = Scratch Scratch- \\ \\ \\ Patches ( \\ \\ \\ Test. msp \\ \\ ) Scratch \\ - \\ \\ Balken. msp Scratch</span><span class="sxs-lookup"><span data-stu-id="bcfd3-123">PATCH=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp;\\\\scratch\\scratch\\XYZ\\bar.msp</span></span>  
<span data-ttu-id="bcfd3-124">Patchfortest = Scratch Scratch- \\ \\ \\ Patches- \\ \\ \\ Test. msp</span><span class="sxs-lookup"><span data-stu-id="bcfd3-124">PATCHFORTEST=\\\\scratch\\scratch\\XYZ\\Patches\\test.msp</span></span>  
</dl>

<span data-ttu-id="bcfd3-125">In diesem Fall ist die Bedingung "true", und die oben beschriebene bedingte Aktion oder das obige Dialogfeld kann für jeden installierten Patch ausgeführt werden: "Test. msp" und "Bar. msp".</span><span class="sxs-lookup"><span data-stu-id="bcfd3-125">In this case, the condition is TRUE and the above conditional action or dialog box can run for each patch being installed, test.msp and bar.msp.</span></span>

<span data-ttu-id="bcfd3-126">Wenn "Test. msp" nicht angewendet wird, schließt das Installationsprogramm es nicht in die **patcheigenschaft** ein und legt "patchfortest" nicht fest.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-126">If test.msp is not being applied, the installer does not include it in the **PATCH** property and does not set PATCHFORTEST.</span></span> <span data-ttu-id="bcfd3-127">In diesem Fall ist die oben genannte Bedingung false, und die bedingte Aktion oder das Dialogfeld wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-127">In this case, the condition above is FALSE and the conditional action or dialog box does not run.</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfd3-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcfd3-128">Requirements</span></span>



| <span data-ttu-id="bcfd3-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcfd3-129">Requirement</span></span> | <span data-ttu-id="bcfd3-130">Wert</span><span class="sxs-lookup"><span data-stu-id="bcfd3-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfd3-131">Version</span><span class="sxs-lookup"><span data-stu-id="bcfd3-131">Version</span></span><br/> | <span data-ttu-id="bcfd3-132">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-132">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bcfd3-133">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-133">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bcfd3-134">Windows Installer unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="bcfd3-134">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bcfd3-135">Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="bcfd3-135">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bcfd3-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcfd3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcfd3-137">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="bcfd3-137">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="bcfd3-138">Syntax der bedingten Anweisung</span><span class="sxs-lookup"><span data-stu-id="bcfd3-138">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="bcfd3-139">Beispiele für bedingte Anweisungs Syntax</span><span class="sxs-lookup"><span data-stu-id="bcfd3-139">Examples of Conditional Statement Syntax</span></span>](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




