---
description: Gibt die aktuelle Schutz Ebene für das Gerät zurück.
ms.assetid: 335d21e8-2a98-4824-a60d-1969a40e8d24
title: D3DAUTHENTICATEDQUERY_PROTECTION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_PROTECTION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 85147d764d5b6580305723e9b05b127b116a660e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214318"
---
# <a name="d3dauthenticatedquery_protection"></a><span data-ttu-id="6f26c-103">D3DAUTHENTICATEDQUERY \_ Schutz</span><span class="sxs-lookup"><span data-stu-id="6f26c-103">D3DAUTHENTICATEDQUERY\_PROTECTION</span></span>

<span data-ttu-id="6f26c-104">Gibt die aktuelle Schutz Ebene für das Gerät zurück.</span><span class="sxs-lookup"><span data-stu-id="6f26c-104">Returns the current protection level for the device.</span></span>



| <span data-ttu-id="6f26c-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f26c-105">Requirement</span></span> | <span data-ttu-id="6f26c-106">Wert</span><span class="sxs-lookup"><span data-stu-id="6f26c-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f26c-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="6f26c-107">Query GUID</span></span>  | <span data-ttu-id="6f26c-108">**D3DAUTHENTICATEDQUERY \_ Schutz**</span><span class="sxs-lookup"><span data-stu-id="6f26c-108">**D3DAUTHENTICATEDQUERY\_PROTECTION**</span></span>                                                                      |
| <span data-ttu-id="6f26c-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="6f26c-109">Input data</span></span>  | [<span data-ttu-id="6f26c-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="6f26c-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                       |
| <span data-ttu-id="6f26c-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="6f26c-111">Return data</span></span> | [<span data-ttu-id="6f26c-112">**D3DAUTHENTICATEDCHANNEL \_ queryprotection- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="6f26c-112">**D3DAUTHENTICATEDCHANNEL\_QUERYPROTECTION\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryprotection-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="6f26c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f26c-113">Remarks</span></span>

<span data-ttu-id="6f26c-114">Diese Abfrage ist für alle Kanaltypen gültig.</span><span class="sxs-lookup"><span data-stu-id="6f26c-114">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f26c-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f26c-115">Requirements</span></span>



| <span data-ttu-id="6f26c-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f26c-116">Requirement</span></span> | <span data-ttu-id="6f26c-117">Wert</span><span class="sxs-lookup"><span data-stu-id="6f26c-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6f26c-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f26c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6f26c-119">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f26c-119">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6f26c-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f26c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6f26c-121">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f26c-121">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6f26c-122">Header</span><span class="sxs-lookup"><span data-stu-id="6f26c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6f26c-123"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="6f26c-123"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f26c-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f26c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f26c-125">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="6f26c-125">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="6f26c-126">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="6f26c-126">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="6f26c-127">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="6f26c-127">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




