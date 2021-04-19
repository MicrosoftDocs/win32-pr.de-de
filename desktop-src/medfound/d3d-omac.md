---
description: Enthält einen Nachrichtenauthentifizierungscode (Mac).
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: D3D_OMAC-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346049"
---
# <a name="d3d_omac-structure"></a><span data-ttu-id="19003-103">D3D \_ OMAC-Struktur</span><span class="sxs-lookup"><span data-stu-id="19003-103">D3D\_OMAC structure</span></span>

<span data-ttu-id="19003-104">Enthält einen Nachrichtenauthentifizierungscode (Mac).</span><span class="sxs-lookup"><span data-stu-id="19003-104">Contains a Message Authentication Code (MAC).</span></span>

## <a name="syntax"></a><span data-ttu-id="19003-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="19003-105">Syntax</span></span>


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a><span data-ttu-id="19003-106">Member</span><span class="sxs-lookup"><span data-stu-id="19003-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="19003-107">**OMAC**</span><span class="sxs-lookup"><span data-stu-id="19003-107">**Omac**</span></span>
</dt> <dd>

<span data-ttu-id="19003-108">Ein Bytearray, das den kryptografischen Mac-Wert der Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="19003-108">A byte array that contains the cryptographic MAC value of the message.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19003-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="19003-109">Requirements</span></span>



| <span data-ttu-id="19003-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="19003-110">Requirement</span></span> | <span data-ttu-id="19003-111">Wert</span><span class="sxs-lookup"><span data-stu-id="19003-111">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19003-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="19003-112">Minimum supported client</span></span><br/> | <span data-ttu-id="19003-113">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19003-113">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="19003-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="19003-114">Minimum supported server</span></span><br/> | <span data-ttu-id="19003-115">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="19003-115">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="19003-116">Header</span><span class="sxs-lookup"><span data-stu-id="19003-116">Header</span></span><br/>                   | <dl> <span data-ttu-id="19003-117"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="19003-117"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19003-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="19003-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19003-119">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="19003-119">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




