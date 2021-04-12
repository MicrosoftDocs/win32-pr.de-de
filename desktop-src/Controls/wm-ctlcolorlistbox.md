---
title: WM_CTLCOLORLISTBOX Meldung (Winuser. h)
description: Wird an das übergeordnete Fenster eines Listen Felds gesendet, bevor das System das Listenfeld zeichnet. Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster die Text-und Hintergrundfarben des Listen Felds mit dem angegebenen Kontext Handle für den Anzeigegerät festlegen.
ms.assetid: e128e77f-e966-44c4-9f0e-efcf421b6c82
keywords:
- Windows-Steuerelemente für WM_CTLCOLORLISTBOX Meldung
topic_type:
- apiref
api_name:
- WM_CTLCOLORLISTBOX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e949af76bd05aa9ad3a3e720c89be33cfe76ed8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103547"
---
# <a name="wm_ctlcolorlistbox-message"></a><span data-ttu-id="5e5cd-105">\_Ctlcolorlistbox-Nachricht für WM</span><span class="sxs-lookup"><span data-stu-id="5e5cd-105">WM\_CTLCOLORLISTBOX message</span></span>

<span data-ttu-id="5e5cd-106">Wird an das übergeordnete Fenster eines Listen Felds gesendet, bevor das System das Listenfeld zeichnet.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-106">Sent to the parent window of a list box before the system draws the list box.</span></span> <span data-ttu-id="5e5cd-107">Wenn Sie auf diese Meldung reagieren, kann das übergeordnete Fenster die Text-und Hintergrundfarben des Listen Felds mit dem angegebenen Kontext Handle für den Anzeigegerät festlegen.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-107">By responding to this message, the parent window can set the text and background colors of the list box by using the specified display device context handle.</span></span>


```C++
WM_CTLCOLORLISTBOX

    WPARAM wParam;
    LPARAM lParam; 
```



## <a name="parameters"></a><span data-ttu-id="5e5cd-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e5cd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e5cd-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5e5cd-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e5cd-110">Handle für den Gerätekontext für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-110">Handle to the device context for the list box.</span></span>

</dd> <dt>

<span data-ttu-id="5e5cd-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5e5cd-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5e5cd-112">Handle für das Listenfeld.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-112">Handle to the list box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e5cd-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e5cd-113">Return value</span></span>

<span data-ttu-id="5e5cd-114">Wenn eine Anwendung diese Nachricht verarbeitet, muss Sie ein Handle für einen Pinsel zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-114">If an application processes this message, it must return a handle to a brush.</span></span> <span data-ttu-id="5e5cd-115">Das System verwendet den Pinsel zum Zeichnen des Hintergrunds des Listen Felds.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-115">The system uses the brush to paint the background of the list box.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e5cd-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e5cd-116">Remarks</span></span>

<span data-ttu-id="5e5cd-117">Standardmäßig wählt die [**defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) -Funktion die Standardsystem Farben für das Listenfeld aus.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-117">By default, the [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) function selects the default system colors for the list box.</span></span>

<span data-ttu-id="5e5cd-118">Die " **WM \_ ctlcolorlistbox** "-Meldung wird nie zwischen Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-118">The **WM\_CTLCOLORLISTBOX** message is never sent between threads.</span></span> <span data-ttu-id="5e5cd-119">Sie wird nur innerhalb eines Threads gesendet.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-119">It is sent only within one thread.</span></span>

<span data-ttu-id="5e5cd-120">Wenn eine Dialogfeld Prozedur diese Nachricht behandelt, sollte Sie den gewünschten Rückgabewert in ein **int- \_ ptr** umwandeln und den Wert direkt zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-120">If a dialog box procedure handles this message, it should cast the desired return value to a **INT\_PTR** and return the value directly.</span></span> <span data-ttu-id="5e5cd-121">Wenn die Dialogfeld Prozedur **false** zurückgibt, wird die standardmäßige Nachrichtenverarbeitung ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-121">If the dialog box procedure returns **FALSE**, then default message handling is performed.</span></span> <span data-ttu-id="5e5cd-122">Der von der [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion festgelegte **DWL- \_ msgresult** -Wert wird ignoriert.</span><span class="sxs-lookup"><span data-stu-id="5e5cd-122">The **DWL\_MSGRESULT** value set by the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e5cd-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e5cd-123">Requirements</span></span>



| <span data-ttu-id="5e5cd-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5e5cd-124">Requirement</span></span> | <span data-ttu-id="5e5cd-125">Wert</span><span class="sxs-lookup"><span data-stu-id="5e5cd-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e5cd-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5e5cd-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5e5cd-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e5cd-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="5e5cd-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5e5cd-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5e5cd-129">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5e5cd-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5e5cd-130">Header</span><span class="sxs-lookup"><span data-stu-id="5e5cd-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="5e5cd-131"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5e5cd-131"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e5cd-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5e5cd-132">See also</span></span>

<dl> <dt>

<span data-ttu-id="5e5cd-133">**Andere Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5e5cd-133">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="5e5cd-134">**RealizePalette**</span><span class="sxs-lookup"><span data-stu-id="5e5cd-134">**RealizePalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-realizepalette)
</dt> <dt>

[<span data-ttu-id="5e5cd-135">**SelectPalette**</span><span class="sxs-lookup"><span data-stu-id="5e5cd-135">**SelectPalette**</span></span>](/windows/desktop/api/wingdi/nf-wingdi-selectpalette)
</dt> <dt>

[<span data-ttu-id="5e5cd-136">**DefWindowProc**</span><span class="sxs-lookup"><span data-stu-id="5e5cd-136">**DefWindowProc**</span></span>](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> </dl>

 

