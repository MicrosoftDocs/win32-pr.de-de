---
description: '\_ \_ WPD-INHALTSTYPPROGRAMM \_'
ms.assetid: 81eaf8cf-0f4f-4587-911a-063630af1c8e
title: WPD_CONTENT_TYPE_PROGRAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ddf3c5d406c16891c692e84fb37c4d21757f702
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423770"
---
# <a name="wpd_content_type_program"></a><span data-ttu-id="ba83f-103">\_ \_ WPD-INHALTSTYPPROGRAMM \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-103">WPD\_CONTENT\_TYPE\_PROGRAM</span></span>

<span data-ttu-id="ba83f-104">Ein Objekt, das seinen Typ als WPD CONTENT TYPE PROGRAM beschreibt, \_ \_ stellt ein \_ ausführbares Programm dar.</span><span class="sxs-lookup"><span data-stu-id="ba83f-104">An object that describes its type as WPD\_CONTENT\_TYPE\_PROGRAM represents an executable program.</span></span>

<span data-ttu-id="ba83f-105">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ba83f-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="ba83f-106">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="ba83f-106">Property Name</span></span>     | <span data-ttu-id="ba83f-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="ba83f-107">Required or Optional</span></span>      |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [<span data-ttu-id="ba83f-108">\_ \_ WPD-OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="ba83f-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="ba83f-109">Erforderlich, aber schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ba83f-109">Required, but read-only.</span></span> <span data-ttu-id="ba83f-110">Ein Client kann diese Eigenschaft auch zur Erstellungszeit nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba83f-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="ba83f-111">ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="ba83f-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="ba83f-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba83f-112">Required.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-113">\_WPD-OBJEKTNAME \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="ba83f-114">Erforderlich, wenn das -Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba83f-114">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="ba83f-115">\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS</span><span class="sxs-lookup"><span data-stu-id="ba83f-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="ba83f-116">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ba83f-116">Required, read-only.</span></span> <span data-ttu-id="ba83f-117">Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="ba83f-117">A client cannot set this property even at creation time.</span></span>      |
| [<span data-ttu-id="ba83f-118">\_WPD-OBJEKTFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-118">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="ba83f-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba83f-119">Required.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-120">\_ \_ WPD-OBJEKTINHALTSTYP \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-120">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="ba83f-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba83f-121">Required.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-122">\_WPD-OBJEKT \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="ba83f-122">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="ba83f-123">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ba83f-123">Required if the object is hidden.</span></span>                                                  |
| [<span data-ttu-id="ba83f-124">WPD \_ OBJECT \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="ba83f-124">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="ba83f-125">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="ba83f-125">Required if the object is a system object (represents a system file).</span></span>              |
| [<span data-ttu-id="ba83f-126">\_WPD-OBJEKTGRÖßE \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-126">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="ba83f-127">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="ba83f-127">Required if the object has at least one resource.</span></span>                                  |
| [<span data-ttu-id="ba83f-128">\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME</span><span class="sxs-lookup"><span data-stu-id="ba83f-128">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="ba83f-129">Erforderlich, wenn das -Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba83f-129">Required if the object represents a file.</span></span>                                          |
| [<span data-ttu-id="ba83f-130">\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR</span><span class="sxs-lookup"><span data-stu-id="ba83f-130">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="ba83f-131">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="ba83f-131">Recommended if the object is not meant for consumption by the device.</span></span>              |
| [<span data-ttu-id="ba83f-132">\_ \_ WPD-OBJEKTVERWEISE</span><span class="sxs-lookup"><span data-stu-id="ba83f-132">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="ba83f-133">Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="ba83f-133">Required if the object has references to other objects.</span></span>                            |
| [<span data-ttu-id="ba83f-134">\_WPD-OBJEKTSCHLÜSSELWÖRTER \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-134">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="ba83f-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-135">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-136">\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-136">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="ba83f-137">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-137">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-138">\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT</span><span class="sxs-lookup"><span data-stu-id="ba83f-138">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="ba83f-139">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="ba83f-139">Required if the object is protected by DRM technology.</span></span>                             |
| [<span data-ttu-id="ba83f-140">ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-140">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="ba83f-141">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-141">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-142">\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT</span><span class="sxs-lookup"><span data-stu-id="ba83f-142">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="ba83f-143">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ba83f-143">Recommended.</span></span>                                                                       |
| [<span data-ttu-id="ba83f-144">ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-144">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="ba83f-145">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-145">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-146">WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)</span><span class="sxs-lookup"><span data-stu-id="ba83f-146">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="ba83f-147">Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ba83f-147">Recommended if the object is referenced by another object.</span></span>                         |
| [<span data-ttu-id="ba83f-148">\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="ba83f-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="ba83f-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-149">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-150">\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHT AUS \_ RESSOURCE</span><span class="sxs-lookup"><span data-stu-id="ba83f-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="ba83f-151">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-151">Optional.</span></span>                                                                          |
| [<span data-ttu-id="ba83f-152">\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN</span><span class="sxs-lookup"><span data-stu-id="ba83f-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="ba83f-153">Erforderlich, wenn das Objekt nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="ba83f-153">Required if the object cannot be deleted.</span></span>                                          |
| [<span data-ttu-id="ba83f-154">\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_</span><span class="sxs-lookup"><span data-stu-id="ba83f-154">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="ba83f-155">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ba83f-155">Optional.</span></span>                                                                          |



 

## <a name="typical-resources"></a><span data-ttu-id="ba83f-156">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ba83f-156">Typical Resources</span></span>

<span data-ttu-id="ba83f-157">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="ba83f-157">These objects typically include the following resources.</span></span>



| <span data-ttu-id="ba83f-158">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="ba83f-158">Resource Name</span></span>                                          | <span data-ttu-id="ba83f-159">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="ba83f-159">Required or Optional</span></span> | <span data-ttu-id="ba83f-160">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba83f-160">Description</span></span>                |
|--------------------------------------------------------|----------------------|----------------------------|
| [<span data-ttu-id="ba83f-161">**\_WPD-RESSOURCENSTANDARD \_**</span><span class="sxs-lookup"><span data-stu-id="ba83f-161">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="ba83f-162">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ba83f-162">Required.</span></span>            | <span data-ttu-id="ba83f-163">Enthält die Programmdatei.</span><span class="sxs-lookup"><span data-stu-id="ba83f-163">Contains the program file.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ba83f-164">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ba83f-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba83f-165">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="ba83f-165">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



