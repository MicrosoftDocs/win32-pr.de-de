---
description: Mit der removepatches-Methode werden ein oder mehrere Patches zu Produkten entfernt, die zum Empfangen des Patches berechtigt sind. Die removepatches-Methode ruft msiremovepatches auf.
ms.assetid: 09c6ad3a-9f5e-4f9a-82c8-be7e411efd60
title: Installer. removepatches-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.RemovePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 2130ae2958f03eb16b5145e5eb61e42f869ad775
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355926"
---
# <a name="installerremovepatches-method"></a><span data-ttu-id="217bb-104">Installer. removepatches-Methode</span><span class="sxs-lookup"><span data-stu-id="217bb-104">Installer.RemovePatches method</span></span>

<span data-ttu-id="217bb-105">Mit der **removepatches** -Methode werden ein oder mehrere Patches zu Produkten entfernt, die zum Empfangen des Patches berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="217bb-105">The **RemovePatches** method removes one or more patches to products eligible to receive the patch.</span></span> <span data-ttu-id="217bb-106">Die **removepatches** -Methode ruft [**msiremovepatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)auf.</span><span class="sxs-lookup"><span data-stu-id="217bb-106">The **RemovePatches** method calls [**MsiRemovePatches**](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa).</span></span>

## <a name="syntax"></a><span data-ttu-id="217bb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="217bb-107">Syntax</span></span>


```JScript
Installer.RemovePatches(
  PatchList,
  ProductCode,
  UninstallType,
  PropertyList
)
```



## <a name="parameters"></a><span data-ttu-id="217bb-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="217bb-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="217bb-109">*Patchliste*</span><span class="sxs-lookup"><span data-stu-id="217bb-109">*PatchList*</span></span> 
</dt> <dd>

<span data-ttu-id="217bb-110">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der zu entfernenden Patches enthält.</span><span class="sxs-lookup"><span data-stu-id="217bb-110">A string that contains a semicolon delimited list of patches to remove.</span></span> <span data-ttu-id="217bb-111">Jeder Patch kann entweder durch den vollständigen Pfad zum Patchpaket oder durch die Patch-GUID dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="217bb-111">Each patch can be represented by either the full path to the patch package or by patch GUID.</span></span> <span data-ttu-id="217bb-112">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="217bb-112">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="217bb-113">*ProductCode*</span><span class="sxs-lookup"><span data-stu-id="217bb-113">*ProductCode*</span></span> 
</dt> <dd>

<span data-ttu-id="217bb-114">Eine Zeichenfolge mit der GUID des Produkts, von dem die Patches entfernt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="217bb-114">A string with the GUID of the product from which the patches are to be removed.</span></span> <span data-ttu-id="217bb-115">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="217bb-115">This parameter is required.</span></span>

</dd> <dt>

<span data-ttu-id="217bb-116">*Uninstalltype*</span><span class="sxs-lookup"><span data-stu-id="217bb-116">*UninstallType*</span></span> 
</dt> <dd>

<span data-ttu-id="217bb-117">Ein ganzzahliger Wert, der den Typ der Patchentfernung angibt.</span><span class="sxs-lookup"><span data-stu-id="217bb-117">An integer value that specifies the type of patch removal.</span></span> <span data-ttu-id="217bb-118">Dieser Parameter muss " **msiinstalltypesinglabstance**" lauten.</span><span class="sxs-lookup"><span data-stu-id="217bb-118">This parameter must be **msiInstallTypeSingleInstance**.</span></span>

</dd> <dt>

<span data-ttu-id="217bb-119">*Eigenschaftsliste*</span><span class="sxs-lookup"><span data-stu-id="217bb-119">*PropertyList*</span></span> 
</dt> <dd>

<span data-ttu-id="217bb-120">Eine Zeichenfolge, die die einzuschließ-Wert Paare der Eigenschaft = Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="217bb-120">A string that specifies the Property=Value pairs to include.</span></span> <span data-ttu-id="217bb-121">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="217bb-121">This parameter is optional.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="217bb-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="217bb-122">Return value</span></span>

<span data-ttu-id="217bb-123">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="217bb-123">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="217bb-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="217bb-124">Remarks</span></span>

<span data-ttu-id="217bb-125">Unter [Deinstallieren von Patches](uninstalling-patches.md) finden Sie ein Beispiel, das veranschaulicht, wie eine Anwendung einen Patch von allen Produkten entfernen kann, die für den Benutzer verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="217bb-125">See [Uninstalling Patches](uninstalling-patches.md) for an example that demonstrates how an application can remove a patch from all products that are available to the user.</span></span>

## <a name="requirements"></a><span data-ttu-id="217bb-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="217bb-126">Requirements</span></span>



| <span data-ttu-id="217bb-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="217bb-127">Requirement</span></span> | <span data-ttu-id="217bb-128">Wert</span><span class="sxs-lookup"><span data-stu-id="217bb-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="217bb-129">Version</span><span class="sxs-lookup"><span data-stu-id="217bb-129">Version</span></span><br/> | <span data-ttu-id="217bb-130">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="217bb-130">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="217bb-131">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="217bb-131">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="217bb-132">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="217bb-132">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="217bb-133">DLL</span><span class="sxs-lookup"><span data-stu-id="217bb-133">DLL</span></span><br/>     | <dl> <span data-ttu-id="217bb-134"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="217bb-134"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="217bb-135">IID</span><span class="sxs-lookup"><span data-stu-id="217bb-135">IID</span></span><br/>     | <span data-ttu-id="217bb-136">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="217bb-136">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="217bb-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="217bb-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="217bb-138">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="217bb-138">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="217bb-139">**Msiremovepatches**</span><span class="sxs-lookup"><span data-stu-id="217bb-139">**MsiRemovePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiremovepatchesa)
</dt> <dt>

[<span data-ttu-id="217bb-140">Patches werden deinstalliert.</span><span class="sxs-lookup"><span data-stu-id="217bb-140">Uninstalling Patches</span></span>](uninstalling-patches.md)
</dt> <dt>

[<span data-ttu-id="217bb-141">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="217bb-141">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




