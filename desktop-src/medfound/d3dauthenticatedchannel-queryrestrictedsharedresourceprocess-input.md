---
description: Enthält Eingabedaten für eine D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess-Abfrage.
ms.assetid: a1ceb394-7af9-4f05-9f58-a3103bf0150e
title: D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT-Struktur (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 06c4421f048af80186077da022fdecfaea79dca6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346047"
---
# <a name="d3dauthenticatedchannel_queryrestrictedsharedresourceprocess_input-structure"></a><span data-ttu-id="877a5-103">D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Eingabe Struktur</span><span class="sxs-lookup"><span data-stu-id="877a5-103">D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT structure</span></span>

<span data-ttu-id="877a5-104">Enthält Eingabedaten für eine [**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) -Abfrage.</span><span class="sxs-lookup"><span data-stu-id="877a5-104">Contains input data for a [**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**](d3dauthenticatedquery-restrictedsharedresourceprocess.md) query.</span></span>

<span data-ttu-id="877a5-105">Um diese Abfrage zu senden, nennen Sie [**IDirect3DAuthenticatedChannel9:: Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span><span class="sxs-lookup"><span data-stu-id="877a5-105">To send this query, call [**IDirect3DAuthenticatedChannel9::Query**](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query).</span></span>

## <a name="syntax"></a><span data-ttu-id="877a5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="877a5-106">Syntax</span></span>


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT {
  D3DAUTHENTICATEDCHANNEL_QUERY_INPUT Input;
  UINT                                ProcessIndex;
} D3DAUTHENTICATEDCHANNEL_QUERYRESTRICTEDSHAREDRESOURCEPROCESS_INPUT;
```



## <a name="members"></a><span data-ttu-id="877a5-107">Member</span><span class="sxs-lookup"><span data-stu-id="877a5-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="877a5-108">**Input** (Eingabe)</span><span class="sxs-lookup"><span data-stu-id="877a5-108">**Input**</span></span>
</dt> <dd>

<span data-ttu-id="877a5-109">Eine [**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**](d3dauthenticatedchannel-query-input.md) Struktur, die die GUID für die Abfrage und andere Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="877a5-109">A [**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**](d3dauthenticatedchannel-query-input.md) structure that contains the GUID for the query and other data.</span></span>

</dd> <dt>

<span data-ttu-id="877a5-110">**Processindex**</span><span class="sxs-lookup"><span data-stu-id="877a5-110">**ProcessIndex**</span></span>
</dt> <dd>

<span data-ttu-id="877a5-111">Der Index des Prozesses.</span><span class="sxs-lookup"><span data-stu-id="877a5-111">The index of the process.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="877a5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="877a5-112">Requirements</span></span>



| <span data-ttu-id="877a5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="877a5-113">Requirement</span></span> | <span data-ttu-id="877a5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="877a5-114">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="877a5-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="877a5-115">Minimum supported client</span></span><br/> | <span data-ttu-id="877a5-116">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="877a5-116">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="877a5-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="877a5-117">Minimum supported server</span></span><br/> | <span data-ttu-id="877a5-118">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="877a5-118">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="877a5-119">Header</span><span class="sxs-lookup"><span data-stu-id="877a5-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="877a5-120"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="877a5-120"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="877a5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="877a5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="877a5-122">Direct3D-Video Strukturen</span><span class="sxs-lookup"><span data-stu-id="877a5-122">Direct3D Video Structures</span></span>](direct3d-video-structures.md)
</dt> <dt>

[<span data-ttu-id="877a5-123">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="877a5-123">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




