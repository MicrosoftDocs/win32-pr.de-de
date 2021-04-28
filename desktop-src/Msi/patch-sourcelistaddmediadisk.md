---
description: 'Patch.SourceListAddMediaDisk-Methode: Die SourceListAddMediaDisk-Methode fügt dem Satz registrierter Datenträger einen Datenträger hinzu. Akzeptiert Diskid, VolumeLabel und DiskPrompt als Parameter. Diese Methode ruft für MsiSourceListAddMediaDisk auf.'
ms.assetid: 6feaf2d3-7e39-4e22-9e74-9a2f98369eac
title: Patch.SourceListAddMediaDisk-Methode
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
ms.openlocfilehash: 052831befb95976358b53d989db36d5b2fa43efe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084371"
---
# <a name="patchsourcelistaddmediadisk-method"></a><span data-ttu-id="b990f-105">Patch.SourceListAddMediaDisk-Methode</span><span class="sxs-lookup"><span data-stu-id="b990f-105">Patch.SourceListAddMediaDisk method</span></span>

<span data-ttu-id="b990f-106">Die **SourceListAddMediaDisk-Methode** fügt dem Satz registrierter Datenträger einen Datenträger hinzu.</span><span class="sxs-lookup"><span data-stu-id="b990f-106">The **SourceListAddMediaDisk** method adds a disk to the set of registered disks.</span></span> <span data-ttu-id="b990f-107">Akzeptiert *Diskid,* *VolumeLabel* und *DiskPrompt* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="b990f-107">Accepts *Diskid*, *VolumeLabel* and *DiskPrompt* as parameters.</span></span> <span data-ttu-id="b990f-108">Diese Methode ruft für [**MsiSourceListAddMediaDisk auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)</span><span class="sxs-lookup"><span data-stu-id="b990f-108">This method calls on [**MsiSourceListAddMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="b990f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b990f-109">Syntax</span></span>


```JScript
Patch.SourceListAddMediaDisk(
  Diskid,
  VolumeLabel,
  DiskPrompt
)
```



## <a name="parameters"></a><span data-ttu-id="b990f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b990f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b990f-111">*Diskid*</span><span class="sxs-lookup"><span data-stu-id="b990f-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="b990f-112">Dieser Parameter gibt die ID des Datenträgers an, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b990f-112">This parameter provides the ID of the disk being added or updated.</span></span>

</dd> <dt>

<span data-ttu-id="b990f-113">*VolumeLabel*</span><span class="sxs-lookup"><span data-stu-id="b990f-113">*VolumeLabel*</span></span> 
</dt> <dd>

<span data-ttu-id="b990f-114">Dieser Parameter gibt die Bezeichnung des Datenträgers an, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b990f-114">This parameter provides the label of the disk being added or updated.</span></span> <span data-ttu-id="b990f-115">Ein Update überschreibt die vorhandene Volumebezeichnung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b990f-115">An update, overwrites the existing volume label in the registry.</span></span> <span data-ttu-id="b990f-116">Um nur die Datenträgeraufforderung zu ändern, erhalten Sie die vorhandene registrierte Volumebezeichnung, und geben Sie sie zusammen mit der eingabeaufforderung für den neuen Datenträger an.</span><span class="sxs-lookup"><span data-stu-id="b990f-116">To change the disk prompt only, get the existing registered volume label and provide it along with the new disk prompt.</span></span> <span data-ttu-id="b990f-117">Eine NULL- oder leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte länge) als Volumebezeichnung.</span><span class="sxs-lookup"><span data-stu-id="b990f-117">A NULL or empty string registers an empty string (0 bytes in length) as the volume label.</span></span>

</dd> <dt>

<span data-ttu-id="b990f-118">*DiskPrompt*</span><span class="sxs-lookup"><span data-stu-id="b990f-118">*DiskPrompt*</span></span> 
</dt> <dd>

<span data-ttu-id="b990f-119">Dieser Parameter stellt die Datenträgeraufforderung des Datenträgers zur Eingabe, der hinzugefügt oder aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="b990f-119">This parameter provides the disk prompt of the disk being added or updated.</span></span> <span data-ttu-id="b990f-120">Ein Update überschreibt die vorhandene Datenträgeraufforderung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="b990f-120">An update overwrites the existing disk prompt in the registry.</span></span> <span data-ttu-id="b990f-121">Um nur die Volumebezeichnung zu ändern, erhalten Sie die vorhandene Datenträgeraufforderung aus der Registrierung, und geben Sie die neue Volumebezeichnung an.</span><span class="sxs-lookup"><span data-stu-id="b990f-121">To change the volume label only, get the existing disk prompt from the registry and provide it with the new volume label.</span></span> <span data-ttu-id="b990f-122">Eine NULL- oder leere Zeichenfolge registriert eine leere Zeichenfolge (0 Byte lang) als Datenträgeraufforderung.</span><span class="sxs-lookup"><span data-stu-id="b990f-122">A NULL or empty string registers an empty string (0 bytes in length) as the disk prompt.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b990f-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b990f-123">Return value</span></span>

<span data-ttu-id="b990f-124">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="b990f-124">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="b990f-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b990f-125">Requirements</span></span>



| <span data-ttu-id="b990f-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b990f-126">Requirement</span></span> | <span data-ttu-id="b990f-127">Wert</span><span class="sxs-lookup"><span data-stu-id="b990f-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b990f-128">Version</span><span class="sxs-lookup"><span data-stu-id="b990f-128">Version</span></span><br/> | <span data-ttu-id="b990f-129">Windows Installer 5.0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="b990f-129">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="b990f-130">Windows Installer 4.0 oder Windows Installer 4.5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b990f-130">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="b990f-131">Windows Installer 3.0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="b990f-131">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="b990f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="b990f-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="b990f-133"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b990f-133"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="b990f-134">IID</span><span class="sxs-lookup"><span data-stu-id="b990f-134">IID</span></span><br/>     | <span data-ttu-id="b990f-135">IID \_ IPatch ist als 000C10A1-0000-0000-C000-000000000046 definiert.</span><span class="sxs-lookup"><span data-stu-id="b990f-135">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="b990f-136">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b990f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b990f-137">**Patch**</span><span class="sxs-lookup"><span data-stu-id="b990f-137">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="b990f-138">**MsiSourceListAddMediaDisk**</span><span class="sxs-lookup"><span data-stu-id="b990f-138">**MsiSourceListAddMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistaddmediadiska)
</dt> <dt>

[<span data-ttu-id="b990f-139">In Windows Installer 2.0 und früher nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b990f-139">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




