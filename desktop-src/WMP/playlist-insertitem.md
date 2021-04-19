---
title: Wiedergabe. InsertItem-Methode
description: Die InsertItem-Methode fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.
ms.assetid: c186abc4-0a15-49d2-bbc4-5660e8cc0a4b
keywords:
- InsertItem-Methode, Windows-Media Player
- InsertItem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, InsertItem-Methode
topic_type:
- apiref
api_name:
- Playlist.insertItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a456b7a359d59958ce7693cc48c16eabba435621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367450"
---
# <a name="playlistinsertitem-method"></a><span data-ttu-id="d5395-106">Wiedergabe. InsertItem-Methode</span><span class="sxs-lookup"><span data-stu-id="d5395-106">Playlist.insertItem method</span></span>

<span data-ttu-id="d5395-107">Die **InsertItem** -Methode fügt ein Medien Element an der angegebenen Position in die Wiedergabeliste ein.</span><span class="sxs-lookup"><span data-stu-id="d5395-107">The **insertItem** method inserts a media item into the playlist at the specified location.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5395-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5395-108">Syntax</span></span>


```JScript
Playlist.insertItem(
  index,
  item
)
```



## <a name="parameters"></a><span data-ttu-id="d5395-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5395-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5395-110">*Index* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5395-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5395-111">**Zahl** (**Long**), die den Index enthält, an dem das Element hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5395-111">**Number** (**long**) containing the index at which to add the item.</span></span>

</dd> <dt>

<span data-ttu-id="d5395-112">*Element* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d5395-112">*item* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5395-113">**Medien** Objekt, das eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d5395-113">**Media** object to insert.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5395-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5395-114">Return value</span></span>

<span data-ttu-id="d5395-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5395-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5395-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5395-116">Remarks</span></span>

<span data-ttu-id="d5395-117">Alle Elemente nach dem eingefügten Element werden die Indexnummern um 1 erhöhen.</span><span class="sxs-lookup"><span data-stu-id="d5395-117">All items after the inserted item will have their index numbers increased by one.</span></span>

<span data-ttu-id="d5395-118">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d5395-118">To use this method, full access to the library is required.</span></span> <span data-ttu-id="d5395-119">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="d5395-119">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d5395-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5395-120">Requirements</span></span>



| <span data-ttu-id="d5395-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5395-121">Requirement</span></span> | <span data-ttu-id="d5395-122">Wert</span><span class="sxs-lookup"><span data-stu-id="d5395-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5395-123">Version</span><span class="sxs-lookup"><span data-stu-id="d5395-123">Version</span></span><br/> | <span data-ttu-id="d5395-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d5395-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d5395-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d5395-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="d5395-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5395-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5395-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5395-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5395-128">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="d5395-128">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="d5395-129">**Wiedergabeliste. Element**</span><span class="sxs-lookup"><span data-stu-id="d5395-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="d5395-130">**Wiedergabeliste. RemoveItem**</span><span class="sxs-lookup"><span data-stu-id="d5395-130">**Playlist.removeItem**</span></span>](playlist-removeitem.md)
</dt> <dt>

[<span data-ttu-id="d5395-131">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="d5395-131">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="d5395-132">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="d5395-132">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





