---
description: Ein Objekt, das den Typ beschreibt, da der WPD- \_ \_ Inhaltstyp \_ Fernsehen eine Fernsehaufzeichnung darstellt.
ms.assetid: b8e8da1a-94a9-4540-a4eb-fe0c0cd383f9
title: WPD_CONTENT_TYPE_TELEVISION
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e5141be847c0701f8828af0de8df41b8be21e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347379"
---
# <a name="wpd_content_type_television"></a><span data-ttu-id="5d21e-103">WPD \_ - \_ Inhaltstyp \_ Fernsehen</span><span class="sxs-lookup"><span data-stu-id="5d21e-103">WPD\_CONTENT\_TYPE\_TELEVISION</span></span>

<span data-ttu-id="5d21e-104">Ein Objekt, das den Typ beschreibt, da der WPD- \_ \_ Inhaltstyp \_ Fernsehen eine Fernsehaufzeichnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d21e-104">An object that describes its type as WPD\_CONTENT\_TYPE\_TELEVISION represents a television recording.</span></span>

<span data-ttu-id="5d21e-105">Dieser Objekttyp sollte die folgenden Eigenschaften hosten.</span><span class="sxs-lookup"><span data-stu-id="5d21e-105">This type of object should host the following properties.</span></span>



| <span data-ttu-id="5d21e-106">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="5d21e-106">Property Name</span></span>                                                                                                         | <span data-ttu-id="5d21e-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="5d21e-107">Required or Optional</span></span>                                                         |
|-----------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| [<span data-ttu-id="5d21e-108">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="5d21e-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="5d21e-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d21e-109">Required.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-110">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="5d21e-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="5d21e-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d21e-111">Required.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-112">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="5d21e-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="5d21e-113">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d21e-113">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="5d21e-114">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="5d21e-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="5d21e-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d21e-115">Required.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-116">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="5d21e-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="5d21e-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d21e-117">Required.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-118">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="5d21e-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="5d21e-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5d21e-119">Required.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-120">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="5d21e-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d21e-121">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="5d21e-121">Required if the object is hidden.</span></span>                                            |
| [<span data-ttu-id="5d21e-122">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="5d21e-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d21e-123">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="5d21e-123">Required if the object is a system object (represents a system file).</span></span>        |
| [<span data-ttu-id="5d21e-124">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="5d21e-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="5d21e-125">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="5d21e-125">Required if the object has at least one resource.</span></span>                            |
| [<span data-ttu-id="5d21e-126">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="5d21e-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="5d21e-127">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="5d21e-127">Required if the object represents a file.</span></span>                                    |
| [<span data-ttu-id="5d21e-128">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="5d21e-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="5d21e-129">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="5d21e-129">Recommended if the object is not meant for consumption by the device.</span></span>        |
| [<span data-ttu-id="5d21e-130">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="5d21e-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="5d21e-131">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="5d21e-131">Required if the object has references to other objects.</span></span>                      |
| [<span data-ttu-id="5d21e-132">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="5d21e-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="5d21e-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-133">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-134">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="5d21e-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="5d21e-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-135">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-136">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="5d21e-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="5d21e-137">Erforderlich, wenn das Objekt durch Digital Rights Management-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="5d21e-137">Required if the object is protected by Digital Rights Management technology.</span></span> |
| [<span data-ttu-id="5d21e-138">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="5d21e-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="5d21e-139">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-139">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-140">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="5d21e-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="5d21e-141">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5d21e-141">Recommended.</span></span>                                                                 |
| [<span data-ttu-id="5d21e-142">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="5d21e-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="5d21e-143">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-143">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-144">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="5d21e-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                     | <span data-ttu-id="5d21e-145">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5d21e-145">Recommended if the object is referenced by another object.</span></span>                   |
| [<span data-ttu-id="5d21e-146">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="5d21e-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="5d21e-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-147">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-148">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="5d21e-148">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="5d21e-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-149">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-150">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="5d21e-150">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="5d21e-151">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="5d21e-151">Optional.</span></span>                                                                    |
| [<span data-ttu-id="5d21e-152">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="5d21e-152">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="5d21e-153">Erforderlich, wenn das Objekt nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d21e-153">Required if the object cannot be deleted.</span></span>                                    |



 

## <a name="typical-resources"></a><span data-ttu-id="5d21e-154">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d21e-154">Typical Resources</span></span>

<span data-ttu-id="5d21e-155">Keine.</span><span class="sxs-lookup"><span data-stu-id="5d21e-155">None.</span></span>

## <a name="see-also"></a><span data-ttu-id="5d21e-156">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5d21e-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d21e-157">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="5d21e-157">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



