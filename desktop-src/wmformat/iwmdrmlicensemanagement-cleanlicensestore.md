---
title: Iwmdrmlicenabmanagement cleanlicensstore-Methode (wmdrmsdk. h)
description: Die cleanlicenserstore-Methode entfernt nicht verwendbare Lizenzen aus dem temporären Lizenz Speicher und defragmentiert den lokalen Lizenz Speicher, um die Leistung zu verbessern.
ms.assetid: 07ddd6f8-a091-4c18-81d3-c4d0c6026b6b
keywords:
- Cleanlicenerstore-Methode Windows Media-Format
- Cleanlicenerstore-Methode Windows Media-Format, iwmdrmlicenermanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, cleanlicenerstore-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CleanLicenseStore
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9327fd836cf742f5495c29767be93d914c0f187
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351213"
---
# <a name="iwmdrmlicensemanagementcleanlicensestore-method"></a><span data-ttu-id="5a773-106">Iwmdrmlicenabmanagement:: cleanlicensstore-Methode</span><span class="sxs-lookup"><span data-stu-id="5a773-106">IWMDRMLicenseManagement::CleanLicenseStore method</span></span>

<span data-ttu-id="5a773-107">Die **cleanlicenserstore** -Methode entfernt nicht verwendbare Lizenzen aus dem temporären Lizenz Speicher und defragmentiert den lokalen Lizenz Speicher, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="5a773-107">The **CleanLicenseStore** method removes unusable licenses from the temporary license store and defragments the local license store to improve performance.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a773-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a773-108">Syntax</span></span>


```C++
HRESULT CleanLicenseStore(
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="5a773-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a773-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a773-110">*dwFlags* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5a773-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5a773-111">Flags, die die zu verwendenden Reinigungs Optionen für den Lizenz Speicher angeben.</span><span class="sxs-lookup"><span data-stu-id="5a773-111">Flags specifying the license store cleaning options to use.</span></span> <span data-ttu-id="5a773-112">Legen Sie auf eine der Konstanten in der folgenden Tabelle fest.</span><span class="sxs-lookup"><span data-stu-id="5a773-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="5a773-113">Konstante</span><span class="sxs-lookup"><span data-stu-id="5a773-113">Constant</span></span>                            | <span data-ttu-id="5a773-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5a773-114">Description</span></span>                                                                                                                                                                    |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a773-115">Synchronisierung des WMDRM- \_ \_ Lizenz \_ Speicher bereinigen \_</span><span class="sxs-lookup"><span data-stu-id="5a773-115">WMDRM\_CLEAN\_LICENSE\_STORE\_SYNC</span></span>  | <span data-ttu-id="5a773-116">Der Clean-Vorgang wird synchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a773-116">The clean operation will be performed synchronously.</span></span> <span data-ttu-id="5a773-117">Diese Methode wird erst zurückgegeben, wenn der Vorgang beendet ist.</span><span class="sxs-lookup"><span data-stu-id="5a773-117">This method will not return until the operation is complete.</span></span>                                                              |
| <span data-ttu-id="5a773-118">WMDRM- \_ Clean \_ License \_ Store \_ Async</span><span class="sxs-lookup"><span data-stu-id="5a773-118">WMDRM\_CLEAN\_LICENSE\_STORE\_ASYNC</span></span> | <span data-ttu-id="5a773-119">Der Clean-Vorgang wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a773-119">The clean operation will be performed asynchronously.</span></span> <span data-ttu-id="5a773-120">Diese Methode wird sofort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5a773-120">This method will return immediately.</span></span> <span data-ttu-id="5a773-121">Wenn der Vorgang beendet ist, wird das Medienereignis "melicensetup" gesendet.</span><span class="sxs-lookup"><span data-stu-id="5a773-121">When the operation is complete, the media event MELicenseStoreCleaned will be sent.</span></span> |



 

</dd> <dt>

<span data-ttu-id="5a773-122">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5a773-122">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a773-123">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5a773-123">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="5a773-124">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5a773-124">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a773-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5a773-125">Return value</span></span>

<span data-ttu-id="5a773-126">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a773-126">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5a773-127">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="5a773-127">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5a773-128">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5a773-128">Return code</span></span>                                                                                            | <span data-ttu-id="5a773-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a773-129">Description</span></span>                                                            |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5a773-130"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5a773-130"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="5a773-131">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a773-131">The method succeeded.</span></span><br/>                                       |
| <dl> <span data-ttu-id="5a773-132"><dt>**DRM- \_ E \_ licensenotfound**</dt></span><span class="sxs-lookup"><span data-stu-id="5a773-132"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="5a773-133">Auf dem Client Computer ist kein temporärer Lizenz Speicher vorhanden.</span><span class="sxs-lookup"><span data-stu-id="5a773-133">There is no temporary license store on the client computer.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5a773-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a773-134">Remarks</span></span>

<span data-ttu-id="5a773-135">Diese Methode wird asynchron ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a773-135">This method executes asynchronously.</span></span> <span data-ttu-id="5a773-136">Sie wird sofort nach dem Aufruf von zurückgegeben und generiert dann ein **mewmdrmlicenabgelig-Ereignis** , wenn die Verarbeitung fertiggestellt ist.</span><span class="sxs-lookup"><span data-stu-id="5a773-136">It returns immediately after being called and then generates an **MEWMDRMLicenseStoreCleaned** event when processing is complete.</span></span>

<span data-ttu-id="5a773-137">Weitere Informationen zur Verwendung der asynchronen Methoden der erweiterten APIs für den Windows Media DRM-Client finden [Sie unter Verwenden des Media Foundation-Ereignis Modells](using-the-media-foundation-model.md).</span><span class="sxs-lookup"><span data-stu-id="5a773-137">For more information about using the asynchronous methods of the Windows Media DRM Client Extended APIs, see [Using the Media Foundation Event Model](using-the-media-foundation-model.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a773-138">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5a773-138">Requirements</span></span>



| <span data-ttu-id="5a773-139">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5a773-139">Requirement</span></span> | <span data-ttu-id="5a773-140">Wert</span><span class="sxs-lookup"><span data-stu-id="5a773-140">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5a773-141">Header</span><span class="sxs-lookup"><span data-stu-id="5a773-141">Header</span></span><br/>  | <dl> <span data-ttu-id="5a773-142"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="5a773-142"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="5a773-143">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5a773-143">Library</span></span><br/> | <dl> <span data-ttu-id="5a773-144"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5a773-144"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a773-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a773-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a773-146">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="5a773-146">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





