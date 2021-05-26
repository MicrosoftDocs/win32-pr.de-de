---
description: '\_WPD-INHALTSTYP \_ \_ NICHT ANGEGEBEN'
ms.assetid: 0175940e-2de2-4e2b-a98e-8dcc59e7020f
title: WPD_CONTENT_TYPE_UNSPECIFIED
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd955ee5ebf31b2348efd3f70c85ae9c004edb83
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423680"
---
# <a name="wpd_content_type_unspecified"></a><span data-ttu-id="36a20-103">\_WPD-INHALTSTYP \_ \_ NICHT ANGEGEBEN</span><span class="sxs-lookup"><span data-stu-id="36a20-103">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span>

<span data-ttu-id="36a20-104">Ein Objekt, das seinen Typ als WPD \_ CONTENT \_ TYPE \_ UNSPECIFIED beschreibt, stellt ein generisches Objekt dar, das möglicherweise über eine zugrunde liegende physische Datei verfügt.</span><span class="sxs-lookup"><span data-stu-id="36a20-104">An object that describes its type as WPD\_CONTENT\_TYPE\_UNSPECIFIED represents a generic object that may or may not have an underlying physical file.</span></span> <span data-ttu-id="36a20-105">Der Unterschied zwischen diesem Typ und DER GENERISCHEN DATEI DES \_ \_ \_ \_ WPD-INHALTSTYPs besteht darin, dass GENERISCHE DATEIobjekte des \_ WPD-INHALTSTYPs \_ über eine zugrunde liegende physische \_ \_ Datei verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="36a20-105">The difference between this type and WPD\_CONTENT\_TYPE\_GENERIC\_FILE is that WPD\_CONTENT\_TYPE\_GENERIC\_FILE objects must have an underlying physical file.</span></span>

<span data-ttu-id="36a20-106">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="36a20-106">This type of object supports the following properties.</span></span>



| <span data-ttu-id="36a20-107">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="36a20-107">Property Name</span></span>       | <span data-ttu-id="36a20-108">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="36a20-108">Required or Optional</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="36a20-109">\_ \_ WPD-OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="36a20-109">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                                                | <span data-ttu-id="36a20-110">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="36a20-110">Required, read-only.</span></span> <span data-ttu-id="36a20-111">Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="36a20-111">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="36a20-112">ÜBERGEORDNETE \_ \_ \_ WPD-OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="36a20-112">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                                 | <span data-ttu-id="36a20-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="36a20-113">Required.</span></span>                                                                     |
| [<span data-ttu-id="36a20-114">\_WPD-OBJEKTNAME \_</span><span class="sxs-lookup"><span data-stu-id="36a20-114">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                                            | <span data-ttu-id="36a20-115">Erforderlich, wenn das -Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="36a20-115">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="36a20-116">\_PERSISTENTE EINDEUTIGE ID DES \_ \_ \_ WPD-OBJEKTS</span><span class="sxs-lookup"><span data-stu-id="36a20-116">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)                          | <span data-ttu-id="36a20-117">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="36a20-117">Required, read-only.</span></span> <span data-ttu-id="36a20-118">Ein Client kann diese Eigenschaft nicht einmal zur Erstellungszeit festlegen.</span><span class="sxs-lookup"><span data-stu-id="36a20-118">A client cannot set this property even at creation time.</span></span> |
| [<span data-ttu-id="36a20-119">\_WPD-OBJEKTFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="36a20-119">WPD\_OBJECT\_FORMAT</span></span>](object-properties.md)                                                        | <span data-ttu-id="36a20-120">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="36a20-120">Required.</span></span>                                                                     |
| [<span data-ttu-id="36a20-121">\_ \_ WPD-OBJEKTINHALTSTYP \_</span><span class="sxs-lookup"><span data-stu-id="36a20-121">WPD\_OBJECT\_CONTENT\_TYPE</span></span>](object-properties.md)                                           | <span data-ttu-id="36a20-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="36a20-122">Required.</span></span>                                                                     |
| [<span data-ttu-id="36a20-123">\_WPD-OBJEKT \_ ISHIDDEN</span><span class="sxs-lookup"><span data-stu-id="36a20-123">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                                    | <span data-ttu-id="36a20-124">Erforderlich, wenn das Objekt ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="36a20-124">Required if the object is hidden.</span></span>                                             |
| [<span data-ttu-id="36a20-125">\_WPD-OBJEKT \_ ISSYSTEM</span><span class="sxs-lookup"><span data-stu-id="36a20-125">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                                    | <span data-ttu-id="36a20-126">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="36a20-126">Required if the object is a system object (represents a system file).</span></span>         |
| [<span data-ttu-id="36a20-127">\_WPD-OBJEKTGRÖßE \_</span><span class="sxs-lookup"><span data-stu-id="36a20-127">WPD\_OBJECT\_SIZE</span></span>](object-properties.md)                                                            | <span data-ttu-id="36a20-128">Erforderlich, wenn das Objekt über mindestens eine Ressource verfügt.</span><span class="sxs-lookup"><span data-stu-id="36a20-128">Required if the object has at least one resource.</span></span>                             |
| [<span data-ttu-id="36a20-129">\_WPD-OBJEKT \_ \_ URSPRÜNGLICHER \_ DATEINAME</span><span class="sxs-lookup"><span data-stu-id="36a20-129">WPD\_OBJECT\_ORIGINAL\_FILE\_NAME</span></span>](object-properties.md)                              | <span data-ttu-id="36a20-130">Erforderlich, wenn das -Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="36a20-130">Required if the object represents a file.</span></span>                                     |
| [<span data-ttu-id="36a20-131">\_WPD-OBJEKT \_ NICHT \_ VERWENDBAR</span><span class="sxs-lookup"><span data-stu-id="36a20-131">WPD\_OBJECT\_NON\_CONSUMABLE</span></span>](object-properties.md)                                       | <span data-ttu-id="36a20-132">Empfohlen, wenn das Objekt nicht für die Verwendung durch das Gerät bestimmt ist.</span><span class="sxs-lookup"><span data-stu-id="36a20-132">Recommended if the object is not meant for consumption by the device.</span></span>         |
| [<span data-ttu-id="36a20-133">\_ \_ WPD-OBJEKTVERWEISE</span><span class="sxs-lookup"><span data-stu-id="36a20-133">WPD\_OBJECT\_REFERENCES</span></span>](object-properties.md)                                                | <span data-ttu-id="36a20-134">Erforderlich, wenn das -Objekt Verweise auf andere Objekte enthält.</span><span class="sxs-lookup"><span data-stu-id="36a20-134">Required if the object has references to other objects.</span></span>                       |
| [<span data-ttu-id="36a20-135">\_WPD-OBJEKTSCHLÜSSELWÖRTER \_</span><span class="sxs-lookup"><span data-stu-id="36a20-135">WPD\_OBJECT\_KEYWORDS</span></span>](object-properties.md)                                                    | <span data-ttu-id="36a20-136">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-136">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-137">\_ \_ WPD-OBJEKTSYNCHRONISIERUNGS-ID \_</span><span class="sxs-lookup"><span data-stu-id="36a20-137">WPD\_OBJECT\_SYNC\_ID</span></span>](object-properties.md)                                                     | <span data-ttu-id="36a20-138">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-138">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-139">\_WPD-OBJEKT \_ IST \_ \_ DRM-GESCHÜTZT</span><span class="sxs-lookup"><span data-stu-id="36a20-139">WPD\_OBJECT\_IS\_DRM\_PROTECTED</span></span>](object-properties.md)                                  | <span data-ttu-id="36a20-140">Erforderlich, wenn das Objekt durch DRM-Technologie geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="36a20-140">Required if the object is protected by DRM technology.</span></span>                        |
| [<span data-ttu-id="36a20-141">ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="36a20-141">WPD\_OBJECT\_DATE\_CREATED</span></span>](object-properties.md)                                           | <span data-ttu-id="36a20-142">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-142">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-143">\_WPD-OBJEKTDATUM \_ \_ GEÄNDERT</span><span class="sxs-lookup"><span data-stu-id="36a20-143">WPD\_OBJECT\_DATE\_MODIFIED</span></span>](object-properties.md)                                         | <span data-ttu-id="36a20-144">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="36a20-144">Recommended.</span></span>                                                                  |
| [<span data-ttu-id="36a20-145">ERSTELLUNGSDATUM \_ DES WPD-OBJEKTS \_ \_</span><span class="sxs-lookup"><span data-stu-id="36a20-145">WPD\_OBJECT\_DATE\_AUTHORED</span></span>](object-properties.md)                                         | <span data-ttu-id="36a20-146">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-146">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-147">WPD \_ OBJECT BACK REFERENCES (WPD-OBJEKTVERWEISE \_ \_ ZURÜCK)</span><span class="sxs-lookup"><span data-stu-id="36a20-147">WPD\_OBJECT\_BACK\_REFERENCES</span></span>](object-properties.md)                                                                | <span data-ttu-id="36a20-148">Wird empfohlen, wenn auf das Objekt von einem anderen Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="36a20-148">Recommended if the object is referenced by another object.</span></span>                    |
| [<span data-ttu-id="36a20-149">\_ \_ WPD-OBJEKTCONTAINER \_ FUNKTIONALE \_ \_ OBJEKT-ID</span><span class="sxs-lookup"><span data-stu-id="36a20-149">WPD\_OBJECT\_CONTAINER\_FUNCTIONAL\_OBJECT\_ID</span></span>](object-properties.md)     | <span data-ttu-id="36a20-150">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-150">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-151">\_WPD-OBJEKT \_ GENERIERT \_ \_ MINIATURANSICHTEN AUS \_ RESSOURCE</span><span class="sxs-lookup"><span data-stu-id="36a20-151">WPD\_OBJECT\_GENERATE\_THUMBNAIL\_FROM\_RESOURCE</span></span>](object-properties.md) | <span data-ttu-id="36a20-152">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-152">Optional.</span></span>                                                                     |
| [<span data-ttu-id="36a20-153">\_WPD-OBJEKT \_ KANN GELÖSCHT \_ WERDEN</span><span class="sxs-lookup"><span data-stu-id="36a20-153">WPD\_OBJECT\_CAN\_DELETE</span></span>](object-properties.md)                                                                     | <span data-ttu-id="36a20-154">Erforderlich, wenn das Objekt nicht gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="36a20-154">Required if the object cannot be deleted.</span></span>                                     |
| [<span data-ttu-id="36a20-155">\_GEBIETSSCHEMA DER WPD-OBJEKTSPRACHE \_ \_</span><span class="sxs-lookup"><span data-stu-id="36a20-155">WPD\_OBJECT\_LANGUAGE\_LOCALE</span></span>](object-properties.md)                                                                | <span data-ttu-id="36a20-156">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="36a20-156">Optional.</span></span>                                                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="36a20-157">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="36a20-157">Typical Resources</span></span>

<span data-ttu-id="36a20-158">Diese Objekte enthalten in der Regel die folgenden Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="36a20-158">These objects typically include the following resources.</span></span>



| <span data-ttu-id="36a20-159">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="36a20-159">Resource Name</span></span>                                          | <span data-ttu-id="36a20-160">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="36a20-160">Required or Optional</span></span>                             | <span data-ttu-id="36a20-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36a20-161">Description</span></span>               |
|--------------------------------------------------------|--------------------------------------------------|---------------------------|
| [<span data-ttu-id="36a20-162">**\_WPD-RESSOURCENSTANDARD \_**</span><span class="sxs-lookup"><span data-stu-id="36a20-162">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md) | <span data-ttu-id="36a20-163">Erforderlich, wenn das Objekt durch Binärdaten gesichert wird.</span><span class="sxs-lookup"><span data-stu-id="36a20-163">Required if the object is backed by binary data.</span></span> | <span data-ttu-id="36a20-164">Enthält die Binärdaten.</span><span class="sxs-lookup"><span data-stu-id="36a20-164">Contains the binary data.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="36a20-165">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36a20-165">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a20-166">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="36a20-166">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



