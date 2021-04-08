---
description: WPD \_ - \_ Inhaltstyp \_ Programm
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0187d4e87f47e8210e94a676ca9ccd1e1364cf1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758437"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="fb3cf-103">WPD \_ - \_ Inhaltstyp \_ Programm</span><span class="sxs-lookup"><span data-stu-id="fb3cf-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="fb3cf-104">Ein-Objekt, das den Typ als WPD- \_ Inhaltstyp Programm beschreibt, das \_ \_ ein ausführbares Programm darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="fb3cf-105">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                                    |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3cf-106">**Eigenschaftenname**</span><span class="sxs-lookup"><span data-stu-id="fb3cf-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="fb3cf-107">**Erforderlich oder optional**</span><span class="sxs-lookup"><span data-stu-id="fb3cf-107">**Required or Optional**</span></span>                                                           |
| [<span data-ttu-id="fb3cf-108">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="fb3cf-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="fb3cf-109">Erforderlich, jedoch schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-109">Required, but read-only.</span></span> <span data-ttu-id="fb3cf-110">Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="fb3cf-111">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="fb3cf-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="fb3cf-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-113">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="fb3cf-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="fb3cf-114">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="fb3cf-115">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="fb3cf-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="fb3cf-116">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-116">Required, read-only.</span></span> <span data-ttu-id="fb3cf-117">Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="fb3cf-118">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="fb3cf-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="fb3cf-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-120">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="fb3cf-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="fb3cf-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-122">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="fb3cf-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="fb3cf-123">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="fb3cf-124">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="fb3cf-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="fb3cf-125">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="fb3cf-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="fb3cf-126">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="fb3cf-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="fb3cf-127">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="fb3cf-128">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="fb3cf-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="fb3cf-129">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="fb3cf-130">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="fb3cf-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="fb3cf-131">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="fb3cf-132">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="fb3cf-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="fb3cf-133">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="fb3cf-134">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="fb3cf-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="fb3cf-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-136">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="fb3cf-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="fb3cf-137">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-138">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="fb3cf-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="fb3cf-139">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="fb3cf-140">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="fb3cf-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="fb3cf-141">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-142">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="fb3cf-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="fb3cf-143">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="fb3cf-144">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="fb3cf-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="fb3cf-145">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-146">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="fb3cf-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="fb3cf-147">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="fb3cf-148">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="fb3cf-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="fb3cf-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-150">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="fb3cf-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="fb3cf-151">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="fb3cf-152">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="fb3cf-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="fb3cf-153">Erforderlich, wenn das Objekt nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="fb3cf-154">Gebiets Schema der WPD- \_ Objekt \_ Sprache \_</span><span class="sxs-lookup"><span data-stu-id="fb3cf-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="fb3cf-155">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="fb3cf-156">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fb3cf-156">Typical Resources</span></span>

<span data-ttu-id="fb3cf-157">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="fb3cf-158">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="fb3cf-158">Resource Name</span></span>                                          | <span data-ttu-id="fb3cf-159">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="fb3cf-159">Required or Optional</span></span> | <span data-ttu-id="fb3cf-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fb3cf-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="fb3cf-161">**WPD- \_ Ressourcen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="fb3cf-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="fb3cf-162">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-162">Required.</span></span>            | <span data-ttu-id="fb3cf-163">Enthält die Programmdatei.</span><span class="sxs-lookup"><span data-stu-id="fb3cf-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="fb3cf-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fb3cf-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fb3cf-165">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="fb3cf-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



