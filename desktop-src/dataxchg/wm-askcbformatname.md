---
title: WM_ASKCBFORMATNAME Meldung (Winuser. h)
description: Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, um den Namen eines CF-Besitzer \_ Anzeige-Zwischenablage Formats anzufordern.
ms.assetid: eee026ec-58db-41b3-9705-30a17eebbd70
keywords:
- WM_ASKCBFORMATNAME Nachrichten Datenaustausch
topic_type:
- apiref
api_name:
- WM_ASKCBFORMATNAME
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b14a7f2fc2ff57076d6b694061466fd60e09dce0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103251"
---
# <a name="wm_askcbformatname-message"></a><span data-ttu-id="41739-104">WM- \_ askcbformatname-Meldung</span><span class="sxs-lookup"><span data-stu-id="41739-104">WM\_ASKCBFORMATNAME message</span></span>

<span data-ttu-id="41739-105">Wird von einem Fenster der Zwischenablage Anzeige an den Besitzer der Zwischenablage gesendet, um den Namen eines CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) -Zwischenablage Formats anzufordern.</span><span class="sxs-lookup"><span data-stu-id="41739-105">Sent to the clipboard owner by a clipboard viewer window to request the name of a [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) clipboard format.</span></span>

<span data-ttu-id="41739-106">Ein Fenster empfängt diese Meldung über seine [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="41739-106">A window receives this message through its [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) function.</span></span>


```C++
#define WM_ASKCBFORMATNAME              0x030C
```



## <a name="parameters"></a><span data-ttu-id="41739-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="41739-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41739-108">*wParam*</span><span class="sxs-lookup"><span data-stu-id="41739-108">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41739-109">Die Größe des Puffers in Zeichen, auf den der *LPARAM* -Parameter zeigt.</span><span class="sxs-lookup"><span data-stu-id="41739-109">The size, in characters, of the buffer pointed to by the *lParam* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="41739-110">*lParam*</span><span class="sxs-lookup"><span data-stu-id="41739-110">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="41739-111">Ein Zeiger auf den Puffer, der den Format Namen der Zwischenablage empfangen soll.</span><span class="sxs-lookup"><span data-stu-id="41739-111">A pointer to the buffer that is to receive the clipboard format name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41739-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41739-112">Return value</span></span>

<span data-ttu-id="41739-113">Wenn eine Anwendung diese Nachricht verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="41739-113">If an application processes this message, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="41739-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41739-114">Remarks</span></span>

<span data-ttu-id="41739-115">Als Antwort auf diese Nachricht sollte der Besitzer der Zwischenablage den Namen des Besitzers-Anzeige Formats in den angegebenen Puffer kopieren, wobei die vom *wParam* -Parameter angegebene Puffergröße nicht überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="41739-115">In response to this message, the clipboard owner should copy the name of the owner-display format to the specified buffer, not exceeding the buffer size specified by the *wParam* parameter.</span></span>

<span data-ttu-id="41739-116">Ein Fenster der Zwischenablage Anzeige sendet diese Nachricht an den Besitzer der Zwischenablage, um den Namen des CF-Besitzer [**\_ Anzeige**](standard-clipboard-formats.md) Formats zu ermitteln, um z. b. eine Menü Liste mit verfügbaren Formaten zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="41739-116">A clipboard viewer window sends this message to the clipboard owner to determine the name of the [**CF\_OWNERDISPLAY**](standard-clipboard-formats.md) format   for example, to initialize a menu listing available formats.</span></span>

## <a name="requirements"></a><span data-ttu-id="41739-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="41739-117">Requirements</span></span>



| <span data-ttu-id="41739-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="41739-118">Requirement</span></span> | <span data-ttu-id="41739-119">Wert</span><span class="sxs-lookup"><span data-stu-id="41739-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="41739-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="41739-120">Minimum supported client</span></span><br/> | <span data-ttu-id="41739-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41739-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="41739-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="41739-122">Minimum supported server</span></span><br/> | <span data-ttu-id="41739-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="41739-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="41739-124">Header</span><span class="sxs-lookup"><span data-stu-id="41739-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="41739-125"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="41739-125"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41739-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41739-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41739-127">Übersicht über Zwischenablage</span><span class="sxs-lookup"><span data-stu-id="41739-127">Clipboard Overview</span></span>](clipboard.md)
</dt> </dl>

 

