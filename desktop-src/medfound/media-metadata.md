---
description: Medien Metadaten
ms.assetid: dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9
title: Medien Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb17f286673663976e17b4178239507765c2101
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106365000"
---
# <a name="media-metadata"></a><span data-ttu-id="05b0a-103">Medien Metadaten</span><span class="sxs-lookup"><span data-stu-id="05b0a-103">Media Metadata</span></span>

<span data-ttu-id="05b0a-104">Mediendateien enthalten Eigenschaften, die den Inhalt der Datei beschreiben.</span><span class="sxs-lookup"><span data-stu-id="05b0a-104">Media files contain properties that describe the contents of the file.</span></span> <span data-ttu-id="05b0a-105">In Microsoft Media Foundation können diese Eigenschaften wie folgt kategorisiert werden:</span><span class="sxs-lookup"><span data-stu-id="05b0a-105">In Microsoft Media Foundation, these properties can be categorized as follows:</span></span>

-   <span data-ttu-id="05b0a-106">**Medientyp Attribute** geben die Codierungs Parameter an, z. b. den Codierungs Algorithmus (Medien Untertyp), Video Frame Größe, Video Frame Rate, Audiobitrate und audiobeispielrate.</span><span class="sxs-lookup"><span data-stu-id="05b0a-106">**Media-type attributes** specify the encoding parameters, such as the encoding algorithm (media subtype), video frame size, video frame rate, audio bit rate, and audio sample rate.</span></span> <span data-ttu-id="05b0a-107">Weitere Informationen zu Medientyp Attributen finden Sie unter [Medientypen](media-types.md).</span><span class="sxs-lookup"><span data-stu-id="05b0a-107">For more information about media-type attributes, see [Media Types](media-types.md).</span></span>
-   <span data-ttu-id="05b0a-108">**Metadaten** enthalten beschreibende Informationen für den Medieninhalt, z. b. Titel, Interpret, Composer und Genre.</span><span class="sxs-lookup"><span data-stu-id="05b0a-108">**Metadata** contains descriptive information for the media content, such as title, artist, composer, and genre.</span></span> <span data-ttu-id="05b0a-109">Metadaten können auch Codierungs Parameter beschreiben.</span><span class="sxs-lookup"><span data-stu-id="05b0a-109">Metadata can also describe encoding parameters.</span></span> <span data-ttu-id="05b0a-110">Es kann schneller sein, über Metadaten auf diese Informationen zuzugreifen, als mithilfe von Medientyp Attributen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-110">It can be faster to access this information through metadata than through media-type attributes.</span></span>
-   <span data-ttu-id="05b0a-111">**DRM-Eigenschaften** enthalten Informationen zu Nutzungseinschränkungen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-111">**DRM properties** contain information on usage restrictions.</span></span> <span data-ttu-id="05b0a-112">Derzeit werden von Media Foundation keine DRM-Eigenschaften durch Metadaten unterstützt, mit Ausnahme der **pkey DRM-Eigenschaft \_ \_ IsProtected** .</span><span class="sxs-lookup"><span data-stu-id="05b0a-112">Currently Media Foundation does not support DRM properties through metadata, with the exception of the **PKEY\_DRM\_IsProtected** property.</span></span>

<span data-ttu-id="05b0a-113">Es gibt zwei Möglichkeiten, Metadaten in Media Foundation zu lesen:</span><span class="sxs-lookup"><span data-stu-id="05b0a-113">There are two ways to read metadata in Media Foundation:</span></span>

-   <span data-ttu-id="05b0a-114">Die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle (Media Foundation Metadaten der Version 1).</span><span class="sxs-lookup"><span data-stu-id="05b0a-114">The [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface (Media Foundation version 1 metadata).</span></span>
-   <span data-ttu-id="05b0a-115">Die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle von Windows Shell (shellmetadaten).</span><span class="sxs-lookup"><span data-stu-id="05b0a-115">The Windows Shell [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface (Shell metadata).</span></span>

<span data-ttu-id="05b0a-116">Shellmetadaten beziehen sich nicht nur auf Mediendateien, sondern auf eine viel größere Anzahl von Dateien auf dem System.</span><span class="sxs-lookup"><span data-stu-id="05b0a-116">Shell metadata pertains not only to media files but to a much wider range of files on the system.</span></span>

<span data-ttu-id="05b0a-117">In der folgenden Tabelle werden die Features und Einschränkungen der einzelnen Metadaten-APIs verglichen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-117">The following table compares the features and limitations of each metadata API.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="05b0a-118">Media Foundation v1-Metadaten</span><span class="sxs-lookup"><span data-stu-id="05b0a-118">Media Foundation v1 Metadata</span></span></th>
<th><span data-ttu-id="05b0a-119">Shellmetadaten</span><span class="sxs-lookup"><span data-stu-id="05b0a-119">Shell Metadata</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="05b0a-120">Erfordert Windows Vista oder höher.</span><span class="sxs-lookup"><span data-stu-id="05b0a-120">Requires Windows Vista or later.</span></span></td>
<td><span data-ttu-id="05b0a-121">Erfordert Windows 7.</span><span class="sxs-lookup"><span data-stu-id="05b0a-121">Requires Windows 7.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="05b0a-122">Shell-Metadaten im Allgemeinen erfordern nicht Windows 7, aber Media Foundation keine shellmetadaten vor Windows 7 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05b0a-122">Shell metadata in general does not require Windows 7, but Media Foundation did not support Shell metadata prior to Windows 7.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05b0a-123">Eigenschaften sind nicht mit dem shelleigenschaftensystem kompatibel.</span><span class="sxs-lookup"><span data-stu-id="05b0a-123">Properties are not compatible with Shell property system.</span></span></td>
<td><span data-ttu-id="05b0a-124">Eigenschaften sind mit dem shelleigenschaftensystem kompatibel.</span><span class="sxs-lookup"><span data-stu-id="05b0a-124">Properties are compatible with the Shell property system.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05b0a-125">Eigenschaften können auf die gesamte Datei oder auf Streamebene angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="05b0a-125">Properties can apply to the entire file, or at the stream level.</span></span></td>
<td><span data-ttu-id="05b0a-126">Es werden nur Eigenschaften auf Dateiebene unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05b0a-126">Only file-level properties are supported.</span></span> <span data-ttu-id="05b0a-127">Eigenschaften auf Streamebene werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05b0a-127">Stream-level properties are not supported.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05b0a-128">Eigenschaften können über Werte in mehreren Sprachen verfügen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-128">Properties can have values in multiple languages.</span></span></td>
<td><span data-ttu-id="05b0a-129">Werte in mehreren Sprachen werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="05b0a-129">Values in multiple languages are not supported.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="05b0a-130">Eigenschafts Schlüssel sind Zeichen folgen mit breit Zeichen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-130">Property keys are wide-character strings.</span></span></td>
<td><span data-ttu-id="05b0a-131">Eigenschafts Schlüssel sind <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PropertyKey</strong></a> -Werte.</span><span class="sxs-lookup"><span data-stu-id="05b0a-131">Property keys are <a href="/windows/desktop/api/wtypes/ns-wtypes-propertykey"><strong>PROPERTYKEY</strong></a> values.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="05b0a-132">Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> -Werte.</span><span class="sxs-lookup"><span data-stu-id="05b0a-132">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
<td><span data-ttu-id="05b0a-133">Eigenschaftswerte sind <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> -Werte.</span><span class="sxs-lookup"><span data-stu-id="05b0a-133">Property values are <a href="/windows/win32/api/propidl/ns-propidl-propvariant"><strong>PROPVARIANT</strong></a> values.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="in-this-section"></a><span data-ttu-id="05b0a-134">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="05b0a-134">In this section</span></span>



| <span data-ttu-id="05b0a-135">Thema</span><span class="sxs-lookup"><span data-stu-id="05b0a-135">Topic</span></span>                                                                                     | <span data-ttu-id="05b0a-136">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="05b0a-136">Description</span></span>                                                                                                                                |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05b0a-137">Shellmetadatenanbieter</span><span class="sxs-lookup"><span data-stu-id="05b0a-137">Shell Metadata Providers</span></span>](shell-metadata-providers.md)<br/>                       | <span data-ttu-id="05b0a-138">Ab Windows 7 macht Media Foundation Metadaten über die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05b0a-138">Starting in Windows 7, Media Foundation exposes metadata through the [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) interface.</span></span><br/> |
| [<span data-ttu-id="05b0a-139">Metadateneigenschaften für Mediendateien</span><span class="sxs-lookup"><span data-stu-id="05b0a-139">Metadata Properties for Media Files</span></span>](metadata-properties-for-media-files.md)<br/> | <span data-ttu-id="05b0a-140">In diesem Thema werden die gängigsten Metadateneigenschaften für Mediendateien aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="05b0a-140">This topic lists the most common metadata properties for media files.</span></span><br/>                                                           |
| [<span data-ttu-id="05b0a-141">Metadatenanbieter in Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05b0a-141">Metadata Providers in Windows Vista</span></span>](metadata-providers-in-windows-vista.md)<br/> | <span data-ttu-id="05b0a-142">In Windows Vista macht Media Foundation Metadaten über die [**IMF Metadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="05b0a-142">In Windows Vista, Media Foundation exposes metadata through the [**IMFMetadata**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadata) interface.</span></span><br/>                   |



 

<span data-ttu-id="05b0a-143">Wenn Sie eine benutzerdefinierte Medienquelle implementieren und shellmetadaten verfügbar machen möchten, finden Sie unter [benutzerdefinierte Metadatenanbieter für Mediendateien](custom-metadata-providers-for-media-files.md)Weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="05b0a-143">If you are implementing a custom media source and want to expose Shell metadata, see [Custom Metadata Providers for Media Files](custom-metadata-providers-for-media-files.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05b0a-144">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="05b0a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05b0a-145">Media Foundation-Programmier Handbuch</span><span class="sxs-lookup"><span data-stu-id="05b0a-145">Media Foundation Programming Guide</span></span>](media-foundation-programming-guide.md)
</dt> </dl>

 

 
