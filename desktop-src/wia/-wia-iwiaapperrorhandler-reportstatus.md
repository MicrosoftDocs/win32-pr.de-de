---
description: Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.
ms.assetid: 8d3ba598-8649-4108-aebc-94f2bcb64ad8
title: 'Iwiaapperrorhandler:: Report Status-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaAppErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 1285b5391014919d7108f207917b0c44c03fa360
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356532"
---
# <a name="iwiaapperrorhandlerreportstatus-method"></a><span data-ttu-id="afc82-103">Iwiaapperrorhandler:: Report Status-Methode</span><span class="sxs-lookup"><span data-stu-id="afc82-103">IWiaAppErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="afc82-104">Verarbeitet den Gerätestatus und Fehlermeldungen während der Bild Datenübertragungen und zeigt dem Benutzer die Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="afc82-104">Handles device status and error messages during image data transfers and displays the messages to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="afc82-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="afc82-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] LONG      lFlags,
  [in] IWiaItem2 *pWiaItem2,
  [in] HRESULT   hrStatus,
  [in] LONG      lPercentComplete
);
```



## <a name="parameters"></a><span data-ttu-id="afc82-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="afc82-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="afc82-107">*lFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc82-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc82-108">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="afc82-108">Type: **LONG**</span></span>

<span data-ttu-id="afc82-109">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="afc82-109">Not used.</span></span> <span data-ttu-id="afc82-110">Auf 0 festlegen.</span><span class="sxs-lookup"><span data-stu-id="afc82-110">Set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="afc82-111">*pWiaItem2* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc82-111">*pWiaItem2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc82-112">Typ: \**[**IWiaItem2**](-wia-iwiaitem2.md) \** _</span><span class="sxs-lookup"><span data-stu-id="afc82-112">Type: \**[**IWiaItem2**](-wia-iwiaitem2.md)\** _</span></span>

<span data-ttu-id="afc82-113">Zeiger auf das Element, das übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="afc82-113">Pointer to the item being transferred.</span></span>

</dd> <dt>

<span data-ttu-id="afc82-114">_hrStatus \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc82-114">_hrStatus\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc82-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="afc82-115">Type: **HRESULT**</span></span>

<span data-ttu-id="afc82-116">Gerätestatus Code.</span><span class="sxs-lookup"><span data-stu-id="afc82-116">Device status code.</span></span>

</dd> <dt>

<span data-ttu-id="afc82-117">*lprozentuabgeschlossen* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="afc82-117">*lPercentComplete* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="afc82-118">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="afc82-118">Type: **LONG**</span></span>

<span data-ttu-id="afc82-119">Der Prozentsatz des aktuellen Vorgangs.</span><span class="sxs-lookup"><span data-stu-id="afc82-119">Percentage completed of current operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="afc82-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="afc82-120">Return value</span></span>

<span data-ttu-id="afc82-121">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="afc82-121">Type: **HRESULT**</span></span>

<span data-ttu-id="afc82-122">Gibt " *hrStatus* " zurück, wenn die Wiederherstellung nach dem Fehler nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="afc82-122">Returns *hrStatus* if recovery from the error is not possible.</span></span> <span data-ttu-id="afc82-123">Andernfalls wird einer der folgenden Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="afc82-123">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="afc82-124">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="afc82-124">Return code</span></span>                                                                                              | <span data-ttu-id="afc82-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="afc82-125">Description</span></span>                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="afc82-126"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-126"><dt>**S\_OK**</dt></span></span> </dl>                     | <span data-ttu-id="afc82-127">Wenn *hrStatus* ein Fehler ist, wurde die entsprechende Aktion ausgeführt, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="afc82-127">If *hrStatus* is an error, the appropriate action was taken to correct the error, and the transfer can continue.</span></span> <span data-ttu-id="afc82-128">Wenn *hrStatus* Information lautet, wurde der Benutzer über ein nicht modalem Dialogfeld informiert, und die Übertragung konnte nicht abgebrochen werden.</span><span class="sxs-lookup"><span data-stu-id="afc82-128">If *hrStatus* is informational, the user was informed with a modeless dialog box and chose not to cancel the transfer.</span></span><br/> |
| <dl> <span data-ttu-id="afc82-129"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-129"><dt>**S\_FALSE**</dt></span></span> </dl>                  | <span data-ttu-id="afc82-130">Der Benutzer hat die Übertragung aus dem Dialogfeld "Fehlerhandler-nicht modelliert" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="afc82-130">The user cancelled the transfer from the error handler modeless dialog box.</span></span> <span data-ttu-id="afc82-131">Dieser Wert kann jederzeit unabhängig von *hrStatus* zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="afc82-131">This value can be returned at any point no matter what *hrStatus* is.</span></span> <br/>                                                                                      |
| <dl> <span data-ttu-id="afc82-132"><dt>**WIA- \_ Status \_ nicht \_ behandelt**</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-132"><dt>**WIA\_STATUS\_NOT\_HANDLED**</dt></span></span> </dl> | <span data-ttu-id="afc82-133">Es wurde keine Aktion ausgeführt. Das heißt, dem Benutzer wurde kein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="afc82-133">No action was taken; that is, no dialog box was presented to the user.</span></span> <span data-ttu-id="afc82-134">Der nächste Fehlerhandler wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="afc82-134">The next error handler will be invoked.</span></span> <span data-ttu-id="afc82-135">Die Reihenfolge von Fehler Handlern lautet: Anwendung, Treiber und System Standard.</span><span class="sxs-lookup"><span data-stu-id="afc82-135">The order of error handlers is: application, driver, and system default.</span></span><br/>                                                 |



 

## <a name="remarks"></a><span data-ttu-id="afc82-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afc82-136">Remarks</span></span>

<span data-ttu-id="afc82-137">Der *lprozentucomplete* -Parameter ermöglicht einem fehlerhandlerfenster, den Fortschritt anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="afc82-137">The *lPercentComplete* parameter enables an error handler window to show progress.</span></span> <span data-ttu-id="afc82-138">Ein Treiber könnte z. b. eine Schätzung der Dauer der "Aufwärm Dauer" bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="afc82-138">For example, a driver might provide an estimate of how long "warming up" takes.</span></span> <span data-ttu-id="afc82-139">Der an **iwiaapperrorhandler:: Report Status** übergebenen *lprozentucomplete* -Parameter ist derselbe Wert wie der **lprozentucomplete** , den der Treiber in der [**wiatransferparameams**](-wia-wiatransferparams.md) -Struktur festlegt.</span><span class="sxs-lookup"><span data-stu-id="afc82-139">The *lPercentComplete* parameter passed into **IWiaAppErrorHandler::ReportStatus** is the same value as the **lPercentComplete** that the driver sets into the [**WiaTransferParams**](-wia-wiatransferparams.md) structure.</span></span>

<span data-ttu-id="afc82-140">Ein Fehlerhandler kann die Makros "erfolgreich" und "fehlgeschlagen" verwenden, um herauszufinden, ob " *hrStatus* " einen Schweregrad \_ oder einen Schweregrad " \_</span><span class="sxs-lookup"><span data-stu-id="afc82-140">An error handler can use the SUCCEEDED and FAILED macros to find out if *hrStatus* has SEVERITY\_ERROR or SEVERITY\_SUCCESS.</span></span>

<span data-ttu-id="afc82-141">Wenn *hrStatus* den Schweregrad \_ Success hat, sollte der Benutzer die Übertragung abbrechen dürfen.</span><span class="sxs-lookup"><span data-stu-id="afc82-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

<span data-ttu-id="afc82-142">Wenn für *hrStatus* der Schweregrad \_ Fehler vorliegt, sollte der Fehlerhandler ein modales Dialogfeld im Besitz des übergeordneten Fensters der Anwendung anzeigen.</span><span class="sxs-lookup"><span data-stu-id="afc82-142">If *hrStatus* is SEVERITY\_ERROR, the error handler should display a modal dialog box owned by the application parent window.</span></span>

## <a name="requirements"></a><span data-ttu-id="afc82-143">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afc82-143">Requirements</span></span>



| <span data-ttu-id="afc82-144">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afc82-144">Requirement</span></span> | <span data-ttu-id="afc82-145">Wert</span><span class="sxs-lookup"><span data-stu-id="afc82-145">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="afc82-146">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afc82-146">Minimum supported client</span></span><br/> | <span data-ttu-id="afc82-147">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc82-147">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="afc82-148">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afc82-148">Minimum supported server</span></span><br/> | <span data-ttu-id="afc82-149">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afc82-149">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="afc82-150">Header</span><span class="sxs-lookup"><span data-stu-id="afc82-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="afc82-151"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-151"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="afc82-152">IDL</span><span class="sxs-lookup"><span data-stu-id="afc82-152">IDL</span></span><br/>                      | <dl> <span data-ttu-id="afc82-153"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-153"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="afc82-154">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="afc82-154">Library</span></span><br/>                  | <dl> <span data-ttu-id="afc82-155"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="afc82-155"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 




