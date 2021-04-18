---
description: Die applymultiplepatches-Methode wendet ein oder mehrere Patches auf Produkte an, die zum Empfangen des Patches berechtigt sind. Mit der-Methode wird die Patch-Eigenschaft festgelegt.
ms.assetid: 40c40e2c-60ef-4492-a4ab-0bb6b874fe80
title: Installer. applymultiplepatches-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ApplyMultiplePatches
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d96d96157f7b1d81617be6980804fb54a6e6659f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357685"
---
# <a name="installerapplymultiplepatches-method"></a><span data-ttu-id="56cfd-104">Installer. applymultiplepatches-Methode</span><span class="sxs-lookup"><span data-stu-id="56cfd-104">Installer.ApplyMultiplePatches method</span></span>

<span data-ttu-id="56cfd-105">Die **applymultiplepatches** -Methode wendet ein oder mehrere Patches auf Produkte an, die zum Empfangen des Patches berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="56cfd-105">The **ApplyMultiplePatches** method applies one or more patches to products that are eligible to receive the patch.</span></span> <span data-ttu-id="56cfd-106">Mit der-Methode wird die [**Patch**](patch.md) -Eigenschaft festgelegt.</span><span class="sxs-lookup"><span data-stu-id="56cfd-106">The method sets the [**PATCH**](patch.md) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="56cfd-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="56cfd-107">Syntax</span></span>


```JScript
Installer.ApplyMultiplePatches(
  PatchPackagesList,
  Product,
  szPropertiesList
)
```



## <a name="parameters"></a><span data-ttu-id="56cfd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="56cfd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56cfd-109">*Patchpackageslist*</span><span class="sxs-lookup"><span data-stu-id="56cfd-109">*PatchPackagesList*</span></span> 
</dt> <dd>

<span data-ttu-id="56cfd-110">Eine Zeichenfolge, die eine durch Semikolons getrennte Liste der Pfade zu Patchdateien enthält.</span><span class="sxs-lookup"><span data-stu-id="56cfd-110">A string that contains a semicolon-delimited list of the paths to patch files.</span></span> <span data-ttu-id="56cfd-111">Beispiel: "" c: \\ SUS \\ Download \\ Cache \\ Office \\ SP1. msp; c: \\ SUS \\ Download \\ Cache \\ Office \\ QFE1. msp; c: \\ SUS \\ Download \\ Cache \\ Office \\ qfen. msp ""</span><span class="sxs-lookup"><span data-stu-id="56cfd-111">For example: ""c:\\sus\\download\\cache\\Office\\sp1.msp; c:\\sus\\download\\cache\\Office\\QFE1.msp;c:\\sus\\download\\cache\\Office\\QFEn.msp""</span></span>

</dd> <dt>

<span data-ttu-id="56cfd-112">*Produkt*</span><span class="sxs-lookup"><span data-stu-id="56cfd-112">*Product*</span></span> 
</dt> <dd>

<span data-ttu-id="56cfd-113">Dieser Parameter stellt den [**ProductCode**](productcode.md) des Produkts bereit, das gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="56cfd-113">This parameter provides the [**ProductCode**](productcode.md) of the product being patched.</span></span> <span data-ttu-id="56cfd-114">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="56cfd-114">This parameter is optional.</span></span> <span data-ttu-id="56cfd-115">Wenn dieser Parameter NULL ist, werden die Patches auf alle Produkte angewendet, die für den Empfang dieser Patches berechtigt sind.</span><span class="sxs-lookup"><span data-stu-id="56cfd-115">When this parameter is null, the patches are applied to all products that are eligible to receive these patches.</span></span>

</dd> <dt>

<span data-ttu-id="56cfd-116">*szpropertieslist*</span><span class="sxs-lookup"><span data-stu-id="56cfd-116">*szPropertiesList*</span></span> 
</dt> <dd>

<span data-ttu-id="56cfd-117">Eine auf NULL endenden Zeichenfolge, die Befehlszeilen-Eigenschafts Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="56cfd-117">A null-terminated string that specifies command-line property settings.</span></span> <span data-ttu-id="56cfd-118">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="56cfd-118">This parameter is optional.</span></span> <span data-ttu-id="56cfd-119">Weitere Informationen finden Sie unter [Informationen zu Eigenschaften](about-properties.md) und [festlegen öffentlicher Eigenschaftswerte in der Befehlszeile](setting-public-property-values-on-the-command-line.md).</span><span class="sxs-lookup"><span data-stu-id="56cfd-119">See [About Properties](about-properties.md) and [Setting Public Property Values on the Command Line](setting-public-property-values-on-the-command-line.md).</span></span> <span data-ttu-id="56cfd-120">Diese Eigenschaften werden von allen Ziel Produkten gemeinsam genutzt.</span><span class="sxs-lookup"><span data-stu-id="56cfd-120">These properties are shared by all target products.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56cfd-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56cfd-121">Return value</span></span>

<span data-ttu-id="56cfd-122">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="56cfd-122">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="56cfd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="56cfd-123">Requirements</span></span>



| <span data-ttu-id="56cfd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="56cfd-124">Requirement</span></span> | <span data-ttu-id="56cfd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="56cfd-125">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="56cfd-126">Version</span><span class="sxs-lookup"><span data-stu-id="56cfd-126">Version</span></span><br/> | <span data-ttu-id="56cfd-127">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="56cfd-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="56cfd-128">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="56cfd-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="56cfd-129">Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.</span><span class="sxs-lookup"><span data-stu-id="56cfd-129">Windows Installer 3.0 or later on Windows Server 2003 or Windows XP.</span></span><br/> |
| <span data-ttu-id="56cfd-130">DLL</span><span class="sxs-lookup"><span data-stu-id="56cfd-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="56cfd-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56cfd-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                    |
| <span data-ttu-id="56cfd-132">IID</span><span class="sxs-lookup"><span data-stu-id="56cfd-132">IID</span></span><br/>     | <span data-ttu-id="56cfd-133">IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="56cfd-133">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="56cfd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56cfd-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56cfd-135">Informationen zu Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="56cfd-135">About Properties</span></span>](about-properties.md)
</dt> <dt>

[<span data-ttu-id="56cfd-136">**ProductCode**</span><span class="sxs-lookup"><span data-stu-id="56cfd-136">**ProductCode**</span></span>](productcode.md)
</dt> <dt>

[<span data-ttu-id="56cfd-137">**Patch**</span><span class="sxs-lookup"><span data-stu-id="56cfd-137">**PATCH**</span></span>](patch.md)
</dt> <dt>

[<span data-ttu-id="56cfd-138">Festlegen von Werten für öffentliche Eigenschaften in der Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="56cfd-138">Setting Public Property Values on the Command Line</span></span>](setting-public-property-values-on-the-command-line.md)
</dt> <dt>

[<span data-ttu-id="56cfd-139">**Msiapplymultiplepatches**</span><span class="sxs-lookup"><span data-stu-id="56cfd-139">**MsiApplyMultiplePatches**</span></span>](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa)
</dt> <dt>

[<span data-ttu-id="56cfd-140">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="56cfd-140">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




