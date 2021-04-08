---
description: Gibt einen der Ausgabe Bezeichner zurück, der einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet ist.
ms.assetid: 7b56055a-fb36-4e54-9bee-ab9401b09267
title: D3DAUTHENTICATEDQUERY_OUTPUTID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_OUTPUTID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: fa970ae6e7b10f553679376d7a924d1c8b67c595
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749296"
---
# <a name="d3dauthenticatedquery_outputid"></a><span data-ttu-id="1ddcd-103">D3DAUTHENTICATEDQUERY \_ OutputID</span><span class="sxs-lookup"><span data-stu-id="1ddcd-103">D3DAUTHENTICATEDQUERY\_OUTPUTID</span></span>

<span data-ttu-id="1ddcd-104">Gibt einen der Ausgabe Bezeichner zurück, der einer angegebenen Kryptografiesitzung und einem Direct3D-Gerät zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="1ddcd-104">Returns one of the output identifiers that is associated with a specified cryptographic session and Direct3D device.</span></span>



| <span data-ttu-id="1ddcd-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ddcd-105">Requirement</span></span> | <span data-ttu-id="1ddcd-106">Wert</span><span class="sxs-lookup"><span data-stu-id="1ddcd-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddcd-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="1ddcd-107">Query GUID</span></span>  | <span data-ttu-id="1ddcd-108">**D3DAUTHENTICATEDQUERY \_ OutputID**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-108">**D3DAUTHENTICATEDQUERY\_OUTPUTID**</span></span>                                                                    |
| <span data-ttu-id="1ddcd-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="1ddcd-109">Input data</span></span>  | [<span data-ttu-id="1ddcd-110">**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-110">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_INPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-input.md)   |
| <span data-ttu-id="1ddcd-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="1ddcd-111">Return data</span></span> | [<span data-ttu-id="1ddcd-112">**D3DAUTHENTICATEDCHANNEL \_ queryoutputid- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-112">**D3DAUTHENTICATEDCHANNEL\_QUERYOUTPUTID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryoutputid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="1ddcd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ddcd-113">Remarks</span></span>

<span data-ttu-id="1ddcd-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1ddcd-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="1ddcd-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="1ddcd-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="1ddcd-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ddcd-117">Requirements</span></span>



| <span data-ttu-id="1ddcd-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ddcd-118">Requirement</span></span> | <span data-ttu-id="1ddcd-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1ddcd-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ddcd-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ddcd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1ddcd-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ddcd-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1ddcd-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ddcd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1ddcd-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1ddcd-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1ddcd-124">Header</span><span class="sxs-lookup"><span data-stu-id="1ddcd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ddcd-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ddcd-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ddcd-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ddcd-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ddcd-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="1ddcd-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="1ddcd-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="1ddcd-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="1ddcd-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="1ddcd-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




