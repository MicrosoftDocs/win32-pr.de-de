---
title: Player. openplayer-Methode
description: Die openplayer-Methode öffnet Windows Media Player unter Verwendung der angegebenen URL. | Player. openplayer-Methode
ms.assetid: 9ddd63c9-f4a0-490a-8543-51ad0fa74a26
keywords:
- openplayer-Methode, Windows-Media Player
- openplayer-Methode, Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, openplayer-Methode
topic_type:
- apiref
api_name:
- Player.openPlayer
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3378df48f961f1aa5e3fccec72e79b7f1c26ff08
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356427"
---
# <a name="playeropenplayer-method"></a><span data-ttu-id="a504f-107">Player. openplayer-Methode</span><span class="sxs-lookup"><span data-stu-id="a504f-107">Player.openPlayer method</span></span>

<span data-ttu-id="a504f-108">Die **openplayer** -Methode öffnet Windows Media Player unter Verwendung der angegebenen URL.</span><span class="sxs-lookup"><span data-stu-id="a504f-108">The **openPlayer** method opens Windows Media Player using the specified URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="a504f-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="a504f-109">Syntax</span></span>


```JScript
Player.openPlayer(
  URL
)
```



## <a name="parameters"></a><span data-ttu-id="a504f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a504f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a504f-111">*URL* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a504f-111">*URL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a504f-112">**Zeichenfolge** , die die URL des wieder zugebende Medien Elements darstellt.</span><span class="sxs-lookup"><span data-stu-id="a504f-112">**String** representing the URL of the media item to play.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a504f-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a504f-113">Return value</span></span>

<span data-ttu-id="a504f-114">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="a504f-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a504f-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a504f-115">Remarks</span></span>

<span data-ttu-id="a504f-116">Mit dieser Methode wird Windows Media Player gestartet, wobei der angegebene URL als Aktuelles Medien Element festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="a504f-116">This method launches Windows Media Player with the specified URL set as the current media item.</span></span> <span data-ttu-id="a504f-117">Wenn der Spieler zuvor im Skin-Modus geschlossen wurde, wird er mithilfe der Skin geöffnet, die zuletzt vom Benutzer ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="a504f-117">If the Player was previously closed in skin mode it will open using the skin last chosen by the user.</span></span> <span data-ttu-id="a504f-118">Andernfalls wird der Spieler im vollständigen Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a504f-118">Otherwise, the Player opens in full mode.</span></span>

<span data-ttu-id="a504f-119">Wenn diese Methode von einem Windows Media-playeractivex-Steuerelement aufgerufen wird, das im Remote Modus eingebettet ist, ist das Verhalten mit der *playerapplication* identisch. **switchtoplayerapplication** -Methode.</span><span class="sxs-lookup"><span data-stu-id="a504f-119">If this method is called from a Windows Media PlayerActiveX control embedded in remote mode, its behavior is identical to the *PlayerApplication*.**switchToPlayerApplication** method.</span></span>

<span data-ttu-id="a504f-120">**Windows Media Player 10 Mobile:** Diese Methode wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a504f-120">**Windows Media Player 10 Mobile:** This method is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="a504f-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a504f-121">Requirements</span></span>



| <span data-ttu-id="a504f-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a504f-122">Requirement</span></span> | <span data-ttu-id="a504f-123">Wert</span><span class="sxs-lookup"><span data-stu-id="a504f-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a504f-124">Version</span><span class="sxs-lookup"><span data-stu-id="a504f-124">Version</span></span><br/> | <span data-ttu-id="a504f-125">Windows Media Player 9 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a504f-125">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="a504f-126">DLL</span><span class="sxs-lookup"><span data-stu-id="a504f-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="a504f-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a504f-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a504f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a504f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a504f-129">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="a504f-129">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="a504f-130">**Playerapplication. switchtoplayerapplication**</span><span class="sxs-lookup"><span data-stu-id="a504f-130">**PlayerApplication.switchToPlayerApplication**</span></span>](playerapplication-switchtoplayerapplication.md)
</dt> </dl>

 

 





