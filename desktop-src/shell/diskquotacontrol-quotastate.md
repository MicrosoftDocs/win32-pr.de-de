---
description: Legt den Status der Datenträger Kontingente des Volumes fest oder ruft ihn ab.
title: Diskquotacontrol. quotastate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 460decc1068642ae797723b31f7350082f591d8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485523"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="73b52-103">Diskquotacontrol. quotastate (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="73b52-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="73b52-104">Legt den Status der Datenträger Kontingente des Volumes fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="73b52-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="73b52-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="73b52-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73b52-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73b52-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="73b52-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="73b52-107">Property value</span></span>

<span data-ttu-id="73b52-108">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="73b52-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="73b52-109">State</span><span class="sxs-lookup"><span data-stu-id="73b52-109">State</span></span>          | <span data-ttu-id="73b52-110">Wert</span><span class="sxs-lookup"><span data-stu-id="73b52-110">Value</span></span> | <span data-ttu-id="73b52-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73b52-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="73b52-112">dqstatedeaktivieren</span><span class="sxs-lookup"><span data-stu-id="73b52-112">dqStateDisable</span></span> | <span data-ttu-id="73b52-113">0</span><span class="sxs-lookup"><span data-stu-id="73b52-113">0</span></span>     | <span data-ttu-id="73b52-114">Datenträger Kontingente sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="73b52-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="73b52-115">dqstatetrack</span><span class="sxs-lookup"><span data-stu-id="73b52-115">dqStateTrack</span></span>   | <span data-ttu-id="73b52-116">1</span><span class="sxs-lookup"><span data-stu-id="73b52-116">1</span></span>     | <span data-ttu-id="73b52-117">Datenträger Kontingente sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="73b52-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="73b52-118">dqstateerzwingen</span><span class="sxs-lookup"><span data-stu-id="73b52-118">dqStateEnforce</span></span> | <span data-ttu-id="73b52-119">2</span><span class="sxs-lookup"><span data-stu-id="73b52-119">2</span></span>     | <span data-ttu-id="73b52-120">Kontingent Limit erzwingen.</span><span class="sxs-lookup"><span data-stu-id="73b52-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="73b52-121">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="73b52-121">Requirements</span></span>



| <span data-ttu-id="73b52-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="73b52-122">Requirement</span></span> | <span data-ttu-id="73b52-123">Wert</span><span class="sxs-lookup"><span data-stu-id="73b52-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73b52-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="73b52-124">Minimum supported client</span></span><br/> | <span data-ttu-id="73b52-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73b52-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="73b52-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="73b52-126">Minimum supported server</span></span><br/> | <span data-ttu-id="73b52-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="73b52-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="73b52-128">DLL</span><span class="sxs-lookup"><span data-stu-id="73b52-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73b52-129"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="73b52-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73b52-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="73b52-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73b52-131">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="73b52-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




