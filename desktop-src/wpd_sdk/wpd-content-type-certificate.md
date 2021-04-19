---
description: WPD \_ - \_ Inhaltstyp \_ Zertifikat
ms.assetid: 5fcaf17b-f583-4ba7-aec3-cdb02dbf3bbc
title: WPD_CONTENT_TYPE_CERTIFICATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde0ff631cd8eed28226d1e374d84e65d9756b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349609"
---
# <a name="wpd_content_type_certificate"></a><span data-ttu-id="e2616-103">WPD \_ - \_ Inhaltstyp \_ Zertifikat</span><span class="sxs-lookup"><span data-stu-id="e2616-103">WPD\_CONTENT\_TYPE\_CERTIFICATE</span></span>

<span data-ttu-id="e2616-104">Ein Objekt, das den Typ als WPD \_ - \_ Inhaltstyp Zertifikat beschreibt, \_ stellt ein für die Authentifizierung verwendetes Zertifikat dar.</span><span class="sxs-lookup"><span data-stu-id="e2616-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CERTIFICATE represents a certificate used for authentication.</span></span>

<span data-ttu-id="e2616-105">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e2616-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="e2616-106">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="e2616-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="e2616-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="e2616-107">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="e2616-108">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="e2616-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="e2616-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-109">Required.</span></span>                                                             |
| [<span data-ttu-id="e2616-110">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="e2616-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="e2616-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-111">Required.</span></span>                                                             |
| [<span data-ttu-id="e2616-112">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="e2616-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="e2616-113">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2616-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="e2616-114">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="e2616-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="e2616-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-115">Required.</span></span>                                                             |
| [<span data-ttu-id="e2616-116">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="e2616-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="e2616-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-117">Required.</span></span>                                                             |
| [<span data-ttu-id="e2616-118">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="e2616-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="e2616-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-119">Required.</span></span>                                                             |
| [<span data-ttu-id="e2616-120">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="e2616-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="e2616-121">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="e2616-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="e2616-122">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="e2616-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="e2616-123">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="e2616-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="e2616-124">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="e2616-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="e2616-125">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="e2616-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="e2616-126">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="e2616-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="e2616-127">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2616-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="e2616-128">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="e2616-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="e2616-129">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="e2616-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="e2616-130">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="e2616-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="e2616-131">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="e2616-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="e2616-132">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="e2616-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="e2616-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-134">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="e2616-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="e2616-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-136">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="e2616-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="e2616-137">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="e2616-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="e2616-138">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="e2616-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="e2616-139">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-140">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="e2616-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="e2616-141">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="e2616-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="e2616-142">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="e2616-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="e2616-143">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-144">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="e2616-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="e2616-145">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="e2616-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="e2616-146">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="e2616-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="e2616-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-148">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="e2616-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="e2616-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="e2616-150">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="e2616-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="e2616-151">Erforderlich, wenn das Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2616-151">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="e2616-152">Gebiets Schema der WPD- \_ Objekt \_ Sprache \_</span><span class="sxs-lookup"><span data-stu-id="e2616-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="e2616-153">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="e2616-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="e2616-154">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2616-154">Typical Resources</span></span>

<span data-ttu-id="e2616-155">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="e2616-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="e2616-156">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="e2616-156">Resource Name</span></span>                                          | <span data-ttu-id="e2616-157">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="e2616-157">Required or Optional</span></span> | <span data-ttu-id="e2616-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2616-158">Description</span></span>        |
|--------------------------------------------------------|----------------------|--------------------|
| [<span data-ttu-id="e2616-159">**WPD- \_ Ressourcen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="e2616-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="e2616-160">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e2616-160">Required.</span></span>            | <span data-ttu-id="e2616-161">Enthält die Daten.</span><span class="sxs-lookup"><span data-stu-id="e2616-161">Contains the data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="e2616-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2616-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2616-163">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="e2616-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



