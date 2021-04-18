---
description: WPD \_ - \_ Inhaltstyp \_ Kalender
ms.assetid: b5fccaa8-03c7-4998-be46-82fc6aeb308b
title: WPD_CONTENT_TYPE_CALENDAR
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d202b21c0ac690c4a0b9621b876f6926c4c0efe5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351006"
---
# <a name="wpd_content_type_calendar"></a><span data-ttu-id="8daf7-103">WPD \_ - \_ Inhaltstyp \_ Kalender</span><span class="sxs-lookup"><span data-stu-id="8daf7-103">WPD\_CONTENT\_TYPE\_CALENDAR</span></span>

<span data-ttu-id="8daf7-104">Ein-Objekt, das den Typ beschreibt, weil der WPD- \_ \_ Inhaltstyp \_ Kalender einen Kalender darstellt.</span><span class="sxs-lookup"><span data-stu-id="8daf7-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CALENDAR represents a calendar.</span></span> <span data-ttu-id="8daf7-105">Bei dem Objekt kann es sich um eine Datei mit Kalenderinformationen oder einem Ordner handeln, der andere Kalender bezogene Objekte (z. b. Tasks, Termine usw.) enthält.</span><span class="sxs-lookup"><span data-stu-id="8daf7-105">The object can be a file that contains calendar information or a folder that contains other calendar-related objects, such as tasks, appointments, and so on.</span></span>

<span data-ttu-id="8daf7-106">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8daf7-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="8daf7-107">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="8daf7-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="8daf7-108">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="8daf7-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="8daf7-109">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="8daf7-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="8daf7-110">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8daf7-110">Required.</span></span>                                                             |
| [<span data-ttu-id="8daf7-111">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="8daf7-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="8daf7-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8daf7-112">Required.</span></span>                                                             |
| [<span data-ttu-id="8daf7-113">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="8daf7-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="8daf7-114">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="8daf7-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="8daf7-115">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="8daf7-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="8daf7-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8daf7-116">Required.</span></span>                                                             |
| [<span data-ttu-id="8daf7-117">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="8daf7-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="8daf7-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8daf7-118">Required.</span></span>                                                             |
| [<span data-ttu-id="8daf7-119">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="8daf7-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="8daf7-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8daf7-120">Required.</span></span>                                                             |
| [<span data-ttu-id="8daf7-121">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="8daf7-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="8daf7-122">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="8daf7-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="8daf7-123">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="8daf7-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="8daf7-124">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="8daf7-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="8daf7-125">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="8daf7-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="8daf7-126">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="8daf7-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="8daf7-127">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="8daf7-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="8daf7-128">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="8daf7-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="8daf7-129">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="8daf7-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="8daf7-130">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="8daf7-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="8daf7-131">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="8daf7-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="8daf7-132">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="8daf7-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="8daf7-133">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="8daf7-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="8daf7-134">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-135">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="8daf7-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="8daf7-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-137">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="8daf7-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="8daf7-138">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="8daf7-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="8daf7-139">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="8daf7-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="8daf7-140">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-141">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="8daf7-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="8daf7-142">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8daf7-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="8daf7-143">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="8daf7-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="8daf7-144">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-145">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="8daf7-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="8daf7-146">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8daf7-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="8daf7-147">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="8daf7-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="8daf7-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-149">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="8daf7-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="8daf7-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-150">Optional.</span></span>                                                             |
| [<span data-ttu-id="8daf7-151">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="8daf7-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="8daf7-152">Erforderlich, wenn das Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8daf7-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="8daf7-153">Gebiets Schema der WPD- \_ Objekt \_ Sprache \_</span><span class="sxs-lookup"><span data-stu-id="8daf7-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="8daf7-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8daf7-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="8daf7-155">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8daf7-155">Typical Resources</span></span>

<span data-ttu-id="8daf7-156">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8daf7-156">These objects typically include the following resources.</span></span>



| <span data-ttu-id="8daf7-157">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="8daf7-157">Resource Name</span></span>                                          | <span data-ttu-id="8daf7-158">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="8daf7-158">Required or Optional</span></span>                             | <span data-ttu-id="8daf7-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8daf7-159">Description</span></span>        |
|--------------------------------------------------------|--------------------------------------------------|--------------------|
| [<span data-ttu-id="8daf7-160">**WPD- \_ Ressourcen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="8daf7-160">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="8daf7-161">Erforderlich, wenn das Objekt durch binäre Daten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8daf7-161">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="8daf7-162">Enthält die Daten.</span><span class="sxs-lookup"><span data-stu-id="8daf7-162">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8daf7-163">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8daf7-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8daf7-164">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="8daf7-164">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



