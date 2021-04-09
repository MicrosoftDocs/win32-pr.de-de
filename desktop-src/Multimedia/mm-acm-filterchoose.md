---
title: MM_ACM_FILTERCHOOSE Meldung (MSACM. h)
description: Die mm \_ ACM \_ filterchoose-Meldung benachrichtigt eine acmfilterchoose-Dialogfeld-Hookfunktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- MM_ACM_FILTERCHOOSE-Nachricht (Multimedia)
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103038"
---
# <a name="mm_acm_filterchoose-message"></a><span data-ttu-id="02463-104">MM \_ ACM \_ filterchoose-Meldung</span><span class="sxs-lookup"><span data-stu-id="02463-104">MM\_ACM\_FILTERCHOOSE message</span></span>

<span data-ttu-id="02463-105">Die **mm \_ ACM \_ filterchoose** -Meldung benachrichtigt eine [**acmfilterchoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) -Dialogfeld-Hookfunktion, bevor ein Element zu einem der drei Dropdown-Listenfelder hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-105">The **MM\_ACM\_FILTERCHOOSE** message notifies an [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) dialog box hook function before adding an element to one of the three drop-down list boxes.</span></span> <span data-ttu-id="02463-106">Diese Meldung ermöglicht es einer Anwendung, die auf der Benutzeroberfläche verfügbare Auswahl weiter anzupassen.</span><span class="sxs-lookup"><span data-stu-id="02463-106">This message allows an application to further customize the selections available through the user interface.</span></span>


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a><span data-ttu-id="02463-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="02463-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="02463-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wdropdown*</span><span class="sxs-lookup"><span data-stu-id="02463-108"><span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*</span></span>
</dt> <dd>

<span data-ttu-id="02463-109">Dropdown-Listenfeld, das initialisiert wird, und ein Vorgang zum Überprüfen oder hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="02463-109">Drop-down list box being initialized and a verify or add operation.</span></span>



| <span data-ttu-id="02463-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02463-110">Requirement</span></span> | <span data-ttu-id="02463-111">Wert</span><span class="sxs-lookup"><span data-stu-id="02463-111">Value</span></span> |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02463-112">Filter Choose \_ Custom \_ Verify</span><span class="sxs-lookup"><span data-stu-id="02463-112">FILTERCHOOSE\_CUSTOM\_VERIFY</span></span>    | <span data-ttu-id="02463-113">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) Struktur, die dem Dropdown-Listenfeld benutzerdefinierter Name hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-113">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the custom Name drop-down list box.</span></span>                                                                                                   |
| <span data-ttu-id="02463-114">\_Filter Auswahl Filter \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="02463-114">FILTERCHOOSE\_FILTER\_ADD</span></span>       | <span data-ttu-id="02463-115">Der *LPARAM* -Parameter ist ein Zeiger auf einen Puffer, der eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) -Struktur akzeptiert, die dem Dropdown-Listenfeld Filter hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-115">The *lParam* parameter is a pointer to a buffer that will accept a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span> <span data-ttu-id="02463-116">Die Anwendung muss die Filter Struktur kopieren, die in diesen Puffer eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="02463-116">The application must copy the filter structure to be added into this buffer.</span></span> |
| <span data-ttu-id="02463-117">\_Filter Auswahl Filter \_ überprüfen</span><span class="sxs-lookup"><span data-stu-id="02463-117">FILTERCHOOSE\_FILTER\_VERIFY</span></span>    | <span data-ttu-id="02463-118">Der *LPARAM* -Parameter ist ein Zeiger auf eine [**Wellen Filter**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) Struktur, die dem Dropdown-Listenfeld Filter hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-118">The *lParam* parameter is a pointer to a [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) structure to be added to the Filter drop-down list box.</span></span>                                                                                                        |
| <span data-ttu-id="02463-119">filterchoose \_ Filtertag \_ Hinzufügen</span><span class="sxs-lookup"><span data-stu-id="02463-119">FILTERCHOOSE\_FILTERTAG\_ADD</span></span>    | <span data-ttu-id="02463-120">Der *LPARAM* -Parameter ist ein Zeiger auf ein **DWORD** , das ein Waveform-audiofiltertag akzeptiert, das dem Dropdown-Listenfeld für den Filtertag hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-120">The *lParam* parameter is a pointer to a **DWORD** that will accept a waveform-audio filter tag to be added to the Filter Tag drop-down list box.</span></span>                                                                                        |
| <span data-ttu-id="02463-121">filterchoose \_ Filtertag \_ verify überprüfen</span><span class="sxs-lookup"><span data-stu-id="02463-121">FILTERCHOOSE\_FILTERTAG\_VERIFY</span></span> | <span data-ttu-id="02463-122">Der *LPARAM* -Parameter ist ein Waveform-audiofiltertag, das im Dropdown-Listenfeld für den Filtertag aufgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02463-122">The *lParam* parameter is a waveform-audio filter tag to be listed in the Filter Tag drop-down list box.</span></span>                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="02463-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lcustom*</span><span class="sxs-lookup"><span data-stu-id="02463-123"><span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*</span></span>
</dt> <dd>

<span data-ttu-id="02463-124">Der Wert, der durch das im **wParam** -Parameter angegebene Listenfeld definiert wird.</span><span class="sxs-lookup"><span data-stu-id="02463-124">Value defined by the list box specified in the **wParam** parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="02463-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="02463-125">Return Value</span></span>

<span data-ttu-id="02463-126">Gibt " **true** " zurück, wenn eine Anwendung diese Nachricht behandelt, andernfalls " **false** ".</span><span class="sxs-lookup"><span data-stu-id="02463-126">Returns **TRUE** if an application handles this message or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="02463-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="02463-127">Remarks</span></span>

<span data-ttu-id="02463-128">Wenn die Anwendung den filterchoose- \_ Filter \_ Add-Vorgang verarbeitet, wird die Größe des in *LPARAM* angegebenen Speicherpuffers aus der [**acmmetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) -Funktion bestimmt.</span><span class="sxs-lookup"><span data-stu-id="02463-128">If the application processes the FILTERCHOOSE\_FILTER\_ADD operation, the size of the memory buffer supplied in *lParam* will be determined from the [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) function.</span></span>

<span data-ttu-id="02463-129">Wenn die Anwendung einen Verifizierungs Vorgang verarbeitet, die Anwendung muss dem Rückgabewert mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long) **false**) vorangestellt sein, um zu verhindern, dass das Dialogfeld diese Auswahl auflistet, oder mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**true**), damit das Dialogfeld diese Auswahl auflisten kann.</span><span class="sxs-lookup"><span data-stu-id="02463-129">If the application processes a verify operation, the application must precede the return value with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG) **FALSE**) to prevent the dialog box from listing this selection or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) to allow the dialog box to list this selection.</span></span> <span data-ttu-id="02463-130">Wenn Sie einen Add-Vorgang verarbeiten, muss die Anwendung vor der Rückgabe mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**false**) stehen, um anzugeben, dass keine weiteren Ergänzungen erforderlich sind, oder mit **SetWindowLong** (HWND, DWL \_ msgresult, (Long)**true**), wenn weitere Ergänzungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="02463-130">If processing an add operation, the application must precede the return with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**FALSE**) to indicate that no more additions are required or with **SetWindowLong** (hwnd, DWL\_MSGRESULT, (LONG)**TRUE**) if more additions are required.</span></span>

## <a name="requirements"></a><span data-ttu-id="02463-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="02463-131">Requirements</span></span>



| <span data-ttu-id="02463-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="02463-132">Requirement</span></span> | <span data-ttu-id="02463-133">Wert</span><span class="sxs-lookup"><span data-stu-id="02463-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="02463-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="02463-134">Minimum supported client</span></span><br/> | <span data-ttu-id="02463-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02463-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                         |
| <span data-ttu-id="02463-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="02463-136">Minimum supported server</span></span><br/> | <span data-ttu-id="02463-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="02463-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="02463-138">Header</span><span class="sxs-lookup"><span data-stu-id="02463-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="02463-139"><dt>MSACM. h</dt></span><span class="sxs-lookup"><span data-stu-id="02463-139"><dt>Msacm.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="02463-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02463-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="02463-141">Audiokomprimierungs-Manager</span><span class="sxs-lookup"><span data-stu-id="02463-141">Audio Compression Manager</span></span>](audio-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="02463-142">Audiokomprimierungs Meldungen</span><span class="sxs-lookup"><span data-stu-id="02463-142">Audio Compression Messages</span></span>](audio-compression-messages.md)
</dt> </dl>

 

 





