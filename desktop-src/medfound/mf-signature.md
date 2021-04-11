---
description: Enthält eine GRL-Signatur (Global Sperrlist).
ms.assetid: 388a901c-6202-41cf-9c3d-f29d8ccca76b
title: MF_SIGNATURE Struktur
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_SIGNATURE
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4827fea8e4259609cbb54f2b58a3d1c88ad6c23e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218117"
---
# <a name="mf_signature-structure"></a><span data-ttu-id="62e1a-103">MF- \_ Signatur Struktur</span><span class="sxs-lookup"><span data-stu-id="62e1a-103">MF\_SIGNATURE structure</span></span>

<span data-ttu-id="62e1a-104">Enthält eine GRL-Signatur (Global Sperrlist).</span><span class="sxs-lookup"><span data-stu-id="62e1a-104">Contains a global revocation list (GRL) signature.</span></span>

## <a name="syntax"></a><span data-ttu-id="62e1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62e1a-105">Syntax</span></span>


```C++
typedef struct _MF_SIGNATURE {
  DWORD dwSignVer;
  DWORD cbSign;
  BYTE  rgSign[1];
} MF_SIGNATURE;
```



## <a name="members"></a><span data-ttu-id="62e1a-106">Member</span><span class="sxs-lookup"><span data-stu-id="62e1a-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="62e1a-107">**dwsignver**</span><span class="sxs-lookup"><span data-stu-id="62e1a-107">**dwSignVer**</span></span>
</dt> <dd>

<span data-ttu-id="62e1a-108">Die Signatur Versionsnummer.</span><span class="sxs-lookup"><span data-stu-id="62e1a-108">The signature version number.</span></span>

</dd> <dt>

<span data-ttu-id="62e1a-109">**cbsign**</span><span class="sxs-lookup"><span data-stu-id="62e1a-109">**cbSign**</span></span>
</dt> <dd>

<span data-ttu-id="62e1a-110">Die Größe der Signatur in Bytes.</span><span class="sxs-lookup"><span data-stu-id="62e1a-110">The size of the signature in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="62e1a-111">**rgsign**</span><span class="sxs-lookup"><span data-stu-id="62e1a-111">**rgSign**</span></span>
</dt> <dd>

<span data-ttu-id="62e1a-112">Ein Bytearray der Größe **cbsign** , das die Signatur enthält.</span><span class="sxs-lookup"><span data-stu-id="62e1a-112">A byte array of size **cbSign** that contains the signature.</span></span> <span data-ttu-id="62e1a-113">Die tatsächliche Array Größe ist größer als die in der Struktur Deklaration angegebene Größe.</span><span class="sxs-lookup"><span data-stu-id="62e1a-113">The actual array size is larger than the size given in the structure declaration.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62e1a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62e1a-114">Remarks</span></span>

<span data-ttu-id="62e1a-115">Diese Struktur ist nicht in einem SDK-Header deklariert.</span><span class="sxs-lookup"><span data-stu-id="62e1a-115">This structure is not declared in an SDK header.</span></span> <span data-ttu-id="62e1a-116">Um diese Struktur zu verwenden, fügen Sie die hier gezeigte Deklaration dem Quellcode hinzu.</span><span class="sxs-lookup"><span data-stu-id="62e1a-116">To use this structure, add the declaration shown here to your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="62e1a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62e1a-117">Requirements</span></span>



| <span data-ttu-id="62e1a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62e1a-118">Requirement</span></span> | <span data-ttu-id="62e1a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="62e1a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="62e1a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62e1a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="62e1a-121">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62e1a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="62e1a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62e1a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="62e1a-123">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62e1a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62e1a-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62e1a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62e1a-125">OPM-Zertifikat Sperrung</span><span class="sxs-lookup"><span data-stu-id="62e1a-125">OPM Certificate Revocation</span></span>](opm-certificate-revocation.md)
</dt> <dt>

[<span data-ttu-id="62e1a-126">OPM-Strukturen</span><span class="sxs-lookup"><span data-stu-id="62e1a-126">OPM Structures</span></span>](opm-structures.md)
</dt> </dl>

 

 




