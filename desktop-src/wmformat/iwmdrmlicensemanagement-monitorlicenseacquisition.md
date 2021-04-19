---
title: Iwmdrmlicenabacquisition-Methode (wmdrmsdk. h)
description: Die monitorlicensererwerbs-Methode initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.
ms.assetid: 725cd51a-a50b-4ff5-a880-7f551f6dba8f
keywords:
- Monitorlicenabacquisition-Methode Windows Media-Format
- Monitorlicenaberwerbs-Methode Windows Media-Format, iwmdrmlicenabsmanagement-Schnittstelle
- Iwmdrmlicenabmanagement Interface Windows Media-Format, monitorliceneracquisition-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.MonitorLicenseAcquisition
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25171d36a9d360f7c8eb77211c580c4f7676618f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357305"
---
# <a name="iwmdrmlicensemanagementmonitorlicenseacquisition-method"></a><span data-ttu-id="63847-106">Iwmdrmlicensmanagement:: monitorliceneracquisition-Methode</span><span class="sxs-lookup"><span data-stu-id="63847-106">IWMDRMLicenseManagement::MonitorLicenseAcquisition method</span></span>

<span data-ttu-id="63847-107">Die **monitorlicensererwerbs** -Methode initiiert die Überwachung für einen Lizenz Erwerbs Vorgang.</span><span class="sxs-lookup"><span data-stu-id="63847-107">The **MonitorLicenseAcquisition** method initiates monitoring for a license acquisition process.</span></span>

## <a name="syntax"></a><span data-ttu-id="63847-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="63847-108">Syntax</span></span>


```C++
HRESULT MonitorLicenseAcquisition(
  [in]  BSTR     bstrKID,
  [in]  BSTR     bstrHeader,
  [in]  BSTR     bstrActions,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="63847-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="63847-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63847-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63847-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63847-111">Die Schlüssel-ID (Kid) der erworbenen Lizenz.</span><span class="sxs-lookup"><span data-stu-id="63847-111">Key ID (KID) of the license being acquired.</span></span>

</dd> <dt>

<span data-ttu-id="63847-112">*bstrauch Header* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63847-112">*bstrHeader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63847-113">Inhalts Header, der im Aufrufen der [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) -Methode verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="63847-113">Content header that was used in the call to the [**AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="63847-114">*bstractions* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63847-114">*bstrActions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63847-115">Zeichenfolge, die die im Aufrufen der **AcquireLicense** -Methode angeforderten Aktionen enthält.</span><span class="sxs-lookup"><span data-stu-id="63847-115">String containing the actions requested in the call to the **AcquireLicense** method.</span></span>

</dd> <dt>

<span data-ttu-id="63847-116">*ppunkcancelationcookie* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="63847-116">*ppunkCancelationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63847-117">Ein Zeiger, der einen Zeiger auf die **IUnknown** -Schnittstelle eines Objekts empfängt, das diesen asynchronen-Befehl identifiziert.</span><span class="sxs-lookup"><span data-stu-id="63847-117">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="63847-118">Dieser Schnittstellen Zeiger kann zum Abbrechen des asynchronen Aufrufs verwendet werden, indem die [**iwmdrmeventgenerator:: cancelasyncoperation**](iwmdrmeventgenerator-cancelasyncoperation.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="63847-118">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63847-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="63847-119">Return value</span></span>

<span data-ttu-id="63847-120">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="63847-120">The method returns an **HRESULT**.</span></span> <span data-ttu-id="63847-121">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="63847-121">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="63847-122">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="63847-122">Return code</span></span>                                                                          | <span data-ttu-id="63847-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="63847-123">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="63847-124"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="63847-124"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="63847-125">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="63847-125">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="63847-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63847-126">Remarks</span></span>

<span data-ttu-id="63847-127">Keine.</span><span class="sxs-lookup"><span data-stu-id="63847-127">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="63847-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63847-128">Requirements</span></span>



| <span data-ttu-id="63847-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63847-129">Requirement</span></span> | <span data-ttu-id="63847-130">Wert</span><span class="sxs-lookup"><span data-stu-id="63847-130">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="63847-131">Header</span><span class="sxs-lookup"><span data-stu-id="63847-131">Header</span></span><br/>  | <dl> <span data-ttu-id="63847-132"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="63847-132"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="63847-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="63847-133">Library</span></span><br/> | <dl> <span data-ttu-id="63847-134"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63847-134"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63847-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63847-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63847-136">**Iwmdrmlicenabmanagement-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="63847-136">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





