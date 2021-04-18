---
description: Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.
ms.assetid: 669d9623-3a96-4661-9dae-3f283a990fe8
title: D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_RESTRICTEDSHAREDRESOURCEPROCESS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 74bb829510fee4425648412f58d4f7cea74b1f72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106338939"
---
# <a name="d3dauthenticatedquery_restrictedsharedresourceprocess"></a><span data-ttu-id="9d4be-103">D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess</span><span class="sxs-lookup"><span data-stu-id="9d4be-103">D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS</span></span>

<span data-ttu-id="9d4be-104">Gibt Informationen zu einem Prozess zurück, der freigegebene Ressourcen mit eingeschränktem Zugriff öffnen darf.</span><span class="sxs-lookup"><span data-stu-id="9d4be-104">Returns information about a process that is allowed to open shared resources with restricted access.</span></span>



| <span data-ttu-id="9d4be-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d4be-105">Requirement</span></span> | <span data-ttu-id="9d4be-106">Wert</span><span class="sxs-lookup"><span data-stu-id="9d4be-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4be-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="9d4be-107">Query GUID</span></span>  | <span data-ttu-id="9d4be-108">**D3DAUTHENTICATEDQUERY \_ restrictedsharedresourceprocess**</span><span class="sxs-lookup"><span data-stu-id="9d4be-108">**D3DAUTHENTICATEDQUERY\_RESTRICTEDSHAREDRESOURCEPROCESS**</span></span>                                                                                           |
| <span data-ttu-id="9d4be-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="9d4be-109">Input data</span></span>  | [<span data-ttu-id="9d4be-110">**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="9d4be-110">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_INPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-input.md)   |
| <span data-ttu-id="9d4be-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="9d4be-111">Return data</span></span> | [<span data-ttu-id="9d4be-112">**D3DAUTHENTICATEDCHANNEL \_ queryrestrictedsharedresourceprocess- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="9d4be-112">**D3DAUTHENTICATEDCHANNEL\_QUERYRESTRICTEDSHAREDRESOURCEPROCESS\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryrestrictedsharedresourceprocess-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="9d4be-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9d4be-113">Remarks</span></span>

<span data-ttu-id="9d4be-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9d4be-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="9d4be-115">**D3DAUTHENTICATEDCHANNEL \_ d3d9**</span><span class="sxs-lookup"><span data-stu-id="9d4be-115">**D3DAUTHENTICATEDCHANNEL\_D3D9**</span></span>
-   <span data-ttu-id="9d4be-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="9d4be-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="9d4be-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9d4be-117">Requirements</span></span>



| <span data-ttu-id="9d4be-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9d4be-118">Requirement</span></span> | <span data-ttu-id="9d4be-119">Wert</span><span class="sxs-lookup"><span data-stu-id="9d4be-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d4be-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9d4be-120">Minimum supported client</span></span><br/> | <span data-ttu-id="9d4be-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4be-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9d4be-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9d4be-122">Minimum supported server</span></span><br/> | <span data-ttu-id="9d4be-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9d4be-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9d4be-124">Header</span><span class="sxs-lookup"><span data-stu-id="9d4be-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d4be-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d4be-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d4be-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d4be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d4be-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="9d4be-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="9d4be-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="9d4be-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="9d4be-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="9d4be-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




