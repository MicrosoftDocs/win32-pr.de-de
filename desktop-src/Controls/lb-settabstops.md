---
title: LB_SETTABSTOPS Meldung (Winuser. h)
description: Legt die Position der Tabstopps in einem Listenfeld fest.
ms.assetid: b96b974e-b1e6-4361-98bb-4dc21c752690
keywords:
- Windows-Steuerelemente für LB_SETTABSTOPS Meldung
topic_type:
- apiref
api_name:
- LB_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f21927aaf82624242e8d42ef4a7459f1e36cdf74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859160"
---
# <a name="lb_settabstops-message"></a><span data-ttu-id="bb757-104">LB- \_ settabstopps-Meldung</span><span class="sxs-lookup"><span data-stu-id="bb757-104">LB\_SETTABSTOPS message</span></span>

<span data-ttu-id="bb757-105">Legt die Position der Tabstopps in einem Listenfeld fest.</span><span class="sxs-lookup"><span data-stu-id="bb757-105">Sets the tab-stop positions in a list box.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb757-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bb757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb757-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="bb757-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb757-108">Gibt die Anzahl der Tabstopps an.</span><span class="sxs-lookup"><span data-stu-id="bb757-108">Specifies the number of tab stops.</span></span>

</dd> <dt>

<span data-ttu-id="bb757-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="bb757-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="bb757-110">Zeiger auf den ersten Member eines Arrays von ganzen Zahlen, das die Tabstopps enthält.</span><span class="sxs-lookup"><span data-stu-id="bb757-110">Pointer to the first member of an array of integers containing the tab stops.</span></span> <span data-ttu-id="bb757-111">Die ganzen Zahlen stellen die Anzahl von Quartalen der durchschnittlichen Zeichenbreite für die Schriftart dar, die im Listenfeld ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="bb757-111">The integers represent the number of quarters of the average character width for the font that is selected into the list box.</span></span> <span data-ttu-id="bb757-112">Beispielsweise wird ein Tabstopp von 4 bei 1,0 Zeicheneinheiten platziert, und ein Tabstopp von 6 wird bei 1,5 durchschnittlichen Zeicheneinheiten platziert.</span><span class="sxs-lookup"><span data-stu-id="bb757-112">For example, a tab stop of 4 is placed at 1.0 character units, and a tab stop of 6 is placed at 1.5 average character units.</span></span> <span data-ttu-id="bb757-113">Wenn das Listenfeld jedoch Teil eines Dialog Felds ist, befinden sich die ganzen Zahlen in den Dialogfeld Vorlagen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="bb757-113">However, if the list box is part of a dialog box, the integers are in dialog template units.</span></span> <span data-ttu-id="bb757-114">Die Tabstopps müssen in aufsteigender Reihenfolge sortiert werden. rückwärts Registerkarten sind nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="bb757-114">The tab stops must be sorted in ascending order; backward tabs are not allowed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bb757-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bb757-115">Return value</span></span>

<span data-ttu-id="bb757-116">Wenn alle angegebenen Registerkarten festgelegt sind, ist der Rückgabewert " **true**". Andernfalls ist Sie **false**.</span><span class="sxs-lookup"><span data-stu-id="bb757-116">If all the specified tabs are set, the return value is **TRUE**; otherwise, it is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="bb757-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bb757-117">Remarks</span></span>

<span data-ttu-id="bb757-118">Um auf die **lb- \_ settabstopps** -Nachricht zu reagieren, muss das Listenfeld mit dem [**lbs- \_ UseTabStops**](list-box-styles.md) -Stil erstellt worden sein.</span><span class="sxs-lookup"><span data-stu-id="bb757-118">To respond to the **LB\_SETTABSTOPS** message, the list box must have been created with the [**LBS\_USETABSTOPS**](list-box-styles.md) style.</span></span>

<span data-ttu-id="bb757-119">Wenn *wParam* den Wert 0 hat und *LPARAM* den Wert **null** hat, handelt es sich beim Standard-Tabstopp um zwei Dialogfeld Vorlagen Einheiten.</span><span class="sxs-lookup"><span data-stu-id="bb757-119">If *wParam* is 0 and *lParam* is **NULL**, the default tab stop is two dialog template units.</span></span> <span data-ttu-id="bb757-120">Wenn *wParam* den Wert 1 hat, werden Tabstopps im Listenfeld durch die durch *LPARAM* angegebene Entfernung getrennt.</span><span class="sxs-lookup"><span data-stu-id="bb757-120">If *wParam* is 1, the list box will have tab stops separated by the distance specified by *lParam*.</span></span>

<span data-ttu-id="bb757-121">Wenn *LPARAM* auf mehr als einen einzelnen Wert verweist, wird für jeden Wert in *LPARAM* ein Tabstopp festgelegt, bis zu der von *wParam* angegebenen Zahl.</span><span class="sxs-lookup"><span data-stu-id="bb757-121">If *lParam* points to more than a single value, a tab stop will be set for each value in *lParam*, up to the number specified by *wParam*.</span></span>

<span data-ttu-id="bb757-122">Die von *LPARAM* angegebenen Werte befinden sich in Dialogfeld Vorlagen Einheiten, bei denen es sich um die geräteunabhängigen Einheiten handelt, die in Dialogfeld Vorlagen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bb757-122">The values specified by *lParam* are in dialog template units, which are the device-independent units used in dialog box templates.</span></span> <span data-ttu-id="bb757-123">Verwenden Sie die [**mapdialogrect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) -Funktion, um Messungen von Dialogfeld Vorlagen-Einheiten in Bildschirm Einheiten (Pixel) zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="bb757-123">To convert measurements from dialog template units to screen units (pixels), use the [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) function.</span></span>

<span data-ttu-id="bb757-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me): der Puffer, auf den *LPARAM* zeigt, muss sich in einem beschreibbaren Speicher befinden, auch wenn die Nachricht das Array nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="bb757-124">Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : The buffer pointed to by *lParam* must reside in writable memory, even though the message does not modify the array.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb757-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bb757-125">Requirements</span></span>



| <span data-ttu-id="bb757-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bb757-126">Requirement</span></span> | <span data-ttu-id="bb757-127">Wert</span><span class="sxs-lookup"><span data-stu-id="bb757-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb757-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bb757-128">Minimum supported client</span></span><br/> | <span data-ttu-id="bb757-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb757-129">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="bb757-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bb757-130">Minimum supported server</span></span><br/> | <span data-ttu-id="bb757-131">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bb757-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="bb757-132">Header</span><span class="sxs-lookup"><span data-stu-id="bb757-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb757-133"><dt>Winuser. h (Windows. h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="bb757-133"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb757-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb757-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb757-135">**Mapdialogrect**</span><span class="sxs-lookup"><span data-stu-id="bb757-135">**MapDialogRect**</span></span>](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

