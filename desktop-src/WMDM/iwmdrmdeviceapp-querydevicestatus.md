---
title: Iwmdrmdeviceapp querydevicestatus-Methode (wmdrmdeviceapp. h)
description: Die querydevicestatus-Methode fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.
ms.assetid: cd5a75d5-d7f8-4077-a9fc-6e7ddd7c796b
keywords:
- Querydevicestatus-Methode, Windows Media Device Manager
- Querydevicestatus-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, querydevicestatus-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.QueryDeviceStatus
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8e0f4fad5ff9026ce70fc21712506eb4796d76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369692"
---
# <a name="iwmdrmdeviceappquerydevicestatus-method"></a><span data-ttu-id="b738e-106">Iwmdrmdeviceapp:: querydevicestatus-Methode</span><span class="sxs-lookup"><span data-stu-id="b738e-106">IWMDRMDeviceApp::QueryDeviceStatus method</span></span>

<span data-ttu-id="b738e-107">Die **querydevicestatus** -Methode fragt ein Gerät nach dem aktuellen DRM-Status und den zugehörigen Funktionen ab.</span><span class="sxs-lookup"><span data-stu-id="b738e-107">The **QueryDeviceStatus** method queries a device for its current DRM status and capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="b738e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b738e-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus(
  [in]  IWMDMDevice *pDevice,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="b738e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b738e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b738e-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b738e-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b738e-111">Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b738e-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="b738e-112">*pdwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="b738e-112">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b738e-113">NULL oder mehr der folgenden **DWORD** -Werte, die die DRM-Aspekte des Geräts beschreiben, kombiniert mit einem bitweisen **or**.</span><span class="sxs-lookup"><span data-stu-id="b738e-113">Zero or more of the following **DWORD** values describing the DRM aspects of the device, combined with a bitwise **OR**.</span></span> <span data-ttu-id="b738e-114">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="b738e-114">See Remarks.</span></span>



| <span data-ttu-id="b738e-115">Status</span><span class="sxs-lookup"><span data-stu-id="b738e-115">Status</span></span>                      | <span data-ttu-id="b738e-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b738e-116">Description</span></span>                                  |
|-----------------------------|----------------------------------------------|
| <span data-ttu-id="b738e-117">WMDRM- \_ Gerät \_ iswmdrm</span><span class="sxs-lookup"><span data-stu-id="b738e-117">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="b738e-118">Das Gerät unterstützt Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="b738e-118">The device supports Windows Media DRM.</span></span>       |
| <span data-ttu-id="b738e-119">WMDRM- \_ Geräte- \_ needclock</span><span class="sxs-lookup"><span data-stu-id="b738e-119">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="b738e-120">Das Gerät hat keine sichere Uhr.</span><span class="sxs-lookup"><span data-stu-id="b738e-120">The device does not have a secure clock.</span></span>     |
| <span data-ttu-id="b738e-121">WMDRM- \_ Gerät gesperrt \_</span><span class="sxs-lookup"><span data-stu-id="b738e-121">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="b738e-122">Das Gerät wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="b738e-122">The device has been revoked.</span></span>                 |
| <span data-ttu-id="b738e-123">WMDRM- \_ Client- \_ needindiv</span><span class="sxs-lookup"><span data-stu-id="b738e-123">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="b738e-124">Die DRM-Sicherheit muss individualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b738e-124">The DRM security needs to be individualized.</span></span> |
| <span data-ttu-id="b738e-125">WMDRM- \_ Geräte \_ Erfrischung</span><span class="sxs-lookup"><span data-stu-id="b738e-125">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="b738e-126">Die Uhr muss aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="b738e-126">The clock needs to be refreshed.</span></span>             |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b738e-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b738e-127">Return value</span></span>

<span data-ttu-id="b738e-128">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="b738e-128">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b738e-129">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b738e-129">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b738e-130">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="b738e-130">Return code</span></span>                                                                                                              | <span data-ttu-id="b738e-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b738e-131">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b738e-132"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-132"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="b738e-133">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b738e-133">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="b738e-134"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-134"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="b738e-135">Das Eingabe Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b738e-135">The input argument is not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="b738e-136"><dt>**\_Ungültiges NS E- \_ DRM- \_ \_ Zertifikat**</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-136"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="b738e-137">Das vom Gerät abgerufene Gerätezertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b738e-137">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="b738e-138"><dt>**NS \_ E \_ DRM \_ kann \_ das \_ \_ Geräte \_ Zertifikat nicht erhalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-138"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="b738e-139">Fehler beim Abrufen des Geräte Zertifikats vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="b738e-139">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="b738e-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b738e-140">Remarks</span></span>

<span data-ttu-id="b738e-141">Diese Methode sollte aufgerufen werden, bevor Eingeschränkte Aktionen für DRM-Inhalte durchgeführt werden, z. b. das Übertragen von DRM-Inhalten auf das Gerät oder das Abrufen von Messungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="b738e-141">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="b738e-142">Wenn die von *pdwstatus* abgerufenen Werte angeben, dass eine Aktion ausgeführt werden muss (z. b. die individuelle Bereitstellung des Desktops oder das Abrufen einer Uhr für das Gerät), sollte die Anwendung [**acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den abgerufenen *pdwstatus* -Wert aus dieser Funktion an den *dwFlags* -Parameter in **acquiredevicedata** übergeben.</span><span class="sxs-lookup"><span data-stu-id="b738e-142">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="b738e-143">Wenn 0 (null) zurückgegeben wird, unterstützt das Gerät Windows Media DRM 10 für tragbare Geräte nicht, und es müssen keine Aktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b738e-143">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="b738e-144">Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="b738e-144">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="examples"></a><span data-ttu-id="b738e-145">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b738e-145">Examples</span></span>

<span data-ttu-id="b738e-146">Im folgenden C++-Codebeispiel wird ein **wmdrmdeviceapp** -Objekt erstellt, und es wird überprüft, ob das Gerät ein Windows Media DRM 10-Gerät ist, dass seine Uhr genau ist, und dann die Messungs Daten anfordert.</span><span class="sxs-lookup"><span data-stu-id="b738e-146">The following C++ code example creates a **WMDRMDeviceApp** object, verifies that the device is a Windows Media DRM 10 device, that its clock is accurate, and then requests the metering data.</span></span>


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
```



## <a name="requirements"></a><span data-ttu-id="b738e-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b738e-147">Requirements</span></span>



| <span data-ttu-id="b738e-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b738e-148">Requirement</span></span> | <span data-ttu-id="b738e-149">Wert</span><span class="sxs-lookup"><span data-stu-id="b738e-149">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b738e-150">Header</span><span class="sxs-lookup"><span data-stu-id="b738e-150">Header</span></span><br/>  | <dl> <span data-ttu-id="b738e-151"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-151"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="b738e-152">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b738e-152">Library</span></span><br/> | <dl> <span data-ttu-id="b738e-153"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b738e-153"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="b738e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b738e-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b738e-155">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="b738e-155">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="b738e-156">**Iwmdrmdeviceapp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b738e-156">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> <dt>

[<span data-ttu-id="b738e-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span><span class="sxs-lookup"><span data-stu-id="b738e-157">**IWMDRMDeviceApp2::QueryDeviceStatus2**</span></span>](iwmdrmdeviceapp2-querydevicestatus2.md)
</dt> </dl>

 

 





