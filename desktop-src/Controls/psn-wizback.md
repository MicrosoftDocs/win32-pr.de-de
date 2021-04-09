---
title: PSN_WIZBACK Benachrichtigungs Code (prsht. h)
description: Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche "zurück" geklickt hat. Dieser Benachrichtigungs Code wird in Form einer WM-Benachrichtigungs \_ Meldung gesendet.
ms.assetid: 784f92e7-6f10-40fc-b513-bea022f13ae1
keywords:
- Windows-Steuerelemente für PSN_WIZBACK Benachrichtigungs
topic_type:
- apiref
api_name:
- PSN_WIZBACK
api_location:
- Prsht.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aed1cdd742d78473266db07899796de5a5450310
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858639"
---
# <a name="psn_wizback-notification-code"></a><span data-ttu-id="ffd2b-105">\_Benachrichtigungs Code für PSN-witzback</span><span class="sxs-lookup"><span data-stu-id="ffd2b-105">PSN\_WIZBACK notification code</span></span>

<span data-ttu-id="ffd2b-106">Benachrichtigt eine Seite, dass der Benutzer in einem Assistenten auf die Schaltfläche " **zurück** " geklickt hat.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-106">Notifies a page that the user has clicked the **Back** button in a wizard.</span></span> <span data-ttu-id="ffd2b-107">Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
PSN_WIZBACK 

    lppsn = (LPPSHNOTIFY) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="ffd2b-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ffd2b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffd2b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ffd2b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ffd2b-110">Zeiger auf eine [**pshnotify**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) -Struktur, die Informationen über den Benachrichtigungs Code enthält.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-110">Pointer to a [**PSHNOTIFY**](/windows/desktop/api/Prsht/ns-prsht-pshnotify) structure that contains information about the notification code.</span></span> <span data-ttu-id="ffd2b-111">Diese Struktur enthält eine [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) -Struktur als ersten Member, **HDR**. Der **hwndfrom** -Member dieser **NMHDR** -Struktur enthält das Handle für das Eigenschaften Blatt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-111">This structure contains an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure as its first member, **hdr**. The **hwndFrom** member of this **NMHDR** structure contains the handle to the property sheet.</span></span> <span data-ttu-id="ffd2b-112">Der **LPARAM** -Member der **pshnotify** -Struktur enthält keine Informationen.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-112">The **lParam** member of the **PSHNOTIFY** structure does not contain any information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffd2b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ffd2b-113">Return value</span></span>

<span data-ttu-id="ffd2b-114">Gibt 0 zurück, um zuzulassen, dass der Assistent zur vorherigen Seite wechselt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-114">Returns 0 to allow the wizard to go to the previous page.</span></span> <span data-ttu-id="ffd2b-115">Gibt-1 zurück, um zu verhindern, dass der Assistent Seiten ändert.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-115">Returns -1 to prevent the wizard from changing pages.</span></span> <span data-ttu-id="ffd2b-116">Um eine bestimmte Seite anzuzeigen, geben Sie den Ressourcen Bezeichner des Dialog Felds zurück.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-116">To display a particular page, return its dialog resource identifier.</span></span> <span data-ttu-id="ffd2b-117">Wenn das Dialogfeld mit dem kennflag " [**PSP \_ dlgindirect**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) " angegeben wurde, gibt diese Benachrichtigung den Zeiger auf die Dialogfeld Vorlage zurück.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-117">If the dialog was specified with the [**PSP\_DLGINDIRECT**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) flag, this notification returns the pointer to the dialog template.</span></span>

## <a name="remarks"></a><span data-ttu-id="ffd2b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffd2b-118">Remarks</span></span>

<span data-ttu-id="ffd2b-119">Um den Rückgabewert festzulegen, muss die Dialogfeld Prozedur für die Seite die [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) -Funktion mit dem **DWL-Wert \_ msgresult** aufrufen und **true** zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-119">To set the return value, the dialog box procedure for the page must call the [**SetWindowLong**](/windows/desktop/api/winuser/nf-winuser-setwindowlonga) function with the **DWL\_MSGRESULT** value and return **TRUE**.</span></span> <span data-ttu-id="ffd2b-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ffd2b-120">For example:</span></span>

``` syntax
case PSN_WIZBACK :
    SetWindowLong(hDlg, DWL_MSGRESULT, 0);
    break;

case PSN_WIZNEXT :
    ...
```

> [!Note]  
> <span data-ttu-id="ffd2b-121">Das Eigenschaften Blatt bearbeitet die Liste der Seiten, wenn der Benachrichtigungs Code des PSN-wids \_ gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-121">The property sheet is in the process of manipulating the list of pages when the PSN\_WIZBACK notification code is sent.</span></span> <span data-ttu-id="ffd2b-122">Sie können Seiten als Reaktion auf diese Benachrichtigungs Codes hinzufügen, einfügen oder entfernen, aber es muss besonders darauf geachtet werden, dass Seiten vor der aktuellen Seite eingefügt oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-122">You can add, insert, or remove pages in response to these notification codes, but special care must be taken if you insert or remove pages before the current page.</span></span>

 

<span data-ttu-id="ffd2b-123">Wenn Sie Seiten vor der aktuellen Seite einfügen oder entfernen, müssen Sie (über **DWL \_ msgresult**) einen Wert ungleich 0 (null) zurückgeben, um die gewünschte neue Seite anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-123">If you insert or remove pages before the current page, you must return (through **DWL\_MSGRESULT**) a nonzero value to specify the desired new page.</span></span> <span data-ttu-id="ffd2b-124">Beachten Sie jedoch Folgendes: Wenn Sie eine Seite einfügen oder entfernen, die sich vor der aktuellen Seite befindet (die einen kleineren Index als die aktuelle Seite aufweist), wird " [PSN \_ killactive](psn-killactive.md) " möglicherweise an die falsche Seite gesendet.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-124">Note, however, that if you insert or remove a page that is located before the current page (that has a smaller index than the current page), [PSN\_KILLACTIVE](psn-killactive.md) might be sent to the wrong page.</span></span>

<span data-ttu-id="ffd2b-125">Aus diesem Grund empfiehlt es sich, Assistenten zu verwenden, die als Reaktion auf "PSN-und" PSN-Wort Antworten "Seiten dynamisch hinzufügen und entfernen [ \_ ](psn-wiznext.md) \_ .</span><span class="sxs-lookup"><span data-stu-id="ffd2b-125">For this reason, it is recommended that wizards that add and remove pages dynamically in response to [PSN\_WIZNEXT](psn-wiznext.md) and PSN\_WIZBACK do so only to pages at the end of the list.</span></span> <span data-ttu-id="ffd2b-126">Wenn Sie möchten, dass der Assistent Seiten genau entfernt, behalten Sie die dynamischen Seiten am Ende der Liste bei, und kehren Sie zu permanenten Seiten zurück, bevor Sie Sie löschen.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-126">If you want your wizard to remove pages accurately, keep the dynamic pages at the end of the list and jump back to permanent pages before deleting them.</span></span>

<span data-ttu-id="ffd2b-127">Nehmen wir beispielsweise an, dass ein Assistent aus einer Einführungsseite, einer Reihe dynamischer Seiten und einer Abschluss Seite besteht und Sie die dynamischen Seiten löschen möchten, wenn der Benutzer die Abschluss Seite erreicht.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-127">For example, suppose a wizard consists of an introductory page, a series of dynamic pages, and a completion page, and you want to delete the dynamic pages when the user reaches the completion page.</span></span>

1.  <span data-ttu-id="ffd2b-128">Der Assistent beginnt mit zwei Seiten: "Introduction" und "completion".</span><span class="sxs-lookup"><span data-stu-id="ffd2b-128">The wizard would begin with two pages, "Introduction" and "Completion."</span></span> <span data-ttu-id="ffd2b-129">Der Benutzer beginnt auf der Seite "Introduction" (Einführung).</span><span class="sxs-lookup"><span data-stu-id="ffd2b-129">The user begins on the "Introduction" page.</span></span>
    1.  <span data-ttu-id="ffd2b-130">Einführung (Benutzer ist hier)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-130">Introduction (User is here)</span></span>
    2.  <span data-ttu-id="ffd2b-131">Completion</span><span class="sxs-lookup"><span data-stu-id="ffd2b-131">Completion</span></span>
2.  <span data-ttu-id="ffd2b-132">Wenn der Benutzer von der "Einführung" weg navigiert, fügt der Assistent die dynamischen Seiten hinzu und platziert den Benutzer auf der ersten dynamischen Seite, indem er (über DWL msgresult) den Dialog Bezeichner der Seite "Dynamic 1" (durch **DWL \_ msgresult**) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-132">When the user navigates away from "Introduction," the wizard adds the dynamic pages and places the user at the first dynamic page by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Dynamic 1."</span></span> <span data-ttu-id="ffd2b-133">In diesem Beispiel gibt es drei dynamische Seiten.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-133">In this example, there are three dynamic pages.</span></span>
    1.  <span data-ttu-id="ffd2b-134">Einführung</span><span class="sxs-lookup"><span data-stu-id="ffd2b-134">Introduction</span></span>
    2.  <span data-ttu-id="ffd2b-135">Completion</span><span class="sxs-lookup"><span data-stu-id="ffd2b-135">Completion</span></span>
    3.  <span data-ttu-id="ffd2b-136">Dynamisch 1 (Benutzer ist hier)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-136">Dynamic 1 (User is here)</span></span>
    4.  <span data-ttu-id="ffd2b-137">Dynamisch 2</span><span class="sxs-lookup"><span data-stu-id="ffd2b-137">Dynamic 2</span></span>
    5.  <span data-ttu-id="ffd2b-138">Dynamisch 3</span><span class="sxs-lookup"><span data-stu-id="ffd2b-138">Dynamic 3</span></span>
3.  <span data-ttu-id="ffd2b-139">Nachdem der Benutzer die dynamischen Seiten zu "Dynamic 3" navigiert und dann zur nächsten Seite navigiert hat, sollte die Anwendung den Benutzer auf der Seite "Abschluss" platzieren.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-139">After the user navigates through the dynamic pages to "Dynamic 3" and then navigates to the next page, the application should place the user at the page "Completion."</span></span> <span data-ttu-id="ffd2b-140">Dies erfolgt wiederum durch Zurückgeben von (über **DWL \_ msgresult**) dem Dialog Bezeichner der Seite "Abschluss".</span><span class="sxs-lookup"><span data-stu-id="ffd2b-140">Again, this is done by returning (through **DWL\_MSGRESULT**) the dialog identifier of the page "Completion."</span></span>
    1.  <span data-ttu-id="ffd2b-141">Einführung</span><span class="sxs-lookup"><span data-stu-id="ffd2b-141">Introduction</span></span>
    2.  <span data-ttu-id="ffd2b-142">Abschluss (Benutzer ist hier)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-142">Completion (User is here)</span></span>
    3.  <span data-ttu-id="ffd2b-143">Dynamisch 1</span><span class="sxs-lookup"><span data-stu-id="ffd2b-143">Dynamic 1</span></span>
    4.  <span data-ttu-id="ffd2b-144">Dynamisch 2</span><span class="sxs-lookup"><span data-stu-id="ffd2b-144">Dynamic 2</span></span>
    5.  <span data-ttu-id="ffd2b-145">Dynamisch 3</span><span class="sxs-lookup"><span data-stu-id="ffd2b-145">Dynamic 3</span></span>
4.  <span data-ttu-id="ffd2b-146">Die Anwendung kann dann die drei dynamischen Seiten (in drei bis fünf nummerierte Seiten) sicher entfernen.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-146">The application can then remove the three dynamic pages (numbered three through five) safely.</span></span>
    1.  <span data-ttu-id="ffd2b-147">Einführung</span><span class="sxs-lookup"><span data-stu-id="ffd2b-147">Introduction</span></span>
    2.  <span data-ttu-id="ffd2b-148">Abschluss (Benutzer ist hier)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-148">Completion (User is here)</span></span>

<span data-ttu-id="ffd2b-149">Beachten Sie, dass diese Technik nur erforderlich ist, wenn der Assistent Seiten dynamisch entfernt.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-149">Note that this technique is necessary only if your wizard removes pages dynamically.</span></span> <span data-ttu-id="ffd2b-150">Wenn der Assistent nur Seiten dynamisch hinzufügt, ist dieser Vorgang nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ffd2b-150">If your wizard only adds pages dynamically, this process is not necessary.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffd2b-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ffd2b-151">Requirements</span></span>



| <span data-ttu-id="ffd2b-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ffd2b-152">Requirement</span></span> | <span data-ttu-id="ffd2b-153">Wert</span><span class="sxs-lookup"><span data-stu-id="ffd2b-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ffd2b-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="ffd2b-155">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-155">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ffd2b-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ffd2b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="ffd2b-157">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ffd2b-157">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ffd2b-158">Header</span><span class="sxs-lookup"><span data-stu-id="ffd2b-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffd2b-159"><dt>Prsht. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffd2b-159"><dt>Prsht.h</dt></span></span> </dl> |



 

