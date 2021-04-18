---
description: Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.
ms.assetid: 23e85c63-80b9-4510-854d-289c8d23be2d
title: 'Iwiaerrorhandler:: Report Status-Methode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.ReportStatus
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 30a082502d4c7bc5b789fd1ec19fdb76f63d8fab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357770"
---
# <a name="iwiaerrorhandlerreportstatus-method"></a><span data-ttu-id="54620-103">Iwiaerrorhandler:: Report Status-Methode</span><span class="sxs-lookup"><span data-stu-id="54620-103">IWiaErrorHandler::ReportStatus method</span></span>

<span data-ttu-id="54620-104">Verarbeitet Status-und Fehlermeldungen während der Bild Datenübertragungen und zeigt Sie dem Benutzer an.</span><span class="sxs-lookup"><span data-stu-id="54620-104">Handles status and error messages during image data transfers and displays them to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="54620-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="54620-105">Syntax</span></span>


```C++
HRESULT ReportStatus(
  [in] HWND     hwndParent,
  [in] IUnknown *punkItem,
  [in] HRESULT  hrStatus,
  [in] LONG     cbResLength,
  [in] BYTE     *pbData
);
```



## <a name="parameters"></a><span data-ttu-id="54620-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54620-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54620-107">*hwndParent* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54620-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54620-108">Typ: **HWND**</span><span class="sxs-lookup"><span data-stu-id="54620-108">Type: **HWND**</span></span>

<span data-ttu-id="54620-109">**HWND** , das das übergeordnete Fenster für das Nachrichtenfenster ist.</span><span class="sxs-lookup"><span data-stu-id="54620-109">**HWND** that is the parent window for the message window.</span></span>

</dd> <dt>

<span data-ttu-id="54620-110">*punkitem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54620-110">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54620-111">Typ: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="54620-111">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="54620-112">Ein Zeiger auf die [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle des übertragenen Elements.</span><span class="sxs-lookup"><span data-stu-id="54620-112">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface of the item being transferred.</span></span> <span data-ttu-id="54620-113">Dieses Objekt implementiert mindestens [_ *IWiaItem2* \*](-wia-iwiaitem2.md) und [**iwiadatatransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="54620-113">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="54620-114">*hrStatus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54620-114">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54620-115">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="54620-115">Type: **HRESULT**</span></span>

<span data-ttu-id="54620-116">**HRESULT** , das der von [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangene Statuscode ist.</span><span class="sxs-lookup"><span data-stu-id="54620-116">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="54620-117">*cbreslength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54620-117">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54620-118">Type: **Long**</span><span class="sxs-lookup"><span data-stu-id="54620-118">Type: **LONG**</span></span>

<span data-ttu-id="54620-119">**Long** , d. h. die Größe der Daten, auf die von *pbData* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="54620-119">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="54620-120">*pbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="54620-120">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54620-121">Typ: \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="54620-121">Type: \**BYTE\** _</span></span>

<span data-ttu-id="54620-122">Zeiger auf den Datenpuffer, wie von [_ *banbeddatacallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)empfangen.</span><span class="sxs-lookup"><span data-stu-id="54620-122">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54620-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54620-123">Return value</span></span>

<span data-ttu-id="54620-124">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="54620-124">Type: **HRESULT**</span></span>

<span data-ttu-id="54620-125">Gibt *hrStatus* zurück, wenn der Fehler nicht von wieder hergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="54620-125">Returns *hrStatus* if the error cannot be recovered from.</span></span> <span data-ttu-id="54620-126">Andernfalls wird einer der folgenden Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54620-126">Otherwise, it returns one of the following values.</span></span>



| <span data-ttu-id="54620-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="54620-127">Return code</span></span>                                                                             | <span data-ttu-id="54620-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="54620-128">Description</span></span>                                                                                      |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="54620-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="54620-129"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="54620-130">Die entsprechende Aktion wurde durchgeführt, um den Fehler zu beheben, und die Übertragung kann fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="54620-130">The appropriate action was taken to correct the error and the transfer can continue.</span></span> <br/> |
| <dl> <span data-ttu-id="54620-131"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="54620-131"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="54620-132">Es wurde keine Aktion zum Behandeln des Fehlers oder zum Melden des Status für den Benutzer ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54620-132">No action was taken to handle the error or report status to the user.</span></span> <br/>                |
| <dl> <span data-ttu-id="54620-133"><dt>**E \_ Abbrechen**</dt></span><span class="sxs-lookup"><span data-stu-id="54620-133"><dt>**E\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="54620-134">Der Benutzer hat die Übertragung als Reaktion auf das angezeigte Dialogfeld abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="54620-134">The user chose to abort the transfer in response to the displayed dialog box.</span></span> <br/>        |



 

## <a name="remarks"></a><span data-ttu-id="54620-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54620-135">Remarks</span></span>

<span data-ttu-id="54620-136">Windows-Abbild Beschaffung (WIA) 2,0 ruft **iwiaerrorhandler:: Report Status** auf, wenn der Treiber eine IT-Nachrichten **\_ \_ Geräte \_ Status** Meldung an [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback)sendet.</span><span class="sxs-lookup"><span data-stu-id="54620-136">Windows Image Acquisition (WIA) 2.0 calls **IWiaErrorHandler::ReportStatus** when the driver sends an **IT\_MSG\_DEVICE\_STATUS** message to [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span> <span data-ttu-id="54620-137">Diese Methode verarbeitet die Nachricht und zeigt dem Benutzerinformationen zum Status oder Fehler an.</span><span class="sxs-lookup"><span data-stu-id="54620-137">This method handles the message and displays information to the user about the status or error.</span></span> <span data-ttu-id="54620-138">Wenn es sich bei der Nachricht um einen Fehler handelt, kann der Benutzer die Methode nach Möglichkeit auswählen, ob versucht werden soll, den Fehler zu beheben und die Übertragung fortzusetzen oder abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="54620-138">If the message is about an error, the method lets the user choose, if possible, whether to try to recover from the error and continue the transfer or to abort.</span></span>

<span data-ttu-id="54620-139">*hrStatus* ist auf WIA \_ Status \_ Transfer BEGIN festgelegt \_ , um den Handler darüber zu informieren, dass eine Übertragung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="54620-139">*hrStatus* is set to WIA\_STATUS\_TRANSFER\_BEGIN to inform the handler a transfer has started.</span></span> <span data-ttu-id="54620-140">\_ \_ \_ Wenn die Übertragung abgeschlossen ist, wird Sie auf das Ende der Status Übertragung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54620-140">It is set to WIA\_STATUS\_TRANSFER\_END when the transfer is complete.</span></span>

<span data-ttu-id="54620-141">Wenn *hrStatus* den Schweregrad \_ Success hat, sollte der Benutzer die Übertragung abbrechen dürfen.</span><span class="sxs-lookup"><span data-stu-id="54620-141">If *hrStatus* is SEVERITY\_SUCCESS, the user should be allowed to cancel the transfer.</span></span>

## <a name="requirements"></a><span data-ttu-id="54620-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="54620-142">Requirements</span></span>



| <span data-ttu-id="54620-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="54620-143">Requirement</span></span> | <span data-ttu-id="54620-144">Wert</span><span class="sxs-lookup"><span data-stu-id="54620-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="54620-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="54620-145">Minimum supported client</span></span><br/> | <span data-ttu-id="54620-146">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54620-146">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="54620-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="54620-147">Minimum supported server</span></span><br/> | <span data-ttu-id="54620-148">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="54620-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="54620-149">Header</span><span class="sxs-lookup"><span data-stu-id="54620-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="54620-150"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="54620-150"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="54620-151">IDL</span><span class="sxs-lookup"><span data-stu-id="54620-151">IDL</span></span><br/>                      | <dl> <span data-ttu-id="54620-152"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="54620-152"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="54620-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="54620-153">Library</span></span><br/>                  | <dl> <span data-ttu-id="54620-154"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="54620-154"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
