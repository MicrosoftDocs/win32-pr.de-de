---
title: Iwmdrmdeviceapp generatemeterchallenge-Methode (wmdrmdeviceapp. h)
description: Mit der generatemeterchallenge-Methode werden Messungs Daten von einem Gerät angefordert.
ms.assetid: 2457cab7-bd45-49a7-ba69-74ae022207ce
keywords:
- Generatemeterchallenge-Methode, Windows Media Device Manager
- Generatemeterchallenge-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, generatemeterchallenge-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.GenerateMeterChallenge
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06a71f04a5837f09575a2f4bccf4b17e34e30d63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354161"
---
# <a name="iwmdrmdeviceappgeneratemeterchallenge-method"></a><span data-ttu-id="dae0c-106">Iwmdrmdeviceapp:: generatemeterchallenge-Methode</span><span class="sxs-lookup"><span data-stu-id="dae0c-106">IWMDRMDeviceApp::GenerateMeterChallenge method</span></span>

<span data-ttu-id="dae0c-107">Mit der **generatemeterchallenge** -Methode werden Messungs Daten von einem Gerät angefordert.</span><span class="sxs-lookup"><span data-stu-id="dae0c-107">The **GenerateMeterChallenge** method acquires metering data from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="dae0c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="dae0c-108">Syntax</span></span>


```C++
HRESULT GenerateMeterChallenge(
  [in]  IWMDMDevice *pDevice,
  [in]  BSTR        bstrMeterCert,
  [out] BSTR        *pbstrMeterURL,
  [out] BSTR        *pbstrMeterData
);
```



## <a name="parameters"></a><span data-ttu-id="dae0c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="dae0c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dae0c-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dae0c-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0c-111">Zeiger auf eine [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dae0c-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) interface.</span></span> <span data-ttu-id="dae0c-112">Wenn die Anwendung in **null** übergeht, werden Messungs Informationen, die auf dem Computer gespeichert sind, anstelle von Messungs Informationen eines verbundenen Geräts verwendet.</span><span class="sxs-lookup"><span data-stu-id="dae0c-112">If the application passes in **NULL**, metering information stored on the computer is used instead of metering information from a connected device.</span></span>

</dd> <dt>

<span data-ttu-id="dae0c-113">*bstrinmetercert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="dae0c-113">*bstrMeterCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0c-114">Das Messungs Zertifikat der Anwendung als **BSTR**.</span><span class="sxs-lookup"><span data-stu-id="dae0c-114">The application's metering certificate, as a **BSTR**.</span></span> <span data-ttu-id="dae0c-115">Dies ist ein von Microsoft empfangenes signiertes Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="dae0c-115">This is a signed certificate received from Microsoft.</span></span>

</dd> <dt>

<span data-ttu-id="dae0c-116">*pbstrinmeterurl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dae0c-116">*pbstrMeterURL* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0c-117">Die URL, an die Messungs Daten gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dae0c-117">The URL where metering data should be sent.</span></span> <span data-ttu-id="dae0c-118">Diese wird von Windows Media Device Manager zugeordnet und muss vom Aufrufer mit **SysFreeString** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dae0c-118">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> <dt>

<span data-ttu-id="dae0c-119">*pbstrinmeterdaten* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="dae0c-119">*pbstrMeterData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dae0c-120">Messungs Daten, die an den Messungs Dienst gesendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dae0c-120">Metering data to send to the metering service.</span></span> <span data-ttu-id="dae0c-121">Diese wird von Windows Media Device Manager zugeordnet und muss vom Aufrufer mit **SysFreeString** freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dae0c-121">This is allocated by Windows Media Device Manager, and must be free by the caller using **SysFreeString**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dae0c-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dae0c-122">Return value</span></span>

<span data-ttu-id="dae0c-123">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="dae0c-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dae0c-124">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="dae0c-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dae0c-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="dae0c-125">Return code</span></span>                                                                                                      | <span data-ttu-id="dae0c-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dae0c-126">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dae0c-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-127"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="dae0c-128">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dae0c-128">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="dae0c-129"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-129"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="dae0c-130">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="dae0c-130">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="dae0c-131"><dt>**DRM \_ E \_ invalidxmltag**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-131"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>             | <span data-ttu-id="dae0c-132">XML ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="dae0c-132">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="dae0c-133"><dt>**DRM \_ E \_ noxmlclosetag**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-133"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>             | <span data-ttu-id="dae0c-134">XML ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="dae0c-134">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="dae0c-135"><dt>**DRM \_ E \_ noxmlopentag**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-135"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>              | <span data-ttu-id="dae0c-136">XML ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="dae0c-136">XML is improperly formed.</span></span><br/>                                          |
| <dl> <span data-ttu-id="dae0c-137"><dt>**DRM \_ E \_ xmlnotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-137"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>               | <span data-ttu-id="dae0c-138">Fehler beim Suchen eines erforderlichen XML-Tags.</span><span class="sxs-lookup"><span data-stu-id="dae0c-138">Failed to find a required XML tag.</span></span><br/>                                 |
| <dl> <span data-ttu-id="dae0c-139"><dt>**Fehler des Geräts**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-139"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="dae0c-140">Eine beliebige Anzahl von Gerätefehlern.</span><span class="sxs-lookup"><span data-stu-id="dae0c-140">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="dae0c-141"><dt>**Fehler vom DRM-Client**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-141"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="dae0c-142">Eine beliebige Anzahl interner DRM-Client Fehler.</span><span class="sxs-lookup"><span data-stu-id="dae0c-142">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="dae0c-143"><dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-143"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="dae0c-144">Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.</span><span class="sxs-lookup"><span data-stu-id="dae0c-144">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="dae0c-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dae0c-145">Remarks</span></span>

<span data-ttu-id="dae0c-146">Vor dem Aufrufen dieser Methode sollte die Anwendung [**iwmdrmdeviceapp:: querydevicestatus**](iwmdrmdeviceapp-querydevicestatus.md) oder [**IWMDRMDeviceApp2:: QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) aufrufen, um zu überprüfen, ob alle DRM-Komponenten des Geräts auf dem neuesten Stand sind.</span><span class="sxs-lookup"><span data-stu-id="dae0c-146">Before calling this method, the application should call [**IWMDRMDeviceApp::QueryDeviceStatus**](iwmdrmdeviceapp-querydevicestatus.md) or [**IWMDRMDeviceApp2::QueryDeviceStatus2**](iwmdrmdeviceapp2-querydevicestatus2.md) to verify that all the device's DRM components are up to date.</span></span> <span data-ttu-id="dae0c-147">Diese Methode kann nur auf einem Gerät aufgerufen werden, das Windows Media DRM 10 für tragbare Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dae0c-147">This method can only be called on a device that supports Windows Media DRM 10 for Portable Devices.</span></span>

<span data-ttu-id="dae0c-148">Die abgerufenen Daten *pbstrinmeterdata* sollten an die durch *pbstraumeterurl* angegebene URL gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="dae0c-148">The retrieved data *pbstrMeterData* should be sent to the URL specified by *pbstrMeterURL*.</span></span> <span data-ttu-id="dae0c-149">Stellen Sie sicher, dass die abgerufenen Daten URL-codiert werden, damit Sie während der Übertragung nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="dae0c-149">Be sure to URL-encode the retrieved data so that it does not get modified during transfer.</span></span>

<span data-ttu-id="dae0c-150">Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="dae0c-150">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="dae0c-151">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dae0c-151">Examples</span></span>

<span data-ttu-id="dae0c-152">Im folgenden C++-Codebeispiel wird ein **wmdrmdeviceapp** -Objekt erstellt, und es wird überprüft, ob das Gerät ein Windows Media DRM 10-Gerät ist, dass seine Uhr genau ist, und dann die Messungs Daten anfordert.</span><span class="sxs-lookup"><span data-stu-id="dae0c-152">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


```C++
HRESULT hr = S_OK;
// Create the WMDRMDeviceApp object.
CComPtr<IWMDRMDeviceApp> pDRM;
hr = pDRM.CoCreateInstance(CLSID_WMDRMDeviceApp, 0, CLSCTX_ALL);

// Find out first if the device is a WMDRM 10 device, and if it requires
// any clock updates.
DWORD status = 0;
hr = pDRM->QueryDeviceStatus(pDevice, &status);

if (!(WMDRM_DEVICE_ISWMDRM & status)) // Device is not WMDRM 10. Nothing can be updated,
    return E_FAIL;                   // and metering cannot be performed.
else if (status & WMDRM_DEVICE_REVOKED) // Device is revoked.
    return E_FAIL;
else if (status & WMDRM_DEVICE_NEEDCLOCK || 
    status & WMDRM_CLIENT_NEEDINDIV ||
    status & WMDRM_DEVICE_REFRESHCLOCK)
{
    // Need to update device clock. 
    // Using custom function, which is synchronous.
    hr = myAcquireDeviceData(pDRM, pDevice, this, status, &result);
    if (hr != S_OK || result != 0)    // Couldn't perform the updates.
        return E_FAIL;    
}

// Any updates have been performed. Now get the metering information from the device.
CComBSTR meterCert(METERCERT);
CComBSTR URL;
CComBSTR rawdata;
CComBSTR data;
hr = pDRM->GenerateMeterChallenge(pDevice, meterCert, &URL, &rawdata);
if (hr == S_OK)
    ..... Send to URL...
```



## <a name="requirements"></a><span data-ttu-id="dae0c-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dae0c-153">Requirements</span></span>



| <span data-ttu-id="dae0c-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dae0c-154">Requirement</span></span> | <span data-ttu-id="dae0c-155">Wert</span><span class="sxs-lookup"><span data-stu-id="dae0c-155">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dae0c-156">Header</span><span class="sxs-lookup"><span data-stu-id="dae0c-156">Header</span></span><br/>  | <dl> <span data-ttu-id="dae0c-157"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-157"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="dae0c-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="dae0c-158">Library</span></span><br/> | <dl> <span data-ttu-id="dae0c-159"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="dae0c-159"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="dae0c-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dae0c-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dae0c-161">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="dae0c-161">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="dae0c-162">**Iwmdmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dae0c-162">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="dae0c-163">**Iwmdrmdeviceapp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="dae0c-163">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





