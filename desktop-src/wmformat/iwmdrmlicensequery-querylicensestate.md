---
title: Iwmdrmlicensequery querylicenerstate-Methode (wmdrmsdk. h)
description: Die querylicenserstate-Methode fragt den lokalen Lizenz Speicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.
ms.assetid: 17f40c56-2266-4c94-9e95-a33a92ddef74
keywords:
- Querylicenenstate-Methode Windows Media-Format
- Querylicenserstate-Methode Windows Media-Format, iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, querylicenserstate-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryLicenseState
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e101d4ad9b5405906d05ba5e5f230326a1a3f13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372264"
---
# <a name="iwmdrmlicensequeryquerylicensestate-method"></a><span data-ttu-id="c2dc2-106">Iwmdrmlicensequery:: querylicenserstate-Methode</span><span class="sxs-lookup"><span data-stu-id="c2dc2-106">IWMDRMLicenseQuery::QueryLicenseState method</span></span>

<span data-ttu-id="c2dc2-107">Die **querylicenserstate** -Methode fragt den lokalen Lizenz Speicher nach Lizenzinformationen ab, die für eine Schlüssel-ID für ein oder mehrere bestimmte Rechte gelten.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-107">The **QueryLicenseState** method queries the local license store for license information that applies to a Key ID for one or more specific rights.</span></span>

## <a name="syntax"></a><span data-ttu-id="c2dc2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2dc2-108">Syntax</span></span>


```C++
HRESULT QueryLicenseState(
  [in]  BSTR                   bstrKID,
  [in]  DWORD                  cActionsToQuery,
  [in]  BSTR                   rgbstrActionsToQuery[],
  [out] DRM_LICENSE_STATE_DATA rgResultStateData[]
);
```



## <a name="parameters"></a><span data-ttu-id="c2dc2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2dc2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2dc2-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2dc2-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dc2-111">Die Schlüssel-ID, für die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-111">Key ID for which to query.</span></span> <span data-ttu-id="c2dc2-112">Nur Lizenzen, die auf diese Schlüssel-ID zutreffen, werden ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="c2dc2-113">*cactionstoquery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c2dc2-113">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dc2-114">Die Anzahl der Aktionen, für die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-114">The number of actions for which to query.</span></span> <span data-ttu-id="c2dc2-115">Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstractionstoquery* und *rgresultstatedata* übermittelt wurden.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-115">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgResultStateData* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="c2dc2-116">*rgbstractionstoquery \[ \]* \[in\]</span><span class="sxs-lookup"><span data-stu-id="c2dc2-116">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dc2-117">Ein Array von mindestens einem Recht, für das abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-117">Array of one or more rights for which to query.</span></span> <span data-ttu-id="c2dc2-118">Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-118">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="c2dc2-119">Jedes Element muss auf eine der folgenden Konstanten festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-119">Each element must be set to one of the following constants.</span></span>



| <span data-ttu-id="c2dc2-120">Konstante</span><span class="sxs-lookup"><span data-stu-id="c2dc2-120">Constant</span></span>                                        | <span data-ttu-id="c2dc2-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2dc2-121">Description</span></span>                                                                                                                                        |
|-------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dc2-122">g \_ wszwmdrm \_ licenlstate- \_ Sicherung</span><span class="sxs-lookup"><span data-stu-id="c2dc2-122">g\_wszWMDRM\_LicenseState\_Backup</span></span>               | <span data-ttu-id="c2dc2-123">Schließen Sie ein, um die Details zu den rechten zum Sichern und Wiederherstellen der Lizenz abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-123">Include to query for the details about the right to back up and restore the license.</span></span>                                                               |
| <span data-ttu-id="c2dc2-124">g \_ wszwmdrm \_ licen\state \_ kollaborativeplay</span><span class="sxs-lookup"><span data-stu-id="c2dc2-124">g\_wszWMDRM\_LicenseState\_CollaborativePlay</span></span>    | <span data-ttu-id="c2dc2-125">Schließen Sie ein, um die Details über das Recht zur Freigabe des Inhalts für eine Gruppe von Benutzern im Rahmen eines kollaborativen Wiedergabe Szenarios abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-125">Include to query for the details about the right to share the content with a group of users as part of a collaborative playback scenario.</span></span>          |
| <span data-ttu-id="c2dc2-126">"g \_ wszwmdrm \_ licenanstate" \_ Kopieren</span><span class="sxs-lookup"><span data-stu-id="c2dc2-126">g\_wszWMDRM\_LicenseState\_Copy</span></span>                 | <span data-ttu-id="c2dc2-127">Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf externe Geräte oder Medien abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-127">Include to query for the details about the right to copy the content to external devices or media.</span></span>                                                 |
| <span data-ttu-id="c2dc2-128">g \_ wszwmdrm \_ licenanstate \_ copyper CD</span><span class="sxs-lookup"><span data-stu-id="c2dc2-128">g\_wszWMDRM\_LicenseState\_CopyToCD</span></span>             | <span data-ttu-id="c2dc2-129">Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf die CD abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-129">Include to query for the details about the right to copy the content to CD.</span></span>                                                                        |
| <span data-ttu-id="c2dc2-130">g \_ wszwmdrm \_ licensstate \_ copytononsdmidevice</span><span class="sxs-lookup"><span data-stu-id="c2dc2-130">g\_wszWMDRM\_LicenseState\_CopyToNonSDMIDevice</span></span>  | <span data-ttu-id="c2dc2-131">Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf ein Gerät abzufragen, das die Secure Digital Media Initiative (SDMI) nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-131">Include to query for the details about the right to copy the content to a device that does not support the secure digital media initiative (SDMI).</span></span> |
| <span data-ttu-id="c2dc2-132">g \_ wszwmdrm \_ \_ licentarstate copytosdmidevice</span><span class="sxs-lookup"><span data-stu-id="c2dc2-132">g\_wszWMDRM\_LicenseState\_CopyToSDMIDevice</span></span>     | <span data-ttu-id="c2dc2-133">Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf ein Gerät abzufragen, das SDMI unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-133">Include to query for the details about the right to copy the content to a device that supports the SDMI.</span></span>                                           |
| <span data-ttu-id="c2dc2-134">g \_ wszwmdrm \_ \_ licencstate "erstellungenbnailimage"</span><span class="sxs-lookup"><span data-stu-id="c2dc2-134">g\_wszWMDRM\_LicenseState\_CreateThumbnailImage</span></span> | <span data-ttu-id="c2dc2-135">Schließen Sie ein, um die Details über das Recht zum Erstellen eines Miniatur Bilds aus dem Inhalt abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-135">Include to query for the details about the right to create a thumbnail image from the content.</span></span>                                                     |
| <span data-ttu-id="c2dc2-136">g \_ wszwmdrm \_ licenanstate- \_ Wiedergabe</span><span class="sxs-lookup"><span data-stu-id="c2dc2-136">g\_wszWMDRM\_LicenseState\_Playback</span></span>             | <span data-ttu-id="c2dc2-137">Schließen Sie ein, um die Details über das Recht zur Wiedergabe des Inhalts abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-137">Include to query for the details about the right to play the content.</span></span>                                                                              |
| <span data-ttu-id="c2dc2-138">g \_ wszwmdrm \_ licenanstate \_ playlistburn</span><span class="sxs-lookup"><span data-stu-id="c2dc2-138">g\_wszWMDRM\_LicenseState\_PlaylistBurn</span></span>         | <span data-ttu-id="c2dc2-139">Schließen Sie ein, um die Details über das Recht zum Kopieren des Inhalts auf CD als Teil einer Wiedergabeliste abzufragen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-139">Include to query for the details about the right to copy the content to CD as part of a playlist.</span></span>                                                  |



 

</dd> <dt>

<span data-ttu-id="c2dc2-140">*rgresultstatedata \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="c2dc2-140">*rgResultStateData\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c2dc2-141">Ein Array aus mindestens einer [**DRM- \_ Lizenz \_ Status \_ Daten**](drmdrm-license-state-data.md) Struktur, die die Lizenz Zustandsinformationen empfängt, die im entsprechenden-Element des *rgbstractionstoquery* -Parameters auf das Recht zutreffen.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-141">Array of one or more [**DRM\_LICENSE\_STATE\_DATA**](drmdrm-license-state-data.md) structures that receive the license state information that applies to the right in the corresponding element of the *rgbstrActionsToQuery* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2dc2-142">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2dc2-142">Return value</span></span>

<span data-ttu-id="c2dc2-143">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-143">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c2dc2-144">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-144">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c2dc2-145">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="c2dc2-145">Return code</span></span>                                                                          | <span data-ttu-id="c2dc2-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2dc2-146">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="c2dc2-147"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc2-147"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="c2dc2-148">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-148">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c2dc2-149">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2dc2-149">Remarks</span></span>

<span data-ttu-id="c2dc2-150">Alle Lizenzen, die für die angegebene Schlüssel-ID gelten, werden durchsucht und ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-150">All licenses that apply to the specified Key ID will be searched and evaluated.</span></span> <span data-ttu-id="c2dc2-151">Die Ergebnisse werden aggregiert, sodass jede **DRM- \_ Lizenz \_ Status- \_ Daten** Strukturinformationen aus mehreren Lizenzen enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="c2dc2-151">The results are aggregated, so each **DRM\_LICENSE\_STATE\_DATA** structure may contain information from multiple licenses.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2dc2-152">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2dc2-152">Requirements</span></span>



| <span data-ttu-id="c2dc2-153">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2dc2-153">Requirement</span></span> | <span data-ttu-id="c2dc2-154">Wert</span><span class="sxs-lookup"><span data-stu-id="c2dc2-154">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c2dc2-155">Header</span><span class="sxs-lookup"><span data-stu-id="c2dc2-155">Header</span></span><br/>  | <dl> <span data-ttu-id="c2dc2-156"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc2-156"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="c2dc2-157">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c2dc2-157">Library</span></span><br/> | <dl> <span data-ttu-id="c2dc2-158"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="c2dc2-158"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c2dc2-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2dc2-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2dc2-160">**Iwmdrmlicensequery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="c2dc2-160">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> </dl>

 

 





