---
title: Iwmdrmlicensequery-Methode für die Methode "-Methode" (wmdrmsdk. h)
description: Die setactionaccesswedqueryparams-Methode legt Umgebungs spezifische Informationen für genauere Abfrageergebnisse fest, wenn die queryAction Allowed-Methode verwendet wird.
ms.assetid: 1c8f9d4e-999d-4d7c-87fd-9d30e432350c
keywords:
- "\"\"-Methode für die \"\"-Methode \"\" der Methode \"\" in Windows Media"
- Die Methode "" der Klasse "" ist ein Windows Media-Format, die iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, Methode "Methode"
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.SetActionAllowedQueryParams
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a83a28c4d9f3758b711c43ddd83a509c58f8ea8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359262"
---
# <a name="iwmdrmlicensequerysetactionallowedqueryparams-method"></a><span data-ttu-id="95a9a-106">Iwmdrmlicensequery:: ""-Methode</span><span class="sxs-lookup"><span data-stu-id="95a9a-106">IWMDRMLicenseQuery::SetActionAllowedQueryParams method</span></span>

<span data-ttu-id="95a9a-107">Die **setactionaccesswedqueryparams** -Methode legt Umgebungs spezifische Informationen für genauere Abfrageergebnisse fest, wenn die [**queryAction Allowed**](iwmdrmlicensequery-queryactionallowed.md) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95a9a-107">The **SetActionAllowedQueryParams** method sets environment-specific information for more accurate query results when using the [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="95a9a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="95a9a-108">Syntax</span></span>


```C++
HRESULT SetActionAllowedQueryParams(
  [in] BOOL  fIsMF,
  [in] DWORD dwAppSecLevel,
  [in] BOOL  fHasSerialNumber,
  [in] BSTR  bstrDeviceCert
);
```



## <a name="parameters"></a><span data-ttu-id="95a9a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="95a9a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95a9a-110">*fsmf* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95a9a-110">*fIsMF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a9a-111">Gibt an, ob der Inhalt mithilfe der Objekte des Microsoft Media Foundation SDK gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="95a9a-111">Specifies whether the content will be rendered by using the objects of the Microsoft Media Foundation SDK.</span></span> <span data-ttu-id="95a9a-112">**False** gibt das Rendering durch die Objekte des Windows Media Format SDK an.</span><span class="sxs-lookup"><span data-stu-id="95a9a-112">**FALSE** indicates rendering by the objects of the Windows Media Format SDK.</span></span> <span data-ttu-id="95a9a-113">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="95a9a-113">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="95a9a-114">*dwappberclevel* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95a9a-114">*dwAppSecLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a9a-115">Sicherheitsstufe der Abfrageanwendung.</span><span class="sxs-lookup"><span data-stu-id="95a9a-115">Security level of the querying application.</span></span> <span data-ttu-id="95a9a-116">Dieser Wert ist nur wichtig, wenn die Objekte des Windows Media Format SDK verwendet werden. in diesem Fall sollte " *fsmf* " auf " **false**" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="95a9a-116">This value is only important if the objects of the Windows Media Format SDK will be used, in which case *fIsMF* should be set to **FALSE**.</span></span> <span data-ttu-id="95a9a-117">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="95a9a-117">This parameter is optional.</span></span>

</dd> <dt>

<span data-ttu-id="95a9a-118">" *shasserialnumber* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="95a9a-118">*fHasSerialNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a9a-119">Gibt an, ob das Zielgerät für einen Kopiervorgang über eine Seriennummer verfügt.</span><span class="sxs-lookup"><span data-stu-id="95a9a-119">Specifies whether the target device for a copy operation has a serial number.</span></span> <span data-ttu-id="95a9a-120">Dieser Parameter ist optional und gilt nur für Abfragen für Kopiervorgänge.</span><span class="sxs-lookup"><span data-stu-id="95a9a-120">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> <dt>

<span data-ttu-id="95a9a-121">*bstraude vicecert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="95a9a-121">*bstrDeviceCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95a9a-122">Gerätezertifikat des Zielgeräts, wenn Windows Media DRM für tragbare Geräte verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="95a9a-122">Device certificate of the target device when using Windows Media DRM for Portable Devices.</span></span> <span data-ttu-id="95a9a-123">Dieser Parameter ist optional und gilt nur für Abfragen für Kopiervorgänge.</span><span class="sxs-lookup"><span data-stu-id="95a9a-123">This parameter is optional and only applies to queries for copy operations.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95a9a-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95a9a-124">Return value</span></span>

<span data-ttu-id="95a9a-125">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="95a9a-125">The method returns an **HRESULT**.</span></span> <span data-ttu-id="95a9a-126">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="95a9a-126">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="95a9a-127">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="95a9a-127">Return code</span></span>                                                                          | <span data-ttu-id="95a9a-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="95a9a-128">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="95a9a-129"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="95a9a-129"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="95a9a-130">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="95a9a-130">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="95a9a-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95a9a-131">Remarks</span></span>

<span data-ttu-id="95a9a-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="95a9a-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="95a9a-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="95a9a-133">Requirements</span></span>



| <span data-ttu-id="95a9a-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="95a9a-134">Requirement</span></span> | <span data-ttu-id="95a9a-135">Wert</span><span class="sxs-lookup"><span data-stu-id="95a9a-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95a9a-136">Header</span><span class="sxs-lookup"><span data-stu-id="95a9a-136">Header</span></span><br/>  | <dl> <span data-ttu-id="95a9a-137"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="95a9a-137"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="95a9a-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="95a9a-138">Library</span></span><br/> | <dl> <span data-ttu-id="95a9a-139"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95a9a-139"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95a9a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="95a9a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95a9a-141">**Iwmdrmlicensequery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="95a9a-141">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="95a9a-142">**Abfragen ausführlicher Rechte Informationen**</span><span class="sxs-lookup"><span data-stu-id="95a9a-142">**Querying for Detailed Rights Information**</span></span>](querying-for-detailed-rights-information.md)
</dt> </dl>

 

 





