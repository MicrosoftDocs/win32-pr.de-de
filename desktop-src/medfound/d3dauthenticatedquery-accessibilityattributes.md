---
description: Gibt den Typ des e/a-Busses zurück, der zum Senden von Daten an die GPU verwendet wurde.
ms.assetid: 5a180a5c-6798-40ba-9e2c-ce1f755fcc08
title: D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_ACCESSIBILITYATTRIBUTES
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 5119da4e7efaf0c27db1065dacc56e3388a77474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393282"
---
# <a name="d3dauthenticatedquery_accessibilityattributes"></a><span data-ttu-id="8b7e3-103">D3DAUTHENTICATEDQUERY \_ accessibilityattribute</span><span class="sxs-lookup"><span data-stu-id="8b7e3-103">D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES</span></span>

<span data-ttu-id="8b7e3-104">Gibt den Typ des e/a-Busses zurück, der zum Senden von Daten an die GPU verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8b7e3-104">Returns the type of I/O bus used to send data to the GPU.</span></span>



| <span data-ttu-id="8b7e3-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b7e3-105">Requirement</span></span> | <span data-ttu-id="8b7e3-106">Wert</span><span class="sxs-lookup"><span data-stu-id="8b7e3-106">Value</span></span> |
|-------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7e3-107">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="8b7e3-107">Query GUID</span></span>  | <span data-ttu-id="8b7e3-108">**D3DAUTHENTICATEDQUERY \_ accessibilityattribute**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-108">**D3DAUTHENTICATEDQUERY\_ACCESSIBILITYATTRIBUTES**</span></span>                                                           |
| <span data-ttu-id="8b7e3-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="8b7e3-109">Input data</span></span>  | [<span data-ttu-id="8b7e3-110">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-110">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                         |
| <span data-ttu-id="8b7e3-111">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="8b7e3-111">Return data</span></span> | [<span data-ttu-id="8b7e3-112">**D3DAUTHENTICATEDCHANNEL \_ queryinfobustype- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-112">**D3DAUTHENTICATEDCHANNEL\_QUERYINFOBUSTYPE\_OUTPUT**</span></span>](d3dauthenticatedchannel-queryinfobustype-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="8b7e3-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b7e3-113">Remarks</span></span>

<span data-ttu-id="8b7e3-114">Diese Abfrage gibt außerdem Informationen darüber zurück, wie zugänglich der Inhalt ist, wenn er in den Videospeicher eingefügt wird.</span><span class="sxs-lookup"><span data-stu-id="8b7e3-114">This query also returns information about how accessible the content is when put into video memory.</span></span>

<span data-ttu-id="8b7e3-115">Diese Abfrage wird von den folgenden Kanaltypen unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8b7e3-115">The following channel types support this query:</span></span>

-   <span data-ttu-id="8b7e3-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="8b7e3-117">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="8b7e3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b7e3-118">Requirements</span></span>



| <span data-ttu-id="8b7e3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b7e3-119">Requirement</span></span> | <span data-ttu-id="8b7e3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="8b7e3-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8b7e3-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b7e3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="8b7e3-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b7e3-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8b7e3-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b7e3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="8b7e3-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8b7e3-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8b7e3-125">Header</span><span class="sxs-lookup"><span data-stu-id="8b7e3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="8b7e3-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="8b7e3-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b7e3-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b7e3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b7e3-128">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="8b7e3-128">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="8b7e3-129">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="8b7e3-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="8b7e3-130">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="8b7e3-130">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




