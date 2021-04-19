---
description: Gibt ein Handle für das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist.
ms.assetid: 948eac1a-640a-47fd-b538-1de3ea5d8f0b
title: D3DAUTHENTICATEDQUERY_DEVICEHANDLE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDQUERY_DEVICEHANDLE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: a3ebf54530a4ae029a52632eb5bb5afc51b5f152
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343624"
---
# <a name="d3dauthenticatedquery_devicehandle"></a><span data-ttu-id="90228-103">D3DAUTHENTICATEDQUERY-Geräte \_ Umgebung</span><span class="sxs-lookup"><span data-stu-id="90228-103">D3DAUTHENTICATEDQUERY\_DEVICEHANDLE</span></span>

<span data-ttu-id="90228-104">Gibt ein Handle für das Gerät zurück, das diesem authentifizierten Kanal zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="90228-104">Returns a handle to the device that is associated with this authenticated channel.</span></span> <span data-ttu-id="90228-105">Sie können dieses Handle verwenden, um zu überprüfen, ob zwei authentifizierte Kanäle mit demselben Gerät kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="90228-105">You can use this handle to verify whether two authenticated channels are communicating with the same device.</span></span>



| <span data-ttu-id="90228-106">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90228-106">Requirement</span></span> | <span data-ttu-id="90228-107">Wert</span><span class="sxs-lookup"><span data-stu-id="90228-107">Value</span></span> |
|-------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90228-108">Abfrage-GUID</span><span class="sxs-lookup"><span data-stu-id="90228-108">Query GUID</span></span>  | <span data-ttu-id="90228-109">**D3DAUTHENTICATEDQUERY-Geräte \_ Umgebung**</span><span class="sxs-lookup"><span data-stu-id="90228-109">**D3DAUTHENTICATEDQUERY\_DEVICEHANDLE**</span></span>                                                                        |
| <span data-ttu-id="90228-110">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="90228-110">Input data</span></span>  | [<span data-ttu-id="90228-111">**D3DAUTHENTICATEDCHANNEL- \_ Abfrage \_ Eingabe**</span><span class="sxs-lookup"><span data-stu-id="90228-111">**D3DAUTHENTICATEDCHANNEL\_QUERY\_INPUT**</span></span>](d3dauthenticatedchannel-query-input.md)                           |
| <span data-ttu-id="90228-112">Daten zurückgeben</span><span class="sxs-lookup"><span data-stu-id="90228-112">Return data</span></span> | [<span data-ttu-id="90228-113">**D3DAUTHENTICATEDCHANNEL \_ querydevicehandle- \_ Ausgabe**</span><span class="sxs-lookup"><span data-stu-id="90228-113">**D3DAUTHENTICATEDCHANNEL\_QUERYDEVICEHANDLE\_OUTPUT**</span></span>](d3dauthenticatedchannel-querydevicehandle-output.md) |



 

## <a name="remarks"></a><span data-ttu-id="90228-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90228-114">Remarks</span></span>

<span data-ttu-id="90228-115">Diese Abfrage ist für alle Kanaltypen gültig.</span><span class="sxs-lookup"><span data-stu-id="90228-115">This query is valid for all channel types.</span></span>

## <a name="requirements"></a><span data-ttu-id="90228-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="90228-116">Requirements</span></span>



| <span data-ttu-id="90228-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="90228-117">Requirement</span></span> | <span data-ttu-id="90228-118">Wert</span><span class="sxs-lookup"><span data-stu-id="90228-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="90228-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="90228-119">Minimum supported client</span></span><br/> | <span data-ttu-id="90228-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90228-120">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="90228-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="90228-121">Minimum supported server</span></span><br/> | <span data-ttu-id="90228-122">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="90228-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="90228-123">Header</span><span class="sxs-lookup"><span data-stu-id="90228-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="90228-124"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="90228-124"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="90228-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90228-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="90228-126">Content Protection Abfragen</span><span class="sxs-lookup"><span data-stu-id="90228-126">Content Protection Queries</span></span>](content-protection-queries.md)
</dt> <dt>

[<span data-ttu-id="90228-127">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="90228-127">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="90228-128">**IDirect3DAuthenticatedChannel9:: Query**</span><span class="sxs-lookup"><span data-stu-id="90228-128">**IDirect3DAuthenticatedChannel9::Query**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-query)
</dt> </dl>

 

 




