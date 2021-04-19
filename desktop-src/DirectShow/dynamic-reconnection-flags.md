---
description: Die folgenden Flags geben die Ebene der dynamischen Verbindungs Verbindung an, die während des Renderings verwendet werden soll.
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: Dynamische reverbindungsflags (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 322c7d88cd84857ba0ebc1d19ed76a24e11cc3fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369646"
---
# <a name="dynamic-reconnection-flags"></a><span data-ttu-id="587a2-103">Dynamische neuverbindungsflags</span><span class="sxs-lookup"><span data-stu-id="587a2-103">Dynamic Reconnection Flags</span></span>

<span data-ttu-id="587a2-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="587a2-104">\[Deprecated.</span></span> <span data-ttu-id="587a2-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="587a2-105">This API may be removed from future releases of Windows.\]</span></span>

<span data-ttu-id="587a2-106">Die folgenden Flags geben die Ebene der dynamischen Verbindungs Verbindung an, die während des Renderings verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="587a2-106">The following flags specify the level of dynamic reconnection to use during rendering.</span></span>



| <span data-ttu-id="587a2-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="587a2-107">Constant/value</span></span>                                                                                                                                                                                                                                            | <span data-ttu-id="587a2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="587a2-108">Description</span></span>                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <span data-ttu-id="587a2-109"><dt>**Connectf \_ Dynamic \_ None**</dt> <dt>0x00</dt></span><span class="sxs-lookup"><span data-stu-id="587a2-109"><dt>**CONNECTF\_DYNAMIC\_NONE**</dt> <dt>0x00</dt></span></span> </dl>          | <span data-ttu-id="587a2-110">Keine dynamische erneute Verbindung.</span><span class="sxs-lookup"><span data-stu-id="587a2-110">No dynamic reconnection.</span></span> <span data-ttu-id="587a2-111">Laden Sie alles, bevor Sie das Projekt rendern.</span><span class="sxs-lookup"><span data-stu-id="587a2-111">Load everything before rendering the project.</span></span><br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <span data-ttu-id="587a2-112"><dt>**Connectf \_ Dynamische \_ Quellen**</dt> <dt>0x01</dt></span><span class="sxs-lookup"><span data-stu-id="587a2-112"><dt>**CONNECTF\_DYNAMIC\_SOURCES**</dt> <dt>0x01</dt></span></span> </dl> | <span data-ttu-id="587a2-113">Laden Sie Quellen nur nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="587a2-113">Load sources only as needed.</span></span><br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <span data-ttu-id="587a2-114"><dt>**Connectf \_ Dynamische \_ Effekte**</dt> <dt>0x02</dt></span><span class="sxs-lookup"><span data-stu-id="587a2-114"><dt>**CONNECTF\_DYNAMIC\_EFFECTS**</dt> <dt>0x02</dt></span></span> </dl> | <span data-ttu-id="587a2-115">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="587a2-115">Reserved.</span></span> <span data-ttu-id="587a2-116">Darf nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="587a2-116">Do not use.</span></span><br/>                                                  |



## <a name="requirements"></a><span data-ttu-id="587a2-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="587a2-117">Requirements</span></span>



| <span data-ttu-id="587a2-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="587a2-118">Requirement</span></span> | <span data-ttu-id="587a2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="587a2-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="587a2-120">Header</span><span class="sxs-lookup"><span data-stu-id="587a2-120">Header</span></span><br/> | <dl> <span data-ttu-id="587a2-121"><dt>"Qedit. h"</dt></span><span class="sxs-lookup"><span data-stu-id="587a2-121"><dt>Qedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="587a2-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="587a2-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="587a2-123">**"Unenderengine:: setdynamikreconnectlevel"**</span><span class="sxs-lookup"><span data-stu-id="587a2-123">**IRenderEngine::SetDynamicReconnectLevel**</span></span>](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




