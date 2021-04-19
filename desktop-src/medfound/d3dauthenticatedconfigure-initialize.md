---
description: Initialisiert den authentifizierten Kanal.
ms.assetid: a74edbaa-af57-4f8e-9974-f6053f59377f
title: D3DAUTHENTICATEDCONFIGURE_INITIALIZE (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCONFIGURE_INITIALIZE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 2cd3238b7a7eea27356ce76ec9c83bf8aea4d7f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343208"
---
# <a name="d3dauthenticatedconfigure_initialize"></a><span data-ttu-id="e6bc2-103">D3DAUTHENTICATEDCONFIGURE \_ initialisieren</span><span class="sxs-lookup"><span data-stu-id="e6bc2-103">D3DAUTHENTICATEDCONFIGURE\_INITIALIZE</span></span>

<span data-ttu-id="e6bc2-104">Initialisiert den authentifizierten Kanal.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-104">Initializes the authenticated channel.</span></span>



| <span data-ttu-id="e6bc2-105">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6bc2-105">Requirement</span></span> | <span data-ttu-id="e6bc2-106">Wert</span><span class="sxs-lookup"><span data-stu-id="e6bc2-106">Value</span></span> |
|--------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bc2-107">Befehls-GUID</span><span class="sxs-lookup"><span data-stu-id="e6bc2-107">Command GUID</span></span> | <span data-ttu-id="e6bc2-108">**D3DAUTHENTICATEDCONFIGURE \_ initialisieren**</span><span class="sxs-lookup"><span data-stu-id="e6bc2-108">**D3DAUTHENTICATEDCONFIGURE\_INITIALIZE**</span></span>                                                           |
| <span data-ttu-id="e6bc2-109">Eingabedaten</span><span class="sxs-lookup"><span data-stu-id="e6bc2-109">Input data</span></span>   | [<span data-ttu-id="e6bc2-110">**D3DAUTHENTICATEDCHANNEL- \_ Konfiguration erneut initialisieren**</span><span class="sxs-lookup"><span data-stu-id="e6bc2-110">**D3DAUTHENTICATEDCHANNEL\_CONFIGUREINITIALIZE**</span></span>](d3dauthenticatedchannel-configureinitialize.md) |



 

## <a name="remarks"></a><span data-ttu-id="e6bc2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e6bc2-111">Remarks</span></span>

<span data-ttu-id="e6bc2-112">Senden Sie diesen Befehl einmal am Anfang der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-112">Send this command once, at the start of the session.</span></span> <span data-ttu-id="e6bc2-113">Dieser Befehl kann nur ein Mal für jeden authentifizierten Kanal gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-113">This command can be sent only one time for each authenticated channel.</span></span> <span data-ttu-id="e6bc2-114">Die Eingabe Sequenznummer wird für diesen Befehl ignoriert.</span><span class="sxs-lookup"><span data-stu-id="e6bc2-114">The input sequence number is ignored for this command.</span></span>

<span data-ttu-id="e6bc2-115">Der folgende Kanaltyp unterstützt diesen Befehl:</span><span class="sxs-lookup"><span data-stu-id="e6bc2-115">The following channel types support this command:</span></span>

-   <span data-ttu-id="e6bc2-116">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Hardware**</span><span class="sxs-lookup"><span data-stu-id="e6bc2-116">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_HARDWARE**</span></span>
-   <span data-ttu-id="e6bc2-117">**D3DAUTHENTICATEDCHANNEL- \_ Treiber \_ Software**</span><span class="sxs-lookup"><span data-stu-id="e6bc2-117">**D3DAUTHENTICATEDCHANNEL\_DRIVER\_SOFTWARE**</span></span>

## <a name="requirements"></a><span data-ttu-id="e6bc2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6bc2-118">Requirements</span></span>



| <span data-ttu-id="e6bc2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6bc2-119">Requirement</span></span> | <span data-ttu-id="e6bc2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="e6bc2-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6bc2-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6bc2-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e6bc2-122">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6bc2-122">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="e6bc2-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6bc2-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e6bc2-124">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e6bc2-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e6bc2-125">Header</span><span class="sxs-lookup"><span data-stu-id="e6bc2-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6bc2-126"><dt>D3d9types. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6bc2-126"><dt>D3d9types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6bc2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6bc2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6bc2-128">Content Protection-Befehle</span><span class="sxs-lookup"><span data-stu-id="e6bc2-128">Content Protection Commands</span></span>](content-protection-commands.md)
</dt> <dt>

[<span data-ttu-id="e6bc2-129">GPU-basiertes Content Protection</span><span class="sxs-lookup"><span data-stu-id="e6bc2-129">GPU-Based Content Protection</span></span>](gpu-based-content-protection.md)
</dt> <dt>

[<span data-ttu-id="e6bc2-130">**IDirect3DAuthenticatedChannel9:: Configure**</span><span class="sxs-lookup"><span data-stu-id="e6bc2-130">**IDirect3DAuthenticatedChannel9::Configure**</span></span>](/windows/desktop/api/d3d9/nf-d3d9-idirect3dauthenticatedchannel9-configure)
</dt> </dl>

 

 




