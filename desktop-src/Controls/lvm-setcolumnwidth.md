---
title: LVM_SETCOLUMNWIDTH Meldung (kommstrg. h)
description: Ändert die Breite einer Spalte im Berichts Ansichtsmodus oder die Breite aller Spalten im Listen Ansichtsmodus. Sie können diese Nachricht explizit senden oder das ListView \_ setcolumnwidth-Makro verwenden.
ms.assetid: 309aebfb-9fed-4c77-acbb-ea905b32b0e2
keywords:
- Windows-Steuerelemente für LVM_SETCOLUMNWIDTH Meldung
topic_type:
- apiref
api_name:
- LVM_SETCOLUMNWIDTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 529e989b3d66562acc7b6f91c3b3b06527235e8e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104102891"
---
# <a name="lvm_setcolumnwidth-message"></a><span data-ttu-id="9e167-105">LVM- \_ setcolumnwidth-Nachricht</span><span class="sxs-lookup"><span data-stu-id="9e167-105">LVM\_SETCOLUMNWIDTH message</span></span>

<span data-ttu-id="9e167-106">Ändert die Breite einer Spalte im Berichts Ansichtsmodus oder die Breite aller Spalten im Listen Ansichtsmodus.</span><span class="sxs-lookup"><span data-stu-id="9e167-106">Changes the width of a column in report-view mode or the width of all columns in list-view mode.</span></span> <span data-ttu-id="9e167-107">Sie können diese Nachricht explizit senden oder das [**ListView \_ setcolumnwidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) -Makro verwenden.</span><span class="sxs-lookup"><span data-stu-id="9e167-107">You can send this message explicitly or use the [**ListView\_SetColumnWidth**](/windows/desktop/api/Commctrl/nf-commctrl-listview_setcolumnwidth) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="9e167-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e167-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e167-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9e167-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e167-110">NULL basierter Index einer gültigen Spalte.</span><span class="sxs-lookup"><span data-stu-id="9e167-110">Zero-based index of a valid column.</span></span> <span data-ttu-id="9e167-111">Für den Listen Ansichtsmodus muss dieser Parameter auf 0 (null) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="9e167-111">For list-view mode, this parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="9e167-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9e167-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9e167-113">Die neue Breite der Spalte in Pixel.</span><span class="sxs-lookup"><span data-stu-id="9e167-113">New width of the column, in pixels.</span></span> <span data-ttu-id="9e167-114">Für den Berichts Ansichtsmodus werden die folgenden speziellen Werte unterstützt:</span><span class="sxs-lookup"><span data-stu-id="9e167-114">For report-view mode, the following special values are supported:</span></span>



| <span data-ttu-id="9e167-115">Wert</span><span class="sxs-lookup"><span data-stu-id="9e167-115">Value</span></span>                                                                                                                                                                                           | <span data-ttu-id="9e167-116">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="9e167-116">Meaning</span></span>                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LVSCW_AUTOSIZE"></span><span id="lvscw_autosize"></span><dl> <span data-ttu-id="9e167-117"><dt>**Automatische Größe des lvscw \_**</dt></span><span class="sxs-lookup"><span data-stu-id="9e167-117"><dt>**LVSCW\_AUTOSIZE**</dt></span></span> </dl>                                | <span data-ttu-id="9e167-118">Passt die Größe der Spalte automatisch an.</span><span class="sxs-lookup"><span data-stu-id="9e167-118">Automatically sizes the column.</span></span><br/>                                                                                                                                           |
| <span id="LVSCW_AUTOSIZE_USEHEADER"></span><span id="lvscw_autosize_useheader"></span><dl> <span data-ttu-id="9e167-119"><dt>**"lvscw \_ AutoSize"- \_ useheader**</dt></span><span class="sxs-lookup"><span data-stu-id="9e167-119"><dt>**LVSCW\_AUTOSIZE\_USEHEADER**</dt></span></span> </dl> | <span data-ttu-id="9e167-120">Passt die Größe der Spalte automatisch an den Header Text an.</span><span class="sxs-lookup"><span data-stu-id="9e167-120">Automatically sizes the column to fit the header text.</span></span> <span data-ttu-id="9e167-121">Wenn Sie diesen Wert mit der letzten Spalte verwenden, wird seine Breite so festgelegt, dass die verbleibende Breite des Listenansicht-Steuer Elements ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="9e167-121">If you use this value with the last column, its width is set to fill the remaining width of the list-view control.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e167-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e167-122">Return value</span></span>

<span data-ttu-id="9e167-123">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9e167-123">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e167-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e167-124">Remarks</span></span>

<span data-ttu-id="9e167-125">Angenommen, Sie verfügen über ein zweispaltige Listenansicht-Steuerelement mit einer Breite von 500 Pixeln.</span><span class="sxs-lookup"><span data-stu-id="9e167-125">Assume that you have a 2-column list-view control with a width of 500 pixels.</span></span> <span data-ttu-id="9e167-126">Wenn die Breite der Spalte NULL auf 200 Pixel festgelegt ist und Sie diese Nachricht mit *wParam* = 1 und *LPARAM* = lvscw \_ AutoSize \_ useheader senden, wird die zweite (und letzte) Spalte 300 Pixel breit.</span><span class="sxs-lookup"><span data-stu-id="9e167-126">If the width of column zero is set to 200 pixels, and you send this message with *wParam* = 1 and *lParam* = LVSCW\_AUTOSIZE\_USEHEADER, the second (and last) column will be 300 pixels wide.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e167-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e167-127">Requirements</span></span>



| <span data-ttu-id="9e167-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e167-128">Requirement</span></span> | <span data-ttu-id="9e167-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9e167-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9e167-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9e167-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9e167-131">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e167-131">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9e167-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9e167-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9e167-133">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9e167-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9e167-134">Header</span><span class="sxs-lookup"><span data-stu-id="9e167-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e167-135"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e167-135"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





