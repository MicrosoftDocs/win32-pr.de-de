---
title: HDM_SETHOTDIVIDER Meldung (kommstrg. h)
description: Ändert die Farbe eines unter Teilers zwischen Header Elementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben. Sie können diese Nachricht explizit senden oder das-Header-" \_ lthotdivider"-Makro verwenden.
ms.assetid: 56f6e5c6-1df3-4b4d-9ad8-97fb168c5462
keywords:
- Windows-Steuerelemente für HDM_SETHOTDIVIDER Meldung
topic_type:
- apiref
api_name:
- HDM_SETHOTDIVIDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feb894100878e9b3ee85e8e8367a4b81a022a0a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103551"
---
# <a name="hdm_sethotdivider-message"></a><span data-ttu-id="947f5-105">HDM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="947f5-105">HDM\_SETHOTDIVIDER message</span></span>

<span data-ttu-id="947f5-106">Ändert die Farbe eines unter Teilers zwischen Header Elementen, um das Ziel eines externen Drag & Drop-Vorgangs anzugeben.</span><span class="sxs-lookup"><span data-stu-id="947f5-106">Changes the color of a divider between header items to indicate the destination of an external drag-and-drop operation.</span></span> <span data-ttu-id="947f5-107">Sie können diese Nachricht explizit senden oder das- [**Header-" \_ lthotdivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) "-Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="947f5-107">You can send this message explicitly or use the [**Header\_SetHotDivider**](/windows/desktop/api/Commctrl/nf-commctrl-header_sethotdivider) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="947f5-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="947f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="947f5-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="947f5-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="947f5-110">Der Typ des durch *LPARAM* dargestellten Werts.</span><span class="sxs-lookup"><span data-stu-id="947f5-110">The type of value represented by *lParam*.</span></span> <span data-ttu-id="947f5-111">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="947f5-111">This value can be one of the following:</span></span>



| <span data-ttu-id="947f5-112">Wert</span><span class="sxs-lookup"><span data-stu-id="947f5-112">Value</span></span>                                                                                                                                    | <span data-ttu-id="947f5-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="947f5-113">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="947f5-114"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="947f5-114"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="947f5-115">Gibt an, dass *LPARAM* die Client Koordinaten des Zeigers enthält.</span><span class="sxs-lookup"><span data-stu-id="947f5-115">Indicates that *lParam* holds the client coordinates of the pointer.</span></span><br/> |
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="947f5-116"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="947f5-116"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="947f5-117">Gibt an, dass *LPARAM* einen unter Teiler-Indexwert enthält.</span><span class="sxs-lookup"><span data-stu-id="947f5-117">Indicates that *lParam* holds a divider index value.</span></span><br/>                 |



 

</dd> <dt>

<span data-ttu-id="947f5-118">*lParam*</span><span class="sxs-lookup"><span data-stu-id="947f5-118">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="947f5-119">Ein in *LPARAM* gehaltene Wert wird abhängig vom Wert von *wParam* interpretiert.</span><span class="sxs-lookup"><span data-stu-id="947f5-119">A value held in *lParam* is interpreted depending on the value of *wParam*.</span></span>

<span data-ttu-id="947f5-120">Wenn *wParam* den Wert **true** hat, stellt *LPARAM* die x-und y-Koordinaten des Zeigers dar.</span><span class="sxs-lookup"><span data-stu-id="947f5-120">If *wParam* is **TRUE**, *lParam* represents the x- and y-coordinates of the pointer.</span></span> <span data-ttu-id="947f5-121">Die x-Koordinate ist das niedrige Wort, und die y-Koordinate befindet sich im hohen Wort.</span><span class="sxs-lookup"><span data-stu-id="947f5-121">The x-coordinate is in the low word, and the y-coordinate is in the high word.</span></span> <span data-ttu-id="947f5-122">Wenn das Header Steuerelement die Nachricht empfängt, wird der entsprechende unter Teiler basierend auf den *LPARAM* -Koordinaten hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="947f5-122">When the header control receives the message, it highlights the appropriate divider based on the *lParam* coordinates.</span></span>

<span data-ttu-id="947f5-123">Wenn *wParam* den Wert **false** hat, stellt *LPARAM* den ganzzahligen Index des unter Teilers dar, der hervorgehoben werden soll.</span><span class="sxs-lookup"><span data-stu-id="947f5-123">If *wParam* is **FALSE**, *lParam* represents the integer index of the divider to be highlighted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="947f5-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="947f5-124">Return value</span></span>

<span data-ttu-id="947f5-125">Gibt einen Wert zurück, der gleich dem Index des unter Teilers ist, den das Steuerelement hervorgehoben hat.</span><span class="sxs-lookup"><span data-stu-id="947f5-125">Returns a value equal to the index of the divider that the control highlighted.</span></span>

## <a name="remarks"></a><span data-ttu-id="947f5-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="947f5-126">Remarks</span></span>

<span data-ttu-id="947f5-127">Diese Meldung erzeugt einen Effekt, den ein Header Steuerelement automatisch erzeugt, wenn es den [**HDS \_ DragDrop**](header-control-styles.md) -Stil aufweist.</span><span class="sxs-lookup"><span data-stu-id="947f5-127">This message creates an effect that a header control automatically produces when it has the [**HDS\_DRAGDROP**](header-control-styles.md) style.</span></span> <span data-ttu-id="947f5-128">Die **HDM-Nachricht " \_ sthotdivider** " soll verwendet werden, wenn der Besitzer des Steuer Elements Drag & Drop-Vorgänge manuell behandelt.</span><span class="sxs-lookup"><span data-stu-id="947f5-128">The **HDM\_SETHOTDIVIDER** message is intended to be used when the owner of the control handles drag-and-drop operations manually.</span></span>

## <a name="requirements"></a><span data-ttu-id="947f5-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="947f5-129">Requirements</span></span>



| <span data-ttu-id="947f5-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="947f5-130">Requirement</span></span> | <span data-ttu-id="947f5-131">Wert</span><span class="sxs-lookup"><span data-stu-id="947f5-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="947f5-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="947f5-132">Minimum supported client</span></span><br/> | <span data-ttu-id="947f5-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="947f5-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="947f5-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="947f5-134">Minimum supported server</span></span><br/> | <span data-ttu-id="947f5-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="947f5-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="947f5-136">Header</span><span class="sxs-lookup"><span data-stu-id="947f5-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="947f5-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="947f5-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





