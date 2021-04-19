---
description: Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von einem beliebigen Prozess ohne Einschränkungen geöffnet werden können.
ms.assetid: afbd7bb9-de71-4992-919e-e1517228dc69
title: D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b2d834927d21c59ed5c70dcf3a001d100340405d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344638"
---
# <a name="d3dauthenticatedquery_unrestrictedprotectedsharedresourcecount"></a><span data-ttu-id="76358-103">D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount</span><span class="sxs-lookup"><span data-stu-id="76358-103">D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT</span></span>

<span data-ttu-id="76358-104">Gibt die Anzahl der geschützten freigegebenen Ressourcen zurück, die von einem beliebigen Prozess ohne Einschränkungen geöffnet werden können.</span><span class="sxs-lookup"><span data-stu-id="76358-104">Returns the number of protected shared resources that can be opened by any process without restrictions.</span></span>



| <span data-ttu-id="76358-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76358-105">Requirement</span></span> | <span data-ttu-id="76358-106">Wert</span><span class="sxs-lookup"><span data-stu-id="76358-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="76358-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="76358-107">Query GUID</span></span>  | <span data-ttu-id="76358-108">**D3DAUTHENTICATEDQUERY \_ unrestrictedprotectedsharedresourcecount**</span><span class="sxs-lookup"><span data-stu-id="76358-108">**D3DAUTHENTICATEDQUERY\_UNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT**</span></span>                                                                                                    |
| <span data-ttu-id="76358-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="76358-109">Input data</span></span>  | [<span data-ttu-id="76358-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="76358-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                                                   |
| <span data-ttu-id="76358-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="76358-111">Return data</span></span> | [<span data-ttu-id="76358-112">**D3DAUTHENTICATEDCHANNEL \_ queryunrestrictedprotectedsharedresourcecount- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="76358-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNRESTRICTEDPROTECTEDSHAREDRESOURCECOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryunrestrictedprotectedsharedresourcecount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="76358-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="76358-113">Remarks</span></span>

<span data-ttu-id="76358-114">Der einzige Kanaltyp, der diese Abfrage unterstützt, ist die **D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**.</span><span class="sxs-lookup"><span data-stu-id="76358-114">The only channel type that supports this query is **D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="76358-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="76358-115">Requirements</span></span>



| <span data-ttu-id="76358-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="76358-116">Requirement</span></span> | <span data-ttu-id="76358-117">Wert</span><span class="sxs-lookup"><span data-stu-id="76358-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="76358-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="76358-118">Minimum supported client</span></span><br/> | <span data-ttu-id="76358-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76358-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="76358-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="76358-120">Minimum supported server</span></span><br/> | <span data-ttu-id="76358-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="76358-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="76358-122">Header</span><span class="sxs-lookup"><span data-stu-id="76358-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="76358-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="76358-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76358-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76358-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76358-125">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="76358-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="76358-126">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="76358-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="76358-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="76358-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




