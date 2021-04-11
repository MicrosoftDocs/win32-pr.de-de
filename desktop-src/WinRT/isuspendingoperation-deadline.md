---
description: Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.
ms.assetid: A90347F3-75CB-4EEB-930D-30882F43D192
title: Isuspendingoperation::D eadline-Eigenschaft (Windows. applicationmodel. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISuspendingOperation.Deadline
- ISuspendingOperation.get_Deadline
- ISuspendingOperation.put_Deadline
api_type:
- COM
api_location:
- Windows.ApplicationModel.h
ms.openlocfilehash: 305610108b7a138693ccdce97e35ddbe90451806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958935"
---
# <a name="isuspendingoperationdeadline-property"></a><span data-ttu-id="72e25-103">Isuspendingoperation::D eadline-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="72e25-103">ISuspendingOperation::Deadline property</span></span>

<span data-ttu-id="72e25-104">Ruft die verbleibende Zeit ab, bevor eine verzögerte App angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="72e25-104">Gets the time remaining before a delayed app suspending operation continues.</span></span>

<span data-ttu-id="72e25-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="72e25-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e25-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="72e25-106">Syntax</span></span>


```C++
HRESULT put_Deadline();

HRESULT get_Deadline(
  [out, retval] DateTime *value
);
```



## <a name="property-value"></a><span data-ttu-id="72e25-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="72e25-107">Property value</span></span>

<span data-ttu-id="72e25-108">Die verbleibende Zeit bis zum Anhalten eines verzögerten App-Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="72e25-108">The time remaining before a delayed app suspending operation continues.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e25-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72e25-109">Requirements</span></span>



| <span data-ttu-id="72e25-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72e25-110">Requirement</span></span> | <span data-ttu-id="72e25-111">Wert</span><span class="sxs-lookup"><span data-stu-id="72e25-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72e25-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72e25-112">Minimum supported client</span></span><br/> | <span data-ttu-id="72e25-113">Windows 8</span><span class="sxs-lookup"><span data-stu-id="72e25-113">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="72e25-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72e25-114">Minimum supported server</span></span><br/> | <span data-ttu-id="72e25-115">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="72e25-115">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="72e25-116">Header</span><span class="sxs-lookup"><span data-stu-id="72e25-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="72e25-117"><dt>Windows. applicationmodel. h</dt></span><span class="sxs-lookup"><span data-stu-id="72e25-117"><dt>Windows.ApplicationModel.h</dt></span></span> </dl>   |
| <span data-ttu-id="72e25-118">IDL</span><span class="sxs-lookup"><span data-stu-id="72e25-118">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72e25-119"><dt>Windows. applicationmodel. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72e25-119"><dt>Windows.ApplicationModel.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72e25-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72e25-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72e25-121">**Isuspendingoperation**</span><span class="sxs-lookup"><span data-stu-id="72e25-121">**ISuspendingOperation**</span></span>](isuspendingoperation.md)
</dt> </dl>

 

 




