---
title: BG_FILE_RANGE-Struktur (deliveryoptimization. h)
description: Die BG_FILE_RANGE-Struktur identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.
ms.assetid: 58993C51-E42E-4E44-9E8A-15E982B25413
keywords:
- BG_FILE_RANGE Struktur
topic_type:
- apiref
api_name:
- BG_FILE_RANGE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cedabfb066a5905adb2ed8eac9996fd77c0e12be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392129"
---
# <a name="bg_file_range-structure"></a><span data-ttu-id="5c2df-104">BG_FILE_RANGE Struktur</span><span class="sxs-lookup"><span data-stu-id="5c2df-104">BG_FILE_RANGE structure</span></span>

<span data-ttu-id="5c2df-105">Die **BG_FILE_RANGE** -Struktur identifiziert einen Bereich von Bytes, der aus einer Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c2df-105">The **BG_FILE_RANGE** structure identifies a range of bytes to download from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c2df-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c2df-106">Syntax</span></span>


```C++
typedef struct {
  UINT64 InitialOffset;
  UINT64 Length;
} BG_FILE_RANGE;
```



## <a name="members"></a><span data-ttu-id="5c2df-107">Member</span><span class="sxs-lookup"><span data-stu-id="5c2df-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c2df-108">**Initialoffset**</span><span class="sxs-lookup"><span data-stu-id="5c2df-108">**InitialOffset**</span></span>
</dt> <dd>

<span data-ttu-id="5c2df-109">NULL basierter Offset am Anfang des Bereichs von Bytes, der aus einer Datei heruntergeladen werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c2df-109">Zero-based offset to the beginning of the range of bytes to download from a file.</span></span>

</dd> <dt>

<span data-ttu-id="5c2df-110">**Länge**</span><span class="sxs-lookup"><span data-stu-id="5c2df-110">**Length**</span></span>
</dt> <dd>

<span data-ttu-id="5c2df-111">Die Länge des Bereichs in Bytes.</span><span class="sxs-lookup"><span data-stu-id="5c2df-111">The length of the range, in bytes.</span></span> <span data-ttu-id="5c2df-112">Geben Sie keine Byte Länge von 0 (null) an.</span><span class="sxs-lookup"><span data-stu-id="5c2df-112">Do not specify a zero byte length.</span></span> <span data-ttu-id="5c2df-113">Um anzugeben, dass der Bereich bis zum Ende der Datei reicht, geben Sie **BG_LENGTH_TO_EOF** an.</span><span class="sxs-lookup"><span data-stu-id="5c2df-113">To indicate that the range extends to the end of the file, specify **BG_LENGTH_TO_EOF**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="5c2df-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5c2df-114">Remarks</span></span>

<span data-ttu-id="5c2df-115">Der Bereich muss in der Datei vorhanden sein, oder es wird ein **DO_E_INVALID_RANGE** Fehler generiert.</span><span class="sxs-lookup"><span data-stu-id="5c2df-115">The range must exist in the file or DO generates an **DO_E_INVALID_RANGE** error.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c2df-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5c2df-116">Requirements</span></span>



| <span data-ttu-id="5c2df-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5c2df-117">Requirement</span></span> | <span data-ttu-id="5c2df-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5c2df-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c2df-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5c2df-119">Minimum supported client</span></span><br/> | <span data-ttu-id="5c2df-120">Windows 10, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c2df-120">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="5c2df-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5c2df-121">Minimum supported server</span></span><br/> | <span data-ttu-id="5c2df-122">Windows Server, Version 1709, \[ nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5c2df-122">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5c2df-123">Header</span><span class="sxs-lookup"><span data-stu-id="5c2df-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c2df-124"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c2df-124"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c2df-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c2df-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c2df-126">**IBackgroundCopyFile2:: getfileranges**</span><span class="sxs-lookup"><span data-stu-id="5c2df-126">**IBackgroundCopyFile2::GetFileRanges**</span></span>](ibackgroundcopyfile2-getfileranges-method.md)
</dt> </dl>

 

 





