---
title: Extern. librarylocationid
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. librarylocationid
ms.assetid: 9a9bea89-c05c-4759-be22-86588bbeca2c
keywords:
- Externe. librarylocationid-Windows-Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89f411ad8575bc7419cf9300d1aab46073ee869c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355888"
---
# <a name="externallibrarylocationid"></a><span data-ttu-id="82cf7-105">Extern. librarylocationid</span><span class="sxs-lookup"><span data-stu-id="82cf7-105">External.libraryLocationID</span></span>

> [!Note]  
> <span data-ttu-id="82cf7-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="82cf7-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="82cf7-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="82cf7-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="82cf7-108">Die **librarylocationid** -Eigenschaft ruft den Bezeichner des bestimmten Medien Elements ab, das momentan in der Ansicht des Players angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="82cf7-108">The **libraryLocationID** property retrieves the identifier of the specific media item that is currently displayed in the Player's view.</span></span>

``` syntax
window.external.libraryLocationID
      
```

## <a name="possible-values"></a><span data-ttu-id="82cf7-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="82cf7-109">Possible Values</span></span>

<span data-ttu-id="82cf7-110">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="82cf7-110">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="82cf7-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82cf7-111">Remarks</span></span>

<span data-ttu-id="82cf7-112">Diese Eigenschaft funktioniert in Kombination mit der Eigenschaft " [extern. librarylocationtype](external-librarylocationtype.md) ".</span><span class="sxs-lookup"><span data-stu-id="82cf7-112">This property works in combination with the [External.libraryLocationType](external-librarylocationtype.md) property.</span></span> <span data-ttu-id="82cf7-113">Nehmen wir beispielsweise an, dass **librarylocationtype** gleich cpalbumid und **librarylocationid** gleich 3 ist.</span><span class="sxs-lookup"><span data-stu-id="82cf7-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="82cf7-114">Dies bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 anzeigt.</span><span class="sxs-lookup"><span data-stu-id="82cf7-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="82cf7-115">Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="82cf7-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

<span data-ttu-id="82cf7-116">Bestimmte Sichten in Windows-Media Player sind einem bestimmten Medien Element zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82cf7-116">Certain views in Windows Media Player are associated with a particular media item.</span></span> <span data-ttu-id="82cf7-117">Wenn die aktuelle Ansicht z. b. ein einzelnes Album darstellt, ist **librarylocationtype** gleich cpalbumid, und **librarylocationid** ist die ID des Albums.</span><span class="sxs-lookup"><span data-stu-id="82cf7-117">For example, if the current view represents an individual album, **libraryLocationType** is equal to CPAlbumID, and **libraryLocationID** is the ID of the album.</span></span> <span data-ttu-id="82cf7-118">Andere Sichten sind keinem bestimmten Medien Element zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="82cf7-118">Other views are not associated with any particular media item.</span></span> <span data-ttu-id="82cf7-119">Wenn die aktuelle Ansicht z. b. Alle Alben darstellt, ist **librarylocationtype** gleich allcpalbumids, aber es gibt keinen sinnvollen Wert, der **librarylocationid** zugewiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="82cf7-119">For example, if the current view represents all albums, **libraryLocationType** is equal to AllCPAlbumIDs, but there is no meaningful value that can be assigned to **libraryLocationID**.</span></span> <span data-ttu-id="82cf7-120">In Fällen, in denen die **librarylocationid** -Eigenschaft keinen sinnvollen Wert hat, entspricht Sie der leeren Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="82cf7-120">In cases where the **libraryLocationID** property has no meaningful value, it is equal to the empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="82cf7-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82cf7-121">Requirements</span></span>



| <span data-ttu-id="82cf7-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82cf7-122">Requirement</span></span> | <span data-ttu-id="82cf7-123">Wert</span><span class="sxs-lookup"><span data-stu-id="82cf7-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="82cf7-124">Version</span><span class="sxs-lookup"><span data-stu-id="82cf7-124">Version</span></span><br/> | <span data-ttu-id="82cf7-125">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="82cf7-125">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="82cf7-126">DLL</span><span class="sxs-lookup"><span data-stu-id="82cf7-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="82cf7-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82cf7-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82cf7-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82cf7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82cf7-129">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="82cf7-129">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="82cf7-130">**Extern. librarylocationtype**</span><span class="sxs-lookup"><span data-stu-id="82cf7-130">**External.libraryLocationType**</span></span>](external-librarylocationtype.md)
</dt> <dt>

[<span data-ttu-id="82cf7-131">**Speicherort und ausgewähltes Element**</span><span class="sxs-lookup"><span data-stu-id="82cf7-131">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





