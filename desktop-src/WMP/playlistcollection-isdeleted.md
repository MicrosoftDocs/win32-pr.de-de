---
title: Playlistcollection. IsDeleted-Methode
description: Die IsDeleted-Methode ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.
ms.assetid: 5023927a-5d1a-4b61-8122-476947d537c4
keywords:
- IsDeleted-Methode (Windows Media Player)
- IsDeleted-Methode, Windows Media Player, playlistcollection-Klasse
- Playlistcollection-Klasse, Windows Media Player, IsDeleted-Methode
topic_type:
- apiref
api_name:
- PlaylistCollection.isDeleted
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fed3e7e8ff41f23d0f9f741ea99f3382d20532e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371175"
---
# <a name="playlistcollectionisdeleted-method"></a><span data-ttu-id="a1965-106">Playlistcollection. IsDeleted-Methode</span><span class="sxs-lookup"><span data-stu-id="a1965-106">PlaylistCollection.isDeleted method</span></span>

<span data-ttu-id="a1965-107">Die **isDeleted** -Methode ruft einen Wert ab, der angibt, ob sich die angegebene Wiedergabeliste im Ordner "Gelöschte Elemente" befindet.</span><span class="sxs-lookup"><span data-stu-id="a1965-107">The **isDeleted** method retrieves a value indicating whether the specified playlist is in the deleted items folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1965-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1965-108">Syntax</span></span>


```JScript
bRetVal = PlaylistCollection.isDeleted(
  playlist
)
```



## <a name="parameters"></a><span data-ttu-id="a1965-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1965-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1965-110">*Wiedergabeliste* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1965-110">*playlist* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1965-111">Das **Wiedergabe** Listen Objekt, nach dem gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="a1965-111">The **Playlist** object to be searched for.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1965-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a1965-112">Return value</span></span>

<span data-ttu-id="a1965-113">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a1965-113">This method returns a **Boolean**.</span></span>

<span data-ttu-id="a1965-114">**Windows Media Player 10 Mobile**: Diese Methode gibt immer **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="a1965-114">**Windows Media Player 10 Mobile**: This method always returns **false**.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1965-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a1965-115">Requirements</span></span>



| <span data-ttu-id="a1965-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a1965-116">Requirement</span></span> | <span data-ttu-id="a1965-117">Wert</span><span class="sxs-lookup"><span data-stu-id="a1965-117">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1965-118">Version</span><span class="sxs-lookup"><span data-stu-id="a1965-118">Version</span></span><br/> | <span data-ttu-id="a1965-119">Windows Media Player Version 7,0, Windows Media Player Version 7,1 oder Windows Media Player für Windows XP.</span><span class="sxs-lookup"><span data-stu-id="a1965-119">Windows Media Player version 7.0, Windows Media Player version 7.1, or Windows Media Player for Windows XP.</span></span> <span data-ttu-id="a1965-120">Diese Methode wird für Windows Media Player 9-Serie oder höher nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a1965-120">This method is not supported for Windows Media Player 9 Series or later.</span></span><br/> |
| <span data-ttu-id="a1965-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a1965-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a1965-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1965-122"><dt>Wmp.dll</dt></span></span> </dl>                                                                                                              |



## <a name="see-also"></a><span data-ttu-id="a1965-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a1965-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1965-124">**Playlistcollection-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a1965-124">**PlaylistCollection Object**</span></span>](playlistcollection-object.md)
</dt> </dl>

 

 





