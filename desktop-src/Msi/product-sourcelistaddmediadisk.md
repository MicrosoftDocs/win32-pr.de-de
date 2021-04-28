---
description: 'Product.SourceListAddMediaDisk-Methode: Die SourceListAddMediaDisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert Diskid, VolumeLabel und DiskPrompt als Parameter. Diese Methode ruft für MsiSourceListAddMediaDisk auf.'
ms.assetid: 19cb6884-2191-4da3-a6d2-8874564be67d
title: Product.SourceListAddMediaDisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 4cf5fac906b048930b47a07acb2c04c7243d5bbf
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113578"
---
# <a name="productsourcelistaddmediadisk-method"></a><span data-ttu-id="7bfec-105">Product.SourceListAddMediaDisk-Methode</span><span class="sxs-lookup"><span data-stu-id="7bfec-105">Product.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="7bfec-106">Die **SourceListAddMediaDisk-Methode** fügt dem Satz registrierter Datenträger einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="7bfec-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="7bfec-107">Akzeptiert *Diskid,* *VolumeLabel* und *DiskPrompt* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="7bfec-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="7bfec-108">Diese Methode ruft [**für MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)auf.</span><span class="sxs-lookup"><span data-stu-id="7bfec-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bfec-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="7bfec-109">Syntax</span></span>


```JScript
Product.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="7bfec-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7bfec-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bfec-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="7bfec-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfec-112">Dieser Parameter stellt die ID des Datenträgers bereit, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bfec-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="7bfec-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="7bfec-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfec-114">Dieser Parameter stellt die Bezeichnung des Datenträgers bereit, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bfec-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="7bfec-115">Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7bfec-115">An update overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="7bfec-116">Um nur die Datenträgereingabeaufforderung zu ändern, erhalten Sie die vorhandene Bezeichnung für registrierte Volumes, und geben Sie sie zusammen mit der eingabeaufforderung für den neuen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="7bfec-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="7bfec-117">Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte lang) als Volumebezeichnung.</span><span class="sxs-lookup"><span data-stu-id="7bfec-117">An empty string for this parameter registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="7bfec-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="7bfec-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="7bfec-119">Dieser Parameter stellt die Eingabeaufforderung des Datenträgers bereit, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="7bfec-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="7bfec-120">Ein Update überschreibt die vorhandene Datenträgeraufforderung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="7bfec-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="7bfec-121">Um nur die Volumebezeichnung zu ändern, erhalten Sie die vorhandene Datenträgeraufforderung aus der Registrierung, und geben Sie die neue Volumebezeichnung an.</span><span class="sxs-lookup"><span data-stu-id="7bfec-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="7bfec-122">Eine leere Zeichenfolge für diesen Parameter registriert eine leere Zeichenfolge (0 Byte lang) als Eingabeaufforderung für den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="7bfec-122">An empty string for this parameter registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bfec-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7bfec-123">Return value</span></span>

<span data-ttu-id="7bfec-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7bfec-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bfec-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bfec-125">Requirements</span></span>



| <span data-ttu-id="7bfec-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7bfec-126">Requirement</span></span> | <span data-ttu-id="7bfec-127">Wert</span><span class="sxs-lookup"><span data-stu-id="7bfec-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bfec-128">Version</span><span class="sxs-lookup"><span data-stu-id="7bfec-128">Version</span></span><br/> | <span data-ttu-id="7bfec-129">Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="7bfec-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7bfec-130">Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="7bfec-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7bfec-131">Windows Installer 3.0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="7bfec-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="7bfec-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7bfec-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="7bfec-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bfec-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="7bfec-134">IID</span><span class="sxs-lookup"><span data-stu-id="7bfec-134">IID</span></span><br/>     | <span data-ttu-id="7bfec-135">IID IProduct ist als \_ 000C10A0-0000-0000-C000-00000000046 definiert.</span><span class="sxs-lookup"><span data-stu-id="7bfec-135">IID\_IProduct is defined as 000C10A0-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                          |



## <a name="see-also"></a><span data-ttu-id="7bfec-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7bfec-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bfec-137">**Produkt**</span><span class="sxs-lookup"><span data-stu-id="7bfec-137">**Product**</span></span>](product-object.md)
</dt> <dt>

[<span data-ttu-id="7bfec-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="7bfec-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="7bfec-139">In Version Windows Installer 2.0 und früher nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7bfec-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




