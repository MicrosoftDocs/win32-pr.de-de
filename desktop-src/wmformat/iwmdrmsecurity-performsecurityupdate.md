---
title: Iwmdrmsecurity performsecurityupdate-Methode (wmdrmsdk. h)
description: Die performsecurityupdate-Methode initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem lokalen Computer.
ms.assetid: e450a1e3-6024-4c00-9978-fbc88fde2101
keywords:
- Performsecurityupdate-Methode Windows Media-Format
- Performsecurityupdate-Methode Windows Media-Format, iwmdrmsecurity-Schnittstelle
- Iwmdrmsecurity-Schnittstelle Windows Media-Format, performsecurityupdate-Methode
topic_type:
- apiref
api_name:
- IWMDRMSecurity.PerformSecurityUpdate
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a34a1e92edd279655737a2e8f3b7ce4e77e27fd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364603"
---
# <a name="iwmdrmsecurityperformsecurityupdate-method"></a><span data-ttu-id="440e0-106">Iwmdrmsecurity::P erformsecurityupdate-Methode</span><span class="sxs-lookup"><span data-stu-id="440e0-106">IWMDRMSecurity::PerformSecurityUpdate method</span></span>

<span data-ttu-id="440e0-107">Die **performsecurityupdate** -Methode initiiert ein Sicherheitsupdate des DRM-Subsystems auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="440e0-107">The **PerformSecurityUpdate** method initiates a security update to the DRM subsystem on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="440e0-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="440e0-108">Syntax</span></span>


```C++
HRESULT PerformSecurityUpdate(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="440e0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="440e0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="440e0-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="440e0-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="440e0-111">Die Update Option wurde als eines der folgenden Flags ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="440e0-111">Update option expressed as one of the following flags.</span></span>



| <span data-ttu-id="440e0-112">Flag</span><span class="sxs-lookup"><span data-stu-id="440e0-112">Flag</span></span>                                          | <span data-ttu-id="440e0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="440e0-113">Description</span></span>                                                                                     |
|-----------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="440e0-114">WMDRM- \_ Sicherheit \_ Durchführen von \_ indiv</span><span class="sxs-lookup"><span data-stu-id="440e0-114">WMDRM\_SECURITY\_PERFORM\_INDIV</span></span>               | <span data-ttu-id="440e0-115">Bewirkt, dass die DRM-Komponente nur dann individualisiert wird, wenn die Version des Clients veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="440e0-115">Causes the DRM component to be individualized only if the version of the client is out of date.</span></span> |
| <span data-ttu-id="440e0-116">WMDRM- \_ Sicherheit \_ Durchführen der Sperr \_ \_ Aktualisierung</span><span class="sxs-lookup"><span data-stu-id="440e0-116">WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH</span></span> | <span data-ttu-id="440e0-117">Bewirkt, dass die Sperr Listen auf dem Client Computer aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="440e0-117">Causes the revocation lists on the client computer to be updated.</span></span>                               |
| <span data-ttu-id="440e0-118">WMDRM- \_ Sicherheit \_ Durchführen von Force- \_ \_ indiv</span><span class="sxs-lookup"><span data-stu-id="440e0-118">WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV</span></span>        | <span data-ttu-id="440e0-119">Bewirkt, dass die DRM-Komponente individuell ist, auch wenn die Version des Clients auf dem neuesten Stand ist.</span><span class="sxs-lookup"><span data-stu-id="440e0-119">Causes the DRM component to be individualized even if the version of the client is up to date.</span></span>  |



 

</dd> <dt>

<span data-ttu-id="440e0-120">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="440e0-120">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="440e0-121">Adresse einer Variablen, die einen Zeiger auf ein Objekt empfängt, das verwendet werden kann, um diesen Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="440e0-121">Address of a variable that receives a pointer to an object that can be used to cancel this operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="440e0-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="440e0-122">Return value</span></span>

<span data-ttu-id="440e0-123">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="440e0-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="440e0-124">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="440e0-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="440e0-125">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="440e0-125">Return code</span></span>                                                                          | <span data-ttu-id="440e0-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="440e0-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="440e0-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="440e0-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="440e0-128">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="440e0-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="440e0-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="440e0-129">Remarks</span></span>

<span data-ttu-id="440e0-130">Diese Methode wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="440e0-130">This method executes asynchronously.</span></span> <span data-ttu-id="440e0-131">Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann Ereignisse, abhängig von dem im *dwFlags* -Parameter festgelegten Flag.</span><span class="sxs-lookup"><span data-stu-id="440e0-131">It returns immediately after being called and then generates events depending on the flag set in the *dwFlags* parameter.</span></span>

<span data-ttu-id="440e0-132">Für die individuelle Authentifizierung (Flag ist auf WMDRM- \_ Sicherheit \_ Durchführen von \_ indiv oder WMDRM \_ Security do \_ \_ Force \_ indiv festgelegt) wird eine Reihe von **mewmdrmindividualizationprogress** -Ereignissen generiert, gefolgt von einem **mewmdrmindividualizationcomplete** -Ereignis, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="440e0-132">For individualization (flag set to WMDRM\_SECURITY\_PERFORM\_INDIV or WMDRM\_SECURITY\_PERFORM\_FORCE\_INDIV), a series of **MEWMDRMIndividualizationProgress** events is generated followed by an **MEWMDRMIndividualizationCompleted** event when processing is complete.</span></span> <span data-ttu-id="440e0-133">Der Wert jedes **mewmdrmindividualizationprogress** -Ereignisses, das durch Aufrufen von **imfmediaevent:: GetValue** abgerufen wird, ist ein **IUnknown** -Zeiger.</span><span class="sxs-lookup"><span data-stu-id="440e0-133">The value of each of the **MEWMDRMIndividualizationProgress** events obtained by calling **IMFMediaEvent::GetValue** is an **IUnknown** pointer.</span></span> <span data-ttu-id="440e0-134">Sie können die **QueryInterface** -Methode der abgerufenen **IUnknown** -Schnittstelle aufzurufen, um eine Instanz der [**iwmdrmindividualizationstatus**](iwmdrmindividualizationstatus.md) -Schnittstelle zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="440e0-134">You can call the **QueryInterface** method of the retrieved **IUnknown** interface to get an instance of the [**IWMDRMIndividualizationStatus**](iwmdrmindividualizationstatus.md) interface.</span></span>

<span data-ttu-id="440e0-135">Zum Aktualisieren der Sperr Listen (Flag ist auf WMDRM- \_ Sicherheit durchführen der Sperr Aktualisierung festgelegt \_ \_ \_ ) wird ein **mewmdrmrevocationdownloadcomplete** -Ereignis generiert, wenn die Verarbeitung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="440e0-135">For refreshing the revocation lists (flag set to WMDRM\_SECURITY\_PERFORM\_REVOCATION\_REFRESH), an **MEWMDRMREvocationDownloadCompleted** event is generated when processing is complete.</span></span>

> [!Note]  
> <span data-ttu-id="440e0-136">Wenn **performsecurityupdate** die Individualisierung abschließt, sind die einzigen Objekte, die den neuen, individualisierten Zustand widerspiegeln, diejenigen, die von **iwmdrmsecurity** erben.</span><span class="sxs-lookup"><span data-stu-id="440e0-136">When **PerformSecurityUpdate** completes individualization, the only existing objects that will reflect the new individualized state are those that inherit from **IWMDRMSecurity**.</span></span> <span data-ttu-id="440e0-137">Alle anderen vorhandenen Objekte werden nicht aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="440e0-137">All other existing objects will not be updated.</span></span> <span data-ttu-id="440e0-138">Sie müssen alle anderen Objekte freigeben und neu erstellen, damit Sie den neuen, individualisierten Zustand widerspiegeln.</span><span class="sxs-lookup"><span data-stu-id="440e0-138">You must release and re-create any other objects so that they will reflect the new individualized state.</span></span>

 

<span data-ttu-id="440e0-139">Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="440e0-139">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="440e0-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="440e0-140">Requirements</span></span>



| <span data-ttu-id="440e0-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="440e0-141">Requirement</span></span> | <span data-ttu-id="440e0-142">Wert</span><span class="sxs-lookup"><span data-stu-id="440e0-142">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="440e0-143">Header</span><span class="sxs-lookup"><span data-stu-id="440e0-143">Header</span></span><br/>  | <dl> <span data-ttu-id="440e0-144"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="440e0-144"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="440e0-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="440e0-145">Library</span></span><br/> | <dl> <span data-ttu-id="440e0-146"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="440e0-146"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="440e0-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="440e0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="440e0-148">**Automatisierte Sperrung und Erneuerung von Komponenten**</span><span class="sxs-lookup"><span data-stu-id="440e0-148">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="440e0-149">**Beispiel für DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="440e0-149">**DRM Individualization Example**</span></span>](drm-individualization-example.md)
</dt> <dt>

[<span data-ttu-id="440e0-150">**Iwmdrmsecurity-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="440e0-150">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="440e0-151">**Durchführen der DRM-Individualisierung**</span><span class="sxs-lookup"><span data-stu-id="440e0-151">**Performing DRM Individualization**</span></span>](performing-drm-individualization.md)
</dt> </dl>

 

 





