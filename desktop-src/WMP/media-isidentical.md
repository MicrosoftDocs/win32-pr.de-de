---
title: Media. isidentical-Methode
description: Die isidentical-Methode ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist. | Media. isidentical-Methode
ms.assetid: af3266d5-4ac2-4e8c-a9f6-44f7938e9c9d
keywords:
- isidentical-Methode, Windows Media Player
- isidentical-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, isidentical-Methode
topic_type:
- apiref
api_name:
- Media.isIdentical
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196487889c075938e763c2b2305b614cffb5f09f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358603"
---
# <a name="mediaisidentical-method"></a><span data-ttu-id="772e2-107">Media. isidentical-Methode</span><span class="sxs-lookup"><span data-stu-id="772e2-107">Media.isIdentical method</span></span>

<span data-ttu-id="772e2-108">Die **isidentical** -Methode ruft einen Wert ab, der angibt, ob das angegebene Objekt mit dem aktuellen-Objekt identisch ist.</span><span class="sxs-lookup"><span data-stu-id="772e2-108">The **isIdentical** method retrieves a value indicating whether the supplied object is the same as the current one.</span></span>

## <a name="syntax"></a><span data-ttu-id="772e2-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="772e2-109">Syntax</span></span>


```JScript
bRetVal = Media.isIdentical(
  media
)
```



## <a name="parameters"></a><span data-ttu-id="772e2-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="772e2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="772e2-111">*Medien* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="772e2-111">*media* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="772e2-112">**Medien** Objekt, das mit dem aktuellen **Medien** Objekt verglichen werden soll.</span><span class="sxs-lookup"><span data-stu-id="772e2-112">**Media** object to compare with the current **Media** object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="772e2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="772e2-113">Return value</span></span>

<span data-ttu-id="772e2-114">Diese Methode gibt einen **booleschen** Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="772e2-114">This method returns a **Boolean**.</span></span>

## <a name="examples"></a><span data-ttu-id="772e2-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="772e2-115">Examples</span></span>

<span data-ttu-id="772e2-116">Im folgenden JScript-Beispiel werden *Medien* verwendet. **isidentical** , um zu überprüfen, ob ein Medien Element mit dem Namen newmedia mit dem aktuellen Medien Element identisch ist.</span><span class="sxs-lookup"><span data-stu-id="772e2-116">The following JScript example uses *Media*.**isIdentical** to check whether a media item named newMedia is the same as the current media item.</span></span> <span data-ttu-id="772e2-117">Wenn Sie nicht identisch sind, wird das neue Medien Element wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="772e2-117">If they are not the same, the new media item is played.</span></span> <span data-ttu-id="772e2-118">Andernfalls wird das aktuelle Medium weiterhin ununterbrochen abgespielt.</span><span class="sxs-lookup"><span data-stu-id="772e2-118">Otherwise, the current media continues to play uninterrupted.</span></span> <span data-ttu-id="772e2-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="772e2-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Check the new media item to see if it matches the current one.
if (newMedia.isIdentical(Player.currentMedia) != true){

   // Change the current media to the new media item.
   Player.currentMedia = newMedia;

   // Play the new media item.
   Player.controls.play();
}

```



## <a name="requirements"></a><span data-ttu-id="772e2-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="772e2-120">Requirements</span></span>



| <span data-ttu-id="772e2-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="772e2-121">Requirement</span></span> | <span data-ttu-id="772e2-122">Wert</span><span class="sxs-lookup"><span data-stu-id="772e2-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="772e2-123">Version</span><span class="sxs-lookup"><span data-stu-id="772e2-123">Version</span></span><br/> | <span data-ttu-id="772e2-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="772e2-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="772e2-125">DLL</span><span class="sxs-lookup"><span data-stu-id="772e2-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="772e2-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="772e2-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="772e2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="772e2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="772e2-128">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="772e2-128">**Media Object**</span></span>](media-object.md)
</dt> </dl>

 

 





