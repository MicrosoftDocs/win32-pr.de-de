---
title: BITS_FILE_PROPERTY_VALUE-Struktur (deliveryoptimization. h)
description: Die BITS_FILE_PROPERTY_VALUE Union stellt den Eigenschafts Wert der do-Datei auf Grundlage eines Werts aus der BITS_FILE_PROPERTY_ID Enumeration bereit.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- BITS_FILE_PROPERTY_VALUE Struktur
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 639ea0523c5b92d9764671cb573497223ef968fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337493"
---
# <a name="bits_file_property_value-structure"></a><span data-ttu-id="1b2d9-104">BITS_FILE_PROPERTY_VALUE Struktur</span><span class="sxs-lookup"><span data-stu-id="1b2d9-104">BITS_FILE_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="1b2d9-105">Die **BITS_FILE_PROPERTY_VALUE** Union stellt den Eigenschafts Wert der do-Datei auf Grundlage eines Werts aus der [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) Enumeration bereit.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-105">The **BITS_FILE_PROPERTY_VALUE** union provides the property value of the DO file based on a value from the [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b2d9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b2d9-106">Syntax</span></span>


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="1b2d9-107">Member</span><span class="sxs-lookup"><span data-stu-id="1b2d9-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="1b2d9-108">**String**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-108">**String**</span></span>
</dt> <dd>

<span data-ttu-id="1b2d9-109">Dieser Wert wird verwendet, wenn der Enumerationswert **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS** der Eigenschaft ID verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b2d9-109">This value is used when using the property ID enum value **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1b2d9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b2d9-110">Requirements</span></span>



| <span data-ttu-id="1b2d9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b2d9-111">Requirement</span></span> | <span data-ttu-id="1b2d9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="1b2d9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b2d9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b2d9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="1b2d9-114">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b2d9-114">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="1b2d9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b2d9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="1b2d9-116">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b2d9-116">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="1b2d9-117">Header</span><span class="sxs-lookup"><span data-stu-id="1b2d9-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="1b2d9-118"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="1b2d9-118"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b2d9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b2d9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b2d9-120">**BITS_FILE_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-120">**BITS_FILE_PROPERTY_ID**</span></span>](bits-file-property-id-.md)
</dt> <dt>

[<span data-ttu-id="1b2d9-121">**IBackgroundCopyFile5. GetProperty**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-121">**IBackgroundCopyFile5.GetProperty**</span></span>](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[<span data-ttu-id="1b2d9-122">**IBackgroundCopyFile5. SetProperty**</span><span class="sxs-lookup"><span data-stu-id="1b2d9-122">**IBackgroundCopyFile5.SetProperty**</span></span>](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





