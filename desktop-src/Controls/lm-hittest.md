---
title: LM_HITTEST Meldung (kommstrg. h)
description: Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.
ms.assetid: a84c0388-26e7-4eda-9c6c-c5f64142d67a
keywords:
- Windows-Steuerelemente für LM_HITTEST Meldung
topic_type:
- apiref
api_name:
- LM_HITTEST
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497800369203ac8ea7484371e1038ba15d6cc68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858658"
---
# <a name="lm_hittest-message"></a><span data-ttu-id="23365-104">LM- \_ HitTest-Meldung</span><span class="sxs-lookup"><span data-stu-id="23365-104">LM\_HITTEST message</span></span>

<span data-ttu-id="23365-105">Bestimmt, ob der Benutzer auf den angegebenen Link geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="23365-105">Determines whether the user clicked the specified link.</span></span>

## <a name="parameters"></a><span data-ttu-id="23365-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="23365-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23365-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="23365-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="23365-108">Muss **null** sein.</span><span class="sxs-lookup"><span data-stu-id="23365-108">Must be **NULL**.</span></span></dd> <dt>

<span data-ttu-id="23365-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="23365-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="23365-110">Ein Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**lhittestinfo**</a> -Struktur, die mit Informationen über den Link gefüllt werden soll, auf den der Benutzer geklickt hat, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="23365-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lhittestinfo">**LHITTESTINFO**</a> structure to be filled with information about the link the user clicked, if any exists.</span></span> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23365-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23365-111">Return value</span></span>

<span data-ttu-id="23365-112">Gibt **true** zurück, wenn der Benutzer auf einen Link geklickt hat; andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23365-112">Returns **TRUE** if user clicked on a link, otherwise returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="23365-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23365-113">Remarks</span></span>

<span data-ttu-id="23365-114">Wenn die **LM- \_ HitTest** -Nachricht erfolgreich ist, füllt das System [**LItem. iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) und **LItem. szid** aus.</span><span class="sxs-lookup"><span data-stu-id="23365-114">If the **LM\_HITTEST** message succeeds, the system fills in [**LITEM.iLink**](/windows/win32/api/commctrl/ns-commctrl-litem) and **LITEM.szID**.</span></span> <span data-ttu-id="23365-115">Wenn die **LM- \_ HitTest** -Nachricht fehlschlägt, gehen Sie nicht davon aus, dass alle Informationen in **LItem** gültig sind.</span><span class="sxs-lookup"><span data-stu-id="23365-115">If the **LM\_HITTEST** message fails, do not assume that any information in **LITEM** is valid.</span></span>

> [!Note]  
> <span data-ttu-id="23365-116">Um diese API zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="23365-116">To use this API, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="23365-117">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="23365-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="23365-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23365-118">Requirements</span></span>



| <span data-ttu-id="23365-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="23365-119">Requirement</span></span> | <span data-ttu-id="23365-120">Wert</span><span class="sxs-lookup"><span data-stu-id="23365-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="23365-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23365-121">Minimum supported client</span></span><br/> | <span data-ttu-id="23365-122">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23365-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="23365-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23365-123">Minimum supported server</span></span><br/> | <span data-ttu-id="23365-124">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23365-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="23365-125">Header</span><span class="sxs-lookup"><span data-stu-id="23365-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="23365-126"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="23365-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





