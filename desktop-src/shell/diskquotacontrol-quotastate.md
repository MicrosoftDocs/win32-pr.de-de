---
description: Legt den Zustand der Datenträgerkontingente des Volumes fest oder ruft den Status ab.
title: DiskQuotaControl.QuotaState-Eigenschaft
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
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843191"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="7f066-103">DiskQuotaControl.QuotaState-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="7f066-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="7f066-104">Legt den Zustand der Datenträgerkontingente des Volumes fest oder ruft den Status ab.</span><span class="sxs-lookup"><span data-stu-id="7f066-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="7f066-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7f066-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f066-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f066-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="7f066-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="7f066-107">Property value</span></span>

<span data-ttu-id="7f066-108">Diese Eigenschaft kann auf einen der folgenden Werte festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7f066-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="7f066-109">State</span><span class="sxs-lookup"><span data-stu-id="7f066-109">State</span></span>          | <span data-ttu-id="7f066-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7f066-110">Value</span></span> | <span data-ttu-id="7f066-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7f066-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="7f066-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="7f066-112">dqStateDisable</span></span> | <span data-ttu-id="7f066-113">0</span><span class="sxs-lookup"><span data-stu-id="7f066-113">0</span></span>     | <span data-ttu-id="7f066-114">Datenträgerkontingente sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f066-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="7f066-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="7f066-115">dqStateTrack</span></span>   | <span data-ttu-id="7f066-116">1</span><span class="sxs-lookup"><span data-stu-id="7f066-116">1</span></span>     | <span data-ttu-id="7f066-117">Datenträgerkontingente sind deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="7f066-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="7f066-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="7f066-118">dqStateEnforce</span></span> | <span data-ttu-id="7f066-119">2</span><span class="sxs-lookup"><span data-stu-id="7f066-119">2</span></span>     | <span data-ttu-id="7f066-120">Erzwingen Sie das Kontingentlimit.</span><span class="sxs-lookup"><span data-stu-id="7f066-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="7f066-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f066-121">Requirements</span></span>



| <span data-ttu-id="7f066-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f066-122">Requirement</span></span> | <span data-ttu-id="7f066-123">Wert</span><span class="sxs-lookup"><span data-stu-id="7f066-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f066-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f066-124">Minimum supported client</span></span><br/> | <span data-ttu-id="7f066-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f066-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7f066-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f066-126">Minimum supported server</span></span><br/> | <span data-ttu-id="7f066-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7f066-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7f066-128">DLL</span><span class="sxs-lookup"><span data-stu-id="7f066-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f066-129"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7f066-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f066-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f066-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f066-131">**DiskQuotaControl-Objekt**</span><span class="sxs-lookup"><span data-stu-id="7f066-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




