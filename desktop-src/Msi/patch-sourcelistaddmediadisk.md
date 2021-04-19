---
description: Die sourcelistaddmediadisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert DiskId, VolumeLabel und diskprompt als Parameter. Diese Methode ruft auf msisourcelistaddmediadisk auf.
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Patch. sourcelistaddmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListAddMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a7c74ccdfb90a0cb365e6110defc9b60dac1f471
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366727"
---
# <a name="patchsourcelistaddmediadisk-method"></a><span data-ttu-id="9ea89-105">Patch. sourcelistaddmediadisk-Methode</span><span class="sxs-lookup"><span data-stu-id="9ea89-105">Patch.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="9ea89-106">Die **sourcelistaddmediadisk** -Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="9ea89-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="9ea89-107">Akzeptiert *DiskId*, *VolumeLabel* und *diskprompt* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="9ea89-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="9ea89-108">Diese Methode ruft auf [**msisourcelistaddmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)auf.</span><span class="sxs-lookup"><span data-stu-id="9ea89-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea89-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ea89-109">Syntax</span></span>


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="9ea89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ea89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ea89-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="9ea89-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea89-112">Dieser Parameter gibt die ID des Datenträgers an, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ea89-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="9ea89-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="9ea89-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea89-114">Dieser Parameter gibt die Bezeichnung des Datenträgers an, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ea89-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="9ea89-115">Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ea89-115">An update, overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="9ea89-116">Wenn Sie nur die Eingabeaufforderung für den Datenträger ändern möchten, können Sie die vorhandene registrierte Volumebezeichnung sowie die neue Eingabeaufforderung für den Datenträger angeben.</span><span class="sxs-lookup"><span data-stu-id="9ea89-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="9ea89-117">Eine NULL-Zeichenfolge oder eine leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte Länge) als Volumebezeichnung.</span><span class="sxs-lookup"><span data-stu-id="9ea89-117">A NULL or empty string registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="9ea89-118">*Diskprompt*</span><span class="sxs-lookup"><span data-stu-id="9ea89-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="9ea89-119">Dieser Parameter gibt die Eingabeaufforderung des Datenträgers an, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="9ea89-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="9ea89-120">Ein Update überschreibt die vorhandene Datenträger Aufforderung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ea89-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="9ea89-121">Um die Volumebezeichnung nur zu ändern, müssen Sie die vorhandene Datenträger Aufforderung aus der Registrierung erhalten und die neue Volumebezeichnung bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9ea89-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="9ea89-122">Eine NULL-Zeichenfolge oder eine leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte Länge) als Eingabeaufforderung für den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="9ea89-122">A NULL or empty string registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ea89-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ea89-123">Return value</span></span>

<span data-ttu-id="9ea89-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9ea89-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea89-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ea89-125">Requirements</span></span>



| <span data-ttu-id="9ea89-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ea89-126">Requirement</span></span> | <span data-ttu-id="9ea89-127">Wert</span><span class="sxs-lookup"><span data-stu-id="9ea89-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ea89-128">Version</span><span class="sxs-lookup"><span data-stu-id="9ea89-128">Version</span></span><br/> | <span data-ttu-id="9ea89-129">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="9ea89-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="9ea89-130">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9ea89-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="9ea89-131">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="9ea89-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="9ea89-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9ea89-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="9ea89-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ea89-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="9ea89-134">IID</span><span class="sxs-lookup"><span data-stu-id="9ea89-134">IID</span></span><br/>     | <span data-ttu-id="9ea89-135">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="9ea89-135">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="9ea89-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ea89-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea89-137">**Patch**</span><span class="sxs-lookup"><span data-stu-id="9ea89-137">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="9ea89-138">**Msisourcelistaddmediadisk**</span><span class="sxs-lookup"><span data-stu-id="9ea89-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="9ea89-139">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9ea89-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




