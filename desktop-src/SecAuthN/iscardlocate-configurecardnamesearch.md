---
description: Die Methode "konfigurrecardnamesearch" gibt die Kartennamen an, die bei der Suche nach der Smartcard verwendet werden sollen.
ms.assetid: fb406696-0cf0-4d67-8125-8888ee1b8213
title: 'Iscardlocate:: konfiguriert recardnamesearch-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.ConfigureCardNameSearch
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 4af451bea1f08df2af0a673b26e84c9df2a0954b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216534"
---
# <a name="iscardlocateconfigurecardnamesearch-method"></a><span data-ttu-id="cac21-103">Iscardlocate:: konfiguriert recardnamesearch-Methode</span><span class="sxs-lookup"><span data-stu-id="cac21-103">ISCardLocate::ConfigureCardNameSearch method</span></span>

<span data-ttu-id="cac21-104">\[Die Methode " **konfigurrecardnamesearch** " ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="cac21-104">\[The **ConfigureCardNameSearch** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="cac21-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cac21-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="cac21-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="cac21-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="cac21-107">Die Methode " **konfigurrecardnamesearch** " gibt die Kartennamen an, die bei der Suche nach der [*Smartcard*](../secgloss/s-gly.md)verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac21-107">The **ConfigureCardNameSearch** method specifies the card names to be used in the search for the [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="cac21-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cac21-108">Syntax</span></span>


```C++
HRESULT ConfigureCardNameSearch(
  [in] LPSAFEARRAY pCardNames,
  [in] LPSAFEARRAY pGroupNames,
  [in] BSTR        bstrTitle,
  [in] LONG        lFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cac21-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cac21-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cac21-110">*pcardnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac21-110">*pCardNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac21-111">Ein Zeiger auf ein Automatisierungs sicheres Array von Kartennamen in BSTR-Form.</span><span class="sxs-lookup"><span data-stu-id="cac21-111">A pointer to an Automation safe array of card names in BSTR form.</span></span>

</dd> <dt>

<span data-ttu-id="cac21-112">*pgroupnames* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac21-112">*pGroupNames* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac21-113">Ein Zeiger auf ein Automation-sicheres Array mit Namen von Karten-/Lesegruppen in BSTR-Form, die der Suche hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="cac21-113">A pointer to an Automation safe array of names of card/reader groups in BSTR form to add to the search.</span></span>

</dd> <dt>

<span data-ttu-id="cac21-114">*bstrintitle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac21-114">*bstrTitle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac21-115">Dialog Feld Titel für das allgemeine Steuerelement für die Suche.</span><span class="sxs-lookup"><span data-stu-id="cac21-115">Dialog box title for the search common control.</span></span>

</dd> <dt>

<span data-ttu-id="cac21-116">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cac21-116">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cac21-117">Gibt an, wann die [*Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cac21-117">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed.</span></span>



| <span data-ttu-id="cac21-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cac21-118">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="cac21-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="cac21-119">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="cac21-120"><dt>**SC \_ DLG \_ minimale \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-120"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="cac21-121">Zeigt das Dialogfeld nur an, wenn die Karte, die von der aufrufenden Anwendung gesucht wird, nicht gefunden wurde und für die Verwendung in einem Reader verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cac21-121">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="cac21-122">Dadurch kann die Karte gefunden und verbunden werden (entweder über einen internen Dialogfeld Mechanismus oder mithilfe der Benutzer Rückruf Funktionen) und an die aufrufende Anwendung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cac21-122">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="cac21-123"><dt>**SC \_ DLG \_ keine \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-123"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="cac21-124">Bewirkt, dass unabhängig vom Suchergebnis keine Anzeige auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cac21-124">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="cac21-125"><dt>**SC \_ DLG \_ Force \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-125"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="cac21-126">Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="cac21-126">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cac21-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cac21-127">Return value</span></span>

<span data-ttu-id="cac21-128">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cac21-128">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="cac21-129">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="cac21-129">Return code</span></span>                                                                                   | <span data-ttu-id="cac21-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cac21-130">Description</span></span>                                                           |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="cac21-131"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-131"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="cac21-132">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="cac21-132">Operation completed successfully.</span></span><br/>                          |
| <dl> <span data-ttu-id="cac21-133"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-133"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="cac21-134">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="cac21-134">Invalid parameter.</span></span><br/>                                         |
| <dl> <span data-ttu-id="cac21-135"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-135"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="cac21-136">Ein fehlerhafter Zeiger wurde in " *pcardnames* " oder " *pgroupnames*" übergeben.</span><span class="sxs-lookup"><span data-stu-id="cac21-136">A bad pointer was passed in *pCardNames* or *pGroupNames*.</span></span><br/> |
| <dl> <span data-ttu-id="cac21-137"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-137"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="cac21-138">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="cac21-138">Out of memory.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="cac21-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cac21-139">Remarks</span></span>

<span data-ttu-id="cac21-140">Um die [*Smartcard*](../secgloss/s-gly.md)zu suchen, wenden Sie [**findcard**](iscardlocate-findcard.md)an.</span><span class="sxs-lookup"><span data-stu-id="cac21-140">To locate the [*smart card*](../secgloss/s-gly.md), call [**FindCard**](iscardlocate-findcard.md).</span></span>

<span data-ttu-id="cac21-141">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardlocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="cac21-141">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="cac21-142">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="cac21-142">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="cac21-143">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="cac21-143">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cac21-144">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cac21-144">Requirements</span></span>



| <span data-ttu-id="cac21-145">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cac21-145">Requirement</span></span> | <span data-ttu-id="cac21-146">Wert</span><span class="sxs-lookup"><span data-stu-id="cac21-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cac21-147">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cac21-147">Minimum supported client</span></span><br/> | <span data-ttu-id="cac21-148">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cac21-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="cac21-149">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cac21-149">Minimum supported server</span></span><br/> | <span data-ttu-id="cac21-150">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cac21-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="cac21-151">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cac21-151">End of client support</span></span><br/>    | <span data-ttu-id="cac21-152">Windows XP</span><span class="sxs-lookup"><span data-stu-id="cac21-152">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="cac21-153">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cac21-153">End of server support</span></span><br/>    | <span data-ttu-id="cac21-154">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="cac21-154">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="cac21-155">Header</span><span class="sxs-lookup"><span data-stu-id="cac21-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="cac21-156"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-156"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="cac21-157">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="cac21-157">Type library</span></span><br/>             | <dl> <span data-ttu-id="cac21-158"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-158"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="cac21-159">DLL</span><span class="sxs-lookup"><span data-stu-id="cac21-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cac21-160"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cac21-160"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="cac21-161">IID</span><span class="sxs-lookup"><span data-stu-id="cac21-161">IID</span></span><br/>                      | <span data-ttu-id="cac21-162">IID \_ iscardlocate ist als 1461aacd-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="cac21-162">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="cac21-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cac21-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cac21-164">**Findcard**</span><span class="sxs-lookup"><span data-stu-id="cac21-164">**FindCard**</span></span>](iscardlocate-findcard.md)
</dt> <dt>

[<span data-ttu-id="cac21-165">**Iscardsuche**</span><span class="sxs-lookup"><span data-stu-id="cac21-165">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
