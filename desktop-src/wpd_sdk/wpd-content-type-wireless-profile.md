---
description: WPD \_ - \_ Inhaltstyp \_ drahtlos \_ Profil
ms.assetid: 229f6b65-4904-41b1-bb35-8873477a272b
title: WPD_CONTENT_TYPE_WIRELESS_PROFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a327efa9e1a4cd3a1e5927da89ae4f9e7092196a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960402"
---
# <a name="wpd_content_type_wireless_profile"></a><span data-ttu-id="8d15d-103">WPD \_ - \_ Inhaltstyp \_ drahtlos \_ Profil</span><span class="sxs-lookup"><span data-stu-id="8d15d-103">WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE</span></span>

<span data-ttu-id="8d15d-104">Ein Objekt, das den Typ als WPD \_ - \_ Inhaltstyp \_ drahtlos \_ Profil beschreibt, das Informationen für den Zugriff auf ein Drahtlos Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d15d-104">An object that describes its type as WPD\_CONTENT\_TYPE\_WIRELESS\_PROFILE represents information used to access a wireless network.</span></span>

<span data-ttu-id="8d15d-105">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8d15d-105">This type of object supports the following properties.</span></span>



|                                                                                                                       |                                                                       |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span data-ttu-id="8d15d-106">**Eigenschaftenname**</span><span class="sxs-lookup"><span data-stu-id="8d15d-106">**Property Name**</span></span>                                                                                                     | <span data-ttu-id="8d15d-107">**Erforderlich oder optional**</span><span class="sxs-lookup"><span data-stu-id="8d15d-107">**Required or Optional**</span></span>                                              |
| [<span data-ttu-id="8d15d-108">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="8d15d-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="8d15d-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d15d-109">Required.</span></span>                                                             |
| [<span data-ttu-id="8d15d-110">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="8d15d-110">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="8d15d-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d15d-111">Required.</span></span>                                                             |
| [<span data-ttu-id="8d15d-112">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="8d15d-112">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="8d15d-113">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d15d-113">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="8d15d-114">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="8d15d-114">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="8d15d-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d15d-115">Required.</span></span>                                                             |
| [<span data-ttu-id="8d15d-116">WPD- \_ Objekt \_ Format</span><span class="sxs-lookup"><span data-stu-id="8d15d-116">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="8d15d-117">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d15d-117">Required.</span></span>                                                             |
| [<span data-ttu-id="8d15d-118">Inhaltstyp für WPD- \_ Objekt \_ \_</span><span class="sxs-lookup"><span data-stu-id="8d15d-118">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="8d15d-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8d15d-119">Required.</span></span>                                                             |
| [<span data-ttu-id="8d15d-120">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="8d15d-120">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="8d15d-121">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="8d15d-121">Required if the object is hidden.</span></span>                                     |
| [<span data-ttu-id="8d15d-122">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="8d15d-122">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="8d15d-123">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="8d15d-123">Required if the object is a system object (represents a system file).</span></span> |
| [<span data-ttu-id="8d15d-124">WPD- \_ Objekt \_ Größe</span><span class="sxs-lookup"><span data-stu-id="8d15d-124">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="8d15d-125">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="8d15d-125">Required if the object has at least one resource.</span></span>                     |
| [<span data-ttu-id="8d15d-126">\_ \_ ursprünglicher \_ Dateiname \_ des WPD-Objekts</span><span class="sxs-lookup"><span data-stu-id="8d15d-126">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="8d15d-127">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d15d-127">Required if the object represents a file.</span></span>                             |
| [<span data-ttu-id="8d15d-128">WPD- \_ Objekt \_ nicht \_ verwendbar</span><span class="sxs-lookup"><span data-stu-id="8d15d-128">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="8d15d-129">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="8d15d-129">Recommended if the object is not meant for consumption by the device.</span></span> |
| [<span data-ttu-id="8d15d-130">Verweise auf WPD- \_ Objekte \_</span><span class="sxs-lookup"><span data-stu-id="8d15d-130">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="8d15d-131">Erforderlich, wenn das-Objekt über Verweise auf andere-Objekte verfügt.</span><span class="sxs-lookup"><span data-stu-id="8d15d-131">Required if the object has references to other objects.</span></span>               |
| [<span data-ttu-id="8d15d-132">WPD- \_ Objekt \_ Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="8d15d-132">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="8d15d-133">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-133">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-134">WPD- \_ Objekt \_ Synchronisierungs- \_ ID</span><span class="sxs-lookup"><span data-stu-id="8d15d-134">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="8d15d-135">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-135">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-136">WPD- \_ Objekt \_ ist DRM- \_ \_ geschützt</span><span class="sxs-lookup"><span data-stu-id="8d15d-136">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="8d15d-137">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt wird.</span><span class="sxs-lookup"><span data-stu-id="8d15d-137">Required if the object is protected by DRM technology.</span></span>                |
| [<span data-ttu-id="8d15d-138">\_ \_ Erstellungsdatum des WPD-Objekts \_</span><span class="sxs-lookup"><span data-stu-id="8d15d-138">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="8d15d-139">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-139">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-140">Datum des WPD- \_ Objekts \_ \_ geändert</span><span class="sxs-lookup"><span data-stu-id="8d15d-140">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="8d15d-141">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8d15d-141">Recommended.</span></span>                                                          |
| [<span data-ttu-id="8d15d-142">erstelltes WPD- \_ Objekt \_ Datum \_</span><span class="sxs-lookup"><span data-stu-id="8d15d-142">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="8d15d-143">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-143">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-144">\_ \_ zurück \_ Verweise auf WPD-Objekte</span><span class="sxs-lookup"><span data-stu-id="8d15d-144">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="8d15d-145">Empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8d15d-145">Recommended if the object is referenced by another object.</span></span>            |
| [<span data-ttu-id="8d15d-146">\_ \_ \_ Funktions \_ Objekt- \_ ID des WPD-Objekt Containers</span><span class="sxs-lookup"><span data-stu-id="8d15d-146">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="8d15d-147">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-147">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-148">WPD \_ - \_ Objekt \_ generieren \_ der Miniaturansicht aus der \_ Ressource</span><span class="sxs-lookup"><span data-stu-id="8d15d-148">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="8d15d-149">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-149">Optional.</span></span>                                                             |
| [<span data-ttu-id="8d15d-150">WPD- \_ Objekt \_ kann \_ Löschen</span><span class="sxs-lookup"><span data-stu-id="8d15d-150">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                               | <span data-ttu-id="8d15d-151">Erforderlich, wenn das Objekt nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8d15d-151">Required if the object cannot be deleted.</span></span>                             |
| [<span data-ttu-id="8d15d-152">Gebiets Schema der WPD- \_ Objekt \_ Sprache \_</span><span class="sxs-lookup"><span data-stu-id="8d15d-152">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="8d15d-153">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d15d-153">Optional.</span></span>                                                             |



 

## <a name="typical-resources"></a><span data-ttu-id="8d15d-154">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8d15d-154">Typical Resources</span></span>

<span data-ttu-id="8d15d-155">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="8d15d-155">These objects typically include the following resources.</span></span>



| <span data-ttu-id="8d15d-156">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="8d15d-156">Resource Name</span></span>                                          | <span data-ttu-id="8d15d-157">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="8d15d-157">Required or Optional</span></span>                                  | <span data-ttu-id="8d15d-158">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d15d-158">Description</span></span>               |
|--------------------------------------------------------|-------------------------------------------------------|---------------------------|
| [<span data-ttu-id="8d15d-159">**WPD- \_ Ressourcen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="8d15d-159">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="8d15d-160">Erforderlich, wenn das Objekt durch binäre Daten dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="8d15d-160">Required if the object is represented by binary data.</span></span> | <span data-ttu-id="8d15d-161">Enthält die Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="8d15d-161">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="8d15d-162">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="8d15d-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d15d-163">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="8d15d-163">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



