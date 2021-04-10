---
title: STOWED_EXCEPTION_INFORMATION_HEADER Struktur
description: Enthält Informationen, die die übergeordnete Struktur identifizieren.
ms.assetid: 0BC1FDAA-C750-4DEC-AF6A-B2CB3240B67C
keywords:
- STOWED_EXCEPTION_INFORMATION_HEADER Struktur Windows-Fehlerberichterstattung
- PSTOWED_EXCEPTION_INFORMATION_HEADER Struktur Zeiger Windows-Fehlerberichterstattung
topic_type:
- apiref
api_name:
- STOWED_EXCEPTION_INFORMATION_HEADER
api_location:
- none
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 101bb1fb1555c829622a42c17fdfb01488c57636
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040916"
---
# <a name="stowed_exception_information_header-structure"></a><span data-ttu-id="49cf6-105">Header Struktur der verstauten \_ Ausnahme \_ Informationen \_</span><span class="sxs-lookup"><span data-stu-id="49cf6-105">STOWED\_EXCEPTION\_INFORMATION\_HEADER structure</span></span>

<span data-ttu-id="49cf6-106">Enthält Informationen, die die übergeordnete Struktur identifizieren.</span><span class="sxs-lookup"><span data-stu-id="49cf6-106">Contains info that identifies the parent structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="49cf6-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="49cf6-107">Syntax</span></span>


```C++
typedef struct _STOWED_EXCEPTION_INFORMATION_HEADER {
  ULONG Size;
  ULONG Signature;
} STOWED_EXCEPTION_INFORMATION_HEADER, *PSTOWED_EXCEPTION_INFORMATION_HEADER;
```



## <a name="members"></a><span data-ttu-id="49cf6-108">Member</span><span class="sxs-lookup"><span data-stu-id="49cf6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="49cf6-109">**Größe**</span><span class="sxs-lookup"><span data-stu-id="49cf6-109">**Size**</span></span>
</dt> <dd>

<span data-ttu-id="49cf6-110">Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49cf6-110">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="49cf6-111">Größe der übergeordneten Struktur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="49cf6-111">Size, in bytes, of the parent structure.</span></span>

</dd> <dt>

<span data-ttu-id="49cf6-112">**Signature**</span><span class="sxs-lookup"><span data-stu-id="49cf6-112">**Signature**</span></span>
</dt> <dd>

<span data-ttu-id="49cf6-113">Typ: **[ **ulong**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="49cf6-113">Type: **[**ULONG**](/windows/desktop/WinProg/windows-data-types)**</span></span>

</dd> <dd>

<span data-ttu-id="49cf6-114">Ein 32-Bit-Wert, der die Signatur der übergeordneten Struktur angibt.</span><span class="sxs-lookup"><span data-stu-id="49cf6-114">A 32-bit value that specifies the signature of the parent structure.</span></span>



| <span data-ttu-id="49cf6-115">Wert</span><span class="sxs-lookup"><span data-stu-id="49cf6-115">Value</span></span>                                                                                                                                                                                                                                                                                                            | <span data-ttu-id="49cf6-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="49cf6-116">Meaning</span></span>                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="STOWED_EXCEPTION_INFORMATION_V1_SIGNATURE"></span><span id="stowed_exception_information_v1_signature"></span><dl> <span data-ttu-id="49cf6-117"><dt>**Verstauaut \_ Ausnahme \_ Informationen \_ v1- \_ Signatur**</dt> <dt>"SE01"</dt></span><span class="sxs-lookup"><span data-stu-id="49cf6-117"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V1\_SIGNATURE**</dt> <dt>'SE01'</dt></span></span> </dl> | <span data-ttu-id="49cf6-118">Dieser Wert gibt an, dass das übergeordnete Element eine **verstaute \_ Ausnahme \_ Information \_ v1** -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="49cf6-118">This value indicates that the parent is a **STOWED\_EXCEPTION\_INFORMATION\_V1** structure.</span></span><br/>                                        |
| <span id="STOWED_EXCEPTION_INFORMATION_V2_SIGNATURE"></span><span id="stowed_exception_information_v2_signature"></span><dl> <span data-ttu-id="49cf6-119"><dt>**Verstauaut \_ Ausnahme \_ Informationen \_ v2- \_ Signatur**</dt> <dt>"SE02"</dt></span><span class="sxs-lookup"><span data-stu-id="49cf6-119"><dt>**STOWED\_EXCEPTION\_INFORMATION\_V2\_SIGNATURE**</dt> <dt>'SE02'</dt></span></span> </dl> | <span data-ttu-id="49cf6-120">Dieser Wert gibt an, dass das übergeordnete Element eine [**verstaute \_ Ausnahme \_ Information \_ v2**](stowed-exception-information-v2.md) -Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="49cf6-120">This value indicates that the parent is a [**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) structure.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49cf6-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49cf6-121">Remarks</span></span>

<span data-ttu-id="49cf6-122">[**Verstauaut \_ Ausnahme \_ Informationen \_ v2**](stowed-exception-information-v2.md) -und **gestaut- \_ Ausnahme \_ Informations \_ Header** sind zurzeit nicht in einem Header definiert, der öffentlich verfügbar ist, sodass Sie Sie im Quellcode definieren müssen, bevor Sie Sie verwenden.</span><span class="sxs-lookup"><span data-stu-id="49cf6-122">[**STOWED\_EXCEPTION\_INFORMATION\_V2**](stowed-exception-information-v2.md) and **STOWED\_EXCEPTION\_INFORMATION\_HEADER** currently aren't defined in a header that is publicly available so you need to define them in your source code before you use them.</span></span>

<span data-ttu-id="49cf6-123">Die Struktur der **verstauten \_ Ausnahme \_ Informationen \_ v1** ist mit dieser Struktur identisch, außer Sie enthält nicht die Member " **netstedexceptiontype** " und " **netstedexception** ".</span><span class="sxs-lookup"><span data-stu-id="49cf6-123">The **STOWED\_EXCEPTION\_INFORMATION\_V1** structure is identical to this structure except it doesn't contain the **NestedExceptionType** and **NestedException** members.</span></span>

## <a name="requirements"></a><span data-ttu-id="49cf6-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49cf6-124">Requirements</span></span>



| <span data-ttu-id="49cf6-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49cf6-125">Requirement</span></span> | <span data-ttu-id="49cf6-126">Wert</span><span class="sxs-lookup"><span data-stu-id="49cf6-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="49cf6-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49cf6-127">Minimum supported client</span></span><br/> | <span data-ttu-id="49cf6-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49cf6-128">Windows 8 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="49cf6-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49cf6-129">Minimum supported server</span></span><br/> | <span data-ttu-id="49cf6-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49cf6-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="49cf6-131">Header</span><span class="sxs-lookup"><span data-stu-id="49cf6-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="49cf6-132"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="49cf6-132"><dt>None</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49cf6-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49cf6-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49cf6-134">**Informationen zu verstauten \_ Ausnahmen \_ \_ v2**</span><span class="sxs-lookup"><span data-stu-id="49cf6-134">**STOWED\_EXCEPTION\_INFORMATION\_V2**</span></span>](stowed-exception-information-v2.md)
</dt> </dl>

 

