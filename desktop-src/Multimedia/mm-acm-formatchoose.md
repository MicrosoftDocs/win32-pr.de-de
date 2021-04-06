---
title: MM_ACM_FORMATCHOOSE Meldung (MSACM. h)
description: Die mm \_ ACM \_ formatchoose-Meldung benachrichtigt eine acmformatchoose-Dialog Hook-Funktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- MM_ACM_FORMATCHOOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35808e06521cbd83d07f8d6c799779a16f50236b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743921"
---
# <a name="mm_acm_formatchoose-message"></a><span data-ttu-id="92a35-104">MM- \_ ACM \_ formatchoose-Meldung</span><span class="sxs-lookup"><span data-stu-id="92a35-104">MM\_ACM\_FORMATCHOOSE message</span></span>

<span data-ttu-id="92a35-105">Die **mm \_ ACM \_ formatchoose** -Meldung benachrichtigt eine [**acmformatchoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) -Dialog Hook-Funktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-105">The **MM\_ACM\_FORMATCHOOSE** message notifies an [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) dialog hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="92a35-106">Diese Meldung ermöglicht es einer Anwendung, die auf der Benutzeroberfläche verfügbare Auswahl weiter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="92a35-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a><span data-ttu-id="92a35-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="92a35-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a35-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wdropdown*</span><span class="sxs-lookup"><span data-stu-id="92a35-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="92a35-109">Dropdown-Listenfeld, das initialisiert wird, und ein Vorgang zum Überprüfen oder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="92a35-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="92a35-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92a35-110">Requirement</span></span> | <span data-ttu-id="92a35-111">Wert</span><span class="sxs-lookup"><span data-stu-id="92a35-111">Value</span></span> |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92a35-112">formatchoose \_ Custom \_ Verify</span><span class="sxs-lookup"><span data-stu-id="92a35-112">FORMATCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="92a35-113">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur, die dem Dropdown-Listenfeld benutzerdefinierter Name hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-113">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="92a35-114">formatchoose- \_ Format \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="92a35-114">FORMATCHOOSE\_FORMAT\_ADD</span></span>       | <span data-ttu-id="92a35-115">Der *LPARAM* -Parameter ist ein Zeiger auf einen Puffer, der dem Dropdown-Listenfeld Format eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur zuweist.</span><span class="sxs-lookup"><span data-stu-id="92a35-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span> <span data-ttu-id="92a35-116">Die Anwendung muss die Format Struktur kopieren, die in diesen Puffer eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="92a35-116">The application must copy the format structure to be added into this buffer.</span></span> |
| <span data-ttu-id="92a35-117">formatchoose- \_ Format \_ überprüfen</span><span class="sxs-lookup"><span data-stu-id="92a35-117">FORMATCHOOSE\_FORMAT\_VERIFY</span></span>    | <span data-ttu-id="92a35-118">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur, die dem Dropdown-Listenfeld Format hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-118">The *lParam* parameter is a pointer to a [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) structure to be added to the Format drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="92a35-119">Formattag \_ Formattag \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="92a35-119">FORMATCHOOSE\_FORMATTAG\_ADD</span></span>    | <span data-ttu-id="92a35-120">Der *LPARAM* -Parameter ist ein Zeiger auf eine Variable, die ein Waveform-audioformattag akzeptiert, das dem Dropdown-Listenfeld Formattag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-120">The *lParam* parameter is a pointer to a variable that will accept a waveform-audio format tag to be added to the Format Tag drop-down list box.</span></span>                                                                                             |
| <span data-ttu-id="92a35-121">formatchoose \_ Formattag \_ Verify</span><span class="sxs-lookup"><span data-stu-id="92a35-121">FORMATCHOOSE\_FORMATTAG\_VERIFY</span></span> | <span data-ttu-id="92a35-122">Der *LPARAM* -Parameter ist ein Waveform-audioformattag, das im Dropdown-Listenfeld Formattag aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-122">The *lParam* parameter is a waveform-audio format tag to be listed in the Format Tag drop-down list box.</span></span>                                                                                                                                     |



 

</dd> <dt>

<span data-ttu-id="92a35-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lcustom*</span><span class="sxs-lookup"><span data-stu-id="92a35-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="92a35-124">Der Wert, der durch das im **wParam** -Parameter angegebene ListBox-Element definiert wird.</span><span class="sxs-lookup"><span data-stu-id="92a35-124">Value defined by the listbox specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a35-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="92a35-125">Return Value</span></span>

<span data-ttu-id="92a35-126">Gibt " **true** " zurück, wenn eine Anwendung diese Nachricht behandelt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="92a35-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a35-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92a35-127">Remarks</span></span>

<span data-ttu-id="92a35-128">Wenn die Anwendung den Vorgang zum Hinzufügen des filterchoose- \_ Formats verarbeitet \_ , wird die Größe des in *LPARAM* angegebenen Speicherpuffers aus der [**acmmetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) -Funktion bestimmt.</span><span class="sxs-lookup"><span data-stu-id="92a35-128">If the application processes the FILTERCHOOSE\_FORMAT\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="92a35-129">Wenn Ihre Anwendung einen Verifizierungs Vorgang verarbeitet, kann Sie verhindern, dass das Dialogfeld diese Auswahl auflistet, indem Sie die **SetWindowLong** -Funktion aufruft, wobei *nIndex* auf DWL \_ msgresult und *lnewlong* auf **false** festgelegt ist (in einen **Long** -Datentyp umgewandelt).</span><span class="sxs-lookup"><span data-stu-id="92a35-129">If your application is processing a verify operation, it can prevent the dialog box from listing this selection by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="92a35-130">Damit das Dialogfeld diese Auswahl auflisten kann, wird diese Funktion aufgerufen, wenn *lnewlong* auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="92a35-130">To allow the dialog box to list this selection, call this function with *lNewLong* set to **TRUE**.</span></span>

<span data-ttu-id="92a35-131">Wenn Ihre Anwendung einen Add-Vorgang verarbeitet, kann Sie angeben, dass keine weiteren Ergänzungen erforderlich sind, indem Sie die **SetWindowLong** -Funktion aufrufen, wobei *nIndex* auf DWL \_ msgresult und *lnewlong* auf **false** festgelegt ist (in einen **Long** -Datentyp umgewandelt).</span><span class="sxs-lookup"><span data-stu-id="92a35-131">If your application is processing an add operation, it can indicate that no more additions are required by calling the **SetWindowLong** function with *nIndex* set to DWL\_MSGRESULT and *lNewLong* set to **FALSE** (cast to a **LONG** data type).</span></span> <span data-ttu-id="92a35-132">Um anzugeben, dass weitere Ergänzungen erforderlich sind, können Sie diese Funktion mit " *lnewlong* " auf " **true**" setzen.</span><span class="sxs-lookup"><span data-stu-id="92a35-132">To indicate more additions are required, call this function with *lNewLong* set to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="92a35-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="92a35-133">Requirements</span></span>



| <span data-ttu-id="92a35-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="92a35-134">Requirement</span></span> | <span data-ttu-id="92a35-135">Wert</span><span class="sxs-lookup"><span data-stu-id="92a35-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92a35-136">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="92a35-136">Minimum supported client</span></span><br/> | <span data-ttu-id="92a35-137">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92a35-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="92a35-138">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="92a35-138">Minimum supported server</span></span><br/> | <span data-ttu-id="92a35-139">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="92a35-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92a35-140">Header</span><span class="sxs-lookup"><span data-stu-id="92a35-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="92a35-141"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="92a35-141"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92a35-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92a35-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a35-143">Audiokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="92a35-143">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="92a35-144">Audiokomprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="92a35-144">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

