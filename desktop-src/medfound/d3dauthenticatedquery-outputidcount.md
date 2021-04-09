---
description: Gibt die Anzahl von Ausgabe Bezeichner zurück, die einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet sind.
ms.assetid: a5b17250-6a40-40a9-93b6-3b98b56b09d6
title: D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 624b9ca0ee96f71fb9d3cb655aa9c10030a40efe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749289"
---
# <a name="d3dauthenticatedquery_outputidcount"></a><span data-ttu-id="d7850-103">D3DAUTHENTICATEDQUERY \_ outputidcount</span><span class="sxs-lookup"><span data-stu-id="d7850-103">D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT</span></span>

<span data-ttu-id="d7850-104">Gibt die Anzahl von Ausgabe Bezeichner zurück, die einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d7850-104">Returns the number of output identifiers associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="d7850-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7850-105">Requirement</span></span> | <span data-ttu-id="d7850-106">Wert</span><span class="sxs-lookup"><span data-stu-id="d7850-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7850-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="d7850-107">Query GUID</span></span>  | <span data-ttu-id="d7850-108">**D3DAUTHENTICATEDQUERY \_ outputidcount**</span><span class="sxs-lookup"><span data-stu-id="d7850-108">**D3DAUTHENTICATEDQUERY\_OUTPUTIDCOUNT**</span></span>                                                                         |
| <span data-ttu-id="d7850-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="d7850-109">Input data</span></span>  | [<span data-ttu-id="d7850-110">**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="d7850-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-input.md)   |
| <span data-ttu-id="d7850-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="d7850-111">Return data</span></span> | [<span data-ttu-id="d7850-112">**D3DAUTHENTICATEDCHANNEL \_ queryoutputidcount- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="d7850-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="d7850-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d7850-113">Remarks</span></span>

<span data-ttu-id="d7850-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="d7850-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="d7850-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="d7850-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="d7850-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="d7850-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="d7850-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d7850-117">Requirements</span></span>



| <span data-ttu-id="d7850-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d7850-118">Requirement</span></span> | <span data-ttu-id="d7850-119">Wert</span><span class="sxs-lookup"><span data-stu-id="d7850-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7850-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d7850-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d7850-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7850-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d7850-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d7850-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d7850-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d7850-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d7850-124">Header</span><span class="sxs-lookup"><span data-stu-id="d7850-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7850-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7850-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7850-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d7850-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7850-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="d7850-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="d7850-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="d7850-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="d7850-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="d7850-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




