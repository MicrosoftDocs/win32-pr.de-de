---
description: Sperrt oder gibt die Medien frei.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: Lockmedia-Methode der Msvm_DVDDrive-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_DVDDrive.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 650a868d8e25e2ccc47271e49634827fe7d3d967
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104132193"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="05a56-103">Lockmedia-Methode der MSVM- \_ dvddrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="05a56-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="05a56-104">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="05a56-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="05a56-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="05a56-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="05a56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="05a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="05a56-107">*Sperre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="05a56-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="05a56-108">" **true** ", um die Medien zu sperren. **false** zum Freigeben der Medien.</span><span class="sxs-lookup"><span data-stu-id="05a56-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="05a56-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="05a56-109">Return value</span></span>

<span data-ttu-id="05a56-110">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="05a56-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="05a56-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="05a56-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="05a56-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="05a56-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="05a56-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05a56-113">Requirements</span></span>



| <span data-ttu-id="05a56-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05a56-114">Requirement</span></span> | <span data-ttu-id="05a56-115">Wert</span><span class="sxs-lookup"><span data-stu-id="05a56-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="05a56-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="05a56-116">Minimum supported client</span></span><br/> | <span data-ttu-id="05a56-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="05a56-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="05a56-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="05a56-118">Minimum supported server</span></span><br/> | <span data-ttu-id="05a56-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="05a56-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="05a56-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="05a56-120">Namespace</span></span><br/>                | <span data-ttu-id="05a56-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="05a56-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="05a56-122">MOF</span><span class="sxs-lookup"><span data-stu-id="05a56-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="05a56-123"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="05a56-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="05a56-124">DLL</span><span class="sxs-lookup"><span data-stu-id="05a56-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05a56-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="05a56-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="05a56-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05a56-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05a56-127">**MSVM \_ dvddrive**</span><span class="sxs-lookup"><span data-stu-id="05a56-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




