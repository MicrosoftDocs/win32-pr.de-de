---
title: Methode ' iwmdrmdeviceapp acquiredevicedata ' (wmdrmdeviceapp. h)
description: Die acquiredevicedata-Methode initialisiert oder setzt eine sichere Uhr des Geräts zurück.
ms.assetid: 2f1cfdb9-0f07-4bee-94aa-b33b039453d0
keywords:
- Acquiredevicedata-Methode, Windows Media Device Manager
- Acquiredevicedata-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, acquiredevicedata-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.AcquireDeviceData
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 268572e5dad3dffd0fe15956a0ff145f277fb6db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368522"
---
# <a name="iwmdrmdeviceappacquiredevicedata-method"></a><span data-ttu-id="1029c-106">Iwmdrmdeviceapp:: acquiredevicedata-Methode</span><span class="sxs-lookup"><span data-stu-id="1029c-106">IWMDRMDeviceApp::AcquireDeviceData method</span></span>

<span data-ttu-id="1029c-107">Die **acquiredevicedata** -Methode initialisiert oder setzt eine sichere Uhr des Geräts zurück.</span><span class="sxs-lookup"><span data-stu-id="1029c-107">The **AcquireDeviceData** method initializes or resets a device secure clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="1029c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1029c-108">Syntax</span></span>


```C++
HRESULT AcquireDeviceData(
  [in]  IWMDMDevice    *pDevice,
  [in]  IWMDMProgress3 *pProgressCallback,
  [in]  DWORD          dwFlags,
  [out] DWORD          *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="1029c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1029c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1029c-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1029c-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1029c-111">Zeiger auf eine [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle für das Gerät, das Messungs Daten meldet.</span><span class="sxs-lookup"><span data-stu-id="1029c-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface for the device that will report metering data.</span></span>

</dd> <dt>

<span data-ttu-id="1029c-112">*pprogresscallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1029c-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1029c-113">Der Fortschritts Rückruf, über den die Anwendung den Status des Ereignisses verfolgen kann, oder das Ereignis abbrechen.</span><span class="sxs-lookup"><span data-stu-id="1029c-113">Progress callback through which the application can track the progress of the event, or cancel the event.</span></span> <span data-ttu-id="1029c-114">Der Fortschritt wird durch den *EventID-* Parameter der [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) -Methoden identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1029c-114">The progress is identified by the *EventId* parameter of [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) methods.</span></span>

</dd> <dt>

<span data-ttu-id="1029c-115">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1029c-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1029c-116">Ein logisches **or** von einem oder beiden der folgenden Flags, das angibt, welche Aktion ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1029c-116">A logical **OR** of one or both of the following flags, specifying what action to perform.</span></span> <span data-ttu-id="1029c-117">Dieser Wert wird aus dem *pdwstatus* -Parameter von [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1029c-117">This value is retrieved from the *pdwStatus* parameter of [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span> <span data-ttu-id="1029c-118">Sie können das *pdwstatus* -Flag direkt verwenden.</span><span class="sxs-lookup"><span data-stu-id="1029c-118">You can use the *pdwStatus* flag directly.</span></span>



| <span data-ttu-id="1029c-119">Flag</span><span class="sxs-lookup"><span data-stu-id="1029c-119">Flag</span></span>                        | <span data-ttu-id="1029c-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1029c-120">Description</span></span>                                   |
|-----------------------------|-----------------------------------------------|
| <span data-ttu-id="1029c-121">WMDRM- \_ Geräte- \_ needclock</span><span class="sxs-lookup"><span data-stu-id="1029c-121">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="1029c-122">Erwerben Sie eine Uhr von einem sicheren Uhr-Server.</span><span class="sxs-lookup"><span data-stu-id="1029c-122">Acquire a clock from a secure clock server.</span></span>   |
| <span data-ttu-id="1029c-123">WMDRM- \_ Geräte \_ Erfrischung</span><span class="sxs-lookup"><span data-stu-id="1029c-123">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="1029c-124">Aktualisieren Sie die Uhr von einem sicheren Uhr-Server.</span><span class="sxs-lookup"><span data-stu-id="1029c-124">Refresh the clock from a secure clock server.</span></span> |



 

</dd> <dt>

<span data-ttu-id="1029c-125">*pdwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1029c-125">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1029c-126">Einer der folgenden **DWORD** -Werte, der den vom Gerät zurückgegebenen Status angibt.</span><span class="sxs-lookup"><span data-stu-id="1029c-126">One of the following **DWORD** values specifying the status returned by the device.</span></span>



| <span data-ttu-id="1029c-127">Status</span><span class="sxs-lookup"><span data-stu-id="1029c-127">Status</span></span> | <span data-ttu-id="1029c-128">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1029c-128">Description</span></span>                                                     |
|--------|-----------------------------------------------------------------|
| <span data-ttu-id="1029c-129">0</span><span class="sxs-lookup"><span data-stu-id="1029c-129">0</span></span>      | <span data-ttu-id="1029c-130">Die Aktion wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1029c-130">The action is not supported.</span></span>                                    |
| <span data-ttu-id="1029c-131">1</span><span class="sxs-lookup"><span data-stu-id="1029c-131">1</span></span>      | <span data-ttu-id="1029c-132">Die sichere Uhr des Geräts konnte nicht vom Dienst abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1029c-132">The device secure clock could not be acquired from the service.</span></span> |
| <span data-ttu-id="1029c-133">2</span><span class="sxs-lookup"><span data-stu-id="1029c-133">2</span></span>      | <span data-ttu-id="1029c-134">Die sichere Uhr des Geräts konnte nicht festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1029c-134">The device's secure clock could not be set.</span></span>                     |
| <span data-ttu-id="1029c-135">3</span><span class="sxs-lookup"><span data-stu-id="1029c-135">3</span></span>      | <span data-ttu-id="1029c-136">Die sichere Uhr des Geräts wurde festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1029c-136">The device's secure clock was set.</span></span>                              |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1029c-137">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1029c-137">Return value</span></span>

<span data-ttu-id="1029c-138">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1029c-138">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1029c-139">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1029c-139">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1029c-140">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1029c-140">Return code</span></span>                                                                                                                             | <span data-ttu-id="1029c-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1029c-141">Description</span></span>                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1029c-142"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-142"><dt>**S\_OK**</dt></span></span> </dl>                                                    | <span data-ttu-id="1029c-143">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1029c-143">The method succeeded.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="1029c-144"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-144"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                                       | <span data-ttu-id="1029c-145">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1029c-145">One or more arguments are not valid.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="1029c-146"><dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-146"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>                        | <span data-ttu-id="1029c-147">Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.</span><span class="sxs-lookup"><span data-stu-id="1029c-147">The specified device is not a Windows Media DRM compatible device.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="1029c-148"><dt>**NS \_ E \_ DRM \_ kann \_ keine \_ \_ sichere \_ Uhr erhalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-148"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="1029c-149">Fehler beim Abrufen der sicherheitstokenaufforderung vom Gerät, oder die URL der sicheren Uhr konnte nicht abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1029c-149">Failed to retrieve secure clock challenge from the device or unable to retrieve the secure clock URL from the challenge.</span></span><br/> |
| <dl> <span data-ttu-id="1029c-150"><dt>**NS \_ E \_ DRM \_ kann \_ keine \_ \_ sichere \_ Uhr \_ vom \_ Server erhalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-150"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_SECURE\_CLOCK\_FROM\_SERVER**</dt></span></span> </dl> | <span data-ttu-id="1029c-151">Fehler beim Abrufen der Antwort auf sichere Uhr vom Sicherheitstokenserver.</span><span class="sxs-lookup"><span data-stu-id="1029c-151">Failed to retrieve the secure clock response from the secure clock server.</span></span><br/>                                               |
| <dl> <span data-ttu-id="1029c-152"><dt>**NS \_ E \_ DRM \_ kann \_ \_ \_ sichere Uhr nicht \_ festlegen**</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-152"><dt>**NS\_E\_DRM\_UNABLE\_TO\_SET\_SECURE\_CLOCK**</dt></span></span> </dl>               | <span data-ttu-id="1029c-153">Fehler beim Senden der Anforderung für die sichere Uhr an das Gerät, oder das Gerät konnte die Uhr nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="1029c-153">Failed to send the secure clock challenge to the device, or the device failed to set the clock.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="1029c-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1029c-154">Remarks</span></span>

<span data-ttu-id="1029c-155">Dabei handelt es sich um eine asynchrone Methode. das Gerät muss den [**iwmdmprogress:: End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) -Rückruf für diesen Vorgang abwarten, bevor er versucht, lizenzierte Inhalte wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="1029c-155">This is an asynchronous method; the device must await the [**IWMDMProgress::End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmprogress-end) callback for this operation before attempting to play any licensed content.</span></span>

<span data-ttu-id="1029c-156">Eine Anwendung kann lernen, ob das Gerät durch Aufrufen von [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md)die Uhr zurücksetzen oder aktualisieren muss.</span><span class="sxs-lookup"><span data-stu-id="1029c-156">An application can learn if the device must have its clock reset or updated by calling [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md).</span></span>

<span data-ttu-id="1029c-157">Die Anwendung muss über eine Internet Verbindung verfügen, damit Sie eine sichere Uhr abrufen oder zurücksetzen kann.</span><span class="sxs-lookup"><span data-stu-id="1029c-157">Your application must have an Internet connection to enable it to acquire or reset a secure clock.</span></span>

## <a name="requirements"></a><span data-ttu-id="1029c-158">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1029c-158">Requirements</span></span>



| <span data-ttu-id="1029c-159">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1029c-159">Requirement</span></span> | <span data-ttu-id="1029c-160">Wert</span><span class="sxs-lookup"><span data-stu-id="1029c-160">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1029c-161">Header</span><span class="sxs-lookup"><span data-stu-id="1029c-161">Header</span></span><br/>  | <dl> <span data-ttu-id="1029c-162"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-162"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="1029c-163">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1029c-163">Library</span></span><br/> | <dl> <span data-ttu-id="1029c-164"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1029c-164"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1029c-165">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1029c-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1029c-166">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1029c-166">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1029c-167">**Iwmdmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1029c-167">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="1029c-168">**IWMDMProgress3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1029c-168">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="1029c-169">**Iwmdrmdeviceapp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1029c-169">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





