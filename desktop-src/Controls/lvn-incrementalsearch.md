---
title: LVN_INCREMENTALSEARCH Benachrichtigungs Code (kommctrl. h)
description: Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine inkrementelle Suche gestartet wurde. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 34517250-a6ba-490b-b87e-b09048543339
keywords:
- Windows-Steuerelemente für LVN_INCREMENTALSEARCH Benachrichtigungs
topic_type:
- apiref
api_name:
- LVN_INCREMENTALSEARCH
- LVN_INCREMENTALSEARCHA
- LVN_INCREMENTALSEARCHW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4784ed8f2a9df664b203f776dc1102702d2861e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106345534"
---
# <a name="lvn_incrementalsearch-notification-code"></a><span data-ttu-id="44f6e-105">LVN \_ IncrementalSearch-Benachrichtigungs Code</span><span class="sxs-lookup"><span data-stu-id="44f6e-105">LVN\_INCREMENTALSEARCH notification code</span></span>

<span data-ttu-id="44f6e-106">Benachrichtigt das übergeordnete Fenster eines Listenansicht-Steuer Elements, dass eine inkrementelle Suche gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="44f6e-106">Notifies a list-view control's parent window that an incremental search has started.</span></span> <span data-ttu-id="44f6e-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="44f6e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_INCREMENTALSEARCH
          
    pnmv = (LPNMLVFINDITEM) lParam;
```



## <a name="parameters"></a><span data-ttu-id="44f6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="44f6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44f6e-109">*LPARAM* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="44f6e-109">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="44f6e-110">Zeiger auf eine [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur, die den Benachrichtigungs Code beschreibt.</span><span class="sxs-lookup"><span data-stu-id="44f6e-110">Pointer to a [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure that describes the notification code.</span></span> <span data-ttu-id="44f6e-111">Der Aufrufer ist dafür verantwortlich, diese Struktur zuzuordnen, einschließlich der enthaltenen [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -und [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) -Strukturen.</span><span class="sxs-lookup"><span data-stu-id="44f6e-111">The caller is responsible for allocating this structure, including the contained [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) and [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structures.</span></span> <span data-ttu-id="44f6e-112">Legen Sie die Member der **NMHDR** -Struktur fest.</span><span class="sxs-lookup"><span data-stu-id="44f6e-112">Set the members of the **NMHDR** structure.</span></span> <span data-ttu-id="44f6e-113">Der **Codemember** muss auf LVN \_ IncrementalSearch festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="44f6e-113">The **code** member must be set to LVN\_INCREMENTALSEARCH.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44f6e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="44f6e-114">Return value</span></span>

<span data-ttu-id="44f6e-115">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="44f6e-115">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f6e-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="44f6e-116">Remarks</span></span>

<span data-ttu-id="44f6e-117">Der Benachrichtigungs Empfänger wandelt *LPARAM* ein, um die [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur abzurufen.</span><span class="sxs-lookup"><span data-stu-id="44f6e-117">The notification receiver casts *lParam* to retrieve the [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure.</span></span> <span data-ttu-id="44f6e-118">Der *wParam* -Parameter enthält die ID des Steuer Elements, das diesen Benachrichtigungs Code sendet.</span><span class="sxs-lookup"><span data-stu-id="44f6e-118">The *wParam* parameter contains the ID of the control that sends this notification code.</span></span>

<span data-ttu-id="44f6e-119">Dieser Benachrichtigungs Code gibt einer Anwendung (oder dem Benachrichtigungs Empfänger) die Möglichkeit, eine inkrementelle Suche anzupassen.</span><span class="sxs-lookup"><span data-stu-id="44f6e-119">This notification code gives an application (or the notification receiver) the opportunity to customize an incremental search.</span></span> <span data-ttu-id="44f6e-120">Wenn die Such Elemente beispielsweise numerisch sind, kann die Anwendung anstelle einer Zeichen folgen Suche eine numerische Suche durchführen.</span><span class="sxs-lookup"><span data-stu-id="44f6e-120">For example, if the search items are numeric, the application can perform a numerical search instead of a string search.</span></span>

<span data-ttu-id="44f6e-121">Die Anwendung legt den **LPARAM** -Member der [**in der**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) [**nmlvfinditem**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) -Struktur enthaltenen vParam-Struktur auf das Ergebnis der Suche oder einen anderen Anwendungs definierten Wert fest, um die Suche zu misslingen und dem Steuerelement mitzuteilen, wie der Vorgang fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="44f6e-121">The application sets the **lParam** member of the [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) structure contained in [**NMLVFINDITEM**](/windows/win32/api/commctrl/ns-commctrl-nmlvfinditema) structure  to the result of the search, or to another application defined value to fail the search and indicate to the control how to proceed.</span></span>

## <a name="requirements"></a><span data-ttu-id="44f6e-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="44f6e-122">Requirements</span></span>



| <span data-ttu-id="44f6e-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="44f6e-123">Requirement</span></span> | <span data-ttu-id="44f6e-124">Wert</span><span class="sxs-lookup"><span data-stu-id="44f6e-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="44f6e-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="44f6e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="44f6e-126">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44f6e-126">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="44f6e-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="44f6e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="44f6e-128">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="44f6e-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="44f6e-129">Header</span><span class="sxs-lookup"><span data-stu-id="44f6e-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="44f6e-130"><dt>Kommstrg. h</dt></span><span class="sxs-lookup"><span data-stu-id="44f6e-130"><dt>Commctrl.h</dt></span></span> </dl>   |
| <span data-ttu-id="44f6e-131">Unicode- und ANSI-Name</span><span class="sxs-lookup"><span data-stu-id="44f6e-131">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="44f6e-132">**LVN \_ Incrementalsearchw** (Unicode) und **LVN \_ incrementalsearcha** (ANSI)</span><span class="sxs-lookup"><span data-stu-id="44f6e-132">**LVN\_INCREMENTALSEARCHW** (Unicode) and **LVN\_INCREMENTALSEARCHA** (ANSI)</span></span><br/> |



 

 





