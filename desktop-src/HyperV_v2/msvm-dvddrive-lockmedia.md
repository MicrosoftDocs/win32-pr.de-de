---
description: LockMedia-Methode der Msvm_DVDDrive - Sperrt oder gibt die Medien frei.
ms.assetid: 924bc20a-901b-4618-be49-eaacf80c9465
title: LockMedia-Methode der Msvm_DVDDrive-Klasse
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
ms.openlocfilehash: e00780fbeeeec60563b31008c8e5979a09f9d173
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119148"
---
# <a name="lockmedia-method-of-the-msvm_dvddrive-class"></a><span data-ttu-id="e8b17-103">LockMedia-Methode der Msvm \_ DVDDrive-Klasse</span><span class="sxs-lookup"><span data-stu-id="e8b17-103">LockMedia method of the Msvm\_DVDDrive class</span></span>

<span data-ttu-id="e8b17-104">Sperrt oder gibt die Medien frei.</span><span class="sxs-lookup"><span data-stu-id="e8b17-104">Locks or releases the media.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8b17-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8b17-105">Syntax</span></span>


```mof
uint32 LockMedia(
  [in] boolean Lock
);
```



## <a name="parameters"></a><span data-ttu-id="e8b17-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e8b17-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e8b17-107">*Sperre* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="e8b17-107">*Lock* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e8b17-108">**TRUE,** um das Medium zu sperren; **FALSE,** um die Medien frei zu geben.</span><span class="sxs-lookup"><span data-stu-id="e8b17-108">**true** to lock the media; **false** to release the media.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e8b17-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e8b17-109">Return value</span></span>

<span data-ttu-id="e8b17-110">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="e8b17-110">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="e8b17-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="e8b17-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="e8b17-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="e8b17-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="e8b17-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b17-113">Requirements</span></span>



| <span data-ttu-id="e8b17-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8b17-114">Requirement</span></span> | <span data-ttu-id="e8b17-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e8b17-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8b17-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8b17-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e8b17-117">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="e8b17-117">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="e8b17-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8b17-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e8b17-119">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="e8b17-119">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="e8b17-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e8b17-120">Namespace</span></span><br/>                | <span data-ttu-id="e8b17-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="e8b17-121">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e8b17-122">MOF</span><span class="sxs-lookup"><span data-stu-id="e8b17-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e8b17-123"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="e8b17-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e8b17-124">DLL</span><span class="sxs-lookup"><span data-stu-id="e8b17-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8b17-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e8b17-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e8b17-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="e8b17-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8b17-127">**Msvm \_ DVDDrive**</span><span class="sxs-lookup"><span data-stu-id="e8b17-127">**Msvm\_DVDDrive**</span></span>](msvm-dvddrive.md)
</dt> </dl>

 

 




