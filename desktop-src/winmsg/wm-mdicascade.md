---
description: Eine Anwendung sendet die WM- \_ mdicascade-Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierenden Format anzuordnen.
ms.assetid: 33d04859-4220-40a6-be46-74a812a44ca8
title: WM_MDICASCADE Meldung (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6208ce924ab6185399f3f673a435e1fbaca2741
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343199"
---
# <a name="wm_mdicascade-message"></a><span data-ttu-id="cb4b9-103">WM- \_ mdicascade-Nachricht</span><span class="sxs-lookup"><span data-stu-id="cb4b9-103">WM\_MDICASCADE message</span></span>

<span data-ttu-id="cb4b9-104">Eine Anwendung sendet die **WM- \_ mdicascade** -Nachricht an ein MDI-Client Fenster (Multiple Document Interface), um alle untergeordneten Fenster in einem kaskadierenden Format anzuordnen.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-104">An application sends the **WM\_MDICASCADE** message to a multiple-document interface (MDI) client window to arrange all its child windows in a cascade format.</span></span>


```C++
#define WM_MDICASCADE                   0x0227
```



## <a name="parameters"></a><span data-ttu-id="cb4b9-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb4b9-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb4b9-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cb4b9-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4b9-107">Das Überlappungsverhalten.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-107">The cascade behavior.</span></span> <span data-ttu-id="cb4b9-108">Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-108">This parameter can be one or more of the following values.</span></span>



| <span data-ttu-id="cb4b9-109">Wert</span><span class="sxs-lookup"><span data-stu-id="cb4b9-109">Value</span></span>                                                                                                                                                                                                                                          | <span data-ttu-id="cb4b9-110">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cb4b9-110">Meaning</span></span>                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <span id="MDITILE_SKIPDISABLED"></span><span id="mditile_skipdisabled"></span><dl> <span data-ttu-id="cb4b9-111"><dt>**Mditile \_ Überspringen**</dt> von <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="cb4b9-111"><dt>**MDITILE\_SKIPDISABLED**</dt> <dt>0x0002</dt></span></span> </dl> | <span data-ttu-id="cb4b9-112">Verhindert, dass deaktivierte untergeordnete MDI-Fenster kaskadiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-112">Prevents disabled MDI child windows from being cascaded.</span></span> <br/> |
| <span id="MDITILE_ZORDER"></span><span id="mditile_zorder"></span><dl> <span data-ttu-id="cb4b9-113"><dt>**Mditile \_ ZOrder**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="cb4b9-113"><dt>**MDITILE\_ZORDER**</dt> <dt>0x0004</dt></span></span> </dl>                   | <span data-ttu-id="cb4b9-114">Ordnet die Fenster in der Z-Reihenfolge an.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-114">Arranges the windows in Z order.</span></span><br/>                          |



 

</dd> <dt>

<span data-ttu-id="cb4b9-115">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cb4b9-115">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="cb4b9-116">Dieser Parameter wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-116">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb4b9-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb4b9-117">Return value</span></span>

<span data-ttu-id="cb4b9-118">Typ: **bool**</span><span class="sxs-lookup"><span data-stu-id="cb4b9-118">Type: **BOOL**</span></span>

<span data-ttu-id="cb4b9-119">Wenn die Nachricht erfolgreich ist, ist der Rückgabewert " **true**".</span><span class="sxs-lookup"><span data-stu-id="cb4b9-119">If the message succeeds, the return value is **TRUE**.</span></span>

<span data-ttu-id="cb4b9-120">Wenn die Meldung fehlschlägt, ist der Rückgabewert **false**.</span><span class="sxs-lookup"><span data-stu-id="cb4b9-120">If the message fails, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb4b9-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb4b9-121">Requirements</span></span>



| <span data-ttu-id="cb4b9-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb4b9-122">Requirement</span></span> | <span data-ttu-id="cb4b9-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cb4b9-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb4b9-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cb4b9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb4b9-125">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb4b9-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cb4b9-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cb4b9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb4b9-127">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cb4b9-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="cb4b9-128">Header</span><span class="sxs-lookup"><span data-stu-id="cb4b9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="cb4b9-129"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="cb4b9-129"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cb4b9-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb4b9-130">See also</span></span>

<dl> <dt>

<span data-ttu-id="cb4b9-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="cb4b9-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cb4b9-132">**WM- \_ mdiiconarrange**</span><span class="sxs-lookup"><span data-stu-id="cb4b9-132">**WM\_MDIICONARRANGE**</span></span>](wm-mdiiconarrange.md)
</dt> <dt>

[<span data-ttu-id="cb4b9-133">**WM- \_ mditile**</span><span class="sxs-lookup"><span data-stu-id="cb4b9-133">**WM\_MDITILE**</span></span>](wm-mditile.md)
</dt> <dt>

<span data-ttu-id="cb4b9-134">**Licher**</span><span class="sxs-lookup"><span data-stu-id="cb4b9-134">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="cb4b9-135">Mehrere Dokument Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="cb4b9-135">Multiple Document Interface</span></span>](multiple-document-interface.md)
</dt> </dl>

 

 




