---
description: Sperrt und entsperrt die Medien in einem Remote fähigen Zugriffsgerät.
ms.assetid: 357ee552-82d0-4201-bcc2-0acf208e16a0
title: Lockmedia-Methode der CIM_MediaAccessDevice-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MediaAccessDevice.LockMedia
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 12c4aa6c6ba9e57a2ab88e58624b246fb98065f3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104050671"
---
# <a name="lockmedia-method-of-the-cim_mediaaccessdevice-class"></a><span data-ttu-id="5ef76-103">Lockmedia-Methode der CIM \_ mediaaccessdevice-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ef76-103">LockMedia method of the CIM\_MediaAccessDevice class</span></span>

<span data-ttu-id="5ef76-104">Sperrt und entsperrt die Medien in einem Remote fähigen Zugriffsgerät.</span><span class="sxs-lookup"><span data-stu-id="5ef76-104">Locks and unlocks the media in a removeable access device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ef76-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ef76-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="5ef76-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ef76-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ef76-107">*Sperre* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ef76-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ef76-108">Wenn der Wert **true** ist, wird das Medium gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5ef76-108">If **TRUE**, locks the media.</span></span> <span data-ttu-id="5ef76-109">Wenn **false**, wird das Medium von freigegeben.</span><span class="sxs-lookup"><span data-stu-id="5ef76-109">If **FALSE**, releases the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ef76-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ef76-110">Return value</span></span>

<span data-ttu-id="5ef76-111">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5ef76-111">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5ef76-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ef76-112">Requirements</span></span>



| <span data-ttu-id="5ef76-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ef76-113">Requirement</span></span> | <span data-ttu-id="5ef76-114">Wert</span><span class="sxs-lookup"><span data-stu-id="5ef76-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ef76-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ef76-115">Minimum supported client</span></span><br/> | <span data-ttu-id="5ef76-116">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="5ef76-116">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="5ef76-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ef76-117">Minimum supported server</span></span><br/> | <span data-ttu-id="5ef76-118">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="5ef76-118">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="5ef76-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ef76-119">Namespace</span></span><br/>                | <span data-ttu-id="5ef76-120">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="5ef76-120">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="5ef76-121">MOF</span><span class="sxs-lookup"><span data-stu-id="5ef76-121">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ef76-122"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ef76-122"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ef76-123">DLL</span><span class="sxs-lookup"><span data-stu-id="5ef76-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ef76-124"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="5ef76-124"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="5ef76-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ef76-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ef76-126">**CIM \_ mediaaccessdevice**</span><span class="sxs-lookup"><span data-stu-id="5ef76-126">**CIM\_MediaAccessDevice**</span></span>](cim-mediaaccessdevice.md)
</dt> </dl>

 

 




