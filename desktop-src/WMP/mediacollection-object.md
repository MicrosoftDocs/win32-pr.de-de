---
title: Mediacollection-Objekt
description: Das mediacollection-Objekt bietet eine Möglichkeit, eine große Sammlung von Medien Elementen zu organisieren. Sie kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.
ms.assetid: afcb2c51-3ecb-4529-8f3e-56aa6d0ec2b4
keywords:
- Mediacollection-Objekt, Windows Media Player
topic_type:
- apiref
api_name:
- MediaCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2232e3590acd371039494b31c5d592c2e00f0199
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "106341281"
---
# <a name="mediacollection-object"></a><span data-ttu-id="3dd6d-105">Mediacollection-Objekt</span><span class="sxs-lookup"><span data-stu-id="3dd6d-105">MediaCollection Object</span></span>

<span data-ttu-id="3dd6d-106">Das **mediacollection** -Objekt bietet eine Möglichkeit, eine große Sammlung von Medien Elementen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-106">The **MediaCollection** object provides a way to organize a large collection of media items.</span></span> <span data-ttu-id="3dd6d-107">Sie kann abgefragt werden, um Wiedergabelisten automatisch zu generieren.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-107">It can be queried to generate playlists automatically.</span></span>

<span data-ttu-id="3dd6d-108">Das **mediacollection** -Objekt unterstützt die folgenden Methoden.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-108">The **MediaCollection** object supports the following methods.</span></span>



| <span data-ttu-id="3dd6d-109">Methode</span><span class="sxs-lookup"><span data-stu-id="3dd6d-109">Method</span></span>                                                                           | <span data-ttu-id="3dd6d-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3dd6d-110">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3dd6d-111">add</span><span class="sxs-lookup"><span data-stu-id="3dd6d-111">add</span></span>](mediacollection-add.md)                                                   | <span data-ttu-id="3dd6d-112">Fügt der Bibliothek ein neues Medien Element oder eine neue Wiedergabeliste hinzu.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-112">Adds a new media item or playlist to the library.</span></span>                                                                                                              |
| [<span data-ttu-id="3dd6d-113">createQuery</span><span class="sxs-lookup"><span data-stu-id="3dd6d-113">createQuery</span></span>](mediacollection-createquery.md)                                   | <span data-ttu-id="3dd6d-114">Erstellt ein neues [Abfrage](query-object.md) Objekt.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-114">Creates a new [Query](query-object.md) object.</span></span>                                                                                                                |
| [<span data-ttu-id="3dd6d-115">"GetAll"</span><span class="sxs-lookup"><span data-stu-id="3dd6d-115">getAll</span></span>](mediacollection-getall.md)                                             | <span data-ttu-id="3dd6d-116">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das alle Medienelemente in der Bibliothek enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-116">Retrieves a [Playlist](playlist-object.md) object containing all media items in the library.</span></span>                                                                  |
| [<span data-ttu-id="3dd6d-117">getAttributeStringCollection</span><span class="sxs-lookup"><span data-stu-id="3dd6d-117">getAttributeStringCollection</span></span>](mediacollection-getattributestringcollection.md) | <span data-ttu-id="3dd6d-118">Ruft ein [StringCollection](stringcollection-object.md) -Objekt ab, das den Satz aller Werte für ein angegebenes Attribut innerhalb eines angegebenen Medientyps darstellt.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-118">Retrieves a [StringCollection](stringcollection-object.md) object representing the set of all values for a specified attribute within a specified media type.</span></span> |
| [<span data-ttu-id="3dd6d-119">getbyalbum</span><span class="sxs-lookup"><span data-stu-id="3dd6d-119">getByAlbum</span></span>](mediacollection-getbyalbum.md)                                     | <span data-ttu-id="3dd6d-120">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente aus dem angegebenen Album enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-120">Retrieves a [Playlist](playlist-object.md) object containing media items from the specified album.</span></span>                                                            |
| [<span data-ttu-id="3dd6d-121">getbyattribute</span><span class="sxs-lookup"><span data-stu-id="3dd6d-121">getByAttribute</span></span>](mediacollection-getbyattribute.md)                             | <span data-ttu-id="3dd6d-122">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen-Wert mit dem angegebenen-Wert enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-122">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified attribute having the specified value.</span></span>                             |
| [<span data-ttu-id="3dd6d-123">getbyattributeandmediatype</span><span class="sxs-lookup"><span data-stu-id="3dd6d-123">getByAttributeAndMediaType</span></span>](mediacollection-getbyattributeandmediatype.md)     | <span data-ttu-id="3dd6d-124">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das [Medien](media-object.md) Objekte mit dem angegebenen Attribut und Medientyp enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-124">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects having the specified attribute and media type.</span></span>                 |
| [<span data-ttu-id="3dd6d-125">getbyauthor</span><span class="sxs-lookup"><span data-stu-id="3dd6d-125">getByAuthor</span></span>](mediacollection-getbyauthor.md)                                   | <span data-ttu-id="3dd6d-126">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente vom angegebenen Autor enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-126">Retrieves a [Playlist](playlist-object.md) object containing media items by the specified author.</span></span>                                                             |
| [<span data-ttu-id="3dd6d-127">getByGenre</span><span class="sxs-lookup"><span data-stu-id="3dd6d-127">getByGenre</span></span>](mediacollection-getbygenre.md)                                     | <span data-ttu-id="3dd6d-128">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen Genre enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-128">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified genre.</span></span>                                                            |
| [<span data-ttu-id="3dd6d-129">getByName</span><span class="sxs-lookup"><span data-stu-id="3dd6d-129">getByName</span></span>](mediacollection-getbyname.md)                                       | <span data-ttu-id="3dd6d-130">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das Medienelemente mit dem angegebenen Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-130">Retrieves a [Playlist](playlist-object.md) object containing media items with the specified name.</span></span>                                                             |
| [<span data-ttu-id="3dd6d-131">getmediaatom</span><span class="sxs-lookup"><span data-stu-id="3dd6d-131">getMediaAtom</span></span>](mediacollection-getmediaatom.md)                                 | <span data-ttu-id="3dd6d-132">Ruft den Index ab, an dem sich eine angegebene Eigenschaft innerhalb des Satzes verfügbarer Eigenschaften befindet.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-132">Retrieves the index at which a specified property resides within the set of available properties.</span></span>                                                              |
| [<span data-ttu-id="3dd6d-133">getplaylistbyquery</span><span class="sxs-lookup"><span data-stu-id="3dd6d-133">getPlaylistByQuery</span></span>](mediacollection-getplaylistbyquery.md)                     | <span data-ttu-id="3dd6d-134">Ruft ein [Wiedergabe](playlist-object.md) Listen Objekt ab, das [Media](media-object.md) -Objekte enthält, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-134">Retrieves a [Playlist](playlist-object.md) object containing [Media](media-object.md) objects that match the query conditions.</span></span>                               |
| [<span data-ttu-id="3dd6d-135">getstringcollectionbyquery</span><span class="sxs-lookup"><span data-stu-id="3dd6d-135">getStringCollectionByQuery</span></span>](mediacollection-getstringcollectionbyquery.md)     | <span data-ttu-id="3dd6d-136">Ruft ein [StringCollection](stringcollection-object.md) -Objekt ab, das Zeichen folgen enthält, die den Abfragebedingungen entsprechen.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-136">Retrieves a [StringCollection](stringcollection-object.md) object containing strings that match the query conditions.</span></span>                                         |
| [<span data-ttu-id="3dd6d-137">isDeleted</span><span class="sxs-lookup"><span data-stu-id="3dd6d-137">isDeleted</span></span>](mediacollection-isdeleted.md)                                       | <span data-ttu-id="3dd6d-138">Ruft einen Wert ab, der angibt, ob sich das angegebene Medien Element im Ordner "Gelöschte Elemente" befindet.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-138">Retrieves a value indicating whether the specified media item is in the deleted items folder.</span></span>                                                                  |
| [<span data-ttu-id="3dd6d-139">remove</span><span class="sxs-lookup"><span data-stu-id="3dd6d-139">remove</span></span>](mediacollection-remove.md)                                             | <span data-ttu-id="3dd6d-140">Entfernt ein Element aus der Medien Auflistung.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-140">Removes an item from the media collection.</span></span>                                                                                                                     |
| [<span data-ttu-id="3dd6d-141">SetDeleted</span><span class="sxs-lookup"><span data-stu-id="3dd6d-141">setDeleted</span></span>](mediacollection-setdeleted.md)                                     | <span data-ttu-id="3dd6d-142">Verschiebt das angegebene Medien Element in den Ordner "Gelöschte Elemente".</span><span class="sxs-lookup"><span data-stu-id="3dd6d-142">Moves the specified media item to the deleted items folder.</span></span>                                                                                                    |



 

<span data-ttu-id="3dd6d-143">Der Zugriff auf das **mediacollection** -Objekt erfolgt über die folgende Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="3dd6d-143">The **MediaCollection** object is accessed through the following property.</span></span>



| <span data-ttu-id="3dd6d-144">Object</span><span class="sxs-lookup"><span data-stu-id="3dd6d-144">Object</span></span>                      | <span data-ttu-id="3dd6d-145">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3dd6d-145">Property</span></span>                                      |
|-----------------------------|-----------------------------------------------|
| [<span data-ttu-id="3dd6d-146">Player</span><span class="sxs-lookup"><span data-stu-id="3dd6d-146">Player</span></span>](player-object.md) | [<span data-ttu-id="3dd6d-147">mediacollection</span><span class="sxs-lookup"><span data-stu-id="3dd6d-147">mediaCollection</span></span>](player-mediacollection.md) |



 

## <a name="see-also"></a><span data-ttu-id="3dd6d-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3dd6d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3dd6d-149">**Objektmodell Referenz für die Skripterstellung**</span><span class="sxs-lookup"><span data-stu-id="3dd6d-149">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




