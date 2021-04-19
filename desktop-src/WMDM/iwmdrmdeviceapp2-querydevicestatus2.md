---
title: IWMDRMDeviceApp2 QueryDeviceStatus2-Methode (wmdrmdeviceapp. h)
description: Die QueryDeviceStatus2-Methode fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.
ms.assetid: f7e95fb7-5929-4a70-8580-a443e152e6d1
keywords:
- QueryDeviceStatus2-Methode Windows Media Device Manager
- QueryDeviceStatus2-Methode, Windows Media Device Manager, IWMDRMDeviceApp2-Schnittstelle
- IWMDRMDeviceApp2-Schnittstelle Windows Media Device Manager, QueryDeviceStatus2-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp2.QueryDeviceStatus2
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 338d1f03f8d1e63086bb260c9854c7dcf3e88514
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366737"
---
# <a name="iwmdrmdeviceapp2querydevicestatus2-method"></a><span data-ttu-id="408f7-106">IWMDRMDeviceApp2:: QueryDeviceStatus2-Methode</span><span class="sxs-lookup"><span data-stu-id="408f7-106">IWMDRMDeviceApp2::QueryDeviceStatus2 method</span></span>

<span data-ttu-id="408f7-107">Die **QueryDeviceStatus2** -Methode fragt ein Gerät nach einem bestimmten DRM-Status oder einer bestimmten Funktion ab.</span><span class="sxs-lookup"><span data-stu-id="408f7-107">The **QueryDeviceStatus2** method queries a device for a specific DRM status or capability.</span></span>

## <a name="syntax"></a><span data-ttu-id="408f7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="408f7-108">Syntax</span></span>


```C++
HRESULT QueryDeviceStatus2(
  [in]  IWMDMDevice *pDevice,
  [in]  DWORD       dwFlags,
  [out] DWORD       *pdwStatus
);
```



## <a name="parameters"></a><span data-ttu-id="408f7-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="408f7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="408f7-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408f7-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408f7-111">Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="408f7-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="408f7-112">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="408f7-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="408f7-113">Einer oder mehrere der folgenden **DWORD** -Werte, die angeben, welche Funktionen angefordert werden sollen, kombiniert mit einem bitweisen **or**.</span><span class="sxs-lookup"><span data-stu-id="408f7-113">One or more of the following **DWORD** values specifying which capabilities to request, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="408f7-114">Flag</span><span class="sxs-lookup"><span data-stu-id="408f7-114">Flag</span></span>                              | <span data-ttu-id="408f7-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="408f7-115">Description</span></span>                                                                  |
|-----------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="408f7-116">WMDRM- \_ Abfrage \_ Client \_ indivstatus</span><span class="sxs-lookup"><span data-stu-id="408f7-116">WMDRM\_QUERY\_CLIENT\_INDIVSTATUS</span></span> | <span data-ttu-id="408f7-117">Fragen Sie ab, ob die DRM-Komponenten des Computers individualisiert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="408f7-117">Query whether the computer's DRM components need to be individualized.</span></span>       |
| <span data-ttu-id="408f7-118">WMDRM- \_ Abfrage \_ Gerät \_ Clockstatus</span><span class="sxs-lookup"><span data-stu-id="408f7-118">WMDRM\_QUERY\_DEVICE\_CLOCKSTATUS</span></span> | <span data-ttu-id="408f7-119">Fragen Sie ab, ob die sichere Uhr des Geräts hinzugefügt oder aktualisiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="408f7-119">Query whether the device's secure clock needs to be added or updated.</span></span>        |
| <span data-ttu-id="408f7-120">WMDRM- \_ Abfrage \_ Gerät wurde \_ gesperrt.</span><span class="sxs-lookup"><span data-stu-id="408f7-120">WMDRM\_QUERY\_DEVICE\_ISREVOKED</span></span>   | <span data-ttu-id="408f7-121">Fragen Sie ab, ob das Gerät widerrufen wurde.</span><span class="sxs-lookup"><span data-stu-id="408f7-121">Query whether the device is revoked.</span></span>                                         |
| <span data-ttu-id="408f7-122">WMDRM- \_ Abfrage \_ Gerät \_ iswmdrm</span><span class="sxs-lookup"><span data-stu-id="408f7-122">WMDRM\_QUERY\_DEVICE\_ISWMDRM</span></span>     | <span data-ttu-id="408f7-123">Fragen Sie ab, ob das Gerät Windows Media DRM 10 für tragbare Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="408f7-123">Query whether the device supports Windows Media DRM 10 for Portable Devices.</span></span> |



 

</dd> <dt>

<span data-ttu-id="408f7-124">*pdwstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="408f7-124">*pdwStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="408f7-125">NULL oder mehr der folgenden **DWORD** -Werte, die den angeforderten Gerätestatus in Kombination mit einem bitweisen **or** angeben.</span><span class="sxs-lookup"><span data-stu-id="408f7-125">Zero or more of the following **DWORD** values specifying the requested device status, combined with a bitwise **OR**.</span></span>



| <span data-ttu-id="408f7-126">Status</span><span class="sxs-lookup"><span data-stu-id="408f7-126">Status</span></span>                      | <span data-ttu-id="408f7-127">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="408f7-127">Description</span></span>                                              |
|-----------------------------|----------------------------------------------------------|
| <span data-ttu-id="408f7-128">WMDRM- \_ Gerät \_ iswmdrm</span><span class="sxs-lookup"><span data-stu-id="408f7-128">WMDRM\_DEVICE\_ISWMDRM</span></span>      | <span data-ttu-id="408f7-129">Das Gerät unterstützt Windows Media DRM.</span><span class="sxs-lookup"><span data-stu-id="408f7-129">The device supports Windows Media DRM.</span></span>                   |
| <span data-ttu-id="408f7-130">WMDRM- \_ Geräte- \_ needclock</span><span class="sxs-lookup"><span data-stu-id="408f7-130">WMDRM\_DEVICE\_NEEDCLOCK</span></span>    | <span data-ttu-id="408f7-131">Das Gerät hat keine sichere Uhr.</span><span class="sxs-lookup"><span data-stu-id="408f7-131">The device does not have a secure clock.</span></span>                 |
| <span data-ttu-id="408f7-132">WMDRM- \_ Gerät gesperrt \_</span><span class="sxs-lookup"><span data-stu-id="408f7-132">WMDRM\_DEVICE\_REVOKED</span></span>      | <span data-ttu-id="408f7-133">Das Gerät wurde widerrufen.</span><span class="sxs-lookup"><span data-stu-id="408f7-133">The device has been revoked.</span></span>                             |
| <span data-ttu-id="408f7-134">WMDRM- \_ Client- \_ needindiv</span><span class="sxs-lookup"><span data-stu-id="408f7-134">WMDRM\_CLIENT\_NEEDINDIV</span></span>    | <span data-ttu-id="408f7-135">Die DRM-Komponenten des Computers müssen individualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="408f7-135">The computer's DRM components need to be individualized.</span></span> |
| <span data-ttu-id="408f7-136">WMDRM- \_ Geräte \_ Erfrischung</span><span class="sxs-lookup"><span data-stu-id="408f7-136">WMDRM\_DEVICE\_REFRESHCLOCK</span></span> | <span data-ttu-id="408f7-137">Die Uhr muss aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="408f7-137">The clock needs to be refreshed.</span></span>                         |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="408f7-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="408f7-138">Return value</span></span>

<span data-ttu-id="408f7-139">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="408f7-139">The method returns an **HRESULT**.</span></span> <span data-ttu-id="408f7-140">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="408f7-140">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="408f7-141">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="408f7-141">Return code</span></span>                                                                                                              | <span data-ttu-id="408f7-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="408f7-142">Description</span></span>                                                               |
|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="408f7-143"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-143"><dt>**S\_OK**</dt></span></span> </dl>                                     | <span data-ttu-id="408f7-144">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="408f7-144">The method succeeded.</span></span><br/>                                          |
| <dl> <span data-ttu-id="408f7-145"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-145"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                        | <span data-ttu-id="408f7-146">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="408f7-146">One or more arguments are not valid.</span></span><br/>                           |
| <dl> <span data-ttu-id="408f7-147"><dt>**\_Ungültiges NS E- \_ DRM- \_ \_ Zertifikat**</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-147"><dt>**NS\_E\_DRM\_INVALID\_CERTIFICATE**</dt></span></span> </dl>          | <span data-ttu-id="408f7-148">Das vom Gerät abgerufene Gerätezertifikat ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="408f7-148">The device certificate retrieved from the device is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="408f7-149"><dt>**NS \_ E \_ DRM \_ kann \_ das \_ \_ Geräte \_ Zertifikat nicht erhalten.**</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-149"><dt>**NS\_E\_DRM\_UNABLE\_TO\_GET\_DEVICE\_CERT**</dt></span></span> </dl> | <span data-ttu-id="408f7-150">Fehler beim Abrufen des Geräte Zertifikats vom Gerät.</span><span class="sxs-lookup"><span data-stu-id="408f7-150">Failed to retrieve the device certificate from the device.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="408f7-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="408f7-151">Remarks</span></span>

<span data-ttu-id="408f7-152">Diese Methode sollte aufgerufen werden, bevor Eingeschränkte Aktionen für DRM-Inhalte durchgeführt werden, z. b. das Übertragen von DRM-Inhalten auf das Gerät oder das Abrufen von Messungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="408f7-152">This method should be called before performing any restricted actions on DRM content, such as transferring DRM content to the device, or acquiring metering information.</span></span> <span data-ttu-id="408f7-153">Wenn die von *pdwstatus* abgerufenen Werte angeben, dass eine Aktion ausgeführt werden muss (z. b. für den Desktop oder das Abrufen einer Uhr für das Gerät), sollte die [**Anwendung iwmdrmdeviceapp:: acquiredevicedata**](iwmdrmdeviceapp-acquiredevicedata.md) aufrufen und den abgerufenen *pdwstatus* -Wert aus dieser Funktion an den *dwFlags* -Parameter in **acquiredevicedata** übergeben.</span><span class="sxs-lookup"><span data-stu-id="408f7-153">If the values retrieved by *pdwStatus* indicate that some action needs to be performed (such as individualization for the desktop or acquiring a clock for the device), the application should call [**IWMDRMDeviceApp::AcquireDeviceData**](iwmdrmdeviceapp-acquiredevicedata.md) and pass in the retrieved *pdwStatus* value from this function to the *dwFlags* parameter in **AcquireDeviceData**.</span></span> <span data-ttu-id="408f7-154">Wenn 0 (null) zurückgegeben wird, unterstützt das Gerät Windows Media DRM 10 für tragbare Geräte nicht, und es müssen keine Aktionen durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="408f7-154">If zero is returned, the device does not support Windows Media DRM 10 for Portable Devices, and no actions need be taken.</span></span> <span data-ttu-id="408f7-155">Weitere Informationen finden Sie [unter behandeln geschützter Inhalte in der Anwendung](handling-protected-content-in-the-application.md) .</span><span class="sxs-lookup"><span data-stu-id="408f7-155">See [Handling Protected Content in the Application](handling-protected-content-in-the-application.md) for more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="408f7-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="408f7-156">Requirements</span></span>



| <span data-ttu-id="408f7-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="408f7-157">Requirement</span></span> | <span data-ttu-id="408f7-158">Wert</span><span class="sxs-lookup"><span data-stu-id="408f7-158">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="408f7-159">Header</span><span class="sxs-lookup"><span data-stu-id="408f7-159">Header</span></span><br/>  | <dl> <span data-ttu-id="408f7-160"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-160"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="408f7-161">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="408f7-161">Library</span></span><br/> | <dl> <span data-ttu-id="408f7-162"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="408f7-162"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="408f7-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="408f7-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="408f7-164">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="408f7-164">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="408f7-165">**Iwmdrmdeviceapp:: querydevicestatus**</span><span class="sxs-lookup"><span data-stu-id="408f7-165">**IWMDRMDeviceApp::QueryDeviceStatus**</span></span>](iwmdrmdeviceapp-querydevicestatus.md)
</dt> <dt>

[<span data-ttu-id="408f7-166">**IWMDRMDeviceApp2-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="408f7-166">**IWMDRMDeviceApp2 Interface**</span></span>](iwmdrmdeviceapp2.md)
</dt> </dl>

 

 





