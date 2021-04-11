---
description: Kontaktgruppe für WPD- \_ \_ Inhaltstyp \_ \_
ms.assetid: ddebb789-7e60-4728-a0a4-94c06d8a98f9
title: WPD_CONTENT_TYPE_CONTACT_GROUP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43b9db8d82807f854ee6cf04e4654228631eb1f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217496"
---
# <a name="wpd_content_type_contact_group"></a><span data-ttu-id="ae68a-103">Kontaktgruppe für WPD- \_ \_ Inhaltstyp \_ \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-103">WPD\_CONTENT\_TYPE\_CONTACT\_GROUP</span></span>

<span data-ttu-id="ae68a-104">Ein-Objekt, das den Typ der WPD- \_ \_ Inhaltstyp- \_ Kontaktgruppe beschreibt, \_ stellt eine Gruppe von Kontakten dar.</span><span class="sxs-lookup"><span data-stu-id="ae68a-104">An object that describes its type as WPD\_CONTENT\_TYPE\_CONTACT\_GROUP represents a group of contacts.</span></span> <span data-ttu-id="ae68a-105">Die WPD- \_ Objekt Verweise dieses Objekts \_ enthalten eine Liste von Objekt-IDs für verschiedene Contact-Objekte des WPD- \_ Inhalts \_ Typs \_ .</span><span class="sxs-lookup"><span data-stu-id="ae68a-105">This object's WPD\_OBJECT\_REFERENCES contains a list of object IDs for various WPD\_CONTENT\_TYPE\_CONTACT objects.</span></span>

<span data-ttu-id="ae68a-106">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ae68a-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="ae68a-107">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="ae68a-107">Property Name</span></span>                                                                                                         | <span data-ttu-id="ae68a-108">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="ae68a-108">Required or Optional</span></span>                                                  |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="ae68a-109">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="ae68a-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="ae68a-110">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae68a-110">Required.</span></span>                                                             |
| [<span data-ttu-id="ae68a-111">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="ae68a-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="ae68a-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae68a-112">Required.</span></span>                                                             |
| [<span data-ttu-id="ae68a-113">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="ae68a-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="ae68a-114">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae68a-114">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="ae68a-115">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="ae68a-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="ae68a-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae68a-116">Required.</span></span>                                                             |
| [<span data-ttu-id="ae68a-117">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="ae68a-117">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="ae68a-118">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae68a-118">Required.</span></span>                                                             |
| [<span data-ttu-id="ae68a-119">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-119">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="ae68a-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ae68a-120">Required.</span></span>                                                             |
| [<span data-ttu-id="ae68a-121">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="ae68a-121">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="ae68a-122">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="ae68a-122">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="ae68a-123">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="ae68a-123">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="ae68a-124">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="ae68a-124">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="ae68a-125">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="ae68a-125">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="ae68a-126">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="ae68a-126">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="ae68a-127">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="ae68a-127">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="ae68a-128">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="ae68a-128">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="ae68a-129">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="ae68a-129">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="ae68a-130">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="ae68a-130">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="ae68a-131">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-131">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="ae68a-132">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="ae68a-132">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="ae68a-133">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="ae68a-133">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="ae68a-134">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-134">Optional.</span></span>                                                             |
| [<span data-ttu-id="ae68a-135">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="ae68a-135">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="ae68a-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-136">Optional.</span></span>                                                             |
| [<span data-ttu-id="ae68a-137">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="ae68a-137">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="ae68a-138">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="ae68a-138">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="ae68a-139">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-139">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="ae68a-140">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-140">Optional.</span></span>                                                             |
| [<span data-ttu-id="ae68a-141">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="ae68a-141">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="ae68a-142">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="ae68a-142">Recommended.</span></span>                                                          |
| [<span data-ttu-id="ae68a-143">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-143">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="ae68a-144">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-144">Optional.</span></span>                                                             |
| [<span data-ttu-id="ae68a-145">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="ae68a-145">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="ae68a-146">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="ae68a-146">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="ae68a-147">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="ae68a-147">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="ae68a-148">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-148">Optional.</span></span>                                                             |
| [<span data-ttu-id="ae68a-149">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="ae68a-149">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="ae68a-150">Optional</span><span class="sxs-lookup"><span data-stu-id="ae68a-150">Optional</span></span>                                                              |
| [<span data-ttu-id="ae68a-151">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="ae68a-151">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="ae68a-152">Erforderlich, wenn das Objekt gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="ae68a-152">Required if the object can be deleted.</span></span>                                |
| [<span data-ttu-id="ae68a-153">Gebiets Schema der WPD- \_ Objekt \_ Sprache \_</span><span class="sxs-lookup"><span data-stu-id="ae68a-153">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="ae68a-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="ae68a-154">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="ae68a-155">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae68a-155">Typical Resources</span></span>

<span data-ttu-id="ae68a-156">Keine.</span><span class="sxs-lookup"><span data-stu-id="ae68a-156">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ae68a-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ae68a-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ae68a-158">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="ae68a-158">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



