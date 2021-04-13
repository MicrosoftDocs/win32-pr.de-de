---
description: Renderingfehler
ms.assetid: 8901eb78-bb7f-4dfe-bc01-0a267af5140f
title: Renderingfehler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e106a55363bf50e49a4966600662e26b03b53307
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482235"
---
# <a name="rendering-errors"></a><span data-ttu-id="c1591-103">Renderingfehler</span><span class="sxs-lookup"><span data-stu-id="c1591-103">Rendering Errors</span></span>

> [!Note]  
> <span data-ttu-id="c1591-104">\[Veraltet.</span><span class="sxs-lookup"><span data-stu-id="c1591-104">\[Deprecated.</span></span> <span data-ttu-id="c1591-105">Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]</span><span class="sxs-lookup"><span data-stu-id="c1591-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="c1591-106">Microsoft® DirectShow® Bearbeitungs Dienste (des) definiert verschiedene Fehlercodes, die zum Protokollieren von renderingfehlern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1591-106">Microsoft® DirectShow® Editing Services (DES) defines various error codes used to log rendering errors.</span></span> <span data-ttu-id="c1591-107">Wenn ein Projekt nicht ordnungsgemäß gerengt wird, ruft die Renderingengine die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="c1591-107">If a project does not render correctly, the render engine calls the [**IAMErrorLog::LogError**](iamerrorlog-logerror.md) method.</span></span> <span data-ttu-id="c1591-108">In der folgenden Tabelle werden die Parameter von **LogError** zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="c1591-108">The following table summarizes the parameters given to **LogError**:</span></span>

-   <span data-ttu-id="c1591-109">Der Fehlercode ist im *errorCode* -Parameter enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1591-109">The error code is contained in the *ErrorCode* parameter.</span></span>
-   <span data-ttu-id="c1591-110">Die Beschreibung ist im Parameter ErrorString enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1591-110">The description is contained in the ErrorString parameter.</span></span>
-   <span data-ttu-id="c1591-111">Die Beschreibung ist im Parameter *ErrorString* enthalten.</span><span class="sxs-lookup"><span data-stu-id="c1591-111">The description is contained in the *ErrorString* parameter.</span></span>
-   <span data-ttu-id="c1591-112">Wenn zusätzliche Informationen vorliegen, ist der **Variant** -Typ im **VT** -Member der **Variante** enthalten, auf die von *pextrainfo* verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c1591-112">If there is extra information, the **VARIANT** type is contained in the **vt** member of the **VARIANT** pointed to by *pExtraInfo*.</span></span>

> [!Note]  
> <span data-ttu-id="c1591-113">Die hier beschriebenen Fehlercodes sind keine **HRESULT** -Werte.</span><span class="sxs-lookup"><span data-stu-id="c1591-113">The error codes described here are not **HRESULT** values.</span></span> <span data-ttu-id="c1591-114">Eine Liste der **HRESULT** -Rückgabewerte, die für des spezifisch sind, finden Sie unter [Fehler-und Erfolgs Codes](error-and-success-codes.md).</span><span class="sxs-lookup"><span data-stu-id="c1591-114">For a list of **HRESULT** return values specific to DES, see [Error and Success Codes](error-and-success-codes.md).</span></span>

 



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c1591-115">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="c1591-115">Error code</span></span></th>
<th><span data-ttu-id="c1591-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1591-116">Description</span></span></th>
<th><span data-ttu-id="c1591-117">Zusätzliche Informationen</span><span class="sxs-lookup"><span data-stu-id="c1591-117">Extra information</span></span></th>
<th><span data-ttu-id="c1591-118">Varianttyp</span><span class="sxs-lookup"><span data-stu-id="c1591-118">Variant type</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c1591-119">DEX_IDS_BAD_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="c1591-119">DEX_IDS_BAD_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="c1591-120">Der Dateiname ist nicht vorhanden, oder die Dateierweiterung wird nicht von DirectShow erkannt.</span><span class="sxs-lookup"><span data-stu-id="c1591-120">File name doesn't exist, or DirectShow doesn't recognize the file extension.</span></span></td>
<td><span data-ttu-id="c1591-121">Dateiname</span><span class="sxs-lookup"><span data-stu-id="c1591-121">File name</span></span></td>
<td><span data-ttu-id="c1591-122"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-122"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-123">DEX_IDS_BAD_SOURCE_NAME2</span><span class="sxs-lookup"><span data-stu-id="c1591-123">DEX_IDS_BAD_SOURCE_NAME2</span></span></td>
<td><span data-ttu-id="c1591-124">Der Dateityp entspricht nicht der Dateierweiterung, oder die Datei ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c1591-124">File type does not match the file extension or the file is corrupt.</span></span></td>
<td><span data-ttu-id="c1591-125">Dateiname</span><span class="sxs-lookup"><span data-stu-id="c1591-125">File name</span></span></td>
<td><span data-ttu-id="c1591-126"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-126"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-127">DEX_IDS_MISSING_SOURCE_NAME</span><span class="sxs-lookup"><span data-stu-id="c1591-127">DEX_IDS_MISSING_SOURCE_NAME</span></span></td>
<td><span data-ttu-id="c1591-128">Der Dateiname war erforderlich, wurde jedoch nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="c1591-128">File name was required, but wasn't given.</span></span></td>
<td><span data-ttu-id="c1591-129">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-129">None</span></span></td>
<td><span data-ttu-id="c1591-130">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-130">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-131">DEX_IDS_UNKNOWN_SOURCE</span><span class="sxs-lookup"><span data-stu-id="c1591-131">DEX_IDS_UNKNOWN_SOURCE</span></span></td>
<td><span data-ttu-id="c1591-132">Die von dieser Quelle bereitgestellte Datenquelle kann nicht analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="c1591-132">Cannot parse data source provided by this source.</span></span></td>
<td><span data-ttu-id="c1591-133">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-133">None</span></span></td>
<td><span data-ttu-id="c1591-134">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-134">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-135">DEX_IDS_INSTALL_PROBLEM</span><span class="sxs-lookup"><span data-stu-id="c1591-135">DEX_IDS_INSTALL_PROBLEM</span></span></td>
<td><span data-ttu-id="c1591-136">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="c1591-136">Unexpected error.</span></span> <span data-ttu-id="c1591-137">Einige DirectShow-Komponenten sind nicht ordnungsgemäß installiert.</span><span class="sxs-lookup"><span data-stu-id="c1591-137">Some DirectShow component is not installed properly.</span></span></td>
<td><span data-ttu-id="c1591-138">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-138">None</span></span></td>
<td><span data-ttu-id="c1591-139">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-139">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-140">DEX_IDS_NO_SOURCE_NAMES</span><span class="sxs-lookup"><span data-stu-id="c1591-140">DEX_IDS_NO_SOURCE_NAMES</span></span></td>
<td><span data-ttu-id="c1591-141">Der Quell Filter akzeptiert keine Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="c1591-141">Source filter does not accept file names.</span></span></td>
<td><span data-ttu-id="c1591-142">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-142">None</span></span></td>
<td><span data-ttu-id="c1591-143">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-143">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-144">DEX_IDS_BAD_MEDIATYPE</span><span class="sxs-lookup"><span data-stu-id="c1591-144">DEX_IDS_BAD_MEDIATYPE</span></span></td>
<td><span data-ttu-id="c1591-145">Der Medientyp der Gruppe wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c1591-145">Group's media type is not supported.</span></span></td>
<td><span data-ttu-id="c1591-146">Gruppennummer</span><span class="sxs-lookup"><span data-stu-id="c1591-146">Group number</span></span></td>
<td><span data-ttu-id="c1591-147"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-147"><strong>int</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-148">DEX_IDS_STREAM_NUMBER</span><span class="sxs-lookup"><span data-stu-id="c1591-148">DEX_IDS_STREAM_NUMBER</span></span></td>
<td><span data-ttu-id="c1591-149">Ungültige streamnummer für diese Quelle.</span><span class="sxs-lookup"><span data-stu-id="c1591-149">Invalid stream number for this source.</span></span></td>
<td><span data-ttu-id="c1591-150">Streamnummer</span><span class="sxs-lookup"><span data-stu-id="c1591-150">Stream number</span></span></td>
<td><span data-ttu-id="c1591-151"><strong>int</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-151"><strong>int</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-152">DEX_IDS_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="c1591-152">DEX_IDS_OUTOFMEMORY</span></span></td>
<td><span data-ttu-id="c1591-153">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c1591-153">Out of memory.</span></span></td>
<td><span data-ttu-id="c1591-154">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-154">None</span></span></td>
<td><span data-ttu-id="c1591-155">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-155">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-156">DEX_IDS_DIBSEQ_NOTALLSAME</span><span class="sxs-lookup"><span data-stu-id="c1591-156">DEX_IDS_DIBSEQ_NOTALLSAME</span></span></td>
<td><span data-ttu-id="c1591-157">Eine Bitmap in der Sequenz hatte nicht denselben Typ wie die anderen.</span><span class="sxs-lookup"><span data-stu-id="c1591-157">One bitmap in the sequence was not the same type as the others.</span></span></td>
<td><span data-ttu-id="c1591-158">Bitmapname</span><span class="sxs-lookup"><span data-stu-id="c1591-158">Bitmap name</span></span></td>
<td><span data-ttu-id="c1591-159"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-159"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-160">DEX_IDS_CLIPTOOSHORT</span><span class="sxs-lookup"><span data-stu-id="c1591-160">DEX_IDS_CLIPTOOSHORT</span></span></td>
<td><span data-ttu-id="c1591-161">Die Medien Zeiten des Clips sind ungültig, oder die geräteunabhängige Bitmap-Sequenz (DIB) ist zu kurz.</span><span class="sxs-lookup"><span data-stu-id="c1591-161">Clip's media times are invalid, or the device-independent bitmap (DIB) sequence is too short.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="c1591-162">Wenn andere Renderingfehler auftreten, kann dieser Fehler auch dann auftreten, wenn die Medien Zeiten gültig sind.</span><span class="sxs-lookup"><span data-stu-id="c1591-162">If other rendering errors occur, this error might occur even though the media times are valid.</span></span>
</blockquote>
<br/></td>
<td><span data-ttu-id="c1591-163">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-163">None</span></span></td>
<td><span data-ttu-id="c1591-164">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-164">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-165">DEX_IDS_INVALID_DXT</span><span class="sxs-lookup"><span data-stu-id="c1591-165">DEX_IDS_INVALID_DXT</span></span></td>
<td><span data-ttu-id="c1591-166">Der Klassen Bezeichner (CLSID) des Effekts oder Übergangs ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c1591-166">Class identifier (CLSID) of the effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="c1591-167">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1591-167">CLSID</span></span></td>
<td><span data-ttu-id="c1591-168"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-168"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-169">DEX_IDS_INVALID_DEFAULT_DXT</span><span class="sxs-lookup"><span data-stu-id="c1591-169">DEX_IDS_INVALID_DEFAULT_DXT</span></span></td>
<td><span data-ttu-id="c1591-170">Die CLSID des Standard Effekts oder-Übergangs ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="c1591-170">The CLSID of the default effect or transition is not valid.</span></span></td>
<td><span data-ttu-id="c1591-171">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1591-171">CLSID</span></span></td>
<td><span data-ttu-id="c1591-172"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-172"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-173">DEX_IDS_NO_3D</span><span class="sxs-lookup"><span data-stu-id="c1591-173">DEX_IDS_NO_3D</span></span></td>
<td><span data-ttu-id="c1591-174">Die Version von DirectX unterstützt keine dreidimensionalen Übergänge.</span><span class="sxs-lookup"><span data-stu-id="c1591-174">Your version of DirectX does not support three-dimensional transitions.</span></span></td>
<td><span data-ttu-id="c1591-175">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1591-175">CLSID</span></span></td>
<td><span data-ttu-id="c1591-176"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-176"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-177">DEX_IDS_BROKEN_DXT</span><span class="sxs-lookup"><span data-stu-id="c1591-177">DEX_IDS_BROKEN_DXT</span></span></td>
<td><span data-ttu-id="c1591-178">Dieser Effekt ist nicht die richtige Art oder ist beschädigt.</span><span class="sxs-lookup"><span data-stu-id="c1591-178">This effect is not the right kind, or is broken.</span></span></td>
<td><span data-ttu-id="c1591-179">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1591-179">CLSID</span></span></td>
<td><span data-ttu-id="c1591-180"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-180"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-181">DEX_IDS_NO_SUCH_PROPERTY</span><span class="sxs-lookup"><span data-stu-id="c1591-181">DEX_IDS_NO_SUCH_PROPERTY</span></span></td>
<td><span data-ttu-id="c1591-182">Für das Objekt ist keine solche Eigenschaft vorhanden.</span><span class="sxs-lookup"><span data-stu-id="c1591-182">No such property exists on the object.</span></span></td>
<td><span data-ttu-id="c1591-183">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="c1591-183">Property name</span></span></td>
<td><span data-ttu-id="c1591-184"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-184"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span><span class="sxs-lookup"><span data-stu-id="c1591-185">DEX_IDS_ILLEGAL_PROPERTY_VAL</span></span></td>
<td><span data-ttu-id="c1591-186">Ungültiger Wert für diese Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="c1591-186">Illegal value for this property.</span></span></td>
<td><span data-ttu-id="c1591-187">Wert angegeben</span><span class="sxs-lookup"><span data-stu-id="c1591-187">Value specified</span></span></td>
<td><span data-ttu-id="c1591-188"><strong>Konfigur</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-188"><strong>VARIANT</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-189">DEX_IDS_INVALID_XML</span><span class="sxs-lookup"><span data-stu-id="c1591-189">DEX_IDS_INVALID_XML</span></span></td>
<td><span data-ttu-id="c1591-190">Syntax Fehler in der XML-Datei.</span><span class="sxs-lookup"><span data-stu-id="c1591-190">Syntax error in XML file.</span></span></td>
<td><span data-ttu-id="c1591-191">Zeilennummer</span><span class="sxs-lookup"><span data-stu-id="c1591-191">Line number</span></span></td>
<td><span data-ttu-id="c1591-192">VT_I4 (ganze 4-Byte-Zahl)</span><span class="sxs-lookup"><span data-stu-id="c1591-192">VT_I4 (4-byte integer)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-193">DEX_IDS_CANT_FIND_FILTER</span><span class="sxs-lookup"><span data-stu-id="c1591-193">DEX_IDS_CANT_FIND_FILTER</span></span></td>
<td><span data-ttu-id="c1591-194">Der in XML angegebene Filter wurde nach Kategorie und Instanz nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="c1591-194">Cannot find filter specified in XML by category and instance.</span></span></td>
<td><span data-ttu-id="c1591-195">Anzeige Name (Instanz)</span><span class="sxs-lookup"><span data-stu-id="c1591-195">Friendly name (instance)</span></span></td>
<td><span data-ttu-id="c1591-196"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-196"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-197">DEX_IDS_DISK_WRITE_ERROR</span><span class="sxs-lookup"><span data-stu-id="c1591-197">DEX_IDS_DISK_WRITE_ERROR</span></span></td>
<td><span data-ttu-id="c1591-198">Fehler beim Schreiben der XML-Datei auf den Datenträger.</span><span class="sxs-lookup"><span data-stu-id="c1591-198">Error writing XML file to disk.</span></span></td>
<td><span data-ttu-id="c1591-199">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-199">None</span></span></td>
<td><span data-ttu-id="c1591-200">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-200">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c1591-201">DEX_IDS_INVALID_AUDIO_FX</span><span class="sxs-lookup"><span data-stu-id="c1591-201">DEX_IDS_INVALID_AUDIO_FX</span></span></td>
<td><span data-ttu-id="c1591-202">CLSID ist kein gültiger DirectShow-Audioeffekt-Filter.</span><span class="sxs-lookup"><span data-stu-id="c1591-202">CLSID not a valid DirectShow audio effect filter.</span></span></td>
<td><span data-ttu-id="c1591-203">CLSID</span><span class="sxs-lookup"><span data-stu-id="c1591-203">CLSID</span></span></td>
<td><span data-ttu-id="c1591-204"><strong>BSTR</strong></span><span class="sxs-lookup"><span data-stu-id="c1591-204"><strong>BSTR</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c1591-205">DEX_IDS_CANT_FIND_COMPRESSOR</span><span class="sxs-lookup"><span data-stu-id="c1591-205">DEX_IDS_CANT_FIND_COMPRESSOR</span></span></td>
<td><span data-ttu-id="c1591-206">Es wurde kein Kompressor gefunden, der das angegebene Komprimierungs Format erzeugt.</span><span class="sxs-lookup"><span data-stu-id="c1591-206">Cannot find a compressor to produce the specified compression format.</span></span></td>
<td><span data-ttu-id="c1591-207">Keine</span><span class="sxs-lookup"><span data-stu-id="c1591-207">None</span></span></td>
<td><span data-ttu-id="c1591-208">Nicht verfügbar</span><span class="sxs-lookup"><span data-stu-id="c1591-208">Not applicable</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c1591-209">Die folgenden Fehler sollten nie auftreten.</span><span class="sxs-lookup"><span data-stu-id="c1591-209">The following errors should never occur.</span></span> <span data-ttu-id="c1591-210">Wenn einer dieser Fehler auftritt, senden Sie einen Fehlerbericht an Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c1591-210">If you encounter one of these errors, please send a bug report to Microsoft.</span></span>



| <span data-ttu-id="c1591-211">Fehlercode</span><span class="sxs-lookup"><span data-stu-id="c1591-211">Error code</span></span>                 | <span data-ttu-id="c1591-212">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1591-212">Description</span></span>                                 |
|----------------------------|---------------------------------------------|
| <span data-ttu-id="c1591-213">Index- \_ IDs- \_ Zeitachse \_ analysieren</span><span class="sxs-lookup"><span data-stu-id="c1591-213">DEX\_IDS\_TIMELINE\_PARSE</span></span>  | <span data-ttu-id="c1591-214">Unerwarteter Fehler beim Auswerten der Zeitachse.</span><span class="sxs-lookup"><span data-stu-id="c1591-214">Unexpected error parsing the timeline.</span></span>      |
| <span data-ttu-id="c1591-215">Fehler im DEX- \_ IDs- \_ Diagramm \_</span><span class="sxs-lookup"><span data-stu-id="c1591-215">DEX\_IDS\_GRAPH\_ERROR</span></span>     | <span data-ttu-id="c1591-216">Unerwarteter Fehler beim Aufbau des Filter Diagramms.</span><span class="sxs-lookup"><span data-stu-id="c1591-216">Unexpected error building the filter graph.</span></span> |
| <span data-ttu-id="c1591-217">Fehler bei DEX- \_ IDs- \_ Raster \_</span><span class="sxs-lookup"><span data-stu-id="c1591-217">DEX\_IDS\_GRID\_ERROR</span></span>      | <span data-ttu-id="c1591-218">Unerwarteter Fehler beim internen Raster.</span><span class="sxs-lookup"><span data-stu-id="c1591-218">Unexpected error with the internal grid.</span></span>    |
| <span data-ttu-id="c1591-219">\_Schnittstellen-IDs- \_ Schnittstellen \_ Fehler</span><span class="sxs-lookup"><span data-stu-id="c1591-219">DEX\_IDS\_INTERFACE\_ERROR</span></span> | <span data-ttu-id="c1591-220">Unerwarteter Fehler beim erhalten einer Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="c1591-220">Unexpected error getting an interface.</span></span>      |



 

 

 




