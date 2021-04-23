---
description: Der Dvd Copy Protection-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern. Verwenden Sie diesen Eigenschaftensatz, um zu verhindern, dass nicht autorisierte Kopien von vorab aufgezeichneten DVD-Videos erstellt werden.
ms.assetid: da3abefd-8f25-449d-8787-84d2cef928da
title: DVD-Kopierschutz-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 382243a6071fa73361df13ae933d259979686a06
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909478"
---
# <a name="dvd-copy-protection-property-set"></a><span data-ttu-id="60b41-104">DVD Copy Protection-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="60b41-104">DVD Copy Protection Property Set</span></span>

<span data-ttu-id="60b41-105">Der Dvd Copy Protection-Eigenschaftensatz ermöglicht die Authentifizierung von Kopierschutzinformationen von Hardware- oder Softwareentschlüsselern.</span><span class="sxs-lookup"><span data-stu-id="60b41-105">The DVD Copy Protection property set provides authentication of copy protection information from hardware or software decrypters.</span></span> <span data-ttu-id="60b41-106">Verwenden Sie diesen Eigenschaftensatz, um zu verhindern, dass nicht autorisierte Kopien von vorab aufgezeichneten DVD-Videos erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="60b41-106">Use this property set to prevent unauthorized copying from prerecorded DVD-Video.</span></span>

<span data-ttu-id="60b41-107">Microsoft stellt Software bereit, die den für das Verschlüsselungsschema erforderlichen Authentifizierungsprozess erleichtert, sodass ein DVD-ROM-Laufwerk Schlüssel mit einem DVD-Entschlüsselungsprogramm authentifizieren und übertragen kann.</span><span class="sxs-lookup"><span data-stu-id="60b41-107">Microsoft provides software that facilitates the authentication process required by the encryption scheme, thus enabling a DVD-ROM drive to authenticate and transfer keys with a DVD decrypter.</span></span> <span data-ttu-id="60b41-108">Microsoft bietet derzeit keine DVD-Entschlüsseler an und stellt stattdessen Betriebssystemcode bereit, der als Agent fungiert, um die Authentifizierung von Hardware- oder Softwareentschlüsselern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="60b41-108">Microsoft has no current plans to ship a DVD decrypter and, instead, is providing operating system code that will act as the agent to enable authentication of either hardware or software decrypters.</span></span>

<span data-ttu-id="60b41-109">Der DVD-Navigator initiiert und steuert den Schlüsselaustauschprozess.</span><span class="sxs-lookup"><span data-stu-id="60b41-109">The DVD navigator initiates and controls the key exchange process.</span></span> <span data-ttu-id="60b41-110">Der DVD-Minitreiber muss nur die folgenden Eigenschaften implementieren.</span><span class="sxs-lookup"><span data-stu-id="60b41-110">The DVD minidriver needs only to implement the following properties.</span></span> <span data-ttu-id="60b41-111">Andere Komponenten verarbeiten den Rest.</span><span class="sxs-lookup"><span data-stu-id="60b41-111">Other components handle the rest.</span></span>

<span data-ttu-id="60b41-112">Jeder DVD-Eingabestream empfängt Kopierschutzeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60b41-112">Each DVD input stream will receive copy protection properties.</span></span> <span data-ttu-id="60b41-113">Dies gilt auch, wenn die gleiche Hardware alle DVD-Streams steuert.</span><span class="sxs-lookup"><span data-stu-id="60b41-113">This is true even if the same hardware controls all DVD streams.</span></span>

<span data-ttu-id="60b41-114">Die folgenden Informationen enthalten die erforderlichen Konstanten und Datentypen, die für diesen Eigenschaftensatz in Aufrufen von [**IKsPropertySet-Methoden**](ikspropertyset.md) verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="60b41-114">The following information presents the necessary constants and data types to use for this property set in calls to [**IKsPropertySet**](ikspropertyset.md) methods.</span></span> <span data-ttu-id="60b41-115">Sie stellt Werte für die **Parameter GUID** (*guidPropSet),* Eigenschaften-ID (*dwPropID*) und Eigenschaftendatentyp (*pPropData*) bereit.</span><span class="sxs-lookup"><span data-stu-id="60b41-115">It provides values for the **GUID** (*guidPropSet*), property ID (*dwPropID*), and property data type (*pPropData*) parameters.</span></span>



| <span data-ttu-id="60b41-116">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="60b41-116">Label</span></span> | <span data-ttu-id="60b41-117">Wert</span><span class="sxs-lookup"><span data-stu-id="60b41-117">Value</span></span> |
|-------------------|---------------------------|
| <span data-ttu-id="60b41-118">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="60b41-118">Property Set GUID</span></span> | <span data-ttu-id="60b41-119">AM \_ KSPROPSETID \_ CopyProt</span><span class="sxs-lookup"><span data-stu-id="60b41-119">AM\_KSPROPSETID\_CopyProt</span></span> |



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="60b41-120">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="60b41-120">Property ID</span></span></th>
<th><span data-ttu-id="60b41-121">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60b41-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60b41-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span><span class="sxs-lookup"><span data-stu-id="60b41-122"><a href="am-property-copy-analog-component-property.md"><strong>AM_PROPERTY_COPY_ANALOG_COMPONENT</strong></a></span></span></td>
<td><span data-ttu-id="60b41-123">Fragt ab, ob es sich bei der Videoausgabe um ein Analogkomponentenvideo mit Standarddefinition handelt.</span><span class="sxs-lookup"><span data-stu-id="60b41-123">Queries whether the video output is standard-definition, analog component video.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60b41-124">AM_PROPERTY_COPY_MACROVISION</span><span class="sxs-lookup"><span data-stu-id="60b41-124">AM_PROPERTY_COPY_MACROVISION</span></span></td>
<td><span data-ttu-id="60b41-125">Dies ist eine eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60b41-125">This is a set-only property.</span></span> <span data-ttu-id="60b41-126">Diese Eigenschaft legt die analoge Kopierschutzebene für den NTSC-Encoder am Ausgabeende des empfangenden Pins fest.</span><span class="sxs-lookup"><span data-stu-id="60b41-126">This property sets the analog copy protection level for the NTSC encoder on the output end of the receiving pin.</span></span> <span data-ttu-id="60b41-127">Verwendet <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60b41-127">Uses <a href="/previous-versions/ms778996(v=vs.85)"><strong>AM_COPY_MACROVISION</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60b41-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span><span class="sxs-lookup"><span data-stu-id="60b41-128">AM_PROPERTY_DVDCOPY_CHLG_KEY</span></span></td>
<td><span data-ttu-id="60b41-129">Sowohl Get- als auch Set-Vorgänge werden für diese Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60b41-129">Both get and set operations are supported on this property.</span></span> <span data-ttu-id="60b41-130">Ein Get-Vorgang fordert den Decoder auf, seinen Bus-Challenge-Schlüssel zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="60b41-130">A get operation requests the decoder to provide its bus challenge key.</span></span> <span data-ttu-id="60b41-131">Ein Set-Vorgang stellt dem Decoder den Bus-Challenge-Schlüssel aus dem DVD-Laufwerk zurEntschlüsselung.</span><span class="sxs-lookup"><span data-stu-id="60b41-131">A set operation provides the decoder with the bus challenge key from the DVD drive.</span></span> <span data-ttu-id="60b41-132">Die in dieser Eigenschaft übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60b41-132">The data passed in this property will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_chlgkey"><strong>AM_DVDCOPY_CHLGKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60b41-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span><span class="sxs-lookup"><span data-stu-id="60b41-133">AM_PROPERTY_DVDCOPY_DEC_KEY2</span></span></td>
<td><span data-ttu-id="60b41-134">Dies ist eine get-only-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="60b41-134">This is a get-only property.</span></span> <span data-ttu-id="60b41-135">Diese Eigenschaft fordert an, dass der Busschlüssel 2 des Decoders auf das DVD-Laufwerk übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="60b41-135">This property requests that the decoder's bus key 2 be transferred to the DVD drive.</span></span> <span data-ttu-id="60b41-136">Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60b41-136">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60b41-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span><span class="sxs-lookup"><span data-stu-id="60b41-137">AM_PROPERTY_DVDCOPY_DISC_KEY</span></span></td>
<td><span data-ttu-id="60b41-138">Eigenschaft "Nur festlegen".</span><span class="sxs-lookup"><span data-stu-id="60b41-138">Set-only property.</span></span> <span data-ttu-id="60b41-139">Dadurch wird ein Datenträgerschlüssel (Disk Key) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="60b41-139">This provides disc key.</span></span> <span data-ttu-id="60b41-140">Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60b41-140">The key is a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_disckey"><strong>AM_DVDCOPY_DISCKEY</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60b41-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span><span class="sxs-lookup"><span data-stu-id="60b41-141">AM_PROPERTY_DVDCOPY_DVD_KEY1</span></span></td>
<td><span data-ttu-id="60b41-142">Dies ist eine eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60b41-142">This is a set-only property.</span></span> <span data-ttu-id="60b41-143">Diese Eigenschaft stellt den DVD-Laufwerksbusschlüssel 1 für den Decoder zurt.</span><span class="sxs-lookup"><span data-stu-id="60b41-143">This property provides the DVD drive bus key 1 to the decoder.</span></span> <span data-ttu-id="60b41-144">Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY.</strong></a></span><span class="sxs-lookup"><span data-stu-id="60b41-144">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-am_dvdcopy_buskey"><strong>AM_DVDCOPY_BUSKEY</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60b41-145">AM_PROPERTY_DVDCOPY_REGION</span><span class="sxs-lookup"><span data-stu-id="60b41-145">AM_PROPERTY_DVDCOPY_REGION</span></span></td>
<td><span data-ttu-id="60b41-146">Der Regioncode fordert die Vom DVD-Konsortium definierte Regiondefinition an, in der der Decoder wieder verwendet werden darf.</span><span class="sxs-lookup"><span data-stu-id="60b41-146">Region code requests the region definition that the decoder is allowed to play in as defined by the DVD consortium.</span></span> <span data-ttu-id="60b41-147">Dieser Bereich wird als <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION-Struktur</strong></a> definiert.</span><span class="sxs-lookup"><span data-stu-id="60b41-147">This region is defined as a <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-dvd_region"><strong>DVD_REGION</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60b41-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span><span class="sxs-lookup"><span data-stu-id="60b41-148">AM_PROPERTY_DVDCOPY_SET_COPY_STATE</span></span></td>
<td><span data-ttu-id="60b41-149">Sowohl get als auch set werden für diese Eigenschaft unterstützt.</span><span class="sxs-lookup"><span data-stu-id="60b41-149">Both get and set are supported on this property.</span></span> <span data-ttu-id="60b41-150">Get wird zuerst aufgerufen, um zu bestimmen, ob eine Authentifizierung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="60b41-150">Get is called first to determine if authentication is required.</span></span> <span data-ttu-id="60b41-151">Die festgelegten Eigenschaften sind Hinweise darauf, in welche Phase der Kopierschutzaushandlung der Filter eintritt.</span><span class="sxs-lookup"><span data-stu-id="60b41-151">The set properties are indications as to which phase of copy protection negotiation the filter is entering.</span></span> <span data-ttu-id="60b41-152">Die übergebenen Daten sind eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60b41-152">The data passed will be a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_set_copy_state"><strong>AM_DVDCOPY_SET_COPY_STATE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60b41-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span><span class="sxs-lookup"><span data-stu-id="60b41-153">AM_PROPERTY_DVDCOPY_SUPPORTS_NEW_KEYCOUNT</span></span></td>
<td><span data-ttu-id="60b41-154">Wenn diese Eigenschaft <strong>TRUE</strong>ist, sendet der DVD-Navigator vor dem Aushandeln des Datenträgerschlüssels keine <strong>AM_UseNewCSSKey</strong> Beispiele.</span><span class="sxs-lookup"><span data-stu-id="60b41-154">If this property is <strong>TRUE</strong>, the DVD Navigator does not send <strong>AM_UseNewCSSKey</strong> samples before negotiating the disc key.</span></span> <span data-ttu-id="60b41-155">Weitere Informationen finden Sie <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>unter AM_SAMPLE2_PROPERTIES</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60b41-155">See <a href="/windows/win32/api/strmif/ns-strmif-am_sample2_properties"><strong>AM_SAMPLE2_PROPERTIES</strong></a>.</span></span><br/> <span data-ttu-id="60b41-156">Schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="60b41-156">Read-only.</span></span> <span data-ttu-id="60b41-157">Die Eigenschaftsdaten sind ein <strong>BOOL-Wert.</strong></span><span class="sxs-lookup"><span data-stu-id="60b41-157">The property data is a <strong>BOOL</strong> value.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="60b41-158">Gilt für Windows 7.</span><span class="sxs-lookup"><span data-stu-id="60b41-158">Applies to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60b41-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span><span class="sxs-lookup"><span data-stu-id="60b41-159">AM_PROPERTY_DVDCOPY_TITLE_KEY</span></span></td>
<td><span data-ttu-id="60b41-160">Dies ist eine eigenschaft, die nur festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="60b41-160">This is a set-only property.</span></span> <span data-ttu-id="60b41-161">Dadurch wird der Titelschlüssel aus dem aktuellen Inhalt zur Verfügung stellen.</span><span class="sxs-lookup"><span data-stu-id="60b41-161">This provides title key from current content.</span></span> <span data-ttu-id="60b41-162">Der Schlüssel ist eine Struktur vom Typ <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="60b41-162">The key is a structure of type <a href="/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_dvdcopy_titlekey"><strong>AM_DVDCOPY_TITLEKEY</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="60b41-163">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="60b41-163">Requirements</span></span>



| <span data-ttu-id="60b41-164">Anforderung</span><span class="sxs-lookup"><span data-stu-id="60b41-164">Requirement</span></span> | <span data-ttu-id="60b41-165">Wert</span><span class="sxs-lookup"><span data-stu-id="60b41-165">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="60b41-166">Header</span><span class="sxs-lookup"><span data-stu-id="60b41-166">Header</span></span><br/> | <dl> <span data-ttu-id="60b41-167"><dt>Dvdmedia.h</dt></span><span class="sxs-lookup"><span data-stu-id="60b41-167"><dt>Dvdmedia.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b41-168">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="60b41-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b41-169">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="60b41-169">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 




