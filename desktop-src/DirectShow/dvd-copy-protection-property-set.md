---
description: Der Eigenschaften Satz "DVD-Kopierschutz" ermöglicht die Authentifizierung von Informationen zum Kopierschutz von Hardware-oder Software Entschlüsselungs Informationen. Verwenden Sie diesen Eigenschaften Satz, um das nicht autorisierte Kopieren von DVD-Videos zu verhindern.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD-Kopierschutz-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a14146ce0be19a4ed49c23517987a2c91a85da87
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361649"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="79166-104">Eigenschaften Satz für den DVD-Kopierschutz</span><span class="sxs-lookup"><span data-stu-id="79166-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="79166-105">Der Eigenschaften Satz "DVD-Kopierschutz" ermöglicht die Authentifizierung von Informationen zum Kopierschutz von Hardware-oder Software Entschlüsselungs Informationen.</span><span class="sxs-lookup"><span data-stu-id="79166-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="79166-106">Verwenden Sie diesen Eigenschaften Satz, um das nicht autorisierte Kopieren von DVD-Videos zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="79166-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="79166-107">Microsoft stellt Software zur Verfügung, die den für das Verschlüsselungsschema erforderlichen Authentifizierungsprozess vereinfacht, sodass ein DVD-ROM-Laufwerk Schlüssel mit einer DVD-Entschlüsselung authentifizieren und übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="79166-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="79166-108">Microsoft ist nicht in der Lage, eine DVD-Entschlüsselung zu senden und stellt stattdessen Betriebssystem Code bereit, der als Agent fungiert, um die Authentifizierung von Hardware-oder Software Entschlüsselungs Optionen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="79166-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="79166-109">Der DVD-Navigator initiiert und steuert den Schlüsselaustausch Vorgang.</span><span class="sxs-lookup"><span data-stu-id="79166-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="79166-110">Der DVD-Mini Treiber muss lediglich die folgenden Eigenschaften implementieren.</span><span class="sxs-lookup"><span data-stu-id="79166-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="79166-111">Andere Komponenten verarbeiten den Rest.</span><span class="sxs-lookup"><span data-stu-id="79166-111">Other components handle the rest.</span></span>

<span data-ttu-id="79166-112">Jeder DVD-Eingabestream erhält Kopierschutz Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="79166-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="79166-113">Dies gilt auch, wenn dieselbe Hardware alle DVD-Streams steuert.</span><span class="sxs-lookup"><span data-stu-id="79166-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="79166-114">Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen dar, die für diesen Eigenschaften Satz in Aufrufen von " [**ikspropertyset**](ikspropertyset.md) "-Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="79166-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="79166-115">Es werden Werte für die Parameter **GUID** (*guidpropset*), Property ID (*dwpropid*) und Property Data Type (*ppropdata*) bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="79166-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



|                   |                           |
|-------------------|---------------------------|
| <span data-ttu-id="79166-116">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="79166-116">Property Set GUID</span></span> | <span data-ttu-id="79166-117">AM \_ kspropsetid \_ copyprot</span><span class="sxs-lookup"><span data-stu-id="79166-117">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="79166-118">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="79166-118">Property ID</span></span></th>
<th><span data-ttu-id="79166-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79166-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="79166-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="79166-120"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="79166-121">Fragt ab, ob es sich bei der Videoausgabe um ein Video mit der standardmäßigen Definition, Analog</span><span class="sxs-lookup"><span data-stu-id="79166-121">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79166-122">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="79166-122">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="79166-123">Dies ist eine Eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79166-123">This is a set-only property.</span></span> <span data-ttu-id="79166-124">Diese Eigenschaft legt die Ebene des analogen Kopierschutzes für den NTSC-Encoder am Ausgabe Ende der empfangenden PIN fest.</span><span class="sxs-lookup"><span data-stu-id="79166-124">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="79166-125">Verwendet <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-125">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79166-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="79166-126">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="79166-127">Sowohl Get-als auch Set-Vorgänge werden für diese Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79166-127">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="79166-128">Mit einem Get-Vorgang wird der Decoder aufgefordert, seinen busaufforderungs Schlüssel bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="79166-128">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="79166-129">Durch einen Set-Vorgang erhält der Decoder den Bus Challenge-Schlüssel vom DVD-Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="79166-129">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="79166-130">Bei den in dieser Eigenschaft bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-130">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79166-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="79166-131">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="79166-132">Dabei handelt es sich um eine reine Get-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="79166-132">This is a get-only property.</span></span> <span data-ttu-id="79166-133">Diese Eigenschaft fordert an, dass der buskkey 2 des Decoders auf das DVD-Laufwerk übertragen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79166-133">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="79166-134">Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-134">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79166-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="79166-135">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="79166-136">Eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79166-136">Set-only property.</span></span> <span data-ttu-id="79166-137">Dies stellt einen Disc-Schlüssel bereit.</span><span class="sxs-lookup"><span data-stu-id="79166-137">This provides disc key.</span></span> <span data-ttu-id="79166-138">Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-138">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79166-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="79166-139">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="79166-140">Dies ist eine Eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79166-140">This is a set-only property.</span></span> <span data-ttu-id="79166-141">Diese Eigenschaft stellt dem Decoder den DVD-laufwerkbus Schlüssel 1 zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="79166-141">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="79166-142">Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-142">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79166-143">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="79166-143">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="79166-144">Der Regions Code fordert die Regions Definition an, in der der Decoder durch das DVD-Konsortium definiert werden darf.</span><span class="sxs-lookup"><span data-stu-id="79166-144">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="79166-145">Diese Region ist als <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> Struktur definiert.</span><span class="sxs-lookup"><span data-stu-id="79166-145">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79166-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="79166-146">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="79166-147">"Get" und "Set" werden für diese Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79166-147">Both get and set are supported on this property.</span></span> <span data-ttu-id="79166-148">Get wird zuerst aufgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="79166-148">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="79166-149">Die Set-Eigenschaften sind Hinweise darauf, in welcher Phase der Kopierschutz Aushandlung der Filter eintritt.</span><span class="sxs-lookup"><span data-stu-id="79166-149">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="79166-150">Bei den bestandenen Daten handelt es sich um eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-150">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="79166-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="79166-151">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="79166-152">Wenn diese Eigenschaft den Wert <strong>true</strong>hat, sendet der DVD-Navigator vor dem Aushandeln des CD-Schlüssels keine <strong>AM_UseNewCSSKey</strong> Samples.</span><span class="sxs-lookup"><span data-stu-id="79166-152">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="79166-153">Siehe <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-153">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="79166-154">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="79166-154">Read-only.</span></span> <span data-ttu-id="79166-155">Die Eigenschaften Daten sind ein <strong>boolescher</strong> Wert.</span><span class="sxs-lookup"><span data-stu-id="79166-155">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="79166-156">Gilt für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="79166-156">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="79166-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="79166-157">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="79166-158">Dies ist eine Eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="79166-158">This is a set-only property.</span></span> <span data-ttu-id="79166-159">Dadurch wird der Titel Schlüssel aus dem aktuellen Inhalt bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="79166-159">This provides title key from current content.</span></span> <span data-ttu-id="79166-160">Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="79166-160">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="79166-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79166-161">Requirements</span></span>



| <span data-ttu-id="79166-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79166-162">Requirement</span></span> | <span data-ttu-id="79166-163">Wert</span><span class="sxs-lookup"><span data-stu-id="79166-163">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="79166-164">Header</span><span class="sxs-lookup"><span data-stu-id="79166-164">Header</span></span><br/> | <dl> <span data-ttu-id="79166-165"><dt>Dvdmedia. h</dt></span><span class="sxs-lookup"><span data-stu-id="79166-165"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79166-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79166-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79166-167">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="79166-167">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




