---
description: Enthält die Antwort auf eine D3DAUTHENTICATEDQUERY \_ accessibilityattributabfrage.
ms.assetid: 9f66a467-ba05-413b-b001-ea4c5ca4a37d
title: D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 853488c98687825ab55d642b2e01e569f0d435c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341161"
---
# <a name="d3dauthenticatedchannel_queryinfobustype_output-structure"></a><span data-ttu-id="298e2-103">D3DAUTHENTICATEDCHANNEL \_ queryinfobustype- \_ Ausgabestruktur</span><span class="sxs-lookup"><span data-stu-id="298e2-103">D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT structure</span></span>

<span data-ttu-id="298e2-104">Enthält die Antwort auf eine [**D3DAUTHENTICATEDQUERY \_ accessibilityattributabfrage**](d3dauthenticatedquery-accessibilityattributes.md) .</span><span class="sxs-lookup"><span data-stu-id="298e2-104">Contains the response to a [**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**](d3dauthenticatedquery-accessibilityattributes.md) query.</span></span>

<span data-ttu-id="298e2-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="298e2-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="298e2-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="298e2-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_OUTPUT Output;
  D3DBUSTYPE                           BusType;
  BOOL                                 bAccessibleInContiguousBlocks;
  BOOL                                 bAccessibleInNonContiguousBlocks;
} D3DAUTHENTICATEDCHANNEL_QUERYINFOBUSTYPE_OUTPUT;
```



## <a name="members"></a><span data-ttu-id="298e2-107">Member</span><span class="sxs-lookup"><span data-stu-id="298e2-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="298e2-108">**Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="298e2-108">**Output**</span></span>
</dt> <dd>

<span data-ttu-id="298e2-109">Eine [**D3DAUTHENTICATEDCHANNEL \_ Query- \_ Ausgabe**](d3dauthenticatedchannel-query-output.md) Struktur, die eine Nachrichtenauthentifizierungscode (Mac) und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="298e2-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_OUTPUT**](d3dauthenticatedchannel-query-output.md) structure that contains a Message Authentication Code (MAC) and other data.</span></span>

</dd> <dt>

<span data-ttu-id="298e2-110">**BusType**</span><span class="sxs-lookup"><span data-stu-id="298e2-110">**BusType**</span></span>
</dt> <dd>

<span data-ttu-id="298e2-111">Ein bitweises **or** von-Flags aus der [**D3DBUSTYPE**](d3dbustype.md) -Enumeration.</span><span class="sxs-lookup"><span data-stu-id="298e2-111">A bitwise **OR** of flags from the [**D3DBUSTYPE**](d3dbustype.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="298e2-112">**baccessiblancontiguousblocks**</span><span class="sxs-lookup"><span data-stu-id="298e2-112">**bAccessibleInContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="298e2-113">**True** gibt an, dass die CPU oder der Bus auf zusammenhängende Blöcke des Video Speichers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="298e2-113">If **TRUE**, contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> <dt>

<span data-ttu-id="298e2-114">**baccessiblannoncontiguousblocks**</span><span class="sxs-lookup"><span data-stu-id="298e2-114">**bAccessibleInNonContiguousBlocks**</span></span>
</dt> <dd>

<span data-ttu-id="298e2-115">**True** gibt an, dass die CPU oder der Bus auf nicht zusammenhängende Blöcke des Video Speichers zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="298e2-115">If **TRUE**, non-contiguous blocks of video memory may be accessible to the CPU or the bus.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="298e2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="298e2-116">Requirements</span></span>



| <span data-ttu-id="298e2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="298e2-117">Requirement</span></span> | <span data-ttu-id="298e2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="298e2-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="298e2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="298e2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="298e2-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="298e2-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="298e2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="298e2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="298e2-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="298e2-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="298e2-123">Header</span><span class="sxs-lookup"><span data-stu-id="298e2-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="298e2-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="298e2-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="298e2-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="298e2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="298e2-126">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="298e2-126">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="298e2-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="298e2-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




