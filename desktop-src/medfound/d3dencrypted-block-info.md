---
description: Gibt an, welche Bytes in einer geschützten Video Oberfläche verschlüsselt werden.
ms.assetid: 076f4f00-e86b-47e2-80dd-4d7434200138
title: D3DENCRYPTED_BLOCK_INFO-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DENCRYPTED_BLOCK_INFO
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21864dcc41ce86f139361af4357810137acf7f06
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127917"
---
# <a name="d3dencrypted_block_info-structure"></a><span data-ttu-id="d93d3-103">D3DENCRYPTED \_ Block \_ Info-Struktur</span><span class="sxs-lookup"><span data-stu-id="d93d3-103">D3DENCRYPTED\_BLOCK\_INFO structure</span></span>

<span data-ttu-id="d93d3-104">Gibt an, welche Bytes in einer geschützten Video Oberfläche verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d93d3-104">Specifies which bytes are encrypted in a protected video surface.</span></span>

## <a name="syntax"></a><span data-ttu-id="d93d3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d93d3-105">Syntax</span></span>


```C++
typedef struct _D3DENCRYPTED_BLOCK_INFO {
  UINT NumEncryptedBytesAtBeginning;
  UINT NumBytesInSkipPattern;
  UINT NumBytesInEncryptPattern;
} D3DENCRYPTED_BLOCK_INFO;
```



## <a name="members"></a><span data-ttu-id="d93d3-106">Member</span><span class="sxs-lookup"><span data-stu-id="d93d3-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="d93d3-107">**Numverschlüsseltedbytesatstart**</span><span class="sxs-lookup"><span data-stu-id="d93d3-107">**NumEncryptedBytesAtBeginning**</span></span>
</dt> <dd>

<span data-ttu-id="d93d3-108">Die Anzahl der Bytes, die am Anfang des Puffers verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d93d3-108">The number of bytes that are encrypted at the start of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d93d3-109">**Numbytesinskippattern**</span><span class="sxs-lookup"><span data-stu-id="d93d3-109">**NumBytesInSkipPattern**</span></span>
</dt> <dd>

<span data-ttu-id="d93d3-110">Die Anzahl der Bytes, die nach den ersten **numverschlüsseltedbytesatbeginungsbytes** übersprungen werden, und dann nach jedem Block von **numbytesinverschlüsseltpattern** -bytes.</span><span class="sxs-lookup"><span data-stu-id="d93d3-110">The number of bytes that are skipped after the first **NumEncryptedBytesAtBeginning** bytes, and then after each block of **NumBytesInEncryptPattern** bytes.</span></span> <span data-ttu-id="d93d3-111">Übersprungene Bytes werden nicht verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="d93d3-111">Skipped bytes are not encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="d93d3-112">**Numbytesinverschlüsseltpattern**</span><span class="sxs-lookup"><span data-stu-id="d93d3-112">**NumBytesInEncryptPattern**</span></span>
</dt> <dd>

<span data-ttu-id="d93d3-113">Die Anzahl der Bytes, die nach jedem Block von übersprungenen Bytes verschlüsselt werden.</span><span class="sxs-lookup"><span data-stu-id="d93d3-113">The number of bytes that are encrypted after each block of skipped bytes.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d93d3-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d93d3-114">Requirements</span></span>



| <span data-ttu-id="d93d3-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d93d3-115">Requirement</span></span> | <span data-ttu-id="d93d3-116">Wert</span><span class="sxs-lookup"><span data-stu-id="d93d3-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d93d3-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d93d3-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d93d3-118">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d93d3-118">Windows 7 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="d93d3-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d93d3-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d93d3-120">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d93d3-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d93d3-121">Header</span><span class="sxs-lookup"><span data-stu-id="d93d3-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="d93d3-122"><dt>D3d9types. h (Include d3d9. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d93d3-122"><dt>D3d9types.h (include D3d9.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93d3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d93d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93d3-124">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="d93d3-124">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




