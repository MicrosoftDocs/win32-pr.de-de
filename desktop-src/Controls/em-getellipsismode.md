---
title: EM_GETELLIPSISMODE Meldung (RichEdit. h)
description: Ruft den aktuellen Ellipsen Modus ab.
ms.assetid: 01A755F3-6C6E-4974-9866-76BF15E0F3AD
keywords:
- Windows-Steuerelemente für EM_GETELLIPSISMODE Meldung
topic_type:
- apiref
api_name:
- EM_GETELLIPSISMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09b7273cbfd6e87b4591c00267860c9a164aad5e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103785"
---
# <a name="em_getellipsismode-message"></a><span data-ttu-id="74ee7-104">EM \_ getellipsismode-Meldung</span><span class="sxs-lookup"><span data-stu-id="74ee7-104">EM\_GETELLIPSISMODE message</span></span>

<span data-ttu-id="74ee7-105">Ruft den aktuellen Ellipsen Modus ab.</span><span class="sxs-lookup"><span data-stu-id="74ee7-105">Retrieves the current ellipsis mode.</span></span> <span data-ttu-id="74ee7-106">Wenn diese Option aktiviert ist, wird ein Auslassungs Zeichen () für Text angezeigt, der nicht in das Anzeige Fenster passt.</span><span class="sxs-lookup"><span data-stu-id="74ee7-106">When enabled, an ellipsis ( ) is displayed for text that doesn t fit in the display window.</span></span> <span data-ttu-id="74ee7-107">Die Ellipse wird nur verwendet, wenn das Steuerelement nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="74ee7-107">The ellipsis is only used when the control is not active.</span></span> <span data-ttu-id="74ee7-108">Wenn aktiv, werden Scrollleisten verwendet, um Text anzuzeigen, der nicht in das Anzeige Fenster passt.</span><span class="sxs-lookup"><span data-stu-id="74ee7-108">When active, scroll bars are used to reveal text that doesn t fit into the display window.</span></span>


```C++
#define EM_GETELLIPSISMODE       (WM_USER + 305)
```



## <a name="parameters"></a><span data-ttu-id="74ee7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="74ee7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="74ee7-110">*wParam*</span><span class="sxs-lookup"><span data-stu-id="74ee7-110">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ee7-111">Nicht verwendet; muss 0 (null) sein.</span><span class="sxs-lookup"><span data-stu-id="74ee7-111">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="74ee7-112">*lParam*</span><span class="sxs-lookup"><span data-stu-id="74ee7-112">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="74ee7-113">Zeiger auf ein DWORD-Wert, der einen der folgenden Werte empfängt.</span><span class="sxs-lookup"><span data-stu-id="74ee7-113">Pointer to a DWORD which receives one of the following values.</span></span>



| <span data-ttu-id="74ee7-114">Wert</span><span class="sxs-lookup"><span data-stu-id="74ee7-114">Value</span></span>                                                                                                                                                         | <span data-ttu-id="74ee7-115">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="74ee7-115">Meaning</span></span>                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ELLIPSIS_NONE"></span><span id="ellipsis_none"></span><dl> <span data-ttu-id="74ee7-116"><dt>**Ellipse \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="74ee7-116"><dt>**ELLIPSIS\_NONE**</dt></span></span> </dl> | <span data-ttu-id="74ee7-117">Es werden keine Ellipse verwendet.</span><span class="sxs-lookup"><span data-stu-id="74ee7-117">No ellipsis is used.</span></span><br/>                |
| <span id="ELLIPSIS_END"></span><span id="ellipsis_end"></span><dl> <span data-ttu-id="74ee7-118"><dt>**Ende der Auslassungs \_ Punkte**</dt></span><span class="sxs-lookup"><span data-stu-id="74ee7-118"><dt>**ELLIPSIS\_END**</dt></span></span> </dl>    | <span data-ttu-id="74ee7-119">Ellipse am Ende (erzwungene Unterbrechung).</span><span class="sxs-lookup"><span data-stu-id="74ee7-119">Ellipsis at the end (forced break).</span></span><br/> |
| <span id="ELLIPSIS_WORD"></span><span id="ellipsis_word"></span><dl> <span data-ttu-id="74ee7-120"><dt>**Ellipse- \_ Wort**</dt></span><span class="sxs-lookup"><span data-stu-id="74ee7-120"><dt>**ELLIPSIS\_WORD**</dt></span></span> </dl> | <span data-ttu-id="74ee7-121">Ellipse am Ende (Wort Umbruch).</span><span class="sxs-lookup"><span data-stu-id="74ee7-121">Ellipsis at the end (word break).</span></span><br/>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="74ee7-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="74ee7-122">Return value</span></span>

<span data-ttu-id="74ee7-123">Wenn wParam gleich 0 und lParam nicht NULL ist, ist der Rückgabewert true. Andernfalls ist der Rückgabewert false.</span><span class="sxs-lookup"><span data-stu-id="74ee7-123">If wparam is 0 and lparam is not NULL, the return value equals TRUE; otherwise, the return value equals FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="74ee7-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74ee7-124">Requirements</span></span>



| <span data-ttu-id="74ee7-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74ee7-125">Requirement</span></span> | <span data-ttu-id="74ee7-126">Wert</span><span class="sxs-lookup"><span data-stu-id="74ee7-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="74ee7-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="74ee7-127">Minimum supported client</span></span><br/> | <span data-ttu-id="74ee7-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ee7-128">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="74ee7-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="74ee7-129">Minimum supported server</span></span><br/> | <span data-ttu-id="74ee7-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="74ee7-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="74ee7-131">Header</span><span class="sxs-lookup"><span data-stu-id="74ee7-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="74ee7-132"><dt>RichEdit. h</dt></span><span class="sxs-lookup"><span data-stu-id="74ee7-132"><dt>Richedit.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74ee7-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74ee7-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74ee7-134">**EM/ \_ tellipsismode**</span><span class="sxs-lookup"><span data-stu-id="74ee7-134">**EM\_SETELLIPSISMODE**</span></span>](em-setellipsismode.md)
</dt> <dt>

[<span data-ttu-id="74ee7-135">**EM \_ getellipsisstate**</span><span class="sxs-lookup"><span data-stu-id="74ee7-135">**EM\_GETELLIPSISSTATE**</span></span>](em-getellipsisstate.md)
</dt> </dl>

 

 





