---
title: Iwmdrmlicensequery queryaktionallowed-Methode (wmdrmsdk. h)
description: Die queryaktionallowed-Methode führt eine Abfrage für den lokalen Lizenz Speicher aus, um den Lizenzstatus für mindestens eine DRM-Aktion abzurufen, die auf eine angegebene Schlüssel-ID angewendet wird.
ms.assetid: 814c2850-c036-4c44-a64e-861e88f16fb1
keywords:
- Queryaktionallowed-Methode Windows Media-Format
- Queryaktionallowed-Methode, Windows Media-Format, iwmdrmlicensequery-Schnittstelle
- Iwmdrmlicensequery-Schnittstelle Windows Media-Format, queryaktionallowed-Methode
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery.QueryActionAllowed
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6564062fc9f76a840b37f6e134e960480d67a2ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358137"
---
# <a name="iwmdrmlicensequeryqueryactionallowed-method"></a><span data-ttu-id="0c579-106">Iwmdrmlicensequery:: queryaktionallowed-Methode</span><span class="sxs-lookup"><span data-stu-id="0c579-106">IWMDRMLicenseQuery::QueryActionAllowed method</span></span>

<span data-ttu-id="0c579-107">Die **queryaktionallowed** -Methode führt eine Abfrage für den lokalen Lizenz Speicher aus, um den Lizenzstatus für mindestens eine DRM-Aktion abzurufen, die auf eine angegebene Schlüssel-ID angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0c579-107">The **QueryActionAllowed** method performs a query on the local license store to retrieve the license status for one or more DRM actions that apply to a specified Key ID.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c579-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c579-108">Syntax</span></span>


```C++
HRESULT QueryActionAllowed(
  [in]  BSTR  bstrKID,
  [in]  BSTR  bstrMinReqIndivVersion,
  [in]  DWORD cActionsToQuery,
  [in]  BSTR  rgbstrActionsToQuery[],
  [out] DWORD rgdwQueryResult[]
);
```



## <a name="parameters"></a><span data-ttu-id="0c579-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c579-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c579-110">*bstrinkid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c579-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c579-111">Die Schlüssel-ID, für die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c579-111">Key ID for which to query.</span></span> <span data-ttu-id="0c579-112">Nur Lizenzen, die auf diese Schlüssel-ID zutreffen, werden ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="0c579-112">Only licenses that apply to this Key ID will be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="0c579-113">*bstrauminreqindivversion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c579-113">*bstrMinReqIndivVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c579-114">Die minimale Sicherheitsversion, die im-Header der ASF-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0c579-114">The minimum security version specified in the header of the ASF file.</span></span> <span data-ttu-id="0c579-115">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="0c579-115">This parameter is optional.</span></span> <span data-ttu-id="0c579-116">Übergeben Sie **null** , um die Abfrage ohne diese Informationen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0c579-116">Pass **NULL** to perform the query without this information.</span></span>

</dd> <dt>

<span data-ttu-id="0c579-117">*cactionstoquery* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0c579-117">*cActionsToQuery* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c579-118">Die Anzahl der Aktionen, für die abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c579-118">The number of actions for which to query.</span></span> <span data-ttu-id="0c579-119">Dieser Wert muss auf die Anzahl der Elemente in den Arrays festgelegt werden, die für die Parameter *rgbstractionstoquery* und *rgdwqueryresult* übersprungen werden.</span><span class="sxs-lookup"><span data-stu-id="0c579-119">This value must be set to the number of elements in the arrays passed for the *rgbstrActionsToQuery* and *rgdwQueryResult* parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0c579-120">*rgbstractionstoquery \[ \]* \[in\]</span><span class="sxs-lookup"><span data-stu-id="0c579-120">*rgbstrActionsToQuery\[\]* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0c579-121">Ein Array von mindestens einem Recht, für das abgefragt werden soll.</span><span class="sxs-lookup"><span data-stu-id="0c579-121">Array of one or more rights for which to query.</span></span> <span data-ttu-id="0c579-122">Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c579-122">This array must contain as many elements as specified by *cActionsToQuery*.</span></span> <span data-ttu-id="0c579-123">Jedes Element muss auf eine der folgenden Konstanten festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0c579-123">Each element must be set to one of the following constants:</span></span>



| <span data-ttu-id="0c579-124">Konstante</span><span class="sxs-lookup"><span data-stu-id="0c579-124">Constant</span></span>                                         | <span data-ttu-id="0c579-125">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0c579-125">Description</span></span>                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0c579-126">g \_ wszwmdrm- \_ Wiedergabe, Aktions zulässig \_</span><span class="sxs-lookup"><span data-stu-id="0c579-126">g\_wszWMDRM\_ActionAllowed\_Playback</span></span>             | <span data-ttu-id="0c579-127">Einschließen, um das Recht zum Wiedergeben des Inhalts abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0c579-127">Include to query for the right to play the content.</span></span>                              |
| <span data-ttu-id="0c579-128">g \_ wszwmdrm- \_ Aktions zulässige \_ Kopie</span><span class="sxs-lookup"><span data-stu-id="0c579-128">g\_wszWMDRM\_ActionAllowed\_Copy</span></span>                 | <span data-ttu-id="0c579-129">Schließen Sie ein, um das Recht zum Kopieren des Inhalts auf externe Geräte oder Medien zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="0c579-129">Include to query for the right to copy the content to external devices or media.</span></span> |
| <span data-ttu-id="0c579-130">g \_ wszwmdrm \_ Action Allowed \_ playlistburn</span><span class="sxs-lookup"><span data-stu-id="0c579-130">g\_wszWMDRM\_ActionAllowed\_PlaylistBurn</span></span>         | <span data-ttu-id="0c579-131">Schließen Sie ein, um das Recht zum Kopieren des Inhalts als Teil einer Wiedergabeliste auf CD zu Fragen.</span><span class="sxs-lookup"><span data-stu-id="0c579-131">Include to query for the right to copy the content to CD as part of a playlist.</span></span>  |
| <span data-ttu-id="0c579-132">g \_ wszwmdrm- \_ Aktions zulässig ( \_ "") "".</span><span class="sxs-lookup"><span data-stu-id="0c579-132">g\_wszWMDRM\_ActionAllowed\_CreateThumbnailImage</span></span> | <span data-ttu-id="0c579-133">Schließen Sie zum Abfragen der Berechtigung ein, um ein Miniaturbild aus dem Inhalt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0c579-133">Include to query for the right to create a thumbnail image from the content.</span></span>     |
| <span data-ttu-id="0c579-134">g \_ wszwmdrm- \_ Aktions zulässige \_ copyper-CD</span><span class="sxs-lookup"><span data-stu-id="0c579-134">g\_wszWMDRM\_ActionAllowed\_CopyToCD</span></span>             | <span data-ttu-id="0c579-135">Schließen Sie ein, um das Recht zum Kopieren des Inhalts auf die CD abzufragen.</span><span class="sxs-lookup"><span data-stu-id="0c579-135">Include to query for the right to copy the content to CD.</span></span>                        |



 

</dd> <dt>

<span data-ttu-id="0c579-136">*rgdwqueryresult \[ \]* \[out\]</span><span class="sxs-lookup"><span data-stu-id="0c579-136">*rgdwQueryResult\[\]* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0c579-137">Ein Array von mindestens einer DWORD-Variablen, die die Ergebnisse der Abfrage für die durch *rgbstractionstoquery* angegebenen Rechte empfangen.</span><span class="sxs-lookup"><span data-stu-id="0c579-137">Array of one or more DWORD variables that receive the results of the query for the rights specified by *rgbstrActionsToQuery*.</span></span> <span data-ttu-id="0c579-138">Wenn eine Aktion zulässig ist, wird das entsprechende Element auf 0 (null) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c579-138">If an action is allowed, the corresponding element is set to zero.</span></span> <span data-ttu-id="0c579-139">Wenn eine Aktion unzulässig ist, wird das-Element auf einen oder mehrere Werte der DRM- [**\_ Aktion \_ zulässige \_ Abfrage \_ Ergebnis**](drm-action-allowed-query-results.md) Enumeration in Kombination mit dem bitweisen OR-Vorgang festgelegt.</span><span class="sxs-lookup"><span data-stu-id="0c579-139">If an action is not allowed, the element is set to one or more values of the [**DRM\_ACTION\_ALLOWED\_QUERY\_RESULTS**](drm-action-allowed-query-results.md) enumeration combined by using the bitwise OR operation.</span></span> <span data-ttu-id="0c579-140">Dieses Array muss beliebig viele Elemente enthalten, die von *cactionstoquery* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0c579-140">This array must contain as many elements as specified by *cActionsToQuery*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c579-141">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c579-141">Return value</span></span>

<span data-ttu-id="0c579-142">Die-Methode gibt ein **HRESULT** zurück.</span><span class="sxs-lookup"><span data-stu-id="0c579-142">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0c579-143">Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0c579-143">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0c579-144">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="0c579-144">Return code</span></span>                                                                          | <span data-ttu-id="0c579-145">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c579-145">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="0c579-146"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0c579-146"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="0c579-147">Die Methode wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0c579-147">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0c579-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c579-148">Remarks</span></span>

<span data-ttu-id="0c579-149">Beim Abfragen von Wiedergabe-und Kopier rechten erhalten Sie genauere Ergebnisse, indem Sie zuerst die Umgebungsparameter festlegen.</span><span class="sxs-lookup"><span data-stu-id="0c579-149">When querying for play and copy rights, you will get more accurate results by first setting environmental parameters.</span></span> <span data-ttu-id="0c579-150">Legen Sie die Umgebungsparameter mit der [**setactionzugewiesene wedqueryparams**](iwmdrmlicensequery-setactionallowedqueryparams.md) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="0c579-150">Use the [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) method to set the environmental parameters.</span></span> <span data-ttu-id="0c579-151">Die Ergebnisse von Abfragen für das Brennrecht sind von den Umgebungs Parametern nicht betroffen. Sie können die Standardeinstellungen sicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="0c579-151">The results of queries for the burn right are unaffected by the environmental parameters; you can safely use the defaults.</span></span>

<span data-ttu-id="0c579-152">Die von der **queryaktionallowed** -Methode zurückgegebenen Ergebnisse werden von 0 (null) oder mehr Lizenzen im lokalen Lizenz Speicher aggregiert.</span><span class="sxs-lookup"><span data-stu-id="0c579-152">The results returned by the **QueryActionAllowed** method are aggregated from zero or more licenses in the local license store.</span></span> <span data-ttu-id="0c579-153">Die-Methode durchsucht möglicherweise nicht alle Lizenzen, die für die Schlüssel-ID gelten, wenn Sie auf ein aktiviertes Ergebnis stößt.</span><span class="sxs-lookup"><span data-stu-id="0c579-153">The method may not search all of the licenses that apply to the Key ID if it encounters an enabled result.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c579-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c579-154">Requirements</span></span>



| <span data-ttu-id="0c579-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c579-155">Requirement</span></span> | <span data-ttu-id="0c579-156">Wert</span><span class="sxs-lookup"><span data-stu-id="0c579-156">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0c579-157">Header</span><span class="sxs-lookup"><span data-stu-id="0c579-157">Header</span></span><br/>  | <dl> <span data-ttu-id="0c579-158"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c579-158"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="0c579-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c579-159">Library</span></span><br/> | <dl> <span data-ttu-id="0c579-160"><dt>Wmdrmsdk. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0c579-160"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c579-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c579-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c579-162">**Iwmdrmlicensequery-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="0c579-162">**IWMDRMLicenseQuery Interface**</span></span>](iwmdrmlicensequery.md)
</dt> <dt>

[<span data-ttu-id="0c579-163">**Abfragen von einfachen Rechte Informationen**</span><span class="sxs-lookup"><span data-stu-id="0c579-163">**Querying for Simple Rights Information**</span></span>](querying-for-simple-rights-information.md)
</dt> </dl>

 

 





