---
title: Iwmdrmsecurity getcontentenablersfromhashes-Methode (wmdrmsdk. h)
description: Die getcontentenablersfromhashes-Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten auf der Grundlage von Hash Zertifikaten ermöglichen.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- Getcontentenablersfromhashes-Methode Windows Media-Format
- Getcontentenablersfromhashes-Methode, Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, getcontentenablersfromhashes-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f44b4187699cb4a55d0c6215e3f31b430a87d299
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368322"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a><span data-ttu-id="a9f12-106">Iwmdrmsecurity:: getcontentenablersfromhashes-Methode</span><span class="sxs-lookup"><span data-stu-id="a9f12-106">IWMDRMSecurity::GetContentEnablersFromHashes method</span></span>

<span data-ttu-id="a9f12-107">Die **getcontentenablersfromhashes** -Methode ruft inhaltsenabler-Schnittstellen ab, die das Erneuern von Komponenten auf der Grundlage von Hash Zertifikaten ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a9f12-107">The **GetContentEnablersFromHashes** method retrieves content enabler interfaces that enable renewal of components based on hashed certificates.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9f12-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9f12-108">Syntax</span></span>


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a><span data-ttu-id="a9f12-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9f12-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9f12-110">*rgpbcerthashes* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f12-110">*rgpbCertHashes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f12-111">Ein Array von zertifikathashes zum Abrufen von Inhalts Enablern.</span><span class="sxs-lookup"><span data-stu-id="a9f12-111">Array of certificate hashes to obtain content enablers for.</span></span>

</dd> <dt>

<span data-ttu-id="a9f12-112">*ccerts* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f12-112">*cCerts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f12-113">Anzahl von Zertifikaten, für die Inhalts Enabler abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a9f12-113">Number of certificates to retrieve content enablers for.</span></span> <span data-ttu-id="a9f12-114">Dies ist die Anzahl der Elemente im *rgpbcerthashes* -Array.</span><span class="sxs-lookup"><span data-stu-id="a9f12-114">This is the number of elements in the *rgpbCertHashes* array.</span></span>

</dd> <dt>

<span data-ttu-id="a9f12-115">*hresulthint* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a9f12-115">*hResultHint* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f12-116">Rückgabewert, der von dem Vorgang empfangen wurde, der aufgrund eines gesperrten Zertifikats nicht erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="a9f12-116">Return value received from the operation that failed due to a revoked certificate.</span></span> <span data-ttu-id="a9f12-117">Wenn Sie nicht als Antwort auf einen fehlgeschlagenen Methodenaufruf aufrufen, legen Sie auf \_ OK fest.</span><span class="sxs-lookup"><span data-stu-id="a9f12-117">If you are not calling in response to a failed method call, set to S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="a9f12-118">*prgcontentenablers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="a9f12-118">*prgContentEnablers* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f12-119">Ein Array, das die Adressen der neu erstellten **IMF contentenabler** -Schnittstellen empfängt.</span><span class="sxs-lookup"><span data-stu-id="a9f12-119">Array that receives the addresses of the newly created **IMFContentEnabler** interfaces.</span></span> <span data-ttu-id="a9f12-120">Legen Sie diese Einstellung auf **null** fest, um die Anzahl der Inhalts-Enabler im *pccontentenablers* -Parameter zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a9f12-120">Set to **NULL** to get the number of content enablers in the *pcContentEnablers* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a9f12-121">*pccontentenablers* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="a9f12-121">*pcContentEnablers* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a9f12-122">Anzahl der Elemente im *prgcontentenablers* -Array.</span><span class="sxs-lookup"><span data-stu-id="a9f12-122">Number of elements in the *prgContentEnablers* array.</span></span> <span data-ttu-id="a9f12-123">Wenn *prgcontentenablers* den Wert **null** hat, wird dieser Wert auf die Anzahl der benötigten Inhalts-Enabler bei der Ausgabe festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a9f12-123">If *prgContentEnablers* is **NULL**, this value is set to the number of needed content enablers on output.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9f12-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9f12-124">Return value</span></span>

<span data-ttu-id="a9f12-125">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="a9f12-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a9f12-126">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="a9f12-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a9f12-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="a9f12-127">Return code</span></span>                                                                          | <span data-ttu-id="a9f12-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9f12-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a9f12-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="a9f12-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a9f12-130">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a9f12-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a9f12-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9f12-131">Remarks</span></span>

<span data-ttu-id="a9f12-132">Wenn Sie die **imfcontentenabler** -Schnittstelle zum Erneuern von widerrufenen Komponenten verwenden, müssen Sie den Prozess für den Benutzer verdeutlichen.</span><span class="sxs-lookup"><span data-stu-id="a9f12-132">If you use the **IMFContentEnabler** interface to renew revoked components, you must clarify the process to the user.</span></span> <span data-ttu-id="a9f12-133">Diese Erläuterung muss vorgenommen werden, da der Aktualisierungsprozess Informationen vom Client Computer an eine Microsoft-Website sendet.</span><span class="sxs-lookup"><span data-stu-id="a9f12-133">This clarification must be made because the update process sends information from the client computer to a Microsoft Web site.</span></span>

<span data-ttu-id="a9f12-134">Wenn Sie **imfcontentenabler:: automaticenable** aufgerufen haben, wird der Standardbrowser von Content Wegbereiter mit der Adresse des Aktualisierungs Diensts auf der Microsoft-Website gestartet.</span><span class="sxs-lookup"><span data-stu-id="a9f12-134">When you call **IMFContentEnabler::AutomaticEnable**, the content enabler launches the default browser with the address of the update service on the Microsoft Web site.</span></span> <span data-ttu-id="a9f12-135">Ein eindeutiger Bezeichner, der die widerrufene Komponente identifiziert, wird an den Aktualisierungs Dienst gesendet.</span><span class="sxs-lookup"><span data-stu-id="a9f12-135">A unique identifier that identifies the revoked component is sent to the update service.</span></span> <span data-ttu-id="a9f12-136">Der Dienst leitet dann den Browser an eine Webseite weiter, von der aus der Benutzer die neue Version der gesperrten Komponente herunterladen und installieren kann.</span><span class="sxs-lookup"><span data-stu-id="a9f12-136">The service then redirects the browser to a Web page from which the user may be able to download and install the new version of the revoked component.</span></span>

## <a name="requirements"></a><span data-ttu-id="a9f12-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9f12-137">Requirements</span></span>



| <span data-ttu-id="a9f12-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9f12-138">Requirement</span></span> | <span data-ttu-id="a9f12-139">Wert</span><span class="sxs-lookup"><span data-stu-id="a9f12-139">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a9f12-140">Header</span><span class="sxs-lookup"><span data-stu-id="a9f12-140">Header</span></span><br/>  | <dl> <span data-ttu-id="a9f12-141"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9f12-141"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="a9f12-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="a9f12-142">Library</span></span><br/> | <dl> <span data-ttu-id="a9f12-143"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a9f12-143"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9f12-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9f12-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9f12-145">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a9f12-145">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> </dl>

 

 





