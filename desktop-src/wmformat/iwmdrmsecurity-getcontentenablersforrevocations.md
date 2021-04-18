---
title: Iwmdrmsecurity getcontentenablersforrevocations-Methode (wmdrmsdk. h)
description: Die getcontentenablersforrevocations-Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.
ms.assetid: 9e5b58b8-07d6-4607-a40f-cd7df4984ac5
keywords:
- Getcontentenablersforrevocations-Methode, Windows Media-Format
- Getcontentenablersforrevocations-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getcontentenablersforrevocations-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersForRevocations
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdd47ac3b44a1d74cb42113513a44c4b48689a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358376"
---
# <a name="iwmdrmsecuritygetcontentenablersforrevocations-method"></a><span data-ttu-id="49115-106">Iwmdrmsecurity:: getcontentenablersforrevocations-Methode</span><span class="sxs-lookup"><span data-stu-id="49115-106">IWMDRMSecurity::GetContentEnablersForRevocations method</span></span>

<span data-ttu-id="49115-107">Die **getcontentenablersforrevocations** -Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten basierend auf gesperrten Zertifikaten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="49115-107">The **GetContentEnablersForRevocations** method retrieves content enabler interfaces that enable renewal of components based on revoked certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="49115-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="49115-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersForRevocations(
  [in]      BYTE              **rgpbCerts,
  [in]      DWORD             *rgpdwCertSizes,
  [in]      GUID              **rgpguidCerts,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="49115-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="49115-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49115-110">*rgpbcerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49115-110">*rgpbCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-111">Ein Array von Zertifikaten, für die Inhalts Enabler abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49115-111">Array of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="49115-112">Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49115-112">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="49115-113">*rgpdwcertsizes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49115-113">*rgpdwCertSizes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-114">Ein Array, das die Größe der Zertifikate im *rgpbcerts* -Array enthält.</span><span class="sxs-lookup"><span data-stu-id="49115-114">Array containing the sizes of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="49115-115">Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49115-115">The number of elements in the array must be specified by *cCerts*.</span></span>

</dd> <dt>

<span data-ttu-id="49115-116">*rgpguidcerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49115-116">*rgpguidCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-117">Ein Array, das die Typen der Zertifikate im *rgpbcerts* -Array enthält.</span><span class="sxs-lookup"><span data-stu-id="49115-117">Array containing the types of the certificates in the *rgpbCerts* array.</span></span> <span data-ttu-id="49115-118">Die Anzahl der Elemente im Array muss durch *ccerts* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="49115-118">The number of elements in the array must be specified by *cCerts*.</span></span> <span data-ttu-id="49115-119">Verwenden Sie für jedes Element des Arrays einen der folgenden Werte.</span><span class="sxs-lookup"><span data-stu-id="49115-119">For each element of the array, use one of the following values.</span></span>



| <span data-ttu-id="49115-120">GUID-Konstante</span><span class="sxs-lookup"><span data-stu-id="49115-120">GUID constant</span></span>                 | <span data-ttu-id="49115-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="49115-121">Description</span></span>                                                    |
|-------------------------------|----------------------------------------------------------------|
| <span data-ttu-id="49115-122">WMDRM- \_ revocationtype- \_ App</span><span class="sxs-lookup"><span data-stu-id="49115-122">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="49115-123">Gibt ein Anwendungs Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="49115-123">Specifies an application certificate.</span></span>                          |
| <span data-ttu-id="49115-124">WMDRM- \_ revocationtype- \_ Gerät</span><span class="sxs-lookup"><span data-stu-id="49115-124">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="49115-125">Gibt ein Gerätezertifikat an.</span><span class="sxs-lookup"><span data-stu-id="49115-125">Specifies a device certificate.</span></span>                                |
| <span data-ttu-id="49115-126">WMDRM \_ revocationtype \_ Cardea</span><span class="sxs-lookup"><span data-stu-id="49115-126">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="49115-127">Gibt ein Windows Media DRM für Netzwerkgeräte Zertifikat an.</span><span class="sxs-lookup"><span data-stu-id="49115-127">Specifies a Windows Media DRM for Network Devices certificate.</span></span> |



 

</dd> <dt>

<span data-ttu-id="49115-128">*ccerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49115-128">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-129">Anzahl von Zertifikaten, für die Inhalts Enabler abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="49115-129">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="49115-130">Dies ist die Anzahl der Elemente im *rgpbcerts* -Array, des *rgpdwcertsizes* -Arrays und des *rgpguidcerts* -Arrays.</span><span class="sxs-lookup"><span data-stu-id="49115-130">This is the number of elements in the *rgpbCerts* array, the *rgpdwCertSizes* array, and the *rgpguidCerts* array.</span></span>

</dd> <dt>

<span data-ttu-id="49115-131">*hresulthint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="49115-131">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-132">Rückgabewert, der von dem Vorgang empfangen wurde, der aufgrund eines gesperrten Zertifikats nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="49115-132">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="49115-133">Wenn Sie nicht als Antwort auf einen fehlgeschlagenen Methodenaufruf aufrufen, legen Sie auf \_ OK fest.</span><span class="sxs-lookup"><span data-stu-id="49115-133">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="49115-134">*prgcontentenablers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="49115-134">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-135">Ein Array, das die Adressen der neu erstellten **IMF contentenabler** -Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="49115-135">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="49115-136">Legen Sie diese Einstellung auf **null** fest, um die Anzahl der Inhalts-Enabler im *pccontentenablers* -Parameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="49115-136">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="49115-137">*pccontentenablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="49115-137">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="49115-138">Anzahl der Elemente im *prgcontentenablers* -Array.</span><span class="sxs-lookup"><span data-stu-id="49115-138">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="49115-139">Wenn *prgcontentenablers* den Wert **null** hat, wird dieser Wert auf die Anzahl der benötigten Inhalts-Enabler bei der Ausgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="49115-139">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49115-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49115-140">Return value</span></span>

<span data-ttu-id="49115-141">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="49115-141">The method returns an **HRESULT**.</span></span> <span data-ttu-id="49115-142">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="49115-142">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="49115-143">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="49115-143">Return code</span></span>                                                                          | <span data-ttu-id="49115-144">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49115-144">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="49115-145"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="49115-145"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="49115-146">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="49115-146">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="49115-147">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49115-147">Remarks</span></span>

<span data-ttu-id="49115-148">Wenn Sie die **imfcontentenabler** -Schnittstelle zum Erneuern von widerrufenen Komponenten verwenden, müssen Sie den Prozess für den Benutzer verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="49115-148">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="49115-149">Diese Erläuterung muss vorgenommen werden, da der Aktualisierungsprozess Informationen vom Client Computer an eine Microsoft-Website sendet.</span><span class="sxs-lookup"><span data-stu-id="49115-149">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="49115-150">Wenn Sie **imfcontentenabler:: automaticenable** aufgerufen haben, wird der Standardbrowser von Content Wegbereiter mit der Adresse des Aktualisierungs Diensts auf der Microsoft-Website gestartet.</span><span class="sxs-lookup"><span data-stu-id="49115-150">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="49115-151">Ein eindeutiger Bezeichner, der die widerrufene Komponente identifiziert, wird an den Aktualisierungs Dienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="49115-151">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="49115-152">Der Dienst leitet dann den Browser an eine Webseite weiter, von der aus der Benutzer die neue Version der gesperrten Komponente herunterladen und installieren kann.</span><span class="sxs-lookup"><span data-stu-id="49115-152">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="49115-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49115-153">Requirements</span></span>



| <span data-ttu-id="49115-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49115-154">Requirement</span></span> | <span data-ttu-id="49115-155">Wert</span><span class="sxs-lookup"><span data-stu-id="49115-155">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="49115-156">Header</span><span class="sxs-lookup"><span data-stu-id="49115-156">Header</span></span><br/>  | <dl> <span data-ttu-id="49115-157"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="49115-157"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="49115-158">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49115-158">Library</span></span><br/> | <dl> <span data-ttu-id="49115-159"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="49115-159"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49115-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49115-160">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49115-161">**Automatisierte Sperrung und Erneuerung von Komponenten**</span><span class="sxs-lookup"><span data-stu-id="49115-161">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="49115-162">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="49115-162">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





