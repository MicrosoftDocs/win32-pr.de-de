---
description: Die findcard-Methode sucht nach der Smartcard und öffnet eine gültige Verbindung.
ms.assetid: ab97eff2-0f41-4a6f-98b3-d5ad5883fa07
title: 'Iscardlocate:: findcard-Methode (scardmgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardLocate.FindCard
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: bf3cf05ff6e6040d5cac2bde161fa2eea07d5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360517"
---
# <a name="iscardlocatefindcard-method"></a><span data-ttu-id="c4bb9-103">Iscardlocate:: findcard-Methode</span><span class="sxs-lookup"><span data-stu-id="c4bb9-103">ISCardLocate::FindCard method</span></span>

<span data-ttu-id="c4bb9-104">\[Die **findcard** -Methode ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-104">\[The **FindCard** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="c4bb9-105">Es ist nicht für die Verwendung in Windows Server 2003 mit Service Pack 1 (SP1) und höher, Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-105">It is not available for use in Windows Server 2003 with Service Pack 1 (SP1) and later, Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="c4bb9-106">Die [Smartcard-Module](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten eine ähnliche Funktionalität.\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-106">The [Smart Card Modules](/previous-versions/windows/desktop/secsmart/smart-card-modules) provide similar functionality.\]</span></span>

<span data-ttu-id="c4bb9-107">Die **findcard** -Methode sucht nach der [*Smartcard*](../secgloss/s-gly.md) und öffnet eine gültige Verbindung.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-107">The **FindCard** method searches for the [*smart card*](../secgloss/s-gly.md) and opens a valid connection to it.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4bb9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4bb9-108">Syntax</span></span>


```C++
HRESULT FindCard(
  [in]  SCARD_SHARE_MODES ShareMode,
  [in]  SCARD_PROTOCOLS   Protocols,
  [in]  LONG              lFlags,
  [out] LPSCARDINFO       *ppCardInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c4bb9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4bb9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4bb9-110">*Share Mode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-110">*ShareMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bb9-111">Der Modus, in dem die Smartcard gemeinsam genutzt oder nicht freigegeben werden soll, wenn eine Verbindung damit geöffnet ist.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-111">Mode in which to share or not share the smart card when a connection is opened to it.</span></span>



| <span data-ttu-id="c4bb9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="c4bb9-112">Value</span></span>                                                                                                                                            | <span data-ttu-id="c4bb9-113">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4bb9-113">Meaning</span></span>                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <span data-ttu-id="c4bb9-114"><dt>**Ausschließliche**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-114"><dt>**EXCLUSIVE**</dt></span></span> </dl> | <span data-ttu-id="c4bb9-115">Diese Verbindung wird von keiner anderen Person mit der Smartcard verwendet.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-115">No one else use this connection to the smart card.</span></span><br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <span data-ttu-id="c4bb9-116"><dt>**Genu**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-116"><dt>**SHARED**</dt></span></span> </dl>          | <span data-ttu-id="c4bb9-117">Diese Verbindung kann von anderen Anwendungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-117">Other applications can use this connection.</span></span><br/>        |



 

</dd> <dt>

<span data-ttu-id="c4bb9-118">*Protokolle* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-118">*Protocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bb9-119">Protokoll, das beim Herstellen einer Verbindung mit der Karte verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-119">Protocol to use when connecting to the card.</span></span>

<span data-ttu-id="c4bb9-120">T0</span><span class="sxs-lookup"><span data-stu-id="c4bb9-120">T0</span></span>

<span data-ttu-id="c4bb9-121">T1</span><span class="sxs-lookup"><span data-stu-id="c4bb9-121">T1</span></span>

<span data-ttu-id="c4bb9-122">RAW</span><span class="sxs-lookup"><span data-stu-id="c4bb9-122">RAW</span></span>

<span data-ttu-id="c4bb9-123">T0 \| T1</span><span class="sxs-lookup"><span data-stu-id="c4bb9-123">T0\|T1</span></span>

</dd> <dt>

<span data-ttu-id="c4bb9-124">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-124">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bb9-125">Gibt an, wann die [*Benutzeroberfläche*](../secgloss/u-gly.md) angezeigt wird:</span><span class="sxs-lookup"><span data-stu-id="c4bb9-125">Specifies when [*user interface*](../secgloss/u-gly.md) is displayed:</span></span>



| <span data-ttu-id="c4bb9-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c4bb9-126">Value</span></span>                                                                                                                                                                       | <span data-ttu-id="c4bb9-127">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c4bb9-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SC_DLG_MINIMAL_UI"></span><span id="sc_dlg_minimal_ui"></span><dl> <span data-ttu-id="c4bb9-128"><dt>**SC \_ DLG \_ minimale \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-128"><dt>**SC\_DLG\_MINIMAL\_UI**</dt></span></span> </dl> | <span data-ttu-id="c4bb9-129">Zeigt das Dialogfeld nur an, wenn die Karte, die von der aufrufenden Anwendung gesucht wird, nicht gefunden wurde und für die Verwendung in einem Reader verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-129">Displays the dialog box only if the card being searched for by the calling application is not located and available for use in a reader.</span></span> <span data-ttu-id="c4bb9-130">Dadurch kann die Karte gefunden und verbunden werden (entweder über einen internen Dialogfeld Mechanismus oder mithilfe der Benutzer Rückruf Funktionen) und an die aufrufende Anwendung zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-130">This allows the card to be found, connected (either through an internal dialog box mechanism or by using the user callback functions), and returned to the calling application.</span></span><br/> |
| <span id="SC_DLG_NO_UI"></span><span id="sc_dlg_no_ui"></span><dl> <span data-ttu-id="c4bb9-131"><dt>**SC \_ DLG \_ keine \_ Benutzeroberfläche**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-131"><dt>**SC\_DLG\_NO\_UI**</dt></span></span> </dl>                | <span data-ttu-id="c4bb9-132">Bewirkt, dass unabhängig vom Suchergebnis keine Anzeige auf der Benutzeroberfläche angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-132">Causes no UI display, regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                  |
| <span id="SC_DLG_FORCE_UI"></span><span id="sc_dlg_force_ui"></span><dl> <span data-ttu-id="c4bb9-133"><dt>**SC \_ DLG \_ Force \_ UI**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-133"><dt>**SC\_DLG\_FORCE\_UI**</dt></span></span> </dl>       | <span data-ttu-id="c4bb9-134">Bewirkt, dass die Benutzeroberfläche unabhängig vom Suchergebnis angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-134">Causes UI display regardless of the search outcome.</span></span><br/>                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="c4bb9-135">*ppcardinfo* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-135">*ppCardInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c4bb9-136">Ein Zeiger auf einen Zeiger auf eine Datenstruktur, die Informationen über die geöffnete [*Smartcard*](../secgloss/s-gly.md)enthält oder zurückgibt, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-136">Pointer to a pointer to a data structure that contains or returns information about the opened [*smart card*](../secgloss/s-gly.md), if successful.</span></span> <span data-ttu-id="c4bb9-137">Ist **null** , wenn der Vorgang fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-137">Will be **NULL** if operation has failed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4bb9-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c4bb9-138">Return value</span></span>

<span data-ttu-id="c4bb9-139">Die-Methode gibt einen der folgenden möglichen Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-139">The method returns one of the following possible values.</span></span>



| <span data-ttu-id="c4bb9-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c4bb9-140">Return code</span></span>                                                                                   | <span data-ttu-id="c4bb9-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4bb9-141">Description</span></span>                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="c4bb9-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-142"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="c4bb9-143">Operation erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-143">Operation completed successfully.</span></span><br/>         |
| <dl> <span data-ttu-id="c4bb9-144"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-144"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="c4bb9-145">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-145">Invalid parameter.</span></span><br/>                        |
| <dl> <span data-ttu-id="c4bb9-146"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-146"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="c4bb9-147">Ein fehlerhafter Zeiger wurde in *ppcardinfo* übermittelt.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-147">A bad pointer was passed in *ppCardInfo*.</span></span><br/> |
| <dl> <span data-ttu-id="c4bb9-148"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-148"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="c4bb9-149">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-149">Out of memory.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="c4bb9-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c4bb9-150">Remarks</span></span>

<span data-ttu-id="c4bb9-151">Um die Suchkriterien für die Suche festzulegen, geben Sie " [**konfigurierter Name**](iscardlocate-configurecardnamesearch.md) der Smartcard" an.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-151">To set the search criteria of the search, call [**ConfigureCardNameSearch**](iscardlocate-configurecardnamesearch.md) to specify a smart card's card names.</span></span>

<span data-ttu-id="c4bb9-152">Eine Liste aller Methoden, die von dieser Schnittstelle bereitgestellt werden, finden Sie unter [**iscardlocate**](iscardlocate.md).</span><span class="sxs-lookup"><span data-stu-id="c4bb9-152">For a list of all the methods provided by this interface, see [**ISCardLocate**](iscardlocate.md).</span></span>

<span data-ttu-id="c4bb9-153">Zusätzlich zu den oben aufgeführten com-Fehlercodes gibt diese Schnittstelle möglicherweise einen Fehlercode für die Smartcard zurück, wenn eine smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-153">In addition to the COM error codes listed above, this interface may return a smart card error code if a smart card function was called to complete the request.</span></span> <span data-ttu-id="c4bb9-154">Weitere Informationen finden Sie unter [Smartcard-Rückgabewerte](authentication-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="c4bb9-154">For more information, see [Smart Card Return Values](authentication-return-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c4bb9-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c4bb9-155">Requirements</span></span>



| <span data-ttu-id="c4bb9-156">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c4bb9-156">Requirement</span></span> | <span data-ttu-id="c4bb9-157">Wert</span><span class="sxs-lookup"><span data-stu-id="c4bb9-157">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c4bb9-158">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c4bb9-158">Minimum supported client</span></span><br/> | <span data-ttu-id="c4bb9-159">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-159">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c4bb9-160">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c4bb9-160">Minimum supported server</span></span><br/> | <span data-ttu-id="c4bb9-161">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c4bb9-161">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c4bb9-162">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="c4bb9-162">End of client support</span></span><br/>    | <span data-ttu-id="c4bb9-163">Windows XP</span><span class="sxs-lookup"><span data-stu-id="c4bb9-163">Windows XP</span></span><br/>                                                                   |
| <span data-ttu-id="c4bb9-164">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="c4bb9-164">End of server support</span></span><br/>    | <span data-ttu-id="c4bb9-165">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="c4bb9-165">Windows Server 2003</span></span><br/>                                                          |
| <span data-ttu-id="c4bb9-166">Header</span><span class="sxs-lookup"><span data-stu-id="c4bb9-166">Header</span></span><br/>                   | <dl> <span data-ttu-id="c4bb9-167"><dt>"Scardmgr. h"</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-167"><dt>Scardmgr.h</dt></span></span> </dl>   |
| <span data-ttu-id="c4bb9-168">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c4bb9-168">Type library</span></span><br/>             | <dl> <span data-ttu-id="c4bb9-169"><dt>Scardmgr. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-169"><dt>Scardmgr.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c4bb9-170">DLL</span><span class="sxs-lookup"><span data-stu-id="c4bb9-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c4bb9-171"><dt>Scardssp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c4bb9-171"><dt>Scardssp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c4bb9-172">IID</span><span class="sxs-lookup"><span data-stu-id="c4bb9-172">IID</span></span><br/>                      | <span data-ttu-id="c4bb9-173">IID \_ iscardlocate ist als 1461aacd-6810-11D0-918f -00aa00c18068 definiert.</span><span class="sxs-lookup"><span data-stu-id="c4bb9-173">IID\_ISCardLocate is defined as 1461AACD-6810-11D0-918F-00AA00C18068</span></span><br/>         |



## <a name="see-also"></a><span data-ttu-id="c4bb9-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4bb9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4bb9-175">**Konfigurieren von "Konfigurations namesearch"**</span><span class="sxs-lookup"><span data-stu-id="c4bb9-175">**ConfigureCardNameSearch**</span></span>](iscardlocate-configurecardnamesearch.md)
</dt> <dt>

[<span data-ttu-id="c4bb9-176">**Iscardsuche**</span><span class="sxs-lookup"><span data-stu-id="c4bb9-176">**ISCardLocate**</span></span>](iscardlocate.md)
</dt> </dl>

 

 
