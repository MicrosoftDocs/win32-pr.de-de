---
description: Sperrt oder gibt die Medien frei.
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: Lockmedia-Methode der Msvm_DisketteDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DisketteDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f9bce4e9e46d76c3426271af16c28026c242fa9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "103869532"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="e5761-103">Lockmedia-Methode der MSVM \_ diskettedrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="e5761-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="e5761-104">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="e5761-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5761-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5761-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="e5761-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5761-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5761-107">*Sperre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e5761-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5761-108">" **true** ", um die Medien zu sperren. **false** zum Freigeben der Medien.</span><span class="sxs-lookup"><span data-stu-id="e5761-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5761-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e5761-109">Return value</span></span>

<span data-ttu-id="e5761-110">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird einer der folgenden Werte zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="e5761-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e5761-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e5761-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e5761-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e5761-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e5761-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e5761-113">Requirements</span></span>



| <span data-ttu-id="e5761-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e5761-114">Requirement</span></span> | <span data-ttu-id="e5761-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e5761-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e5761-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e5761-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e5761-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e5761-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e5761-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e5761-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e5761-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e5761-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e5761-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5761-120">Namespace</span></span><br/>                | <span data-ttu-id="e5761-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e5761-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e5761-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e5761-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e5761-123"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e5761-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e5761-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e5761-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e5761-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e5761-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e5761-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5761-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5761-127">**MSVM \_ diskettedrive**</span><span class="sxs-lookup"><span data-stu-id="e5761-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




