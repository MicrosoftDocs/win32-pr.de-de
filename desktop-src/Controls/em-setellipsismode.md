---
title: EM_SETELLIPSISMODE Meldung (RichEdit. h)
description: Diese Meldung legt den aktuellen Ellipsen Modus fest.
ms.assetid: C77263E8-424B-4EDE-ACBF-BA85248FC31F
keywords:
- Windows-Steuerelemente für EM_SETELLIPSISMODE Meldung
topic_type:
- apiref
api_name:
- EM_SETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ae3b51dc80ed11d71f4af9c292657b2cf16728
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040898"
---
# <a name="em_setellipsismode-message"></a><span data-ttu-id="d2d0e-104">Nachricht "em \_ abtellipsismode"</span><span class="sxs-lookup"><span data-stu-id="d2d0e-104">EM\_SETELLIPSISMODE message</span></span>

<span data-ttu-id="d2d0e-105">Diese Meldung legt den aktuellen Ellipsen Modus fest.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-105">This message sets the current ellipsis mode.</span></span> <span data-ttu-id="d2d0e-106">Wenn diese Option aktiviert ist, wird ein Auslassungs Zeichen () für Text angezeigt, der nicht in das Anzeige Fenster passt.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="d2d0e-107">Die Ellipse wird nur verwendet, wenn das Steuerelement nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-107">The ellipsis is only used when the control isn t active.</span></span> <span data-ttu-id="d2d0e-108">Wenn aktiv, werden Scrollleisten verwendet, um Text anzuzeigen, der nicht in das Anzeige Fenster passt.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_SETELLIPSISMODE       (WM_USER + 306)
```



## <a name="parameters"></a><span data-ttu-id="d2d0e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2d0e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2d0e-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="d2d0e-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d0e-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="d2d0e-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="d2d0e-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="d2d0e-113">Ein DWORD, das einen der folgenden Werte empfängt.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-113">A DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="d2d0e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d2d0e-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="d2d0e-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="d2d0e-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="d2d0e-116"><dt>**Ellipse \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="d2d0e-117">Es werden keine Ellipse verwendet.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="d2d0e-118"><dt>**Ende der Auslassungs \_ Punkte**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="d2d0e-119">Ellipse am Ende (erzwungene Unterbrechung).</span><span class="sxs-lookup"><span data-stu-id="d2d0e-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="d2d0e-120"><dt>**Ellipse- \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="d2d0e-121">Ellipse am Ende (Wort Umbruch).</span><span class="sxs-lookup"><span data-stu-id="d2d0e-121">Ellipsis at the end (word break).</span></span><br/>   |



 

<span data-ttu-id="d2d0e-122">Die Bits für diese Werte sind alle in die **Ellipse- \_ Maske** passen.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-122">The bits for these values all fit in the **ELLIPSIS\_MASK**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2d0e-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d2d0e-123">Return value</span></span>

<span data-ttu-id="d2d0e-124">Wenn wParam gleich 0 und lParam einer der Werte in der obigen Tabelle ist, ist der Rückgabewert true. Andernfalls ist der Rückgabewert false.</span><span class="sxs-lookup"><span data-stu-id="d2d0e-124">If wparam is 0 and lparam is one of the values in the table above, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2d0e-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d2d0e-125">Requirements</span></span>



| <span data-ttu-id="d2d0e-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2d0e-126">Requirement</span></span> | <span data-ttu-id="d2d0e-127">Wert</span><span class="sxs-lookup"><span data-stu-id="d2d0e-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d2d0e-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2d0e-128">Minimum supported client</span></span><br/> | <span data-ttu-id="d2d0e-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2d0e-129">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d2d0e-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2d0e-130">Minimum supported server</span></span><br/> | <span data-ttu-id="d2d0e-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2d0e-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d2d0e-132">Header</span><span class="sxs-lookup"><span data-stu-id="d2d0e-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2d0e-133"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="d2d0e-133"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2d0e-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d2d0e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2d0e-135">**EM \_ getellipsismode**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-135">**EM\_GETELLIPSISMODE**</span></span>](em-getellipsismode.md)
</dt> <dt>

[<span data-ttu-id="d2d0e-136">**EM \_ getellipsisstate**</span><span class="sxs-lookup"><span data-stu-id="d2d0e-136">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





