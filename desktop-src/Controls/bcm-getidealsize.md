---
title: BCM_GETIDEALSIZE Meldung (kommstrg. h)
description: Ruft die Größe der Schaltfläche ab, die den Text und das Bild am besten anpasst, wenn eine Bildliste vorhanden ist. Sie können diese Nachricht explizit senden oder das \_ getidealsize-Makro der Schaltfläche verwenden.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- Windows-Steuerelemente für BCM_GETIDEALSIZE Meldung
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339570"
---
# <a name="bcm_getidealsize-message"></a><span data-ttu-id="c86f4-105">BCM- \_ getidealsize-Meldung</span><span class="sxs-lookup"><span data-stu-id="c86f4-105">BCM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="c86f4-106">Ruft die Größe der Schaltfläche ab, die den Text und das Bild am besten anpasst, wenn eine Bildliste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c86f4-106">Gets the size of the button that best fits its text and image, if an image list is present.</span></span> <span data-ttu-id="c86f4-107">Sie können diese Nachricht explizit senden oder das [**\_ getidealsize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) -Makro der Schaltfläche verwenden.</span><span class="sxs-lookup"><span data-stu-id="c86f4-107">You can send this message explicitly or use the [**Button\_GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="c86f4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="c86f4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c86f4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="c86f4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c86f4-110">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="c86f4-110">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="c86f4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="c86f4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="c86f4-112">Ein Zeiger auf eine [**Größen**](/previous-versions//dd145106(v=vs.85)) Struktur, die die gewünschte Größe der Schaltfläche erhält, einschließlich Text und Bildliste, falls vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c86f4-112">A pointer to a [**SIZE**](/previous-versions//dd145106(v=vs.85)) structure that receives the desired size of the button, including text and image list, if present.</span></span> <span data-ttu-id="c86f4-113">Die aufrufenden Anwendung ist für die Zuordnung dieser Struktur verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="c86f4-113">The calling application is responsible for allocating this structure.</span></span> <span data-ttu-id="c86f4-114">Legen Sie die Member **CX** und **CY** auf NULL fest, um die ideale Höhe und Breite in der **Größen** Struktur zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c86f4-114">Set the **cx** and **cy** members to zero to have the ideal height and width returned in the **SIZE** structure.</span></span> <span data-ttu-id="c86f4-115">Zum Angeben einer Schaltflächen breite legen Sie den **CX** -Member auf die gewünschte Schaltflächen Breite fest.</span><span class="sxs-lookup"><span data-stu-id="c86f4-115">To specify a button width, set the **cx** member to the desired button width.</span></span> <span data-ttu-id="c86f4-116">Das System berechnet die ideale Höhe für diese Breite und gibt Sie im **CY** -Element zurück.</span><span class="sxs-lookup"><span data-stu-id="c86f4-116">The system will calculate the ideal height for this width and return it in the **cy** member.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c86f4-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c86f4-117">Return value</span></span>

<span data-ttu-id="c86f4-118">Wenn die Nachricht erfolgreich ist, wird **true** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c86f4-118">If the message succeeds, it returns **TRUE**.</span></span> <span data-ttu-id="c86f4-119">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c86f4-119">Otherwise it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c86f4-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c86f4-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="c86f4-121">Wenn keine spezielle Schaltflächen breite gewünscht ist, müssen Sie beide Member der [**Größe**](/previous-versions//dd145106(v=vs.85)) auf NULL festlegen, um die ideale Höhe und Breite zu berechnen und zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="c86f4-121">If no special button width is desired, then you must set both members of [**SIZE**](/previous-versions//dd145106(v=vs.85)) to zero to calculate and return the ideal height and width.</span></span> <span data-ttu-id="c86f4-122">Wenn der Wert des **CX** -Members größer als 0 (null) ist, wird dieser Wert als gewünschte Schaltflächen breite betrachtet, und die ideale Höhe für diese Breite wird berechnet und im **CY** -Element zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c86f4-122">If the value of the **cx** member is greater than zero, then this value is considered the desired button width, and the ideal height for this width is calculated and returned in the **cy** member.</span></span>

 

<span data-ttu-id="c86f4-123">Diese Meldung ist am häufigsten auf Pushbuttons anwendbar.</span><span class="sxs-lookup"><span data-stu-id="c86f4-123">This message is most applicable to PushButtons.</span></span> <span data-ttu-id="c86f4-124">Beim Senden an einen PUSHBUTTON Ruft die Nachricht das umgebende Rechteck ab, das zum Anzeigen des Schaltflächen Texts erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="c86f4-124">When sent to a PushButton, the message retrieves the bounding rectangle required to display the button's text.</span></span> <span data-ttu-id="c86f4-125">Wenn der PUSHBUTTON außerdem eine Bildliste aufweist, wird das umgebende Rechteck ebenfalls so vergrößert, dass es das Bild der Schaltfläche enthält.</span><span class="sxs-lookup"><span data-stu-id="c86f4-125">Additionally, if the PushButton has an image list, the bounding rectangle is also sized to include the button's image.</span></span>

<span data-ttu-id="c86f4-126">Beim Senden an eine Schaltfläche eines beliebigen anderen Typs wird die Größe des Fenster Rechtecks des Steuer Elements abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c86f4-126">When sent to a button of any other type, the size of the control's window rectangle is retrieved.</span></span>

> [!Note]  
> <span data-ttu-id="c86f4-127">Um diese Meldung zu verwenden, müssen Sie ein Manifest bereitstellen, das Comclt32.dll Version 6,0 angibt.</span><span class="sxs-lookup"><span data-stu-id="c86f4-127">To use this message, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="c86f4-128">Weitere Informationen zu Manifesten finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).</span><span class="sxs-lookup"><span data-stu-id="c86f4-128">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="c86f4-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c86f4-129">Requirements</span></span>



| <span data-ttu-id="c86f4-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c86f4-130">Requirement</span></span> | <span data-ttu-id="c86f4-131">Wert</span><span class="sxs-lookup"><span data-stu-id="c86f4-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c86f4-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c86f4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="c86f4-133">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c86f4-133">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c86f4-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c86f4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="c86f4-135">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c86f4-135">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c86f4-136">Header</span><span class="sxs-lookup"><span data-stu-id="c86f4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="c86f4-137"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="c86f4-137"><dt>Commctrl.h</dt></span></span> </dl> |



 

