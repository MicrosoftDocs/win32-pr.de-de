---
description: Gibt die Schutz Ebene für Videoinhalte an.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346255"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a><span data-ttu-id="cf4d9-103">D3DAUTHENTICATEDCHANNEL \_ \_ Schutzflags-Struktur</span><span class="sxs-lookup"><span data-stu-id="cf4d9-103">D3DAUTHENTICATEDCHANNEL\_PROTECTION\_FLAGS structure</span></span>

<span data-ttu-id="cf4d9-104">Gibt die Schutz Ebene für Videoinhalte an.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-104">Specifies the protection level for video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf4d9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf4d9-105">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a><span data-ttu-id="cf4d9-106">Member</span><span class="sxs-lookup"><span data-stu-id="cf4d9-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="cf4d9-107">**Schutz aktiviert**</span><span class="sxs-lookup"><span data-stu-id="cf4d9-107">**ProtectionEnabled**</span></span>
</dt> <dd>

<span data-ttu-id="cf4d9-108">Wenn der Wert 1 ist, ist der Schutz von Videoinhalten aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-108">If 1, video content protection is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="cf4d9-109">**Overlayorfullscreenrequired**</span><span class="sxs-lookup"><span data-stu-id="cf4d9-109">**OverlayOrFullscreenRequired**</span></span>
</dt> <dd>

<span data-ttu-id="cf4d9-110">Wenn 1, erfordert die Anwendung, dass Videos entweder mithilfe eines Hardware Überlagerungs-oder Vollbildmodus angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-110">If 1, the application requires video to be displayed using either a hardware overlay or full-screen exclusive mode.</span></span>

</dd> <dt>

<span data-ttu-id="cf4d9-111">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="cf4d9-111">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="cf4d9-112">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-112">Reserved.</span></span> <span data-ttu-id="cf4d9-113">Legen Sie alle Bits auf 0 fest.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-113">Set all bits to zero.</span></span>

</dd> <dt>

<span data-ttu-id="cf4d9-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="cf4d9-114">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="cf4d9-115">Verwenden Sie diesen Member für den Zugriff auf alle Bits in der Union.</span><span class="sxs-lookup"><span data-stu-id="cf4d9-115">Use this member to access all of the bits in the union.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cf4d9-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf4d9-116">Requirements</span></span>



| <span data-ttu-id="cf4d9-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf4d9-117">Requirement</span></span> | <span data-ttu-id="cf4d9-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cf4d9-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf4d9-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf4d9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="cf4d9-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf4d9-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cf4d9-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf4d9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="cf4d9-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf4d9-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cf4d9-123">Header</span><span class="sxs-lookup"><span data-stu-id="cf4d9-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="cf4d9-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="cf4d9-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf4d9-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf4d9-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf4d9-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="cf4d9-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> </dl>

 

 




