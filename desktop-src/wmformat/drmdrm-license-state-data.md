---
title: DRM_LICENSE_STATE_DATA Struktur (wmdrmsdk. h)
description: Die Datenstruktur des DRM- \_ Lizenz \_ Zustands \_ enthält Informationen zu den Lizenzbeschränkungen für ein DRM-Recht.
ms.assetid: 822d60ae-5d96-4577-8564-0e1adafa5dd5
keywords:
- DRM_LICENSE_STATE_DATA Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b02f38b8f09b7b444949e9477635e6b8770fc168
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370232"
---
# <a name="drm_license_state_data-structure-wmdrmsdkh"></a><span data-ttu-id="1d818-105">DRM_LICENSE_STATE_DATA Struktur (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="1d818-105">DRM_LICENSE_STATE_DATA structure (Wmdrmsdk.h)</span></span>

<span data-ttu-id="1d818-106">Die **Datenstruktur des DRM- \_ Lizenz \_ Zustands \_** enthält Informationen zu den Lizenzbeschränkungen für ein DRM-Recht.</span><span class="sxs-lookup"><span data-stu-id="1d818-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains information about the license restrictions for a DRM right.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d818-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d818-107">Syntax</span></span>


```C++
typedef struct DRM_LICENSE_STATE_DATA {
  DWORD                      dwStreamId;
  DRM_LICENSE_STATE_CATEGORY dwCategory;
  DWORD                      dwNumCounts;
  DWORD                      dwCount[4];
  DWORD                      dwNumDates;
  FILETIME                   datetime[4];
  DWORD                      dwVague;
} ;
```



## <a name="members"></a><span data-ttu-id="1d818-108">Member</span><span class="sxs-lookup"><span data-stu-id="1d818-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="1d818-109">**dwstreamid**</span><span class="sxs-lookup"><span data-stu-id="1d818-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-110">Die streamnummer, für die die Lizenz gilt.</span><span class="sxs-lookup"><span data-stu-id="1d818-110">Stream number to which the license applies.</span></span> <span data-ttu-id="1d818-111">Muss 0 sein. Dies bedeutet, dass die Lizenz für alle Streams in der Datei gilt.</span><span class="sxs-lookup"><span data-stu-id="1d818-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-112">**dwcategory**</span><span class="sxs-lookup"><span data-stu-id="1d818-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-113">Kategorie der anzuzeigenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1d818-113">Category of string to be displayed.</span></span> <span data-ttu-id="1d818-114">Mögliche Werte und deren Bedeutung finden Sie unter [**DRM- \_ Lizenz \_ Zustands \_ Kategorie**](drmdrm-license-state-category.md) .</span><span class="sxs-lookup"><span data-stu-id="1d818-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drmdrm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-115">**dwnumcounts**</span><span class="sxs-lookup"><span data-stu-id="1d818-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-116">Anzahl der Elemente, die in **dwCount** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d818-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="1d818-117">Dieser Wert ist in der Regel 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="1d818-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="1d818-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-119">Ein Array von 0 oder mindestens einem **DWORD** -Wert, der die Häufigkeit darstellt, mit der die in **dwcategory** angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1d818-119">An array of 0 or 1 or more **DWORD** values that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="1d818-120">Siehe Hinweise.</span><span class="sxs-lookup"><span data-stu-id="1d818-120">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-121">**dwnumdates**</span><span class="sxs-lookup"><span data-stu-id="1d818-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-122">Anzahl der Elemente, die in **DateTime** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d818-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="1d818-123">In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. b. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.</span><span class="sxs-lookup"><span data-stu-id="1d818-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="1d818-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-125">Ein Array aus einer oder mehreren **FILETIME** -Strukturen, die ein oder mehrere Datumsangaben in der Lizenz darstellen.</span><span class="sxs-lookup"><span data-stu-id="1d818-125">An array of one or more **FILETIME** structures representing one or more dates in the license.</span></span> <span data-ttu-id="1d818-126">Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwcategory** ab.</span><span class="sxs-lookup"><span data-stu-id="1d818-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="1d818-127">**dwvague**</span><span class="sxs-lookup"><span data-stu-id="1d818-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="1d818-128">NULL oder mehr der folgenden Flags in Kombination mit einem bitweisen **or**-Operator:</span><span class="sxs-lookup"><span data-stu-id="1d818-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="1d818-129">Flag</span><span class="sxs-lookup"><span data-stu-id="1d818-129">Flag</span></span>                                    | <span data-ttu-id="1d818-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d818-130">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-----------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d818-131">DRM- \_ Lizenz \_ Zustandsdaten sind \_ \_ ungenau</span><span class="sxs-lookup"><span data-stu-id="1d818-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="1d818-132">Wenn diese Einstellung festgelegt ist, sind möglicherweise weitere Lizenzen für den Inhalt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="1d818-132">If set, there may be more licenses that apply to the content.</span></span> <span data-ttu-id="1d818-133">Die einzige Möglichkeit, sich über die einzelnen Lizenzen zu kümmern, die für eine bestimmte Schlüssel-ID gelten, ist die Enumeration der Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="1d818-133">The only way to be certain about the individual licenses that apply to a given key ID is to enumerate the licenses.</span></span> <span data-ttu-id="1d818-134">Um dies zu erreichen, nennen Sie [**iwmdrmlicenaberation:: kreatelicensetup**](iwmdrmlicensemanagement-createlicenseenumeration.md), und übergeben Sie dabei die Schlüssel-ID als bstrinkid-Parameter.</span><span class="sxs-lookup"><span data-stu-id="1d818-134">To do this, call [**IWMDRMLicenseManagement::CreateLicenseEnumeration**](iwmdrmlicensemanagement-createlicenseenumeration.md), passing the key ID as the bstrKID parameter.</span></span> <span data-ttu-id="1d818-135">Verwenden Sie dann die abgerufene iwmdrmlicense-Schnittstelle, um die Lizenzen zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1d818-135">Then use the retrieved IWMDRMLicense interface to examine the licenses.</span></span> |
| <span data-ttu-id="1d818-136">DRM- \_ Lizenz \_ Zustandsdaten- \_ \_ OPL \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="1d818-136">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="1d818-137">Wenn diese Option festgelegt ist, enthält die Lizenz die Ausgabe Schutz Ebenen (opls), die abgerufen und mit dem Ziel der Ausgabe der Anwendung überprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="1d818-137">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span>                                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="1d818-138">DRM- \_ Lizenz \_ Zustands \_ Daten \_ SAP \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="1d818-138">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="1d818-139">Wenn diese Einstellung festgelegt ist, muss der Inhalt über einen sicheren Audiopfad (SAP) zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1d818-139">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                                                                                                                                                                                                                                                                                                   |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d818-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d818-140">Remarks</span></span>

<span data-ttu-id="1d818-141">Diese Struktur wird durch Aufrufen von **iwmdrmlicensequery:: querylicenserstate** abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d818-141">This structure is retrieved by calling **IWMDRMLicenseQuery::QueryLicenseState**.</span></span>

<span data-ttu-id="1d818-142">Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** ist, enthält das **DateTime** -Array in der Regel zwei Datumsangaben: ein "from"-Datum und ein "Until"-Datum.</span><span class="sxs-lookup"><span data-stu-id="1d818-142">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL**, then the **datetime** array will typically contain two dates: a "from" date and an "until" date.</span></span> <span data-ttu-id="1d818-143">Es können auch zwei Datums Paare angegeben werden, um komplexere Lizenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1d818-143">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="1d818-144">Die Elemente des **dwCount** -Arrays entsprechen den Datumsangaben oder Datumsbereichen, die im **DateTime** -Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="1d818-144">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="1d818-145">Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** und **DateTime** ein Datums Paar enthält, enthält **dwCount** ein Element.</span><span class="sxs-lookup"><span data-stu-id="1d818-145">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="1d818-146">Wenn **DateTime** zwei Datums Paare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eine für jedes Datums Paar.</span><span class="sxs-lookup"><span data-stu-id="1d818-146">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="1d818-147">In einigen Fällen haben Benutzer möglicherweise mehr als eine Lizenz für eine Datei ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="1d818-147">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="1d818-148">Beispielsweise könnten Sie eine Lizenz erworben haben, die bis zum Ende des Monats fünf Spiele zulässt und später eine zweite Lizenz für unbegrenzte Rechte erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="1d818-148">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="1d818-149">In einem solchen Fall wird das kennflag für die DRM- \_ Lizenz \_ Zustands \_ Daten \_ in **dwvague** () festgelegt, `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` und die DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu ermitteln, die angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="1d818-149">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="1d818-150">Wenn eine Lizenz abläuft, werden die verbleibenden Lizenzen von der DRM-Komponente untersucht usw., bis alle Lizenzen abgelaufen sind.</span><span class="sxs-lookup"><span data-stu-id="1d818-150">When one license expires, the DRM component will examine the remaining licenses, and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d818-151">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d818-151">Requirements</span></span>



| <span data-ttu-id="1d818-152">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d818-152">Requirement</span></span> | <span data-ttu-id="1d818-153">Wert</span><span class="sxs-lookup"><span data-stu-id="1d818-153">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1d818-154">Header</span><span class="sxs-lookup"><span data-stu-id="1d818-154">Header</span></span><br/> | <dl> <span data-ttu-id="1d818-155"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1d818-155"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d818-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d818-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d818-157">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="1d818-157">**Structures**</span></span>](drm-structures.md)
</dt> </dl>

 

 





