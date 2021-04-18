---
title: LVM_SETINFOTIP Meldung (kommstrg. h)
description: Legt den QuickInfo-Text in verzögerter Antwort auf die LVN \_ getinfotip-Benachrichtigung fest.
ms.assetid: 3dbf6a9a-52ec-4619-9c70-041e75942e20
keywords:
- Windows-Steuerelemente für LVM_SETINFOTIP Meldung
topic_type:
- apiref
api_name:
- LVM_SETINFOTIP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90827766a6f1218dbbd631ed4eaf6b2989257944
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339310"
---
# <a name="lvm_setinfotip-message"></a><span data-ttu-id="6ca97-104">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="6ca97-104">LVM\_SETINFOTIP message</span></span>

<span data-ttu-id="6ca97-105">Legt den QuickInfo-Text in verzögerter Antwort auf die [LVN \_ getinfotip](lvn-getinfotip.md) -Benachrichtigung fest.</span><span class="sxs-lookup"><span data-stu-id="6ca97-105">Sets tooltip text in delayed response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification.</span></span>

## <a name="parameters"></a><span data-ttu-id="6ca97-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ca97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ca97-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6ca97-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="6ca97-108">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6ca97-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="6ca97-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6ca97-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="6ca97-110">Zeiger auf eine <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">lvsetinfotip</a> -Struktur, die die festzulegenden Informationen enthält.</span><span class="sxs-lookup"><span data-stu-id="6ca97-110">Pointer to a <a href="/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip">LVSETINFOTIP</a> structure that contains the information to set.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ca97-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ca97-111">Return value</span></span>

<span data-ttu-id="6ca97-112">Gibt **true** zurück, wenn der QuickInfo-Text erfolgreich festgelegt wurde, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="6ca97-112">Returns **TRUE** if the tooltip text is set successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ca97-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ca97-113">Remarks</span></span>

<span data-ttu-id="6ca97-114">Die **LVM \_ setinfotip** -Nachricht ermöglicht einer Anwendung das Berechnen von Infotipps im Hintergrund, indem die folgenden Schritte ausgeführt werden:</span><span class="sxs-lookup"><span data-stu-id="6ca97-114">The **LVM\_SETINFOTIP** message lets an application calculate infotips in the background by performing the following steps:</span></span>

1.  <span data-ttu-id="6ca97-115">Legen Sie als Antwort auf die [LVN \_ getinfotip](lvn-getinfotip.md) -Benachrichtigung den **pszText** -Member der [**nmlvgetinfotip**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) -Struktur auf eine leere Zeichenfolge fest, und geben Sie 0 zurück.</span><span class="sxs-lookup"><span data-stu-id="6ca97-115">In response to the [LVN\_GETINFOTIP](lvn-getinfotip.md) notification, set the **pszText** member of the [**NMLVGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmlvgetinfotipa) structure to an empty string and return 0.</span></span>
2.  <span data-ttu-id="6ca97-116">Im Hintergrund berechnen Sie den infotip.</span><span class="sxs-lookup"><span data-stu-id="6ca97-116">In the background, compute the infotip.</span></span>
3.  <span data-ttu-id="6ca97-117">Nachdem Sie den Infotipp berechnet haben, senden Sie die LVM-Nachricht " **\_ stinfotip** ". Legen Sie dabei den **pszText** -Member der " [**LV* tinfotip*\*](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) "-Struktur auf die Infotipp-und die **iItem** -und **iSubItem** -Elemente auf das Element und das Unterelement fest, für das der Infotipp gilt</span><span class="sxs-lookup"><span data-stu-id="6ca97-117">After computing the infotip, send the **LVM\_SETINFOTIP** message, setting the **pszText** member of the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure to the infotip and the **iItem** and **iSubItem** members to the item and sub-item to which the infotip applies.</span></span>

<span data-ttu-id="6ca97-118">Der Text, der an die LVM-Nachricht " **mesfotip \_** " weitergeleitet wird, wird nur angezeigt, wenn sich das von der Struktur " [**LV* tinfotip*\*](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) " beschriebene Element und Unterelement noch in einem Zustand befinden, der einen InfoTipp erfordert</span><span class="sxs-lookup"><span data-stu-id="6ca97-118">The text passed to the **LVM\_SETINFOTIP** message appears only if the item and sub-item described by the [**LVSETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-lvsetinfotip) structure are still in a state that requires an infotip</span></span>

> [!Note]  
> <span data-ttu-id="6ca97-119">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="6ca97-119">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="6ca97-120">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6ca97-120">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="6ca97-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ca97-121">Requirements</span></span>



| <span data-ttu-id="6ca97-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ca97-122">Requirement</span></span> | <span data-ttu-id="6ca97-123">Wert</span><span class="sxs-lookup"><span data-stu-id="6ca97-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ca97-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6ca97-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6ca97-125">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca97-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6ca97-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6ca97-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6ca97-127">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6ca97-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6ca97-128">Header</span><span class="sxs-lookup"><span data-stu-id="6ca97-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6ca97-129"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ca97-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





