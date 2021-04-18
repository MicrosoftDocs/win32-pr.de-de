---
title: Iwmdrmdeviceapp processmeterresponse-Methode (wmdrmdeviceapp. h)
description: Die processmeterresponse-Methode setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.
ms.assetid: bafc4bb2-aa3c-4b2a-a818-1a78577cefc5
keywords:
- Processmeterresponse-Methode (Windows Media Device Manager)
- Processmeterresponse-Methode Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, processmeterresponse-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.ProcessMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b57312dc2f401207e41f38f5bf75cddf69a13b1e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372375"
---
# <a name="iwmdrmdeviceappprocessmeterresponse-method"></a><span data-ttu-id="1b3a4-106">Iwmdrmdeviceapp::P rocess Meter Response-Methode</span><span class="sxs-lookup"><span data-stu-id="1b3a4-106">IWMDRMDeviceApp::ProcessMeterResponse method</span></span>

<span data-ttu-id="1b3a4-107">Die **processmeterresponse** -Methode setzt einige oder alle Messungs Zähler auf einem Gerät zurück, nachdem die Daten vom Gerät an den Server gesendet und vom Server verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-107">The **ProcessMeterResponse** method resets some or all of the metering counts on a device, after data from the device has been sent to and processed by the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b3a4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b3a4-108">Syntax</span></span>


```C++
HRESULT ProcessMeterResponse(
  [in]  IWMDMDevice *pDevice,
  [in]  BYTE        *pbResponse,
  [in]  DWORD       cbResponse,
  [out] DWORD       *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="1b3a4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b3a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b3a4-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b3a4-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3a4-111">Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a4-112">*pbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b3a4-112">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3a4-113">Antwort von einem Messungs Server nach dem Senden von Daten, die mithilfe von [**generatemeterchallenge**](iwmdrmdeviceapp-generatemeterchallenge.md)generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-113">Response received from a metering server, after sending data generated using [**GenerateMeterChallenge**](iwmdrmdeviceapp-generatemeterchallenge.md).</span></span>

</dd> <dt>

<span data-ttu-id="1b3a4-114">*cbresponse* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1b3a4-114">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3a4-115">Größe von *pbresponse* in Bytes.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-115">Size of *pbResponse*, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="1b3a4-116">*pdwflags* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1b3a4-116">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b3a4-117">Ein **DWORD** aus der folgenden Tabelle, das angibt, ob auf dem zu verarbeitenden Gerät weitere Messungs Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-117">A **DWORD** from the following table indicating whether there is more metering data on the device that needs to be processed.</span></span>



| <span data-ttu-id="1b3a4-118">Flag</span><span class="sxs-lookup"><span data-stu-id="1b3a4-118">Flag</span></span>                            | <span data-ttu-id="1b3a4-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b3a4-119">Description</span></span>                                     |
|---------------------------------|-------------------------------------------------|
| <span data-ttu-id="1b3a4-120">WMDRM- \_ Zähler für \_ \_ alle Zähler</span><span class="sxs-lookup"><span data-stu-id="1b3a4-120">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="1b3a4-121">Alle Messungs Daten wurden verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-121">All metering data has been processed.</span></span>           |
| <span data-ttu-id="1b3a4-122">WMDRM- \_ Messgeräte \_ Antwort \_ partiell</span><span class="sxs-lookup"><span data-stu-id="1b3a4-122">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="1b3a4-123">Zusätzliche Messungs Daten müssen verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-123">Additional metering data needs to be processed.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b3a4-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b3a4-124">Return value</span></span>

<span data-ttu-id="1b3a4-125">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="1b3a4-126">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="1b3a4-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="1b3a4-127">Return code</span></span>                                                                                                      | <span data-ttu-id="1b3a4-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b3a4-128">Description</span></span>                                                                   |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1b3a4-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-129"><dt>**S\_OK**</dt></span></span> </dl>                             | <span data-ttu-id="1b3a4-130">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-130">The method succeeded.</span></span><br/>                                              |
| <dl> <span data-ttu-id="1b3a4-131"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-131"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                | <span data-ttu-id="1b3a4-132">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-132">One or more arguments are not valid.</span></span><br/>                               |
| <dl> <span data-ttu-id="1b3a4-133"><dt>**Fehler des Geräts**</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-133"><dt>**Errors from the device**</dt></span></span> </dl>            | <span data-ttu-id="1b3a4-134">Eine beliebige Anzahl von Gerätefehlern.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-134">Any of a number of device errors.</span></span><br/>                                  |
| <dl> <span data-ttu-id="1b3a4-135"><dt>**Fehler vom DRM-Client**</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-135"><dt>**Errors from the DRM Client**</dt></span></span> </dl>        | <span data-ttu-id="1b3a4-136">Eine beliebige Anzahl interner DRM-Client Fehler.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-136">Any of a number of internal DRM client errors.</span></span><br/>                     |
| <dl> <span data-ttu-id="1b3a4-137"><dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-137"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl> | <span data-ttu-id="1b3a4-138">Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-138">The specified device is not a Windows Media DRM compatible device.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b3a4-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b3a4-139">Remarks</span></span>

<span data-ttu-id="1b3a4-140">Weitere Informationen zur Messung, einschließlich Codebeispielen, finden Sie im Whitepaper [Messung der Verwendung digitaler Medieninhalte mit Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) auf der MSDN-Website.</span><span class="sxs-lookup"><span data-stu-id="1b3a4-140">More information on metering, including code examples, can be found in the whitepaper [Metering the Use of Digital Media Content with Windows Media DRM 10](/previous-versions//bb614723(v=vs.85)) on the MSDN Web site.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b3a4-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b3a4-141">Requirements</span></span>



| <span data-ttu-id="1b3a4-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b3a4-142">Requirement</span></span> | <span data-ttu-id="1b3a4-143">Wert</span><span class="sxs-lookup"><span data-stu-id="1b3a4-143">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b3a4-144">Header</span><span class="sxs-lookup"><span data-stu-id="1b3a4-144">Header</span></span><br/>  | <dl> <span data-ttu-id="1b3a4-145"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-145"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="1b3a4-146">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1b3a4-146">Library</span></span><br/> | <dl> <span data-ttu-id="1b3a4-147"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1b3a4-147"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="1b3a4-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b3a4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b3a4-149">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="1b3a4-149">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="1b3a4-150">**Iwmdmdevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1b3a4-150">**IWMDMDevice Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice)
</dt> <dt>

[<span data-ttu-id="1b3a4-151">**Iwmdrmdeviceapp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="1b3a4-151">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

