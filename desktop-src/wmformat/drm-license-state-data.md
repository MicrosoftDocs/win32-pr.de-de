---
title: DRM_LICENSE_STATE_DATA Struktur (drmexternals. h)
description: Die DRM- \_ Lizenz \_ Status- \_ Datenstruktur enthält Lizenzinformationen zu einem angegebenen DRM-Recht.
ms.assetid: 5ca577b5-d28b-4e36-8af7-6fae4300d464
keywords:
- DRM_LICENSE_STATE_DATA Struktur-Windows Media-Format
- Struktur des Windows-Medien Formats
topic_type:
- apiref
api_name:
- DRM_LICENSE_STATE_DATA
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3bb63bce02a52aefcf1f3351fe34ab008996aa0b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346514"
---
# <a name="drm_license_state_data-structure-drmexternalsh"></a><span data-ttu-id="fed82-105">DRM_LICENSE_STATE_DATA Struktur (drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="fed82-105">DRM_LICENSE_STATE_DATA structure (Drmexternals.h)</span></span>

<span data-ttu-id="fed82-106">Die **DRM- \_ Lizenz \_ Status- \_ Daten** Struktur enthält [*Lizenz*](wmformat-glossary.md) Informationen zu einem angegebenen [*DRM*](wmformat-glossary.md) -Recht.</span><span class="sxs-lookup"><span data-stu-id="fed82-106">The **DRM\_LICENSE\_STATE\_DATA** structure contains [*license*](wmformat-glossary.md) information about a specified [*DRM*](wmformat-glossary.md) right.</span></span>

## <a name="syntax"></a><span data-ttu-id="fed82-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="fed82-107">Syntax</span></span>


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



## <a name="members"></a><span data-ttu-id="fed82-108">Member</span><span class="sxs-lookup"><span data-stu-id="fed82-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="fed82-109">**dwstreamid**</span><span class="sxs-lookup"><span data-stu-id="fed82-109">**dwStreamId**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-110">Die streamnummer, für die die Lizenz gilt.</span><span class="sxs-lookup"><span data-stu-id="fed82-110">Stream number to which the license applies.</span></span> <span data-ttu-id="fed82-111">Muss 0 sein. Dies bedeutet, dass die Lizenz für alle Streams in der Datei gilt.</span><span class="sxs-lookup"><span data-stu-id="fed82-111">Must be 0, which indicates that the license applies to all streams in the file.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-112">**dwcategory**</span><span class="sxs-lookup"><span data-stu-id="fed82-112">**dwCategory**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-113">Kategorie der anzuzeigenden Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="fed82-113">Category of string to be displayed.</span></span> <span data-ttu-id="fed82-114">Mögliche Werte und deren Bedeutung finden Sie unter [**DRM- \_ Lizenz \_ Zustands \_ Kategorie**](drm-license-state-category.md) .</span><span class="sxs-lookup"><span data-stu-id="fed82-114">See [**DRM\_LICENSE\_STATE\_CATEGORY**](drm-license-state-category.md) for possible values and their meaning.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-115">**dwnumcounts**</span><span class="sxs-lookup"><span data-stu-id="fed82-115">**dwNumCounts**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-116">Anzahl der Elemente, die in **dwCount** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fed82-116">Number of items supplied in **dwCount**.</span></span> <span data-ttu-id="fed82-117">Dieser Wert ist in der Regel 0 oder 1.</span><span class="sxs-lookup"><span data-stu-id="fed82-117">This value is typically 0 or 1.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-118">**dwCount \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="fed82-118">**dwCount\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-119">Ein Array von 0 oder mindestens einem **DWORD**-Wert, der die Häufigkeit darstellt, mit der die in **dwcategory** angegebene Aktion ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="fed82-119">An array of 0 or 1 or more **DWORD** s that represent the number of times the action specified in **dwCategory** may be performed.</span></span> <span data-ttu-id="fed82-120">Siehe Bemerkungen.</span><span class="sxs-lookup"><span data-stu-id="fed82-120">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-121">**dwnumdates**</span><span class="sxs-lookup"><span data-stu-id="fed82-121">**dwNumDates**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-122">Anzahl der Elemente, die in **DateTime** bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fed82-122">Number of items supplied in **datetime**.</span></span> <span data-ttu-id="fed82-123">In der Regel werden nicht mehr als zwei Datumsangaben verwendet, z. b. mit einer Lizenz, die von einem Datum bis zu einem anderen Datum gültig ist.</span><span class="sxs-lookup"><span data-stu-id="fed82-123">Typically no more than two dates are used, for example, with a license that is valid from one date until another date.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-124">**DateTime \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="fed82-124">**datetime\[4\]**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-125">Ein Array aus einer oder mehreren FILETIME-Strukturen, die ein oder mehrere Datumsangaben in der Lizenz darstellen.</span><span class="sxs-lookup"><span data-stu-id="fed82-125">An array of one or more FILETIME structures representing one or more dates in the license.</span></span> <span data-ttu-id="fed82-126">Die Bedeutung eines bestimmten Datums hängt vom Wert von **dwcategory** ab.</span><span class="sxs-lookup"><span data-stu-id="fed82-126">The meaning of a particular date depends on the value of **dwCategory**.</span></span>

</dd> <dt>

<span data-ttu-id="fed82-127">**dwvague**</span><span class="sxs-lookup"><span data-stu-id="fed82-127">**dwVague**</span></span>
</dt> <dd>

<span data-ttu-id="fed82-128">NULL oder mehr der folgenden Flags in Kombination mit einem bitweisen **or**-Operator:</span><span class="sxs-lookup"><span data-stu-id="fed82-128">Zero or more of the following flags combined with a bitwise **OR**:</span></span>



| <span data-ttu-id="fed82-129">Flag</span><span class="sxs-lookup"><span data-stu-id="fed82-129">Flag</span></span>                                    | <span data-ttu-id="fed82-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fed82-130">Description</span></span>                                                                                                                                           |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed82-131">DRM- \_ Lizenz \_ Zustandsdaten sind \_ \_ ungenau</span><span class="sxs-lookup"><span data-stu-id="fed82-131">DRM\_LICENSE\_STATE\_DATA\_VAGUE</span></span>        | <span data-ttu-id="fed82-132">Wenn diese Einstellung festgelegt ist, sind möglicherweise weitere Lizenzen für den Inhalt vorhanden.</span><span class="sxs-lookup"><span data-stu-id="fed82-132">If set, there may be more licenses that apply to the content.</span></span>                                                                                         |
| <span data-ttu-id="fed82-133">DRM- \_ Lizenz \_ Zustandsdaten- \_ \_ OPL \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fed82-133">DRM\_LICENSE\_STATE\_DATA\_OPL\_PRESENT</span></span> | <span data-ttu-id="fed82-134">Wenn diese Option festgelegt ist, enthält die Lizenz die Ausgabe Schutz Ebenen (opls), die abgerufen und mit dem Ziel der Ausgabe der Anwendung überprüft werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fed82-134">If set, the license includes output protection levels (OPLs) that must be retrieved and checked against the destination of your application's output.</span></span> |
| <span data-ttu-id="fed82-135">DRM- \_ Lizenz \_ Zustands \_ Daten \_ SAP \_ vorhanden</span><span class="sxs-lookup"><span data-stu-id="fed82-135">DRM\_LICENSE\_STATE\_DATA\_SAP\_PRESENT</span></span> | <span data-ttu-id="fed82-136">Wenn diese Einstellung festgelegt ist, muss der Inhalt über einen sicheren Audiopfad (SAP) zugestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fed82-136">If set, the content must be delivered using secure audio path (SAP).</span></span>                                                                                  |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fed82-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fed82-137">Remarks</span></span>

<span data-ttu-id="fed82-138">Diese Struktur wird von einem [**callmdrmreader:: getdrmproperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) -Befehl zurückgegeben (in einer [**WM- \_ Lizenz \_ Zustands \_ Daten**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) Struktur gekapselt), wenn Sie eine der DRM-Lizenz Zustands Eigenschaften angeben.</span><span class="sxs-lookup"><span data-stu-id="fed82-138">This structure is returned (encapsulated in a [**WM\_LICENSE\_STATE\_DATA**](/previous-versions/windows/desktop/legacy/dd757942(v=vs.85)) structure) from a call to [**IWMDRMReader::GetDRMProperty**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmreader-getdrmproperty) when you specify one of the DRM license state properties.</span></span> <span data-ttu-id="fed82-139">Diese Eigenschaften sind:</span><span class="sxs-lookup"><span data-stu-id="fed82-139">These properties are:</span></span>

-   [<span data-ttu-id="fed82-140">**DRM- \_ Lizenz Zustands \_ Wiedergabe**</span><span class="sxs-lookup"><span data-stu-id="fed82-140">**DRM\_LicenseState\_Playback**</span></span>](drm-licensestate-playback.md)
-   [<span data-ttu-id="fed82-141">**DRM \_ licenanstate \_ copyper CD**</span><span class="sxs-lookup"><span data-stu-id="fed82-141">**DRM\_LicenseState\_CopyToCD**</span></span>](drm-licensestate-copytocd.md)
-   [<span data-ttu-id="fed82-142">**DRM \_ licenanstate \_ copytosdmidevice**</span><span class="sxs-lookup"><span data-stu-id="fed82-142">**DRM\_LicenseState\_CopyToSDMIDevice**</span></span>](drm-licensestate-copytosdmidevice.md)
-   [<span data-ttu-id="fed82-143">**DRM \_ licenanstate \_ copytononsdmidevice**</span><span class="sxs-lookup"><span data-stu-id="fed82-143">**DRM\_LicenseState\_CopyToNonSDMIDevice**</span></span>](drm-licensestate-copytononsdmidevice.md)
-   [<span data-ttu-id="fed82-144">**DRM \_ licenanstate \_ kollaborativeplay**</span><span class="sxs-lookup"><span data-stu-id="fed82-144">**DRM\_LicenseState\_CollaborativePlay**</span></span>](drm-licensestate-collaborativeplay.md)
-   [<span data-ttu-id="fed82-145">**DRM- \_ Lizenzstatus \_ Kopie**</span><span class="sxs-lookup"><span data-stu-id="fed82-145">**DRM\_LicenseState\_Copy**</span></span>](drm-licensestate-copy.md)
-   [<span data-ttu-id="fed82-146">**DRM \_ licenanstate \_ playlistburn**</span><span class="sxs-lookup"><span data-stu-id="fed82-146">**DRM\_LicenseState\_PlaylistBurn**</span></span>](drm-licensestate-playlistburn.md)

<span data-ttu-id="fed82-147">Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von bis ist \_ ,** enthält das **DateTime** -Array in der Regel zwei Datumsangaben, ein "from"-Datum und ein "Until"-Datum.</span><span class="sxs-lookup"><span data-stu-id="fed82-147">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL,** then the **datetime** array will typically contain two dates, a "from" date and an "until" date.</span></span> <span data-ttu-id="fed82-148">Es können auch zwei Datums Paare angegeben werden, um komplexere Lizenzen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fed82-148">Two date pairs may also be specified to create more complex licenses.</span></span>

<span data-ttu-id="fed82-149">Die Elemente des **dwCount** -Arrays entsprechen den Datumsangaben oder Datumsbereichen, die im **DateTime** -Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="fed82-149">The elements of the **dwCount** array correspond to the dates or date ranges specified in the **datetime** array.</span></span> <span data-ttu-id="fed82-150">Wenn **dwcategory** eine **WM- \_ DRM- \_ Lizenz \_ Status \_ Anzahl \_ von \_ bis** und **DateTime** ein Datums Paar enthält, enthält **dwCount** ein Element.</span><span class="sxs-lookup"><span data-stu-id="fed82-150">If **dwCategory** is **WM\_DRM\_LICENSE\_STATE\_COUNT\_FROM\_UNTIL** and **datetime** contains one pair of dates, then **dwCount** will contain one element.</span></span> <span data-ttu-id="fed82-151">Wenn **DateTime** zwei Datums Paare (vier Elemente) enthält, sollte **dwCount** zwei Elemente enthalten, eine für jedes Datums Paar.</span><span class="sxs-lookup"><span data-stu-id="fed82-151">If **datetime** contains two date pairs (four elements), then **dwCount** should contain two elements, one for each date pair.</span></span>

<span data-ttu-id="fed82-152">In einigen Fällen haben Benutzer möglicherweise mehr als eine Lizenz für eine Datei ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="fed82-152">In some cases, users may have been issued more than one license for a file.</span></span> <span data-ttu-id="fed82-153">Beispielsweise könnten Sie eine Lizenz erworben haben, die bis zum Ende des Monats fünf Spiele zulässt und später eine zweite Lizenz für unbegrenzte Rechte erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="fed82-153">For example, they might have acquired a license that allowed five plays until the end of the month, and later acquired a second license for unlimited rights.</span></span> <span data-ttu-id="fed82-154">In einem solchen Fall wird das kennflag für die DRM- \_ Lizenz \_ Zustands \_ Daten \_ in **dwvague** () festgelegt, `dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0` und die DRM-Komponente verwendet einen Algorithmus, um den wahrscheinlichsten Satz von Rechten zu ermitteln, die angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="fed82-154">In such a case, the DRM\_LICENSE\_STATE\_DATA\_VAGUE flag is set in **dwVague** (`dwVague & DRM_LICENSE_STATE_DATA_VAGUE != 0`) and the DRM component will use an algorithm to determine the most likely set of rights that have been applied.</span></span> <span data-ttu-id="fed82-155">Wenn eine Lizenz abläuft, untersucht die DRM-Komponente die verbleibenden Lizenzen usw., bis alle Lizenzen abgelaufen sind.</span><span class="sxs-lookup"><span data-stu-id="fed82-155">When one license expires, the DRM component will examine the remaining license(s), and so on until all licenses have expired.</span></span>

## <a name="requirements"></a><span data-ttu-id="fed82-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fed82-156">Requirements</span></span>



| <span data-ttu-id="fed82-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fed82-157">Requirement</span></span> | <span data-ttu-id="fed82-158">Wert</span><span class="sxs-lookup"><span data-stu-id="fed82-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="fed82-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fed82-159">Minimum supported client</span></span><br/> | <span data-ttu-id="fed82-160">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fed82-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="fed82-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fed82-161">Minimum supported server</span></span><br/> | <span data-ttu-id="fed82-162">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fed82-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="fed82-163">Version</span><span class="sxs-lookup"><span data-stu-id="fed82-163">Version</span></span><br/>                  | <span data-ttu-id="fed82-164">SDK für Windows Media-Format 7 oder höhere Versionen des SDKs</span><span class="sxs-lookup"><span data-stu-id="fed82-164">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="fed82-165">Header</span><span class="sxs-lookup"><span data-stu-id="fed82-165">Header</span></span><br/>                   | <dl> <span data-ttu-id="fed82-166"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="fed82-166"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fed82-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fed82-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fed82-168">**Strukturen**</span><span class="sxs-lookup"><span data-stu-id="fed82-168">**Structures**</span></span>](structures.md)
</dt> </dl>

 

