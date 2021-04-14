---
title: MP_HASH_TYPE-Enumeration (mpclient. h)
description: Mögliche Hashtypen.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE-Enumerationsfunktionen der Legacy-Windows-Umgebung
- PMP_HASH_TYPE enumerationszeiger Legacy-Windows-Umgebungs Features
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478747"
---
# <a name="mp_hash_type-enumeration"></a><span data-ttu-id="848e0-105">MP \_ - \_ Hashtyp-Enumeration</span><span class="sxs-lookup"><span data-stu-id="848e0-105">MP\_HASH\_TYPE enumeration</span></span>

<span data-ttu-id="848e0-106">Mögliche Hashtypen.</span><span class="sxs-lookup"><span data-stu-id="848e0-106">Possible hash types.</span></span>

## <a name="syntax"></a><span data-ttu-id="848e0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="848e0-107">Syntax</span></span>


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="848e0-108">Konstanten</span><span class="sxs-lookup"><span data-stu-id="848e0-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="848e0-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP \_ - \_ Hashtyp " \_ None"**</span><span class="sxs-lookup"><span data-stu-id="848e0-109"><span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**MP\_HASH\_TYPE\_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="848e0-110">Kein Hash.</span><span class="sxs-lookup"><span data-stu-id="848e0-110">No hash.</span></span>

</dd> <dt>

<span data-ttu-id="848e0-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP \_ - \_ Hashtyp \_ CRC32**</span><span class="sxs-lookup"><span data-stu-id="848e0-111"><span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**MP\_HASH\_TYPE\_CRC32**</span></span>
</dt> <dd>

<span data-ttu-id="848e0-112">CRC32</span><span class="sxs-lookup"><span data-stu-id="848e0-112">CRC32</span></span>

</dd> <dt>

<span data-ttu-id="848e0-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP \_ - \_ Hashtyp \_ MD5**</span><span class="sxs-lookup"><span data-stu-id="848e0-113"><span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**MP\_HASH\_TYPE\_MD5**</span></span>
</dt> <dd>

<span data-ttu-id="848e0-114">MD5</span><span class="sxs-lookup"><span data-stu-id="848e0-114">MD5</span></span>

</dd> <dt>

<span data-ttu-id="848e0-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP \_ - \_ Hashtyp \_ SHA1**</span><span class="sxs-lookup"><span data-stu-id="848e0-115"><span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**MP\_HASH\_TYPE\_SHA1**</span></span>
</dt> <dd>

<span data-ttu-id="848e0-116">SHA1</span><span class="sxs-lookup"><span data-stu-id="848e0-116">SHA1</span></span>

</dd> <dt>

<span data-ttu-id="848e0-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP \_ - \_ Hashtyp \_ SHA256**</span><span class="sxs-lookup"><span data-stu-id="848e0-117"><span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**MP\_HASH\_TYPE\_SHA256**</span></span>
</dt> <dd>

<span data-ttu-id="848e0-118">SHA 256</span><span class="sxs-lookup"><span data-stu-id="848e0-118">SHA 256</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="848e0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="848e0-119">Requirements</span></span>



| <span data-ttu-id="848e0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="848e0-120">Requirement</span></span> | <span data-ttu-id="848e0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="848e0-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="848e0-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="848e0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="848e0-123">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848e0-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="848e0-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="848e0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="848e0-125">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="848e0-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="848e0-126">Header</span><span class="sxs-lookup"><span data-stu-id="848e0-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="848e0-127"><dt>Mpclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="848e0-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





