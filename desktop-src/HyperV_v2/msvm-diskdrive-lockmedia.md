---
description: Sperrt oder entsperrt das Medium.
ms.assetid: 805efb2d-71a7-4c74-821f-942644928ff9
title: Lockmedia-Methode der Msvm_DiskDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DiskDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7ddc082ca6ceb7141eaa42bdfddf7a97897a9240
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106361127"
---
# <a name="lockmedia-method-of-the-msvm_diskdrive-class"></a><span data-ttu-id="69d4e-103">Lockmedia-Methode der MSVM \_ diskdrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="69d4e-103">LockMedia method of the Msvm\_DiskDrive class</span></span>

<span data-ttu-id="69d4e-104">Sperrt oder entsperrt das Medium.</span><span class="sxs-lookup"><span data-stu-id="69d4e-104">Locks or unlocks the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="69d4e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="69d4e-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="69d4e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="69d4e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69d4e-107">*Sperre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="69d4e-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69d4e-108">" **true** ", um die Medien zu sperren. **false** zum Freigeben der Medien.</span><span class="sxs-lookup"><span data-stu-id="69d4e-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69d4e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="69d4e-109">Return value</span></span>

<span data-ttu-id="69d4e-110">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="69d4e-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="69d4e-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="69d4e-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="69d4e-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="69d4e-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="69d4e-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="69d4e-113">Requirements</span></span>



| <span data-ttu-id="69d4e-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="69d4e-114">Requirement</span></span> | <span data-ttu-id="69d4e-115">Wert</span><span class="sxs-lookup"><span data-stu-id="69d4e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="69d4e-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="69d4e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="69d4e-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="69d4e-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="69d4e-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="69d4e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="69d4e-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="69d4e-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="69d4e-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="69d4e-120">Namespace</span></span><br/>                | <span data-ttu-id="69d4e-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="69d4e-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="69d4e-122">MOF</span><span class="sxs-lookup"><span data-stu-id="69d4e-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69d4e-123"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="69d4e-124">DLL</span><span class="sxs-lookup"><span data-stu-id="69d4e-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69d4e-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="69d4e-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="69d4e-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69d4e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69d4e-127">**MSVM \_ diskdrive**</span><span class="sxs-lookup"><span data-stu-id="69d4e-127">**Msvm\_DiskDrive**</span></span>](msvm-diskdrive.md)
</dt> </dl>

 

 




