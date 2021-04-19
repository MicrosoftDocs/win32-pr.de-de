---
title: Iwmdrmlicenabmanagement AcquireLicense-Methode (wmdrmsdk. h)
description: Die AcquireLicense-Methode ruft asynchron eine Lizenz von einer angegebenen URL ab.
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- AcquireLicense-Methode, Windows Media-Format
- AcquireLicense-Methode Windows Media-Format, iwmdrmlicensmanagement-Schnittstelle
- Iwmdrmlicenabmanagement-Schnittstelle Windows Media-Format, AcquireLicense-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 279a3d4d84617c4a4fa5454d1f39f6f78f0cf3fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352959"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a><span data-ttu-id="30afa-106">Iwmdrmlicenabmanagement:: AcquireLicense-Methode</span><span class="sxs-lookup"><span data-stu-id="30afa-106">IWMDRMLicenseManagement::AcquireLicense method</span></span>

<span data-ttu-id="30afa-107">Die **AcquireLicense** -Methode ruft asynchron eine Lizenz von einer angegebenen URL ab.</span><span class="sxs-lookup"><span data-stu-id="30afa-107">The **AcquireLicense** method asynchronously acquires a license from a specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="30afa-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30afa-108">Syntax</span></span>


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="30afa-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30afa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30afa-110">*bstrinurl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30afa-110">*bstrURL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30afa-111">Die URL des Lizenzservers, von dem die Lizenz abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="30afa-111">URL of the license server from which to acquire the license.</span></span> <span data-ttu-id="30afa-112">Übergeben Sie **null** , damit die-Methode die URL aus dem Content-Header analysieren muss.</span><span class="sxs-lookup"><span data-stu-id="30afa-112">Pass **NULL** to have the method parse the URL from the content header.</span></span>

</dd> <dt>

<span data-ttu-id="30afa-113">*bstrinheaderdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30afa-113">*bstrHeaderData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30afa-114">Inhalts Header, der an den Lizenzserver übermittelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="30afa-114">Content header to be passed to the license server.</span></span> <span data-ttu-id="30afa-115">Wenn *bstrinurl* **null** ist, analysiert die Methode die URL aus diesem Header.</span><span class="sxs-lookup"><span data-stu-id="30afa-115">If *bstrURL* is **NULL**, the method will parse the URL from this header.</span></span> <span data-ttu-id="30afa-116">Wenn *dwFlags* auf WMDRM-Lizenz "Legacy" für "nicht unbeaufsichtigt" festlegen festgelegt ist \_ \_ \_ \_ , legen Sie diesen Wert auf die Schlüssel-ID anstelle des gesamten Inhalts Headers fest.</span><span class="sxs-lookup"><span data-stu-id="30afa-116">If *dwFlags* is set to WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT, set this value to the key ID instead of the entire content header.</span></span>

</dd> <dt>

<span data-ttu-id="30afa-117">*bstractions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30afa-117">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30afa-118">Eine Zeichenfolge, die NULL oder mehr Aktionen enthält, für die die Berechtigung in der Lizenz angefordert werden soll.</span><span class="sxs-lookup"><span data-stu-id="30afa-118">String containing zero or more actions for which to request permission in the license.</span></span> <span data-ttu-id="30afa-119">Die Zeichenfolge muss wie folgt formatiert werden:</span><span class="sxs-lookup"><span data-stu-id="30afa-119">The string must be formatted as follows:</span></span>

-   <span data-ttu-id="30afa-120">Jede Aktion muss innerhalb eines Action-Elements definiert werden.</span><span class="sxs-lookup"><span data-stu-id="30afa-120">Each action must be defined within an ACTION element.</span></span> <span data-ttu-id="30afa-121">Die Daten des Elements sind die Aktions Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="30afa-121">The data of the element is the action string.</span></span>
-   <span data-ttu-id="30afa-122">Alle Aktions Elemente müssen in einem Action list-Element enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="30afa-122">All ACTION elements must be contained within an ACTIONLIST element.</span></span>

    <span data-ttu-id="30afa-123">Beispielsweise wird die Zeichenfolge zum Anfordern einer Lizenz für die Wiedergabe von Inhalten wie folgt formatiert:</span><span class="sxs-lookup"><span data-stu-id="30afa-123">For example, the string to request a license to play content is formatted like this:</span></span>

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

<span data-ttu-id="30afa-124">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30afa-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30afa-125">Options Flags für die Lizenz Beschaffung.</span><span class="sxs-lookup"><span data-stu-id="30afa-125">License acquisition option flags.</span></span> <span data-ttu-id="30afa-126">Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="30afa-126">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="30afa-127">Konstante</span><span class="sxs-lookup"><span data-stu-id="30afa-127">Constant</span></span>                                   | <span data-ttu-id="30afa-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="30afa-128">Description</span></span>                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30afa-129">WMDRM-Lizenz wird automatisch abgerufen \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="30afa-129">WMDRM\_ACQUIRE\_LICENSE\_SILENT</span></span>            | <span data-ttu-id="30afa-130">Die Lizenz wird ohne Bestätigung durch die Client Anwendung direkt über das Internet ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="30afa-130">The license will be issued directly over the Internet without any confirmation from the client application.</span></span>              |
| <span data-ttu-id="30afa-131">WMDRM \_ - \_ Lizenz \_ nicht unbeaufsichtigt erwerben</span><span class="sxs-lookup"><span data-stu-id="30afa-131">WMDRM\_ACQUIRE\_LICENSE\_NONSILENT</span></span>         | <span data-ttu-id="30afa-132">Das DRM-Subsystem erstellt eine Lizenz Anforderung, die asynchron für die Bereitstellung auf dem Lizenzserver zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="30afa-132">The DRM subsystem will create a license request which will be returned asynchronously for posting to the license server.</span></span> |
| <span data-ttu-id="30afa-133">WMDRM \_ - \_ Lizenz für \_ ältere Lizenz \_</span><span class="sxs-lookup"><span data-stu-id="30afa-133">WMDRM\_ACQUIRE\_LICENSE\_LEGACY\_NONSILENT</span></span> | <span data-ttu-id="30afa-134">Identisch mit der WMDRM \_ - \_ \_ Erstellungs Lizenz, mit der Ausnahme, dass eine Lizenz Herausforderung der DRM-Version 1 erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="30afa-134">The same as WMDRM\_ACQUIRE\_LICENSE\_NONSILENT, except that a DRM version 1 license challenge will be created.</span></span>           |



 

</dd> <dt>

<span data-ttu-id="30afa-135">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="30afa-135">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="30afa-136">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="30afa-136">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="30afa-137">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30afa-137">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30afa-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30afa-138">Return value</span></span>

<span data-ttu-id="30afa-139">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="30afa-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="30afa-140">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30afa-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="30afa-141">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30afa-141">Return code</span></span>                                                                          | <span data-ttu-id="30afa-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30afa-142">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="30afa-143"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30afa-143"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="30afa-144">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30afa-144">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30afa-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30afa-145">Remarks</span></span>

<span data-ttu-id="30afa-146">Diese Methode wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30afa-146">This method executes asynchronously.</span></span> <span data-ttu-id="30afa-147">Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann ein **mewmdrmlicenabacquisitioncomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="30afa-147">It returns immediately after being called and then generates an **MEWMDRMLicenseAcquisitionCompleted** event when processing is complete.</span></span> <span data-ttu-id="30afa-148">Bei nicht automatischen Lizenz Erwerbs Vorgängen ist der Wert des Ereignisses, das durch den Aufruf von **imfmediaevent:: GetValue** abgerufen wurde, ein **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="30afa-148">For non-silent license acquisition operations, the value of the event obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="30afa-149">Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle zum Abrufen einer Instanz der [**iwmdrmnonsilentlicenseaquisition**](iwmdrmnonsilentlicenseaquisition.md) -Schnittstelle abrufen.</span><span class="sxs-lookup"><span data-stu-id="30afa-149">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md) interface.</span></span>

<span data-ttu-id="30afa-150">Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="30afa-150">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30afa-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30afa-151">Requirements</span></span>



| <span data-ttu-id="30afa-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30afa-152">Requirement</span></span> | <span data-ttu-id="30afa-153">Wert</span><span class="sxs-lookup"><span data-stu-id="30afa-153">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30afa-154">Header</span><span class="sxs-lookup"><span data-stu-id="30afa-154">Header</span></span><br/>  | <dl> <span data-ttu-id="30afa-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="30afa-155"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="30afa-156">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30afa-156">Library</span></span><br/> | <dl> <span data-ttu-id="30afa-157"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30afa-157"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30afa-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30afa-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30afa-159">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30afa-159">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> <dt>

[<span data-ttu-id="30afa-160">**Automatische Lizenz Beschaffung**</span><span class="sxs-lookup"><span data-stu-id="30afa-160">**Silent License Acquisition**</span></span>](silent-license-acquisition.md)
</dt> </dl>

 

 





