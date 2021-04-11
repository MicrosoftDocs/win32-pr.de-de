---
description: Das konzeptionelle Modell
ms.assetid: f906466e-acdc-4d0f-bf27-c5a25dc56c01
title: Das konzeptionelle Modell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a17538e7fdb454fa8eb61ab951a3316b0f0c327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217505"
---
# <a name="the-conceptual-model"></a><span data-ttu-id="cab4a-103">Das konzeptionelle Modell</span><span class="sxs-lookup"><span data-stu-id="cab4a-103">The Conceptual Model</span></span>

<span data-ttu-id="cab4a-104">In diesem Abschnitt werden die Objekte, Eigenschaften und Ressourcen beschrieben, die das konzeptionelle WPD-Modell bilden.</span><span class="sxs-lookup"><span data-stu-id="cab4a-104">This section describes the objects, properties, and resources that constitute the WPD conceptual model.</span></span>

### <a name="objects"></a><span data-ttu-id="cab4a-105">Objekte</span><span class="sxs-lookup"><span data-stu-id="cab4a-105">Objects</span></span>

<span data-ttu-id="cab4a-106">In WPD werden logische Entitäten auf Geräten als Objekte bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cab4a-106">In WPD, logical entities on devices are referred to as objects.</span></span> <span data-ttu-id="cab4a-107">In der Regel, aber nicht immer, stellen diese Daten auf dem Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="cab4a-107">Typically, but not always, these represent data on the device.</span></span> <span data-ttu-id="cab4a-108">-Objekte verfügen über Eigenschaften, auf die von Objekt bezeichmern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="cab4a-108">Objects have properties, and are referenced by object identifiers.</span></span> <span data-ttu-id="cab4a-109">Beispiele für Objekte sind Bilder und Ordner auf einer Kamera, Lieder und Wiedergabelisten auf einem Media Player, Kontakte auf einem Mobiltelefon usw.</span><span class="sxs-lookup"><span data-stu-id="cab4a-109">Examples of objects include pictures and folders on a camera, songs and playlists on a media player, contacts on a mobile phone, and so on.</span></span>

<span data-ttu-id="cab4a-110">Objekte können auch Funktions-oder Informationsteile des Geräts darstellen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-110">Objects can also represent functional or informational parts of the device.</span></span> <span data-ttu-id="cab4a-111">Beispiele hierfür sind Player-Steuerelemente (Wiedergabe/Aufzeichnung/Pause), Kameraeinstellungen, SMS-Funktionen eines Mobiltelefons usw.</span><span class="sxs-lookup"><span data-stu-id="cab4a-111">Examples of these include player controls (play/record/pause), camera settings, a mobile phone's SMS capabilities, and so on.</span></span>

<span data-ttu-id="cab4a-112">Die beiden folgenden Themen beschreiben Beispiele und Abbildungen zweier Objekttypen: das Image-Objekt und das Mediacast-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cab4a-112">The two following topics give examples and illustrations of two types of objects: the Image object and the Mediacast object.</span></span>

### <a name="image-object"></a><span data-ttu-id="cab4a-113">Image-Objekt</span><span class="sxs-lookup"><span data-stu-id="cab4a-113">Image Object</span></span>

<span data-ttu-id="cab4a-114">Ein Image-Objekt stellt ein Image dar.</span><span class="sxs-lookup"><span data-stu-id="cab4a-114">An image object represents a still image.</span></span> <span data-ttu-id="cab4a-115">Das folgende Diagramm zeigt die Beziehungen zwischen einem Bild Objekt, seinen Eigenschaften und den zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-115">The following diagram shows the relationships between an Image object, its properties, and its resources.</span></span>

![Diagramm, das ein WPD-Objekt und seine Beziehung zu seinen Eigenschaften und Ressourcen anzeigt](images/wpd-overview-figure2.gif)

<span data-ttu-id="cab4a-117">Weitere Informationen zum Image-Objekt und dessen Eigenschaften finden Sie im Thema [**WPD \_ - \_ Inhaltstyp \_ Image**](wpd-content-type-image.md) .</span><span class="sxs-lookup"><span data-stu-id="cab4a-117">For more information about the Image object and its properties, see the [**WPD\_CONTENT\_TYPE\_IMAGE**](wpd-content-type-image.md) topic.</span></span>

### <a name="mediacast-object"></a><span data-ttu-id="cab4a-118">Mediacast-Objekt</span><span class="sxs-lookup"><span data-stu-id="cab4a-118">Mediacast Object</span></span>

<span data-ttu-id="cab4a-119">Ein Mediacast-Objekt kann als Container Objekt betrachtet werden, das verwandte Inhalte gruppiert, ebenso wie eine Wiedergabeliste Musik gruppiert.</span><span class="sxs-lookup"><span data-stu-id="cab4a-119">A Mediacast object can be thought of as a container object that groups related content, just as a playlist groups music.</span></span> <span data-ttu-id="cab4a-120">Häufig wird ein Mediacast-Objekt verwendet, um Medieninhalte zu gruppieren, die Online veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="cab4a-120">Often, a Mediacast object is used to group media content that was published online.</span></span> <span data-ttu-id="cab4a-121">Beispielsweise kann ein RSS-Kanal als Mediacast-Objekt dargestellt werden, dessen Objekt Verweise auf Inhalts Objekte verweisen, die jedes Element im Kanal darstellen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-121">For example, an RSS channel can be represented as a Mediacast object whose object references point to content objects that represent each item in the channel.</span></span> <span data-ttu-id="cab4a-122">Das folgende Diagramm zeigt die Beziehung zwischen einem Mediacast-Objekt und den darin enthaltenen drei Audioobjekten.</span><span class="sxs-lookup"><span data-stu-id="cab4a-122">The following diagram shows the relationship between a Mediacast object and the three audio objects it contains.</span></span>

![Diagramm mit der hierarchischen Struktur eines medicast-Objekts und drei darin enthaltenen Objekten](images/mediacast1.gif)

<span data-ttu-id="cab4a-124">Die Verweise auf das Audioobjekt werden in der [WPD- \_ Objekt \_ Verweis](object-properties.md) Eigenschaft für das Mediacast-Objekt angegeben.</span><span class="sxs-lookup"><span data-stu-id="cab4a-124">The references to the audio object are specified in the [WPD\_OBJECT\_REFERENCES](object-properties.md) property for the Mediacast object.</span></span> <span data-ttu-id="cab4a-125">Weitere Informationen zu den Eigenschaften, die von einem Mediacast-Objekt unterstützt werden, finden Sie im Thema zum [**WPD- \_ \_ Inhaltstyp \_ Media \_ Cast**](wpd-content-type-media-cast.md) .</span><span class="sxs-lookup"><span data-stu-id="cab4a-125">For more information about the properties supported by a Mediacast object, see the [**WPD\_CONTENT\_TYPE\_MEDIA\_CAST**](wpd-content-type-media-cast.md) topic.</span></span>

### <a name="properties"></a><span data-ttu-id="cab4a-126">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="cab4a-126">Properties</span></span>

<span data-ttu-id="cab4a-127">Objekteigenschaften bieten einen Mechanismus zum Austauschen von Objekt beschreibenden Metadaten.</span><span class="sxs-lookup"><span data-stu-id="cab4a-127">Object properties provide a mechanism for exchanging object-describing metadata.</span></span> <span data-ttu-id="cab4a-128">Ein Image-Objekt kann z. b. Eigenschaften enthalten, die den Dateinamen, die Größe, das Format, die Breite in Pixel usw. beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cab4a-128">For example, an image object may include properties that describe its filename, size, format, width in pixels, and so on.</span></span>

<span data-ttu-id="cab4a-129">Eigenschaften verfügen über einen aktuellen Wert sowie über Attribute.</span><span class="sxs-lookup"><span data-stu-id="cab4a-129">Properties have a current value, as well as attributes.</span></span> <span data-ttu-id="cab4a-130">WPD definiert einen Satz von Standardeigenschaften, die die API-und DDI-Definitionen bilden.</span><span class="sxs-lookup"><span data-stu-id="cab4a-130">WPD defines a set of standard properties that make up the API and DDI definitions.</span></span> <span data-ttu-id="cab4a-131">Anbieter sind nicht auf die vordefinierten WPD-Eigenschaften beschränkt und können Ihre eigenen Eigenschaften hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-131">Vendors are not limited to the predefined WPD properties and are free to add their own.</span></span>

### <a name="property-attributes"></a><span data-ttu-id="cab4a-132">Eigenschaftenattribute</span><span class="sxs-lookup"><span data-stu-id="cab4a-132">Property Attributes</span></span>

<span data-ttu-id="cab4a-133">Eigenschafts Attribute beschreiben die Zugriffsrechte, gültige Werte und andere Informationen, die sich auf eine Eigenschaft beziehen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-133">Property attributes describe the access rights, valid values, and other information related to a property.</span></span> <span data-ttu-id="cab4a-134">Beispielsweise könnte die Eigenschaft, die die Bitrate darstellt, ein Bereich von 8 kbit pro Sekunde (Kbit/s) bis 20 kbit/s mit einem Schrittwert von 1 Kbit/s sein.</span><span class="sxs-lookup"><span data-stu-id="cab4a-134">For example, the property representing bit rate could be a range from 8 kilobits per second (Kbps) to 20 Kbps with a step value of 1 Kbps.</span></span>

<span data-ttu-id="cab4a-135">Zugriffsrechte geben an, ob Aufrufer die Eigenschaft lesen, schreiben und/oder löschen können.</span><span class="sxs-lookup"><span data-stu-id="cab4a-135">Access rights indicate whether callers can read, write and/or delete the property.</span></span> <span data-ttu-id="cab4a-136">Gültige Werte geben Einschränkungen für Eigenschaftswerte an.</span><span class="sxs-lookup"><span data-stu-id="cab4a-136">Valid values indicate restrictions for property values.</span></span> <span data-ttu-id="cab4a-137">Gültige Werte werden als ein bestimmtes Formular bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cab4a-137">Valid values are said to be of a specific form.</span></span> <span data-ttu-id="cab4a-138">Gültige Wert Formulare enthalten den Bereich (d. h. die Eigenschaft kann einen Wert von "min" auf "Max" mit dem angegebenen Schritt annehmen), die Enumeration (der Eigenschafts Wert ist einer der in der angegebenen Liste) und "None" (d. h. es sind keine spezifischen gültigen Werte vorhanden).</span><span class="sxs-lookup"><span data-stu-id="cab4a-138">Valid value forms include Range (that is, property can take a value from Min to Max with specified Step), Enumeration (that is, property value is one of those in the specified List), and None (that is, there are no specific valid values).</span></span>

### <a name="resources"></a><span data-ttu-id="cab4a-139">Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cab4a-139">Resources</span></span>

<span data-ttu-id="cab4a-140">Ressourcen sind Platzhalter für Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="cab4a-140">Resources are placeholders for binary data.</span></span> <span data-ttu-id="cab4a-141">Ein Objekt kann mehr als eine Ressource aufweisen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-141">An object can have more than one resource.</span></span> <span data-ttu-id="cab4a-142">Wenn das Objekt z. b. eine Bilddatei mit einer Audioanmerkung darstellt, können die Ressourcen für dieses Objekt wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="cab4a-142">For example, if the object represented an image file with an audio annotation, then the resources for this object might be as follows:</span></span>

-   <span data-ttu-id="cab4a-143">Eine Standardressource.</span><span class="sxs-lookup"><span data-stu-id="cab4a-143">A default resource.</span></span> <span data-ttu-id="cab4a-144">Diese Ressource stellt die gesamte Bilddatei dar.</span><span class="sxs-lookup"><span data-stu-id="cab4a-144">This resource represents the entire image file.</span></span> <span data-ttu-id="cab4a-145">(Dies schließt alle eingebetteten Daten ein, z. b. Audioanmerkungen, Miniaturansichten usw.)</span><span class="sxs-lookup"><span data-stu-id="cab4a-145">(This includes any embedded data such as audio annotations, thumbnails, and so on)</span></span>
-   <span data-ttu-id="cab4a-146">Eine Miniatur Ansichts Ressource.</span><span class="sxs-lookup"><span data-stu-id="cab4a-146">A thumbnail resource.</span></span> <span data-ttu-id="cab4a-147">Diese Ressource stellt die Miniaturansicht für das Bild dar.</span><span class="sxs-lookup"><span data-stu-id="cab4a-147">This resource represents the thumbnail data for the image.</span></span>
-   <span data-ttu-id="cab4a-148">Eine audioannotation-Ressource.</span><span class="sxs-lookup"><span data-stu-id="cab4a-148">An audio annotation resource.</span></span> <span data-ttu-id="cab4a-149">Diese Ressource stellt die Audiodaten dar, die dem Bild zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="cab4a-149">This resource represents the audio data associated with the image.</span></span>

### <a name="resource-attributes"></a><span data-ttu-id="cab4a-150">Ressourcen Attribute</span><span class="sxs-lookup"><span data-stu-id="cab4a-150">Resource Attributes</span></span>

<span data-ttu-id="cab4a-151">Ähnlich wie Eigenschafts Attribute beschreiben Ressourcen Attribute die Zugriffsrechte, die Größe, das Format und andere Informationen zu einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="cab4a-151">Similar to property attributes, resource attributes describe the access rights, size, format, and other information related to a resource.</span></span> <span data-ttu-id="cab4a-152">Beispielsweise können die Attribute für eine audioannotation-Ressource auf einem Image-Objekt die Bitrate, die Kanalanzahl und das Datenformat der Audiodatei angeben.</span><span class="sxs-lookup"><span data-stu-id="cab4a-152">For example, the attributes for an audio annotation resource on an image object may specify the bit rate, channel count, and data format of the audio.</span></span>

### <a name="rendering-profiles-and-resource-attributes"></a><span data-ttu-id="cab4a-153">Renderingprofile und Ressourcen Attribute</span><span class="sxs-lookup"><span data-stu-id="cab4a-153">Rendering Profiles and Resource Attributes</span></span>

<span data-ttu-id="cab4a-154">Das renderingprofil ist eine Methode, die von Anwendungen verwendet wird, um die gültigen Attribute für eine bestimmte Ressource zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="cab4a-154">The rendering profile is one method that applications use to discover the valid attributes for a given resource.</span></span> <span data-ttu-id="cab4a-155">Ein Mobiltelefon kann z. b. Bitmaps mit spezifischen Einschränkungen der minimalen und maximalen Width-und Height-Werte unterstützen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-155">For example, a mobile phone may support bitmaps with specific restrictions on the minimum and maximum width and height values.</span></span> <span data-ttu-id="cab4a-156">Durch Abfragen der renderingprofile für das Bitmap-Objekt kann eine Anwendung diese exakten Werte abrufen.</span><span class="sxs-lookup"><span data-stu-id="cab4a-156">By querying the rendering profiles for the bitmap object, an application can retrieve those exact values.</span></span>

<span data-ttu-id="cab4a-157">Die folgende Beispielausgabe identifiziert die renderingprofilinformationen, die das Gerät zurückgeben würde, wenn es Bitmaps mit einer Mindesthöhe von 10 Pixeln, eine minimale Breite von 20 Pixeln, eine maximale Höhe von 1000 Pixel und eine maximale Breite von 2000 Pixel unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cab4a-157">The following sample output identifies the rendering profile information that the device would return if it supported bitmaps with a minimum height of 10 pixels, a minimum width of 20 pixels, a maximum height of 1000 pixels and a maximum width of 2000 pixels.</span></span>


```C++
WPD_OBJECT_FORMAT = WPD_OBJECT_FORMAT_BMP
WPD_MEDIA_HEIGHT:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  10
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  10 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_MEDIA_WIDTH:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  20 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX =  2000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE:
        WPD_PROPERTY_ATTRIBUTE_FORM = WPD_PROPERTY_ATTRIBUTE_FORM_RANGE
        WPD_PROPERTY_ATTRIBUTE_DEFAULT_VALUE = 0
        WPD_PROPERTY_ATTRIBUTE_RANGE_MIN =  2000 
        WPD_PROPERTY_ATTRIBUTE_RANGE_MAX = 1000000
        WPD_PROPERTY_ATTRIBUTE_RANGE_STEP = 1
```



<span data-ttu-id="cab4a-158">Eine Beschreibung, wie Ihre Anwendung ein renderingprofil (und die zugehörigen Ressourcen Attribute) abrufen kann, finden Sie im Thema zum Abrufen [der von einem Gerät unterstützten Renderingfunktionen](retrieving-the-rendering-capabilities-supported-by-a-device.md) im-Programmier Handbuch.</span><span class="sxs-lookup"><span data-stu-id="cab4a-158">See the [Retrieving the Rendering Capabilities Supported by a Device](retrieving-the-rendering-capabilities-supported-by-a-device.md) topic in the programming guide for a description of how your application can retrieve a rendering profile (and the associated resource attributes).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cab4a-159">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cab4a-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cab4a-160">**Anwendungs Übersicht**</span><span class="sxs-lookup"><span data-stu-id="cab4a-160">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



