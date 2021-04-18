---
title: Iwmdrmdeviceapp-synchronizelicenses-Methode (wmdrmdeviceapp. h)
description: Die synchronizelicenses-Methode aktualisiert Lizenzen auf einem Gerät, wenn Sie fast abgelaufen sind.
ms.assetid: 352378c1-7432-476c-98e9-d811165c020e
keywords:
- Synchronizelicenses-Methode Windows Media Device Manager
- Synchronizelicenses-Methode, Windows Media Device Manager, iwmdrmdeviceapp-Schnittstelle
- Iwmdrmdeviceapp-Schnittstelle Windows Media Device Manager, synchronizelicenses-Methode
topic_type:
- apiref
api_name:
- IWMDRMDeviceApp.SynchronizeLicenses
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b08f3457fec55a0eb519419feddf4594a2cbfac0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372112"
---
# <a name="iwmdrmdeviceappsynchronizelicenses-method"></a><span data-ttu-id="30d90-106">Iwmdrmdeviceapp:: synchronizelicenses-Methode</span><span class="sxs-lookup"><span data-stu-id="30d90-106">IWMDRMDeviceApp::SynchronizeLicenses method</span></span>

<span data-ttu-id="30d90-107">Die **synchronizelicenses** -Methode aktualisiert Lizenzen auf einem Gerät, wenn Sie fast abgelaufen sind.</span><span class="sxs-lookup"><span data-stu-id="30d90-107">The **SynchronizeLicenses** method updates licenses on a device when they are close to expiring.</span></span>

## <a name="syntax"></a><span data-ttu-id="30d90-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30d90-108">Syntax</span></span>


```C++
HRESULT SynchronizeLicenses(
  [in] IWMDMDevice    *pDevice,
  [in] IWMDMProgress3 *pProgressCallback,
  [in] DWORD          cMinCountThreshold,
  [in] DWORD          cMinHoursThreshold
);
```



## <a name="parameters"></a><span data-ttu-id="30d90-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30d90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30d90-110">*pdevice* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d90-110">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d90-111">Zeiger auf ein [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="30d90-111">Pointer to an [**IWMDMDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) object.</span></span>

</dd> <dt>

<span data-ttu-id="30d90-112">*pprogresscallback* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d90-112">*pProgressCallback* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d90-113">Status Rückruf, der den Fortschritt von eventuell auszuführenden Schritten empfängt. Der Schritt wird durch den *EventID-* Parameter der [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) -Methode identifiziert, die aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="30d90-113">Progress callback that will receive progress of any steps that it might need to carry out. The step is identified by the *EventId* parameter of the [**IWMDMProgress3**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3) method called.</span></span>

</dd> <dt>

<span data-ttu-id="30d90-114">*cminzählthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d90-114">*cMinCountThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d90-115">Optionale minimale Anzahl von verbleibenden spielen für eine Geräte Lizenz.</span><span class="sxs-lookup"><span data-stu-id="30d90-115">Optional minimum remaining play count on a device license.</span></span>

</dd> <dt>

<span data-ttu-id="30d90-116">*cminhoursthreshold* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30d90-116">*cMinHoursThreshold* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30d90-117">Die optionalen minimalen verbleibenden Stunden für eine Geräte Lizenz.</span><span class="sxs-lookup"><span data-stu-id="30d90-117">Optional minimum remaining hours on a device license.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30d90-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30d90-118">Return value</span></span>

<span data-ttu-id="30d90-119">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="30d90-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="30d90-120">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="30d90-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="30d90-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="30d90-121">Return code</span></span>                                                                                                         | <span data-ttu-id="30d90-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30d90-122">Description</span></span>                                                                                                                                                 |
|---------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="30d90-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-123"><dt>**S\_OK**</dt></span></span> </dl>                                | <span data-ttu-id="30d90-124">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="30d90-124">The method succeeded.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="30d90-125"><dt>**DRM \_ E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-125"><dt>**DRM\_E\_INVALIDARG**</dt></span></span> </dl>                   | <span data-ttu-id="30d90-126">Mindestens ein Argument ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="30d90-126">One or more arguments are not valid.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="30d90-127"><dt>**DRM \_ E \_ invalidxmltag**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-127"><dt>**DRM\_E\_INVALIDXMLTAG**</dt></span></span> </dl>                | <span data-ttu-id="30d90-128">XML ist nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="30d90-128">XML is improperly formed.</span></span><br/>                                                                                                                        |
| <dl> <span data-ttu-id="30d90-129"><dt>**DRM \_ E \_ notimpl**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-129"><dt>**DRM\_E\_NOTIMPL**</dt></span></span> </dl>                      | <span data-ttu-id="30d90-130">Diese Funktion ist zurzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="30d90-130">This functionality is not currently implemented.</span></span> <span data-ttu-id="30d90-131">(Synclicenses w/ *pdevice* = null)</span><span class="sxs-lookup"><span data-stu-id="30d90-131">(SyncLicenses w/ *pDevice* =NULL)</span></span><br/>                                                               |
| <dl> <span data-ttu-id="30d90-132"><dt>**DRM \_ E \_ noxmlclosetag**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-132"><dt>**DRM\_E\_NOXMLCLOSETAG**</dt></span></span> </dl>                | <span data-ttu-id="30d90-133">Die Lizenz-XML-Datei wurde nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="30d90-133">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="30d90-134"><dt>**DRM \_ E \_ noxmlopentag**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-134"><dt>**DRM\_E\_NOXMLOPENTAG**</dt></span></span> </dl>                 | <span data-ttu-id="30d90-135">Die Lizenz-XML-Datei wurde nicht ordnungsgemäß formatiert.</span><span class="sxs-lookup"><span data-stu-id="30d90-135">The license XML was improperly formed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="30d90-136"><dt>**DRM- \_ E- \_ outo-Speicher**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-136"><dt>**DRM\_E\_OUTOFMEMORY**</dt></span></span> </dl>                  | <span data-ttu-id="30d90-137">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="30d90-137">Out of memory.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="30d90-138"><dt>**DRM \_ E \_ xmlnotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-138"><dt>**DRM\_E\_XMLNOTFOUND**</dt></span></span> </dl>                  | <span data-ttu-id="30d90-139">Fehler beim Suchen eines erforderlichen XML-Tags in der Lizenz.</span><span class="sxs-lookup"><span data-stu-id="30d90-139">Failed to find a required XML tag in the license.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="30d90-140"><dt>**NS \_ E \_ Gerät \_ nicht \_ WMDRM- \_ Gerät**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-140"><dt>**NS\_E\_DEVICE\_NOT\_WMDRM\_DEVICE**</dt></span></span> </dl>    | <span data-ttu-id="30d90-141">Das angegebene Gerät ist kein Windows Media DRM-kompatibles Gerät.</span><span class="sxs-lookup"><span data-stu-id="30d90-141">The specified device is not a Windows Media DRM-compatible device.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="30d90-142"><dt>**NS \_ E \_ DRM \_ benötigt \_ Individualisierung**</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-142"><dt>**NS\_E\_DRM\_NEEDS\_INDIVIDUALIZATION**</dt></span></span> </dl> | <span data-ttu-id="30d90-143">Das DRM erfordert ein individualisiertes schwarzes Kästchen, um diese Funktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="30d90-143">The DRM requires an individualized black box to perform this function.</span></span> <span data-ttu-id="30d90-144">Anders ausgedrückt: für das Windows Media-Format-SDK ist ein Sicherheits Upgrade erforderlich.</span><span class="sxs-lookup"><span data-stu-id="30d90-144">In other words, the Windows Media Format SDK requires a security upgrade.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="30d90-145">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="30d90-145">Remarks</span></span>

<span data-ttu-id="30d90-146">Dieser Rückruf kann nur auf einem Gerät erfolgen, das Windows Media DRM 10 für tragbare Geräte unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30d90-146">This call can only be made on a device that supports Windows Media DRM 10 for Portable Devices.</span></span> <span data-ttu-id="30d90-147">Sie müssen mindestens einen Schwellenwert Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="30d90-147">You must specify at least one threshold parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="30d90-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30d90-148">Requirements</span></span>



| <span data-ttu-id="30d90-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30d90-149">Requirement</span></span> | <span data-ttu-id="30d90-150">Wert</span><span class="sxs-lookup"><span data-stu-id="30d90-150">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30d90-151">Header</span><span class="sxs-lookup"><span data-stu-id="30d90-151">Header</span></span><br/>  | <dl> <span data-ttu-id="30d90-152"><dt>Wmdrmdeviceapp. h (erfordert auch wmdrmdeviceapp \_ i. c, erstellt von wmdrmdeviceapp. idl)</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-152"><dt>WMDRMDeviceApp.h (also requires Wmdrmdeviceapp\_i.c, built from WMDRMDeviceApp.idl)</dt></span></span> </dl> |
| <span data-ttu-id="30d90-153">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="30d90-153">Library</span></span><br/> | <dl> <span data-ttu-id="30d90-154"><dt>Mssachlp. lib</dt></span><span class="sxs-lookup"><span data-stu-id="30d90-154"><dt>Mssachlp.lib</dt></span></span> </dl>                                                                        |



## <a name="see-also"></a><span data-ttu-id="30d90-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30d90-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30d90-156">**Behandeln geschützter Inhalte in der Anwendung**</span><span class="sxs-lookup"><span data-stu-id="30d90-156">**Handling Protected Content in the Application**</span></span>](handling-protected-content-in-the-application.md)
</dt> <dt>

[<span data-ttu-id="30d90-157">**IWMDMProgress3-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30d90-157">**IWMDMProgress3 Interface**</span></span>](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmprogress3)
</dt> <dt>

[<span data-ttu-id="30d90-158">**Iwmdrmdeviceapp-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="30d90-158">**IWMDRMDeviceApp Interface**</span></span>](iwmdrmdeviceapp.md)
</dt> </dl>

 

 





