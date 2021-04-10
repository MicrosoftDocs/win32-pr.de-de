---
description: Gibt den Verschlüsselungstyp zurück, der angewendet wird, bevor der CPU-oder busbus auf den Inhalt zugreifen kann.
ms.assetid: 89526bb2-1316-4730-b599-3690b1838c3e
title: D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_CURRENTENCRYPTIONWHENACCESSIBLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a8b3374e6d50a50d32b60113318e5d1099083226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214321"
---
# <a name="d3dauthenticatedquery_currentencryptionwhenaccessible"></a><span data-ttu-id="1edaa-103">D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. barrierefreie</span><span class="sxs-lookup"><span data-stu-id="1edaa-103">D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE</span></span>

<span data-ttu-id="1edaa-104">Gibt den Verschlüsselungstyp zurück, der angewendet wird, bevor der CPU-oder busbus auf den Inhalt zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="1edaa-104">Returns the encryption type that is applied before content becomes accessible to the CPU or bus.</span></span>



| <span data-ttu-id="1edaa-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1edaa-105">Requirement</span></span> | <span data-ttu-id="1edaa-106">Wert</span><span class="sxs-lookup"><span data-stu-id="1edaa-106">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1edaa-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="1edaa-107">Query GUID</span></span>  | <span data-ttu-id="1edaa-108">**D3DAUTHENTICATEDQUERY \_ currentverschlüsseltion. barrierefreie**</span><span class="sxs-lookup"><span data-stu-id="1edaa-108">**D3DAUTHENTICATEDQUERY\_CURRENTENCRYPTIONWHENACCESSIBLE**</span></span>                                                                                   |
| <span data-ttu-id="1edaa-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="1edaa-109">Input data</span></span>  | [<span data-ttu-id="1edaa-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="1edaa-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                                                         |
| <span data-ttu-id="1edaa-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="1edaa-111">Return data</span></span> | [<span data-ttu-id="1edaa-112">**D3DAUTHENTICATEDCHANNEL \_ queryuncompressedencryptionlevel- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="1edaa-112">**D3DAUTHENTICATEDCHANNEL\_QUERYUNCOMPRESSEDENCRYPTIONLEVEL\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryuncompressedencryptionlevel-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="1edaa-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1edaa-113">Remarks</span></span>

<span data-ttu-id="1edaa-114">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="1edaa-114">The following channel types support this query:</span></span>

-   <span data-ttu-id="1edaa-115">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="1edaa-115">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="1edaa-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="1edaa-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="1edaa-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1edaa-117">Requirements</span></span>



| <span data-ttu-id="1edaa-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1edaa-118">Requirement</span></span> | <span data-ttu-id="1edaa-119">Wert</span><span class="sxs-lookup"><span data-stu-id="1edaa-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1edaa-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1edaa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="1edaa-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1edaa-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="1edaa-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1edaa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="1edaa-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1edaa-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1edaa-124">Header</span><span class="sxs-lookup"><span data-stu-id="1edaa-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="1edaa-125"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="1edaa-125"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1edaa-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1edaa-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edaa-127">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="1edaa-127">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="1edaa-128">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="1edaa-128">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="1edaa-129">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="1edaa-129">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




