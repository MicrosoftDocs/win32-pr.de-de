---
title: LVN_GETDISPINFO Benachrichtigungs Code (kommctrl. h)
description: Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet. Es ist eine Anforderung für das übergeordnete Fenster, Informationen bereitzustellen, die zum Anzeigen oder Sortieren eines Listen Ansichts Elements erforderlich sind. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 04310e39-69bc-45d7-958c-00452279d7a9
keywords:
- Windows-Steuerelemente für LVN_GETDISPINFO Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_GETDISPINFO
- LVN_GETDISPINFOA
- LVN_GETDISPINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1585524dd447c4a1324dc5c7a235490de776fb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103744001"
---
# <a name="lvn_getdispinfo-notification-code"></a><span data-ttu-id="211d4-106">LVN \_ getdispinfo-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="211d4-106">LVN\_GETDISPINFO notification code</span></span>

<span data-ttu-id="211d4-107">Wird von einem Listenansicht-Steuerelement an das übergeordnete Fenster gesendet.</span><span class="sxs-lookup"><span data-stu-id="211d4-107">Sent by a list-view control to its parent window.</span></span> <span data-ttu-id="211d4-108">Es ist eine Anforderung für das übergeordnete Fenster, Informationen bereitzustellen, die zum Anzeigen oder Sortieren eines Listen Ansichts Elements erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="211d4-108">It is a request for the parent window to provide information needed to display or sort a list-view item.</span></span> <span data-ttu-id="211d4-109">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="211d4-109">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_GETDISPINFO
        
    pdi = (NMLVDISPINFO*) lParam
```



## <a name="parameters"></a><span data-ttu-id="211d4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="211d4-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="211d4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="211d4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="211d4-112">Zeiger auf eine [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="211d4-112">Pointer to an [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="211d4-113">Bei der Eingabe gibt die in dieser Struktur enthaltene [**lvitem**](/windows/win32/api/commctrl/ns-commctrl-lvitema) -Struktur den Typ der erforderlichen Informationen an und identifiziert das Element oder Unterelement, das von Interesse ist.</span><span class="sxs-lookup"><span data-stu-id="211d4-113">On input, the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure contained in this structure specifies the type of information required and identifies the item or subitem of interest.</span></span> <span data-ttu-id="211d4-114">Verwenden Sie die **lvitem** -Struktur, um die angeforderten Informationen an das-Steuerelement zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="211d4-114">Use the **LVITEM** structure to return the requested information to the control.</span></span> <span data-ttu-id="211d4-115">Wenn Ihr Meldungs Handler das lvif \_ di \_ SetItem-Flag im **Masken** -Member der **lvitem** -Struktur festlegt, speichert das Listenansicht-Steuerelement die angeforderten Informationen und fragt es nicht erneut ab.</span><span class="sxs-lookup"><span data-stu-id="211d4-115">If your message handler sets the LVIF\_DI\_SETITEM flag in the **mask** member of the **LVITEM** structure, the list-view control stores the requested information and will not ask for it again.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="211d4-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="211d4-116">Return value</span></span>

<span data-ttu-id="211d4-117">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="211d4-117">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="211d4-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="211d4-118">Remarks</span></span>

<span data-ttu-id="211d4-119">Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvdispinfo**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="211d4-119">The notification receiver casts *lParam* to retrieve the [**NMLVDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmlvdispinfoa) structure.</span></span> <span data-ttu-id="211d4-120">Der *wParam* -Parameter enthält den Benachrichtigungs Code.</span><span class="sxs-lookup"><span data-stu-id="211d4-120">The *wParam* parameter contains the notification code.</span></span>

<span data-ttu-id="211d4-121">Ein Listenansicht-Steuerelement sendet den **LVN \_ getdispinfo** -Benachrichtigungs Code zum Abrufen von Element Informationen, die von der Anwendung gespeichert werden, und nicht vom-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="211d4-121">A list-view control sends the **LVN\_GETDISPINFO** notification code to retrieve item information that is stored by the application rather than the control.</span></span> <span data-ttu-id="211d4-122">Die Informationen können Text-oder Symbol Informationen für ein Element sein.</span><span class="sxs-lookup"><span data-stu-id="211d4-122">The information can be text or icon information for an item.</span></span> <span data-ttu-id="211d4-123">Dabei kann es sich auch um Element Zustandsinformationen handeln.</span><span class="sxs-lookup"><span data-stu-id="211d4-123">It can also be item state information.</span></span> <span data-ttu-id="211d4-124">Weitere Informationen zum Implementieren des Element Zustands auf Rückruf Basis finden Sie in der [**LVM- \_ SetCallbackMask**](lvm-setcallbackmask.md) -Nachricht.</span><span class="sxs-lookup"><span data-stu-id="211d4-124">See the [**LVM\_SETCALLBACKMASK**](lvm-setcallbackmask.md) message for more information on implementing item state on a callback basis.</span></span>

<span data-ttu-id="211d4-125">Weitere Informationen zu List-View-Rückrufen finden Sie unter [Rückruf Elemente und Rückruf Maske](list-view-controls-overview.md).</span><span class="sxs-lookup"><span data-stu-id="211d4-125">For more information on list-view callbacks, see [Callback Items and the Callback Mask](list-view-controls-overview.md).</span></span>

## <a name="examples"></a><span data-ttu-id="211d4-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="211d4-126">Examples</span></span>

<span data-ttu-id="211d4-127">Das folgende Beispiel zeigt, wie dieser Benachrichtigungs Code behandelt werden kann, um den Text in den Spalten einer Listenansicht festzulegen.</span><span class="sxs-lookup"><span data-stu-id="211d4-127">The following example shows how this notification code might be handled to set the text in the columns of a list view.</span></span> <span data-ttu-id="211d4-128">Die Daten für jedes Element werden in der folgenden Struktur gespeichert.</span><span class="sxs-lookup"><span data-stu-id="211d4-128">The data for each item is held in the following structure.</span></span>


```C++
 typedef struct tagPETINFO
{
    TCHAR szName[50];
    TCHAR szBreed[50];
    TCHAR szGender[7];
    TCHAR szPrice[20];
    GroupIds iGroup;
} PETINFO;
            
```



<span data-ttu-id="211d4-129">Der WM- \_ Benachrichtigungs Handler in der Dialogfeld Prozedur lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="211d4-129">The following is from the WM\_NOTIFY handler in the dialog procedure.</span></span>


```C++
    case WM_NOTIFY:
        switch (((LPNMHDR) lParam)->code)
        {
        case LVN_GETDISPINFO:
            {
                NMLVDISPINFO* plvdi = (NMLVDISPINFO*)lParam;    
                switch (plvdi->item.iSubItem)
                {
                case 0:
                    // rgPetInfo is an array of PETINFO structures.
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szName;
                    break;

                case 1:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szBreed;
                    break;

                case 2:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szGender;
                    break;

                case 3:
                    plvdi->item.pszText = rgPetInfo[plvdi->item.iItem].szPrice;
                    break;

                default:
                    break;
                }
                return TRUE;
            }
      // More notifications...
      }
```



## <a name="requirements"></a><span data-ttu-id="211d4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="211d4-130">Requirements</span></span>



| <span data-ttu-id="211d4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="211d4-131">Requirement</span></span> | <span data-ttu-id="211d4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="211d4-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="211d4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="211d4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="211d4-134">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="211d4-134">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="211d4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="211d4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="211d4-136">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="211d4-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="211d4-137">Header</span><span class="sxs-lookup"><span data-stu-id="211d4-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="211d4-138"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="211d4-138"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="211d4-139">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="211d4-139">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="211d4-140">**LVN \_ Getdispinfow** (Unicode) und **LVN \_ getdispinfoa** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="211d4-140">**LVN\_GETDISPINFOW** (Unicode) and **LVN\_GETDISPINFOA** (ANSI)</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="211d4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="211d4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="211d4-142">**LVN \_ setdispinfo**</span><span class="sxs-lookup"><span data-stu-id="211d4-142">**LVN\_SETDISPINFO**</span></span>](lvn-setdispinfo.md)
</dt> </dl>

 

 





