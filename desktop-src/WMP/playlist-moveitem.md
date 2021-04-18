---
title: Playlist. muveitem-Methode
description: Die Methode "muveitem" ändert den Speicherort eines Elements in der Wiedergabeliste.
ms.assetid: 82a8de86-4419-48a7-89f8-f7b9084b51d4
keywords:
- Windows-Media Player für die Windows-
- muveitem-Methode, Windows Media Player, Wiedergabelisten Klasse
- Wiedergabelisten-Klasse, Windows Media Player, Methode "muveitem"
topic_type:
- apiref
api_name:
- Playlist.moveItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06e2e48b2987af4becd8c07357ff2eecf137f31d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354776"
---
# <a name="playlistmoveitem-method"></a><span data-ttu-id="0f6ae-106">Playlist. muveitem-Methode</span><span class="sxs-lookup"><span data-stu-id="0f6ae-106">Playlist.moveItem method</span></span>

<span data-ttu-id="0f6ae-107">Die Methode " **muveitem** " ändert den Speicherort eines Elements in der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-107">The **moveItem** method changes the location of an item in the playlist.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f6ae-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0f6ae-108">Syntax</span></span>


```JScript
Playlist.moveItem(
  oldIndex,
  newIndex
)
```



## <a name="parameters"></a><span data-ttu-id="0f6ae-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0f6ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f6ae-110">*OldIndex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0f6ae-110">*oldIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6ae-111">Die **Zahl** (**Long**), die den alten Index enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-111">**Number** (**long**) containing the old index.</span></span>

</dd> <dt>

<span data-ttu-id="0f6ae-112">" *nwindex* \[ " in\]</span><span class="sxs-lookup"><span data-stu-id="0f6ae-112">*newIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f6ae-113">**Zahl** (**Long**), die den neuen Index enthält.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-113">**Number** (**long**) containing the new index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f6ae-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0f6ae-114">Return value</span></span>

<span data-ttu-id="0f6ae-115">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-115">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f6ae-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0f6ae-116">Remarks</span></span>

<span data-ttu-id="0f6ae-117">In der Bibliothek gespeicherte Wiedergabelisten können sich außerhalb des Steuer Elements ändern.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-117">Playlists stored in the library can change outside your control.</span></span> <span data-ttu-id="0f6ae-118">Achten Sie darauf, alle entsprechenden Wiedergabelisten bezogenen Ereignisse zu überwachen und zu verarbeiten, sodass die Reihenfolge der Elemente in der Wiedergabeliste nicht unerwartet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-118">Be sure to monitor and handle all appropriate playlist-related events so that the order of items in the playlist does not change unexpectedly.</span></span>

<span data-ttu-id="0f6ae-119">Um diese Methode verwenden zu können, ist der vollständige Zugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-119">To use this method, full access to the library is required.</span></span> <span data-ttu-id="0f6ae-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="0f6ae-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f6ae-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0f6ae-121">Requirements</span></span>



| <span data-ttu-id="0f6ae-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0f6ae-122">Requirement</span></span> | <span data-ttu-id="0f6ae-123">Wert</span><span class="sxs-lookup"><span data-stu-id="0f6ae-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0f6ae-124">Version</span><span class="sxs-lookup"><span data-stu-id="0f6ae-124">Version</span></span><br/> | <span data-ttu-id="0f6ae-125">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0f6ae-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0f6ae-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0f6ae-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="0f6ae-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f6ae-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f6ae-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0f6ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f6ae-129">**Wiedergabelisten Objekt**</span><span class="sxs-lookup"><span data-stu-id="0f6ae-129">**Playlist Object**</span></span>](playlist-object.md)
</dt> <dt>

[<span data-ttu-id="0f6ae-130">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0f6ae-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="0f6ae-131">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="0f6ae-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





