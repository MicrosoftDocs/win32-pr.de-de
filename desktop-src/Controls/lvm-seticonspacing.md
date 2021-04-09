---
title: LVM_SETICONSPACING Meldung (kommstrg. h)
description: Legt den Abstand zwischen Symbolen in Listenansicht-Steuerelementen fest, die den LVS- \_ Symbolstil aufweisen. Sie können diese Nachricht explizit oder mithilfe des ListView-Makros "$" senden \_ .
ms.assetid: 2dd3d9df-5b0d-445e-9201-d766fa218f90
keywords:
- Windows-Steuerelemente für LVM_SETICONSPACING Meldung
topic_type:
- apiref
api_name:
- LVM_SETICONSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 972435190ec21bb50db90640a589cef1e394318c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858654"
---
# <a name="lvm_seticonspacing-message"></a><span data-ttu-id="6b099-105">LVM- \_ Nachricht</span><span class="sxs-lookup"><span data-stu-id="6b099-105">LVM\_SETICONSPACING message</span></span>

<span data-ttu-id="6b099-106">Legt den Abstand zwischen Symbolen in Listenansicht-Steuerelementen fest, die den [**LVS- \_**](list-view-window-styles.md) Symbolstil aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b099-106">Sets the spacing between icons in list-view controls that have the [**LVS\_ICON**](list-view-window-styles.md) style.</span></span> <span data-ttu-id="6b099-107">Sie können diese Nachricht explizit oder mithilfe des [**ListView \_**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) -Makros "$" senden.</span><span class="sxs-lookup"><span data-stu-id="6b099-107">You can send this message explicitly or by using the [**ListView\_SetIconSpacing**](/windows/desktop/api/Commctrl/nf-commctrl-listview_seticonspacing) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="6b099-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b099-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b099-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="6b099-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b099-110">Muss Null sein.</span><span class="sxs-lookup"><span data-stu-id="6b099-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="6b099-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="6b099-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="6b099-112">Das [**LoWord**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der x-Achse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b099-112">The [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) specifies the distance, in pixels, to set between icons on the x-axis.</span></span> <span data-ttu-id="6b099-113">Das [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) gibt den Abstand in Pixel an, der zwischen Symbolen auf der y-Achse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b099-113">The [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) specifies the distance, in pixels, to set between icons on the y-axis.</span></span> <span data-ttu-id="6b099-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="6b099-114">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b099-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6b099-115">Return value</span></span>

<span data-ttu-id="6b099-116">Gibt einen **DWORD** -Wert zurück, der den vorherigen Abstand der x-Achse im unteren Wort und den vorherigen Abstand der y-Achse im hohen Wort enthält.</span><span class="sxs-lookup"><span data-stu-id="6b099-116">Returns a **DWORD** value that contains the previous x-axis distance in the low word, and the previous y-axis distance in the high word.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b099-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b099-117">Remarks</span></span>

<span data-ttu-id="6b099-118">Die Werte für *LPARAM* sind relativ zur oberen linken Ecke einer Symbol Bitmap.</span><span class="sxs-lookup"><span data-stu-id="6b099-118">Values for *lParam* are relative to the upper-left corner of an icon bitmap.</span></span> <span data-ttu-id="6b099-119">Um den Abstand zwischen Symbolen festzulegen, die sich nicht überlappen, müssen die *LPARAM* -Werte beispielsweise die Größe des Symbols und den von den Symbolen gewünschten leeren Bereich enthalten.</span><span class="sxs-lookup"><span data-stu-id="6b099-119">Therefore, to set spacing between icons that do not overlap, the *lParam* values must include the size of the icon, plus the amount of empty space desired between icons.</span></span> <span data-ttu-id="6b099-120">Werte, die die Breite des Symbols nicht einschließen, führen zu Überlappungen.</span><span class="sxs-lookup"><span data-stu-id="6b099-120">Values that do not include the width of the icon will result in overlaps.</span></span>

<span data-ttu-id="6b099-121">Wenn Sie den Symbol Abstand definieren, müssen die *LPARAM* -Werte auf 4 oder größer festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6b099-121">When defining the icon spacing, the *lParam* values must set to 4 or larger.</span></span> <span data-ttu-id="6b099-122">Kleinere Werte ergeben nicht das gewünschte Layout.</span><span class="sxs-lookup"><span data-stu-id="6b099-122">Smaller values will not yield the desired layout.</span></span> <span data-ttu-id="6b099-123">Wenn Sie die Symbole auf den Standardabstand zurücksetzen möchten, legen Sie die *LPARAM* -Werte auf-1 fest.</span><span class="sxs-lookup"><span data-stu-id="6b099-123">To reset the icons to the default spacing, set the *lParam* values to -1.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b099-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b099-124">Requirements</span></span>



| <span data-ttu-id="6b099-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b099-125">Requirement</span></span> | <span data-ttu-id="6b099-126">Wert</span><span class="sxs-lookup"><span data-stu-id="6b099-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b099-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6b099-127">Minimum supported client</span></span><br/> | <span data-ttu-id="6b099-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b099-128">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6b099-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6b099-129">Minimum supported server</span></span><br/> | <span data-ttu-id="6b099-130">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6b099-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6b099-131">Header</span><span class="sxs-lookup"><span data-stu-id="6b099-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b099-132"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b099-132"><dt>Commctrl.h</dt></span></span> </dl> |



 

