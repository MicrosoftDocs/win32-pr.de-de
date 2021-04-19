---
description: Die Property-Eigenschaft des SummaryInfo-Objekts legt den Wert für die angegebene Eigenschaft im Zusammenfassungs Informationsdaten Strom fest oder ruft diesen ab.
ms.assetid: 8e8f0987-c92b-43f3-a61a-35099188c629
title: SummaryInfo. Property (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 0e51773a930b8868e31a7e88848300a62b717912
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354135"
---
# <a name="summaryinfoproperty-property"></a><span data-ttu-id="098a6-103">SummaryInfo. Property (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="098a6-103">SummaryInfo.Property property</span></span>

<span data-ttu-id="098a6-104">Die **Property** -Eigenschaft des [**SummaryInfo**](summaryinfo-object.md) -Objekts legt den Wert für die angegebene Eigenschaft im Zusammenfassungs Informationsdaten Strom fest oder ruft diesen ab.</span><span class="sxs-lookup"><span data-stu-id="098a6-104">The **Property** property of the [**SummaryInfo**](summaryinfo-object.md) object sets or gets the value for the specified property in the summary information stream.</span></span> <span data-ttu-id="098a6-105">Die Eigenschaften werden gelesen, wenn das [**SummaryInfo**](summaryinfo-object.md) -Objekt erstellt wird, aber Sie werden erst geschrieben, wenn die [**Persistenzmethode**](summaryinfo-persist.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="098a6-105">The properties are read when the [**SummaryInfo**](summaryinfo-object.md) object is created, but they are not written until the [**Persist**](summaryinfo-persist.md) method is called.</span></span> <span data-ttu-id="098a6-106">Das Festlegen einer Eigenschaft auf "leer" bewirkt, dass entfernt wird. Ebenso gibt das Anfordern einer nicht vorhandenen Eigenschaft einen leeren Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="098a6-106">Setting a property to Empty causes its removal; likewise, requesting a nonexistent property returns an Empty value.</span></span> <span data-ttu-id="098a6-107">Andernfalls können Werte als Zeichen folgen, ganze Zahlen oder Datums-/Uhrzeittypen übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="098a6-107">Otherwise values may be transferred as strings, integers, or date (date time) types.</span></span>

<span data-ttu-id="098a6-108">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="098a6-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="098a6-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="098a6-109">Syntax</span></span>


```JScript
propVal = SummaryInfo.Property
```



## <a name="property-value"></a><span data-ttu-id="098a6-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="098a6-110">Property value</span></span>

<span data-ttu-id="098a6-111">Erforderliche eigen schafts-ID einer der Zusammenfassungs Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="098a6-111">Required property ID of one of the summary properties.</span></span>

## <a name="remarks"></a><span data-ttu-id="098a6-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="098a6-112">Remarks</span></span>

<span data-ttu-id="098a6-113">**Standard mäßige Zusammenfassungs Eigenschaften-IDs**</span><span class="sxs-lookup"><span data-stu-id="098a6-113">**Standard Summary Property IDs**</span></span>

<span data-ttu-id="098a6-114">(keine Enumeration)</span><span class="sxs-lookup"><span data-stu-id="098a6-114">(not an enumeration)</span></span>



| <span data-ttu-id="098a6-115">Parametername</span><span class="sxs-lookup"><span data-stu-id="098a6-115">Parameter name</span></span>     | <span data-ttu-id="098a6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="098a6-116">Value</span></span> | <span data-ttu-id="098a6-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="098a6-117">Description</span></span>                                       |
|--------------------|-------|---------------------------------------------------|
| <span data-ttu-id="098a6-118">PID- \_ Wörterbuch</span><span class="sxs-lookup"><span data-stu-id="098a6-118">PID\_DICTIONARY</span></span>    | <span data-ttu-id="098a6-119">0</span><span class="sxs-lookup"><span data-stu-id="098a6-119">0</span></span>     | <span data-ttu-id="098a6-120">Sonderformat, nicht Unterstützung durch das SummaryInfo-Objekt</span><span class="sxs-lookup"><span data-stu-id="098a6-120">Special format, not support by SummaryInfo object</span></span> |
| <span data-ttu-id="098a6-121">PID- \_ Codepage</span><span class="sxs-lookup"><span data-stu-id="098a6-121">PID\_CODEPAGE</span></span>      | <span data-ttu-id="098a6-122">1</span><span class="sxs-lookup"><span data-stu-id="098a6-122">1</span></span>     | <span data-ttu-id="098a6-123">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="098a6-123">VT\_I2</span></span>                                            |
| <span data-ttu-id="098a6-124">PID- \_ Titel</span><span class="sxs-lookup"><span data-stu-id="098a6-124">PID\_TITLE</span></span>         | <span data-ttu-id="098a6-125">2</span><span class="sxs-lookup"><span data-stu-id="098a6-125">2</span></span>     | <span data-ttu-id="098a6-126">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-126">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-127">PID- \_ Betreff</span><span class="sxs-lookup"><span data-stu-id="098a6-127">PID\_SUBJECT</span></span>       | <span data-ttu-id="098a6-128">3</span><span class="sxs-lookup"><span data-stu-id="098a6-128">3</span></span>     | <span data-ttu-id="098a6-129">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-129">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-130">PID- \_ Autor</span><span class="sxs-lookup"><span data-stu-id="098a6-130">PID\_AUTHOR</span></span>        | <span data-ttu-id="098a6-131">4</span><span class="sxs-lookup"><span data-stu-id="098a6-131">4</span></span>     | <span data-ttu-id="098a6-132">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-132">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-133">PID- \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="098a6-133">PID\_KEYWORDS</span></span>      | <span data-ttu-id="098a6-134">5</span><span class="sxs-lookup"><span data-stu-id="098a6-134">5</span></span>     | <span data-ttu-id="098a6-135">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-135">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-136">PID- \_ Kommentare</span><span class="sxs-lookup"><span data-stu-id="098a6-136">PID\_COMMENTS</span></span>      | <span data-ttu-id="098a6-137">6</span><span class="sxs-lookup"><span data-stu-id="098a6-137">6</span></span>     | <span data-ttu-id="098a6-138">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-138">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-139">PID- \_ Vorlage</span><span class="sxs-lookup"><span data-stu-id="098a6-139">PID\_TEMPLATE</span></span>      | <span data-ttu-id="098a6-140">7</span><span class="sxs-lookup"><span data-stu-id="098a6-140">7</span></span>     | <span data-ttu-id="098a6-141">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-141">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-142">PID \_ lastauthor</span><span class="sxs-lookup"><span data-stu-id="098a6-142">PID\_LASTAUTHOR</span></span>    | <span data-ttu-id="098a6-143">8</span><span class="sxs-lookup"><span data-stu-id="098a6-143">8</span></span>     | <span data-ttu-id="098a6-144">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-144">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-145">PID- \_ revnumber</span><span class="sxs-lookup"><span data-stu-id="098a6-145">PID\_REVNUMBER</span></span>     | <span data-ttu-id="098a6-146">9</span><span class="sxs-lookup"><span data-stu-id="098a6-146">9</span></span>     | <span data-ttu-id="098a6-147">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-147">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-148">PID- \_ EditTime</span><span class="sxs-lookup"><span data-stu-id="098a6-148">PID\_EDITTIME</span></span>      | <span data-ttu-id="098a6-149">10</span><span class="sxs-lookup"><span data-stu-id="098a6-149">10</span></span>    | <span data-ttu-id="098a6-150">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="098a6-150">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="098a6-151">PID \_ lastprint</span><span class="sxs-lookup"><span data-stu-id="098a6-151">PID\_LASTPRINTED</span></span>   | <span data-ttu-id="098a6-152">11</span><span class="sxs-lookup"><span data-stu-id="098a6-152">11</span></span>    | <span data-ttu-id="098a6-153">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="098a6-153">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="098a6-154">PID \_ Erstellen von \_ DTM</span><span class="sxs-lookup"><span data-stu-id="098a6-154">PID\_CREATE\_DTM</span></span>   | <span data-ttu-id="098a6-155">12</span><span class="sxs-lookup"><span data-stu-id="098a6-155">12</span></span>    | <span data-ttu-id="098a6-156">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="098a6-156">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="098a6-157">PID \_ lastsave \_ DTM</span><span class="sxs-lookup"><span data-stu-id="098a6-157">PID\_LASTSAVE\_DTM</span></span> | <span data-ttu-id="098a6-158">13</span><span class="sxs-lookup"><span data-stu-id="098a6-158">13</span></span>    | <span data-ttu-id="098a6-159">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="098a6-159">VT\_FILETIME</span></span>                                      |
| <span data-ttu-id="098a6-160">PID- \_ PageCount</span><span class="sxs-lookup"><span data-stu-id="098a6-160">PID\_PAGECOUNT</span></span>     | <span data-ttu-id="098a6-161">14</span><span class="sxs-lookup"><span data-stu-id="098a6-161">14</span></span>    | <span data-ttu-id="098a6-162">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="098a6-162">VT\_I4</span></span>                                            |
| <span data-ttu-id="098a6-163">PID- \_ WordCount</span><span class="sxs-lookup"><span data-stu-id="098a6-163">PID\_WORDCOUNT</span></span>     | <span data-ttu-id="098a6-164">15</span><span class="sxs-lookup"><span data-stu-id="098a6-164">15</span></span>    | <span data-ttu-id="098a6-165">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="098a6-165">VT\_I4</span></span>                                            |
| <span data-ttu-id="098a6-166">PID- \_ Anzahl</span><span class="sxs-lookup"><span data-stu-id="098a6-166">PID\_CHARCOUNT</span></span>     | <span data-ttu-id="098a6-167">16</span><span class="sxs-lookup"><span data-stu-id="098a6-167">16</span></span>    | <span data-ttu-id="098a6-168">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="098a6-168">VT\_I4</span></span>                                            |
| <span data-ttu-id="098a6-169">PID- \_ Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="098a6-169">PID\_THUMBNAIL</span></span>     | <span data-ttu-id="098a6-170">17</span><span class="sxs-lookup"><span data-stu-id="098a6-170">17</span></span>    | <span data-ttu-id="098a6-171">VT \_ CF (nicht unterstützt)</span><span class="sxs-lookup"><span data-stu-id="098a6-171">VT\_CF (not supported)</span></span>                            |
| <span data-ttu-id="098a6-172">PID- \_ appname</span><span class="sxs-lookup"><span data-stu-id="098a6-172">PID\_APPNAME</span></span>       | <span data-ttu-id="098a6-173">18</span><span class="sxs-lookup"><span data-stu-id="098a6-173">18</span></span>    | <span data-ttu-id="098a6-174">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-174">VT\_LPSTR</span></span>                                         |
| <span data-ttu-id="098a6-175">PID- \_ Sicherheit</span><span class="sxs-lookup"><span data-stu-id="098a6-175">PID\_SECURITY</span></span>      | <span data-ttu-id="098a6-176">19</span><span class="sxs-lookup"><span data-stu-id="098a6-176">19</span></span>    | <span data-ttu-id="098a6-177">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="098a6-177">VT\_I4</span></span>                                            |



 

<span data-ttu-id="098a6-178">**Datentypen von Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="098a6-178">**Property Data Types**</span></span>

<span data-ttu-id="098a6-179">(keine Enumeration)</span><span class="sxs-lookup"><span data-stu-id="098a6-179">(not an enumeration)</span></span>



| <span data-ttu-id="098a6-180">Parametername</span><span class="sxs-lookup"><span data-stu-id="098a6-180">Parameter name</span></span> | <span data-ttu-id="098a6-181">Wert</span><span class="sxs-lookup"><span data-stu-id="098a6-181">Value</span></span> | <span data-ttu-id="098a6-182">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="098a6-182">Description</span></span>                                                                              |
|----------------|-------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="098a6-183">VT \_ I2</span><span class="sxs-lookup"><span data-stu-id="098a6-183">VT\_I2</span></span>         | <span data-ttu-id="098a6-184">2</span><span class="sxs-lookup"><span data-stu-id="098a6-184">2</span></span>     | <span data-ttu-id="098a6-185">16-Bit-Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="098a6-185">16-bit integer</span></span>                                                                           |
| <span data-ttu-id="098a6-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="098a6-186">VT\_I4</span></span>         | <span data-ttu-id="098a6-187">3</span><span class="sxs-lookup"><span data-stu-id="098a6-187">3</span></span>     | <span data-ttu-id="098a6-188">32-bit integer</span><span class="sxs-lookup"><span data-stu-id="098a6-188">32-bit integer</span></span>                                                                           |
| <span data-ttu-id="098a6-189">VT \_ LPSTR</span><span class="sxs-lookup"><span data-stu-id="098a6-189">VT\_LPSTR</span></span>      | <span data-ttu-id="098a6-190">30</span><span class="sxs-lookup"><span data-stu-id="098a6-190">30</span></span>    | <span data-ttu-id="098a6-191">String</span><span class="sxs-lookup"><span data-stu-id="098a6-191">String</span></span>                                                                                   |
| <span data-ttu-id="098a6-192">VT \_ FILETIME</span><span class="sxs-lookup"><span data-stu-id="098a6-192">VT\_FILETIME</span></span>   | <span data-ttu-id="098a6-193">64</span><span class="sxs-lookup"><span data-stu-id="098a6-193">64</span></span>    | <span data-ttu-id="098a6-194">Datum/Uhrzeit (FILETIME, konvertiert in Variant-Zeit)</span><span class="sxs-lookup"><span data-stu-id="098a6-194">Date time (FILETIME, converted to Variant time)</span></span>                                          |
| <span data-ttu-id="098a6-195">VT \_ CF</span><span class="sxs-lookup"><span data-stu-id="098a6-195">VT\_CF</span></span>         | <span data-ttu-id="098a6-196">71</span><span class="sxs-lookup"><span data-stu-id="098a6-196">71</span></span>    | <span data-ttu-id="098a6-197">Zwischenablage Format + Daten, nicht vom [**SummaryInfo**](summaryinfo-object.md) -Objekt behandelt</span><span class="sxs-lookup"><span data-stu-id="098a6-197">Clipboard format + data, not handled by [**SummaryInfo**](summaryinfo-object.md) object</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="098a6-198">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="098a6-198">Requirements</span></span>



| <span data-ttu-id="098a6-199">Anforderung</span><span class="sxs-lookup"><span data-stu-id="098a6-199">Requirement</span></span> | <span data-ttu-id="098a6-200">Wert</span><span class="sxs-lookup"><span data-stu-id="098a6-200">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="098a6-201">Version</span><span class="sxs-lookup"><span data-stu-id="098a6-201">Version</span></span><br/> | <span data-ttu-id="098a6-202">Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7.</span><span class="sxs-lookup"><span data-stu-id="098a6-202">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="098a6-203">Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="098a6-203">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="098a6-204">Windows Installer unter Windows Server 2003 oder Windows XP</span><span class="sxs-lookup"><span data-stu-id="098a6-204">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="098a6-205">DLL</span><span class="sxs-lookup"><span data-stu-id="098a6-205">DLL</span></span><br/>     | <dl> <span data-ttu-id="098a6-206"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="098a6-206"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="098a6-207">IID</span><span class="sxs-lookup"><span data-stu-id="098a6-207">IID</span></span><br/>     | <span data-ttu-id="098a6-208">IID \_ isummaryinfo ist definiert als 000c109b-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="098a6-208">IID\_ISummaryInfo is defined as 000C109B-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="098a6-209">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="098a6-209">See also</span></span>

<dl> <dt>

[<span data-ttu-id="098a6-210">**Msisummaryinfosetproperty**</span><span class="sxs-lookup"><span data-stu-id="098a6-210">**MsiSummaryInfoSetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfosetpropertya)
</dt> <dt>

[<span data-ttu-id="098a6-211">**Msisummaryinfogetproperty**</span><span class="sxs-lookup"><span data-stu-id="098a6-211">**MsiSummaryInfoGetProperty**</span></span>](/windows/desktop/api/Msiquery/nf-msiquery-msisummaryinfogetpropertya)
</dt> </dl>

 

 




