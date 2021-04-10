---
title: RB_HITTEST Meldung (kommstrg. h)
description: Bestimmt, welcher Teil eines Grund leisten Bands an einem bestimmten Punkt auf dem Bildschirm angezeigt wird, wenn ein Info leisten-Band an diesem Punkt vorhanden ist.
ms.assetid: 8f27db21-50d8-438f-a44c-2e65dd93fa2a
keywords:
- Windows-Steuerelemente für RB_HITTEST Meldung
topic_type:
- apiref
api_name:
- RB_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e17283bfce255672391ba9d8b6acd60fe41045b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040165"
---
# <a name="rb_hittest-message"></a><span data-ttu-id="54eba-104">RB \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="54eba-104">RB\_HITTEST message</span></span>

<span data-ttu-id="54eba-105">Bestimmt, welcher Teil eines Grund leisten Bands an einem bestimmten Punkt auf dem Bildschirm angezeigt wird, wenn ein Info leisten-Band an diesem Punkt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="54eba-105">Determines which portion of a rebar band is at a given point on the screen, if a rebar band exists at that point.</span></span>

## <a name="parameters"></a><span data-ttu-id="54eba-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54eba-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54eba-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="54eba-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="54eba-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="54eba-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="54eba-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="54eba-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="54eba-110">Zeiger auf eine [**rbhittestinfo**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="54eba-110">Pointer to an [**RBHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-rbhittestinfo) structure.</span></span> <span data-ttu-id="54eba-111">Bevor die Nachricht gesendet wird, muss der **PT** -Member dieser Struktur in Client Koordinaten mit dem Punkt initialisiert werden, der als Treffer getestet wird.</span><span class="sxs-lookup"><span data-stu-id="54eba-111">Before sending the message, the **pt** member of this structure must be initialized to the point that will be hit tested, in client coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54eba-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54eba-112">Return value</span></span>

<span data-ttu-id="54eba-113">Gibt den NULL basierten Index des Bands am angegebenen Punkt zurück, oder-1, wenn sich kein Grund leisten Band am Punkt befand.</span><span class="sxs-lookup"><span data-stu-id="54eba-113">Returns the zero-based index of the band at the given point, or -1 if no rebar band was at the point.</span></span>

## <a name="requirements"></a><span data-ttu-id="54eba-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54eba-114">Requirements</span></span>



| <span data-ttu-id="54eba-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54eba-115">Requirement</span></span> | <span data-ttu-id="54eba-116">Wert</span><span class="sxs-lookup"><span data-stu-id="54eba-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="54eba-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54eba-117">Minimum supported client</span></span><br/> | <span data-ttu-id="54eba-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54eba-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="54eba-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54eba-119">Minimum supported server</span></span><br/> | <span data-ttu-id="54eba-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54eba-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="54eba-121">Header</span><span class="sxs-lookup"><span data-stu-id="54eba-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="54eba-122"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="54eba-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





