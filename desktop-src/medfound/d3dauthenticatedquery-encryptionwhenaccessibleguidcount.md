---
description: Gibt die Anzahl der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.
ms.assetid: 442b80f5-8467-427d-a01e-5d22f6ddafea
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 9cd281836436c1d11fe07f7a43ecceebc8e3b12e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749297"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguidcount"></a><span data-ttu-id="a381f-103">D3DAUTHENTICATEDQUERY \_ verschlüsselungszuaccessibleguidcount</span><span class="sxs-lookup"><span data-stu-id="a381f-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT</span></span>

<span data-ttu-id="a381f-104">Gibt die Anzahl der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="a381f-104">Returns the number of encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="a381f-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a381f-105">Requirement</span></span> | <span data-ttu-id="a381f-106">Wert</span><span class="sxs-lookup"><span data-stu-id="a381f-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a381f-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="a381f-107">Query GUID</span></span>  | <span data-ttu-id="a381f-108">**D3DAUTHENTICATEDQUERY \_ verschlüsselungszuaccessibleguidcount**</span><span class="sxs-lookup"><span data-stu-id="a381f-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUIDCOUNT**</span></span>                                                                                 |
| <span data-ttu-id="a381f-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="a381f-109">Input data</span></span>  | [<span data-ttu-id="a381f-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="a381f-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="a381f-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="a381f-111">Return data</span></span> | [<span data-ttu-id="a381f-112">**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguidcount- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="a381f-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUIDCOUNT\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguidcount-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="a381f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a381f-113">Remarks</span></span>

<span data-ttu-id="a381f-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="a381f-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="a381f-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="a381f-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="a381f-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="a381f-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="a381f-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a381f-117">Requirements</span></span>



| <span data-ttu-id="a381f-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a381f-118">Requirement</span></span> | <span data-ttu-id="a381f-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a381f-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a381f-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a381f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a381f-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a381f-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="a381f-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a381f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a381f-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a381f-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a381f-124">Header</span><span class="sxs-lookup"><span data-stu-id="a381f-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a381f-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="a381f-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a381f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a381f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a381f-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="a381f-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="a381f-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="a381f-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="a381f-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="a381f-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




