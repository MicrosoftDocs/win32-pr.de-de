---
title: XTYP_MONITOR Transaktion (Ddeml. h)
description: Die DDE-Rückruffunktion (ddecallback) eines dynamischer Datenaustausch (DDE) empfängt die xD- \_ Monitor Transaktion, wenn ein DDE-Ereignis im System auftritt.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR Transaktionsdaten Austausch
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6a1cb86a1cbf7e0c02c082719e0a7d302d03975
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391800"
---
# <a name="xtyp_monitor-transaction"></a><span data-ttu-id="8ce7e-104">XYP- \_ Monitor Transaktion</span><span class="sxs-lookup"><span data-stu-id="8ce7e-104">XTYP\_MONITOR transaction</span></span>

<span data-ttu-id="8ce7e-105">Die DDE-Rückruffunktion ( [*ddecallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback)) eines dynamischer Datenaustausch (DDE) empfängt die **xD- \_ Monitor** Transaktion, wenn ein DDE-Ereignis im System auftritt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-105">A Dynamic Data Exchange (DDE) debugger's DDE callback function, [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), receives the **XTYP\_MONITOR** transaction whenever a DDE event occurs in the system.</span></span> <span data-ttu-id="8ce7e-106">Um diese Transaktion zu erhalten, muss eine Anwendung den **appclass- \_ Monitor** Wert angeben, wenn Sie die [**DDEInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) -Funktion aufruft.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-106">To receive this transaction, an application must specify the **APPCLASS\_MONITOR** value when it calls the [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) function.</span></span>


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
```



## <a name="parameters"></a><span data-ttu-id="8ce7e-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ce7e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ce7e-108">*uType*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-108">*uType*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-109">Der Transaktionstyp:</span><span class="sxs-lookup"><span data-stu-id="8ce7e-109">The transaction type.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-110">*UF*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-110">*uFmt*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-111">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-111">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-112">*has*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-112">*hconv*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-113">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-113">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-114">*hsz1*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-114">*hsz1*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-115">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-115">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-116">*hsz2*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-116">*hsz2*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-117">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-117">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-118">*hdata*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-118">*hdata*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-119">Ein Handle für ein DDE-Objekt, das Informationen über das DDE-Ereignis enthält.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-119">A handle to a DDE object that contains information about the DDE event.</span></span> <span data-ttu-id="8ce7e-120">Die Anwendung sollte die [**DDEBUG Data**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) -Funktion verwenden, um einen Zeiger auf das Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-120">The application should use the [**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) function to obtain a pointer to the object.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-121">*dwData1*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-121">*dwData1*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-122">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-122">Not used.</span></span>

</dd> <dt>

<span data-ttu-id="8ce7e-123">*dwData2*</span><span class="sxs-lookup"><span data-stu-id="8ce7e-123">*dwData2*</span></span> 
</dt> <dd>

<span data-ttu-id="8ce7e-124">Das DDE-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-124">The DDE event.</span></span> <span data-ttu-id="8ce7e-125">Dieser Parameter kann einen der folgenden Werte annehmen.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-125">This parameter can be one of the following values.</span></span>



| <span data-ttu-id="8ce7e-126">Wert</span><span class="sxs-lookup"><span data-stu-id="8ce7e-126">Value</span></span>                                                                                                                                                                                                                      | <span data-ttu-id="8ce7e-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="8ce7e-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <span data-ttu-id="8ce7e-128"><dt>**MF \_ Rückrufe**</dt> <dt>0x08000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-128"><dt>**MF\_CALLBACKS**</dt> <dt>0x08000000</dt></span></span> </dl> | <span data-ttu-id="8ce7e-129">Das System hat eine Transaktion an eine DDE-Rückruffunktion gesendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-129">The system sent a transaction to a DDE callback function.</span></span> <span data-ttu-id="8ce7e-130">Das DDE-Objekt enthält eine [**moncbstruct**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) -Struktur, die Informationen über die Transaktion bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-130">The DDE object contains a [**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) structure that provides information about the transaction.</span></span><br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <span data-ttu-id="8ce7e-131"><dt>**MF \_**</dt>Verbindung mit " <dt>0x40000000</dt> "</span><span class="sxs-lookup"><span data-stu-id="8ce7e-131"><dt>**MF\_CONV**</dt> <dt>0x40000000</dt></span></span> </dl>                | <span data-ttu-id="8ce7e-132">Eine DDE-Konversation wurde eingerichtet oder beendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-132">A DDE conversation was established or terminated.</span></span> <span data-ttu-id="8ce7e-133">Das DDE-Objekt enthält eine [**monkonvstruct**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) -Struktur, die Informationen über die Konversation bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-133">The DDE object contains a [**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) structure that provides information about the conversation.</span></span><br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <span data-ttu-id="8ce7e-134"><dt>**MF \_ Fehler**</dt> <dt>0x10000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-134"><dt>**MF\_ERRORS**</dt> <dt>0x10000000</dt></span></span> </dl>          | <span data-ttu-id="8ce7e-135">DDE-Fehler.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-135">A DDE error occurred.</span></span> <span data-ttu-id="8ce7e-136">Das DDE-Objekt enthält eine [**monerrstruct**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) -Struktur, die Informationen über den Fehler bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-136">The DDE object contains a [**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) structure that provides information about the error.</span></span><br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <span data-ttu-id="8ce7e-137"><dt>**MF \_ Hsz- \_ Info**</dt> <dt>0x01000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-137"><dt>**MF\_HSZ\_INFO**</dt> <dt>0x01000000</dt></span></span> </dl>   | <span data-ttu-id="8ce7e-138">Eine DDE-Anwendung, die den Verwendungs Zähler eines Zeichen folgen Handles erstellt, freigegeben oder inkrementiert hat, oder ein Zeichen folgen Handle wurde als Ergebnis eines Aufrufes der [**DDE Uninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) -Funktion freigegeben.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-138">A DDE application created, freed, or incremented the usage count of a string handle, or a string handle was freed as a result of a call to the [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) function.</span></span> <span data-ttu-id="8ce7e-139">Das DDE-Objekt enthält eine [**monhszstruct**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) -Struktur, die Informationen über das Zeichen folgen handle bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-139">The DDE object contains a [**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) structure that provides information about the string handle.</span></span><br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <span data-ttu-id="8ce7e-140"><dt>**MF \_ Links**</dt> <dt>0x20000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-140"><dt>**MF\_LINKS**</dt> <dt>0x20000000</dt></span></span> </dl>             | <span data-ttu-id="8ce7e-141">Eine DDE-Anwendung hat eine Empfehlung-Schleife gestartet oder angehalten.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-141">A DDE application started or stopped an advise loop.</span></span> <span data-ttu-id="8ce7e-142">Das DDE-Objekt enthält eine [**monlinkstruct**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) -Struktur, die Informationen über die Empfehlung-Schleife bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-142">The DDE object contains a [**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) structure that provides information about the advise loop.</span></span><br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <span data-ttu-id="8ce7e-143"><dt>**MF \_ Postmsgs**</dt> <dt>0x04000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-143"><dt>**MF\_POSTMSGS**</dt> <dt>0x04000000</dt></span></span> </dl>    | <span data-ttu-id="8ce7e-144">Das System oder eine Anwendung hat eine DDE-Nachricht gepostet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-144">The system or an application posted a DDE message.</span></span> <span data-ttu-id="8ce7e-145">Das DDE-Objekt enthält eine [**monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) -Struktur, die Informationen über die Meldung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-145">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <span data-ttu-id="8ce7e-146"><dt>**MF \_ Sendmsgs**</dt> <dt>0x02000000</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-146"><dt>**MF\_SENDMSGS**</dt> <dt>0x02000000</dt></span></span> </dl>    | <span data-ttu-id="8ce7e-147">Das System oder eine Anwendung hat eine DDE-Nachricht gesendet.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-147">The system or an application sent a DDE message.</span></span> <span data-ttu-id="8ce7e-148">Das DDE-Objekt enthält eine [**monmsgstruct**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) -Struktur, die Informationen über die Meldung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-148">The DDE object contains a [**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) structure that provides information about the message.</span></span><br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ce7e-149">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8ce7e-149">Return value</span></span>

<span data-ttu-id="8ce7e-150">Wenn die Rückruffunktion diese Transaktion verarbeitet, sollte Sie 0 (null) zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8ce7e-150">If the callback function processes this transaction, it should return 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ce7e-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8ce7e-151">Requirements</span></span>



| <span data-ttu-id="8ce7e-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8ce7e-152">Requirement</span></span> | <span data-ttu-id="8ce7e-153">Wert</span><span class="sxs-lookup"><span data-stu-id="8ce7e-153">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ce7e-154">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8ce7e-154">Minimum supported client</span></span><br/> | <span data-ttu-id="8ce7e-155">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ce7e-155">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8ce7e-156">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8ce7e-156">Minimum supported server</span></span><br/> | <span data-ttu-id="8ce7e-157">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8ce7e-157">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="8ce7e-158">Header</span><span class="sxs-lookup"><span data-stu-id="8ce7e-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="8ce7e-159"><dt>Ddeml. h (Include Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ce7e-159"><dt>Ddeml.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ce7e-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ce7e-160">See also</span></span>

<dl> <dt>

<span data-ttu-id="8ce7e-161">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-161">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce7e-162">**DDE Access Data**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-162">**DdeAccessData**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[<span data-ttu-id="8ce7e-163">**DDEInitialize**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-163">**DdeInitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[<span data-ttu-id="8ce7e-164">**DDE-Initialisierung**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-164">**DdeUninitialize**</span></span>](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[<span data-ttu-id="8ce7e-165">**Moncbstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-165">**MONCBSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[<span data-ttu-id="8ce7e-166">**Mon-vstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-166">**MONCONVSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[<span data-ttu-id="8ce7e-167">**Monerrstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-167">**MONERRSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[<span data-ttu-id="8ce7e-168">**Monhszstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-168">**MONHSZSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[<span data-ttu-id="8ce7e-169">**Monlinkstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-169">**MONLINKSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[<span data-ttu-id="8ce7e-170">**Monmsgstruct**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-170">**MONMSGSTRUCT**</span></span>](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

<span data-ttu-id="8ce7e-171">**Licher**</span><span class="sxs-lookup"><span data-stu-id="8ce7e-171">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8ce7e-172">dynamischer Datenaustausch-Verwaltungs Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8ce7e-172">Dynamic Data Exchange Management Library</span></span>](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

