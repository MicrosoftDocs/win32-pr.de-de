---
description: Gibt Handles an die Kryptografiesitzung und das Direct3D-Gerät zurück, die einem angegebenen DirectX Video Acceleration 2 (DXVA-2)-Decodergerät zugeordnet sind.
ms.assetid: 90b3bcf3-2988-48de-8acd-62e385d4fdf0
title: D3DAUTHENTICATEDQUERY_CRYPTOSESSION (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CRYPTOSESSION
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: e824514c3fef4e3e036b8f2973d3a958c4e135ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214320"
---
# <a name="d3dauthenticatedquery_cryptosession"></a><span data-ttu-id="55757-103">D3DAUTHENTICATEDQUERY \_ CryptoSession</span><span class="sxs-lookup"><span data-stu-id="55757-103">D3DAUTHENTICATEDQUERY\_CRYPTOSESSION</span></span>

<span data-ttu-id="55757-104">Gibt Handles an die Kryptografiesitzung und das Direct3D-Gerät zurück, die einem angegebenen DirectX Video Acceleration 2 (DXVA-2)-Decodergerät zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="55757-104">Returns handles to the cryptographic session and Direct3D device that are associated with a specified DirectX Video Acceleration 2 (DXVA-2) decoder device.</span></span>



| <span data-ttu-id="55757-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55757-105">Requirement</span></span> | <span data-ttu-id="55757-106">Wert</span><span class="sxs-lookup"><span data-stu-id="55757-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55757-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="55757-107">Query GUID</span></span>  | <span data-ttu-id="55757-108">**D3DAUTHENTICATEDQUERY \_ CryptoSession**</span><span class="sxs-lookup"><span data-stu-id="55757-108">**D3DAUTHENTICATEDQUERY\_CRYPTOSESSION**</span></span>                                                                         |
| <span data-ttu-id="55757-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="55757-109">Input data</span></span>  | [<span data-ttu-id="55757-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="55757-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                             |
| <span data-ttu-id="55757-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="55757-111">Return data</span></span> | [<span data-ttu-id="55757-112">**D3DAUTHENTICATEDCHANNEL \_ querycryptosession- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="55757-112">**D3DAUTHENTICATEDCHANNEL\_QUERYCRYPTOSESSION\_OUTPUT**</span></span>](d3dauthenticatedchannel-querycryptosession-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="55757-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="55757-113">Remarks</span></span>

<span data-ttu-id="55757-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="55757-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="55757-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="55757-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="55757-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="55757-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="55757-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="55757-117">Requirements</span></span>



| <span data-ttu-id="55757-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="55757-118">Requirement</span></span> | <span data-ttu-id="55757-119">Wert</span><span class="sxs-lookup"><span data-stu-id="55757-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="55757-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="55757-120">Minimum supported client</span></span><br/> | <span data-ttu-id="55757-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55757-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="55757-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="55757-122">Minimum supported server</span></span><br/> | <span data-ttu-id="55757-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="55757-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="55757-124">Header</span><span class="sxs-lookup"><span data-stu-id="55757-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="55757-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="55757-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55757-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55757-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55757-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="55757-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="55757-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="55757-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="55757-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="55757-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




