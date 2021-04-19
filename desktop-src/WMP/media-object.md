---
title: Medienobjekt
description: Das Medienobjekt bietet eine Möglichkeit zum angeben oder Abrufen von Eigenschaften eines Medien Elements mithilfe der folgenden Eigenschaften und Methoden.
ms.assetid: 45c1c760-808b-4d11-8e6b-057a2ca685d0
keywords:
- Windows-Media Player für Medienobjekte
topic_type:
- apiref
api_name:
- Media Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 88eff6ee0a97e63df6a0c073ef18425cbb576e85
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341277"
---
# <a name="media-object"></a><span data-ttu-id="34b62-104">Medienobjekt</span><span class="sxs-lookup"><span data-stu-id="34b62-104">Media Object</span></span>

<span data-ttu-id="34b62-105">Das **Medien** Objekt bietet eine Möglichkeit zum angeben oder Abrufen von Eigenschaften eines Medien Elements mithilfe der folgenden Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="34b62-105">The **Media** object provides a way to specify or retrieve properties of a media item, using the following properties and methods.</span></span>

<span data-ttu-id="34b62-106">Das **Medien** Objekt unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="34b62-106">The **Media** object supports the following properties.</span></span>



| <span data-ttu-id="34b62-107">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="34b62-107">Property</span></span>                                         | <span data-ttu-id="34b62-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34b62-108">Description</span></span>                                                                                        |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34b62-109">AttributeCount</span><span class="sxs-lookup"><span data-stu-id="34b62-109">attributeCount</span></span>](media-attributecount.md)       | <span data-ttu-id="34b62-110">Ruft die Anzahl der Attribute ab, die abgefragt und/oder für das Medien Element festgelegt werden können.</span><span class="sxs-lookup"><span data-stu-id="34b62-110">Retrieves the number of attributes that can be queried and/or set for the media item.</span></span>              |
| [<span data-ttu-id="34b62-111">duration</span><span class="sxs-lookup"><span data-stu-id="34b62-111">duration</span></span>](media-duration.md)                   | <span data-ttu-id="34b62-112">Ruft die Dauer des aktuellen Medien Elements in Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-112">Retrieves the duration in seconds of the current media item.</span></span>                                       |
| [<span data-ttu-id="34b62-113">durationString</span><span class="sxs-lookup"><span data-stu-id="34b62-113">durationString</span></span>](media-durationstring.md)       | <span data-ttu-id="34b62-114">Ruft einen **Zeichen** folgen Wert ab, der die Dauer des aktuellen Medien Elements im Format "hh: mm: SS" angibt.</span><span class="sxs-lookup"><span data-stu-id="34b62-114">Retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span> |
| [<span data-ttu-id="34b62-115">error</span><span class="sxs-lookup"><span data-stu-id="34b62-115">error</span></span>](media-error.md)                         | <span data-ttu-id="34b62-116">Ruft ein [ErrorItem](erroritem-object.md) -Objekt ab, wenn das Medien Element einen Fehlerzustand aufweist.</span><span class="sxs-lookup"><span data-stu-id="34b62-116">Retrieves an [ErrorItem](erroritem-object.md) object if the media item has an error condition.</span></span>    |
| [<span data-ttu-id="34b62-117">imagesourceheight</span><span class="sxs-lookup"><span data-stu-id="34b62-117">imageSourceHeight</span></span>](media-imagesourceheight.md) | <span data-ttu-id="34b62-118">Ruft die Höhe des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-118">Retrieves the height of the current media item in pixels.</span></span>                                          |
| [<span data-ttu-id="34b62-119">imagesourcewidth</span><span class="sxs-lookup"><span data-stu-id="34b62-119">imageSourceWidth</span></span>](media-imagesourcewidth.md)   | <span data-ttu-id="34b62-120">Ruft die Breite des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-120">Retrieves the width of the current media item in pixels.</span></span>                                           |
| [<span data-ttu-id="34b62-121">markercount</span><span class="sxs-lookup"><span data-stu-id="34b62-121">markerCount</span></span>](media-markercount.md)             | <span data-ttu-id="34b62-122">Ruft die Anzahl der Marker im Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-122">Retrieves the number of markers in the media item.</span></span>                                                 |
| [<span data-ttu-id="34b62-123">name</span><span class="sxs-lookup"><span data-stu-id="34b62-123">name</span></span>](media-name.md)                           | <span data-ttu-id="34b62-124">Gibt den Namen des Medien Elements an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-124">Specifies or retrieves the name of the media item.</span></span>                                                 |
| [<span data-ttu-id="34b62-125">SourceURL</span><span class="sxs-lookup"><span data-stu-id="34b62-125">sourceURL</span></span>](media-sourceurl.md)                 | <span data-ttu-id="34b62-126">Ruft die URL des Medien Elements ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-126">Retrieves the URL of the media item.</span></span>                                                               |



 

<span data-ttu-id="34b62-127">Das **Medien** Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="34b62-127">The **Media** object supports the following methods.</span></span>



| <span data-ttu-id="34b62-128">Methode</span><span class="sxs-lookup"><span data-stu-id="34b62-128">Method</span></span>                                                       | <span data-ttu-id="34b62-129">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="34b62-129">Description</span></span>                                                                                              |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34b62-130">getattributecountrytbytype</span><span class="sxs-lookup"><span data-stu-id="34b62-130">getAttributeCountByType</span></span>](media-getattributecountbytype.md) | <span data-ttu-id="34b62-131">Ruft die Anzahl der Attribute ab, die dem angegebenen Attributnamen und der Sprache zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="34b62-131">Retrieves the number of attributes associated with the specified attribute name and language.</span></span>            |
| [<span data-ttu-id="34b62-132">GetAttributeName</span><span class="sxs-lookup"><span data-stu-id="34b62-132">getAttributeName</span></span>](media-getattributename.md)               | <span data-ttu-id="34b62-133">Ruft den Namen des Attributs ab, das dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="34b62-133">Retrieves the name of the attribute corresponding to the specified index.</span></span>                                |
| [<span data-ttu-id="34b62-134">getItemInfo</span><span class="sxs-lookup"><span data-stu-id="34b62-134">getItemInfo</span></span>](media-getiteminfo.md)                         | <span data-ttu-id="34b62-135">Ruft den Wert des angegebenen Attributs für das Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-135">Retrieves the value of the specified attribute for the media item.</span></span>                                       |
| [<span data-ttu-id="34b62-136">getiteminfobyatom</span><span class="sxs-lookup"><span data-stu-id="34b62-136">getItemInfoByAtom</span></span>](media-getiteminfobyatom.md)             | <span data-ttu-id="34b62-137">Ruft den Wert des Attributs mit der angegebenen Indexnummer ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-137">Retrieves the value of the attribute with the specified index number.</span></span>                                    |
| [<span data-ttu-id="34b62-138">getItemInfoByType</span><span class="sxs-lookup"><span data-stu-id="34b62-138">getItemInfoByType</span></span>](media-getiteminfobytype.md)             | <span data-ttu-id="34b62-139">Ruft den Wert des Attributs ab, das dem angegebenen Attributnamen, der angegebenen Sprache und dem angegebenen Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="34b62-139">Retrieves the value of the attribute corresponding to the specified attribute name, language, and index.</span></span> |
| [<span data-ttu-id="34b62-140">getmarkername</span><span class="sxs-lookup"><span data-stu-id="34b62-140">getMarkerName</span></span>](media-getmarkername.md)                     | <span data-ttu-id="34b62-141">Ruft den Namen des Markers am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-141">Retrieves the name of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="34b62-142">getmarkertime</span><span class="sxs-lookup"><span data-stu-id="34b62-142">getMarkerTime</span></span>](media-getmarkertime.md)                     | <span data-ttu-id="34b62-143">Ruft die Zeit des Markers am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="34b62-143">Retrieves the time of the marker at the specified index.</span></span>                                                 |
| [<span data-ttu-id="34b62-144">isidentical</span><span class="sxs-lookup"><span data-stu-id="34b62-144">isIdentical</span></span>](media-isidentical.md)                         | <span data-ttu-id="34b62-145">Ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen Objekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="34b62-145">Retrieves a value indicating whether the supplied object is the same as the current one.</span></span>                 |
| [<span data-ttu-id="34b62-146">isMemberOf</span><span class="sxs-lookup"><span data-stu-id="34b62-146">isMemberOf</span></span>](media-ismemberof.md)                           | <span data-ttu-id="34b62-147">Ruft einen Wert ab, der angibt, ob das angegebene Medien Element ein Member der angegebenen Wiedergabeliste ist.</span><span class="sxs-lookup"><span data-stu-id="34b62-147">Retrieves a value indicating whether the specified media item is a member of the specified playlist.</span></span>     |
| [<span data-ttu-id="34b62-148">isread onlyitem</span><span class="sxs-lookup"><span data-stu-id="34b62-148">isReadOnlyItem</span></span>](media-isreadonlyitem.md)                   | <span data-ttu-id="34b62-149">Ruft einen Wert ab, der angibt, ob die Attribute des angegebenen Medien Elements bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="34b62-149">Retrieves a value indicating whether the attributes of the specified media item can be edited.</span></span>           |
| [<span data-ttu-id="34b62-150">"Einstellungs Element"</span><span class="sxs-lookup"><span data-stu-id="34b62-150">setItemInfo</span></span>](media-setiteminfo.md)                         | <span data-ttu-id="34b62-151">Legt den Wert des angegebenen Attributs für das Medien Element fest.</span><span class="sxs-lookup"><span data-stu-id="34b62-151">Sets the value of the specified attribute for the media item.</span></span>                                            |



 

<span data-ttu-id="34b62-152">Der Zugriff auf das **Medien** Objekt erfolgt über die folgenden Eigenschaften und Methoden.</span><span class="sxs-lookup"><span data-stu-id="34b62-152">The **Media** object is accessed through the following properties and methods.</span></span>



| <span data-ttu-id="34b62-153">Object</span><span class="sxs-lookup"><span data-stu-id="34b62-153">Object</span></span>                          | <span data-ttu-id="34b62-154">Eigenschaft oder Methode</span><span class="sxs-lookup"><span data-stu-id="34b62-154">Property or method</span></span>                                                       |
|---------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="34b62-155">Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="34b62-155">Controls</span></span>](controls-object.md) | [<span data-ttu-id="34b62-156">currentItem</span><span class="sxs-lookup"><span data-stu-id="34b62-156">currentItem</span></span>](controls-currentitem.md)                                  |
| [<span data-ttu-id="34b62-157">Player</span><span class="sxs-lookup"><span data-stu-id="34b62-157">Player</span></span>](player-object.md)     | <span data-ttu-id="34b62-158">[currentMedia](player-currentmedia.md), [newmedia](player-newmedia.md)</span><span class="sxs-lookup"><span data-stu-id="34b62-158">[currentMedia](player-currentmedia.md), [newMedia](player-newmedia.md)</span></span> |
| [<span data-ttu-id="34b62-159">Abspielen</span><span class="sxs-lookup"><span data-stu-id="34b62-159">Playlist</span></span>](playlist-object.md) | [<span data-ttu-id="34b62-160">item</span><span class="sxs-lookup"><span data-stu-id="34b62-160">item</span></span>](playlist-item.md)                                                |



 

<span data-ttu-id="34b62-161">Da es sich um die gängigste Zugriffsmethode handelt, ist der *Player*. **currentMedia** wird zur Veranschaulichung in den Abschnitten der Referenz Syntax verwendet.</span><span class="sxs-lookup"><span data-stu-id="34b62-161">Because it is the most common means of access, *player*.**currentMedia** is used for purposes of illustration in the reference syntax sections.</span></span>

## <a name="see-also"></a><span data-ttu-id="34b62-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34b62-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34b62-163">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="34b62-163">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




