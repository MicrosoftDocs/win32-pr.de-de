---
description: 'LockMedia-Methode der Msvm_DisketteDrive-Klasse: Sperrt oder gibt die Medien frei.'
ms.assetid: 90f7e06c-92d0-4742-a74d-68ae6bfc00bf
title: LockMedia-Methode der Msvm_DisketteDrive-Klasse
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
ms.openlocfilehash: 5f5f87354aa7c39534e8b32c8985c5d18b55caa9
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111976"
---
# <a name="lockmedia-method-of-the-msvm_diskettedrive-class"></a><span data-ttu-id="8df80-103">LockMedia-Methode der Msvm \_ DisketteDrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="8df80-103">LockMedia method of the Msvm\_DisketteDrive class</span></span>

<span data-ttu-id="8df80-104">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="8df80-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="8df80-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8df80-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="8df80-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8df80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8df80-107">*Sperren* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="8df80-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8df80-108">**TRUE,** um das Medium zu sperren; **FALSE,** um die Medien freizugeben.</span><span class="sxs-lookup"><span data-stu-id="8df80-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8df80-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8df80-109">Return value</span></span>

<span data-ttu-id="8df80-110">Gibt bei Erfolg den Wert 0 zurück. andernfalls wird einer der folgenden Werte zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="8df80-110">Returns a 0 on success; otherwise, returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="8df80-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="8df80-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="8df80-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="8df80-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="8df80-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df80-113">Requirements</span></span>



| <span data-ttu-id="8df80-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8df80-114">Requirement</span></span> | <span data-ttu-id="8df80-115">Wert</span><span class="sxs-lookup"><span data-stu-id="8df80-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8df80-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8df80-116">Minimum supported client</span></span><br/> | <span data-ttu-id="8df80-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="8df80-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="8df80-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8df80-118">Minimum supported server</span></span><br/> | <span data-ttu-id="8df80-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="8df80-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="8df80-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="8df80-120">Namespace</span></span><br/>                | <span data-ttu-id="8df80-121">\\Root-Virtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="8df80-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="8df80-122">MOF</span><span class="sxs-lookup"><span data-stu-id="8df80-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8df80-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="8df80-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="8df80-124">DLL</span><span class="sxs-lookup"><span data-stu-id="8df80-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8df80-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="8df80-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="8df80-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="8df80-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8df80-127">**Msvm \_ DisketteDrive**</span><span class="sxs-lookup"><span data-stu-id="8df80-127">**Msvm\_DisketteDrive**</span></span>](msvm-diskettedrive.md)
</dt> </dl>

 

 




