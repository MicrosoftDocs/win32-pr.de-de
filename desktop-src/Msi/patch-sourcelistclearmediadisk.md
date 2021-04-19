---
description: Die sourcelistclearmediadisk-Methode des Patch-Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für einen Patch. Akzeptiert DiskId als Parameter. Diese Methode ruft msisourcelistclearmediadisk auf.
ms.assetid: fc52ecb9-2c79-497b-b551-0d3c4f584e86
title: Patch. sourcelistclearmediadisk-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearMediaDisk
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 722b4573d89214312e77e4fde78e1905aefa885f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354071"
---
# <a name="patchsourcelistclearmediadisk-method"></a><span data-ttu-id="216c9-105">Patch. sourcelistclearmediadisk-Methode</span><span class="sxs-lookup"><span data-stu-id="216c9-105">Patch.SourceListClearMediaDisk method</span></span>

<span data-ttu-id="216c9-106">Die **sourcelistclearmediadisk** -Methode des [**Patch**](patch-object.md) -Objekts entfernt einen angegebenen Datenträger aus der Gruppe der registrierten Datenträger für einen Patch.</span><span class="sxs-lookup"><span data-stu-id="216c9-106">The **SourceListClearMediaDisk** method of the [**Patch**](patch-object.md) object removes a specified disk from the set of registered disks for a patch.</span></span> <span data-ttu-id="216c9-107">Akzeptiert *DiskId* als Parameter.</span><span class="sxs-lookup"><span data-stu-id="216c9-107">Accepts *Diskid* as a parameter.</span></span> <span data-ttu-id="216c9-108">Diese Methode ruft [**msisourcelistclearmediadisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)auf.</span><span class="sxs-lookup"><span data-stu-id="216c9-108">This method calls [**MsiSourceListClearMediaDisk**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska).</span></span>

## <a name="syntax"></a><span data-ttu-id="216c9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="216c9-109">Syntax</span></span>


```JScript
Patch.SourceListClearMediaDisk(
  Diskid
)
```



## <a name="parameters"></a><span data-ttu-id="216c9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="216c9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="216c9-111">*DiskId*</span><span class="sxs-lookup"><span data-stu-id="216c9-111">*Diskid*</span></span> 
</dt> <dd>

<span data-ttu-id="216c9-112">Dieser Parameter gibt die ID des zu entfernenden Datenträgers an.</span><span class="sxs-lookup"><span data-stu-id="216c9-112">This parameter provides the ID of the disk to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="216c9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="216c9-113">Return value</span></span>

<span data-ttu-id="216c9-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="216c9-114">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="216c9-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="216c9-115">Requirements</span></span>



| <span data-ttu-id="216c9-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="216c9-116">Requirement</span></span> | <span data-ttu-id="216c9-117">Wert</span><span class="sxs-lookup"><span data-stu-id="216c9-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="216c9-118">Version</span><span class="sxs-lookup"><span data-stu-id="216c9-118">Version</span></span><br/> | <span data-ttu-id="216c9-119">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="216c9-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="216c9-120">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="216c9-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="216c9-121">Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000</span><span class="sxs-lookup"><span data-stu-id="216c9-121">Windows Installer 3.0 or later on Windows Server 2003, Windows XP, and Windows 2000</span></span><br/> |
| <span data-ttu-id="216c9-122">DLL</span><span class="sxs-lookup"><span data-stu-id="216c9-122">DLL</span></span><br/>     | <dl> <span data-ttu-id="216c9-123"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="216c9-123"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                                                   |
| <span data-ttu-id="216c9-124">IID</span><span class="sxs-lookup"><span data-stu-id="216c9-124">IID</span></span><br/>     | <span data-ttu-id="216c9-125">IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="216c9-125">IID\_IPatch is defined as 000C10A1-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                                                            |



## <a name="see-also"></a><span data-ttu-id="216c9-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="216c9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="216c9-127">**Patch**</span><span class="sxs-lookup"><span data-stu-id="216c9-127">**Patch**</span></span>](patch-object.md)
</dt> <dt>

[<span data-ttu-id="216c9-128">**Msisourcelistclearmediadisk**</span><span class="sxs-lookup"><span data-stu-id="216c9-128">**MsiSourceListClearMediaDisk**</span></span>](/windows/desktop/api/Msi/nf-msi-msisourcelistclearmediadiska)
</dt> <dt>

[<span data-ttu-id="216c9-129">Wird in Windows Installer 2,0 und früher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="216c9-129">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




