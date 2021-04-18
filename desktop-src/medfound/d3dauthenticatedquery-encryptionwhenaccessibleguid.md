---
description: Gibt einen der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.
ms.assetid: 263c6f00-8bc9-4e9c-8b98-fb8f87c6c008
title: D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ENCRYPTIONWHENACCESSIBLEGUID
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: b5755a2707ec9d7440cda9b4692eed36ac6deff1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344014"
---
# <a name="d3dauthenticatedquery_encryptionwhenaccessibleguid"></a><span data-ttu-id="43c31-103">D3DAUTHENTICATEDQUERY \_ Verschlüsselung-accessibleguid</span><span class="sxs-lookup"><span data-stu-id="43c31-103">D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID</span></span>

<span data-ttu-id="43c31-104">Gibt einen der Verschlüsselungstypen zurück, die zum Verschlüsseln von Inhalten verwendet werden können, bevor die CPU oder der Bus darauf zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="43c31-104">Returns one of the encryption types that can be used to encrypt content before it becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="43c31-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43c31-105">Requirement</span></span> | <span data-ttu-id="43c31-106">Wert</span><span class="sxs-lookup"><span data-stu-id="43c31-106">Value</span></span> |
|-------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43c31-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="43c31-107">Query GUID</span></span>  | <span data-ttu-id="43c31-108">**D3DAUTHENTICATEDQUERY \_ Verschlüsselung-accessibleguid**</span><span class="sxs-lookup"><span data-stu-id="43c31-108">**D3DAUTHENTICATEDQUERY\_ENCRYPTIONWHENACCESSIBLEGUID**</span></span>                                                                            |
| <span data-ttu-id="43c31-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="43c31-109">Input data</span></span>  | [<span data-ttu-id="43c31-110">**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="43c31-110">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_INPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-input.md)   |
| <span data-ttu-id="43c31-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="43c31-111">Return data</span></span> | [<span data-ttu-id="43c31-112">**D3DAUTHENTICATEDCHANNEL \_ queryevictionverschlüsseltionguid- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="43c31-112">**D3DAUTHENTICATEDCHANNEL\_QUERYEVICTIONENCRYPTIONGUID\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryevictionencryptionguid-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="43c31-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43c31-113">Remarks</span></span>

<span data-ttu-id="43c31-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="43c31-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="43c31-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="43c31-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="43c31-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="43c31-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="43c31-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43c31-117">Requirements</span></span>



| <span data-ttu-id="43c31-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43c31-118">Requirement</span></span> | <span data-ttu-id="43c31-119">Wert</span><span class="sxs-lookup"><span data-stu-id="43c31-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43c31-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="43c31-120">Minimum supported client</span></span><br/> | <span data-ttu-id="43c31-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43c31-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="43c31-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="43c31-122">Minimum supported server</span></span><br/> | <span data-ttu-id="43c31-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="43c31-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="43c31-124">Header</span><span class="sxs-lookup"><span data-stu-id="43c31-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="43c31-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="43c31-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43c31-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43c31-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43c31-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="43c31-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="43c31-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="43c31-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="43c31-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="43c31-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




