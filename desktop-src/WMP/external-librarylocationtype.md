---
title: Extern. librarylocationtype
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. librarylocationtype
ms.assetid: aaf20147-8331-40bd-a5cd-5ee9b8e2d022
keywords:
- Externe. librarylocationtype-Windows-Media Player
topic_type:
- apiref
api_name:
- External.libraryLocationType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2c2f14940a2ad41bed24493396e2bacfba2f0a1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360280"
---
# <a name="externallibrarylocationtype"></a><span data-ttu-id="ab388-105">Extern. librarylocationtype</span><span class="sxs-lookup"><span data-stu-id="ab388-105">External.libraryLocationType</span></span>

> [!Note]  
> <span data-ttu-id="ab388-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="ab388-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="ab388-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ab388-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="ab388-108">Die **librarylocationtype** -Eigenschaft ruft eine [Bibliotheks Speicherort Konstante](library-location-constants.md) ab, die den Typ der aktuellen Ansicht in Windows Media Player angibt.</span><span class="sxs-lookup"><span data-stu-id="ab388-108">The **libraryLocationType** property retrieves a [library location constant](library-location-constants.md) that indicates the type of the current view in Windows Media Player.</span></span>

``` syntax
window.external.libraryLocationType
      
```

## <a name="possible-values"></a><span data-ttu-id="ab388-109">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="ab388-109">Possible Values</span></span>

<span data-ttu-id="ab388-110">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die eine der Bibliotheks Speicherort Konstanten enthält.</span><span class="sxs-lookup"><span data-stu-id="ab388-110">This property is a read-only **String** that contains one of the library location constants.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab388-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ab388-111">Remarks</span></span>

<span data-ttu-id="ab388-112">Diese Eigenschaft funktioniert in Kombination mit der [externen. librarylocationid](external-librarylocationid.md) -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="ab388-112">This property works in combination with the [External.libraryLocationID](external-librarylocationid.md) property.</span></span> <span data-ttu-id="ab388-113">Nehmen wir beispielsweise an, dass **librarylocationtype** gleich cpalbumid und **librarylocationid** gleich 3 ist.</span><span class="sxs-lookup"><span data-stu-id="ab388-113">For example, suppose **libraryLocationType** is equal to CPAlbumID and **libraryLocationID** is equal to 3.</span></span> <span data-ttu-id="ab388-114">Dies bedeutet, dass die aktuelle Ansicht in Windows Media Player das Album mit der ID 3 anzeigt.</span><span class="sxs-lookup"><span data-stu-id="ab388-114">That means the current view in Windows Media Player is showing the album that has an ID of 3.</span></span> <span data-ttu-id="ab388-115">Weitere Informationen zur kennzeichnen von Ansichten von Online Store-Inhalten durch Windows Media Player finden Sie unter [Standort und ausgewähltes Element](location-and-selected-item.md).</span><span class="sxs-lookup"><span data-stu-id="ab388-115">For more information about how Windows Media Player characterizes views of online store content, see [Location and Selected Item](location-and-selected-item.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab388-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ab388-116">Requirements</span></span>



| <span data-ttu-id="ab388-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ab388-117">Requirement</span></span> | <span data-ttu-id="ab388-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ab388-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ab388-119">Version</span><span class="sxs-lookup"><span data-stu-id="ab388-119">Version</span></span><br/> | <span data-ttu-id="ab388-120">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="ab388-120">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="ab388-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ab388-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="ab388-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab388-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab388-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab388-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab388-124">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="ab388-124">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="ab388-125">**Extern. librarylocationid**</span><span class="sxs-lookup"><span data-stu-id="ab388-125">**External.libraryLocationID**</span></span>](external-librarylocationid.md)
</dt> <dt>

[<span data-ttu-id="ab388-126">**Speicherort und ausgewähltes Element**</span><span class="sxs-lookup"><span data-stu-id="ab388-126">**Location and Selected Item**</span></span>](location-and-selected-item.md)
</dt> </dl>

 

 





