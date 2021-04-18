---
title: Player. currentmediaitemavailable-Ereignis
description: Das currentmediaitemavailable-Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird. | Player. currentmediaitemavailable-Ereignis
ms.assetid: dc692b14-67d3-4867-8f99-ddfcf7d1610c
keywords:
- Currentmediaitemavailable-Ereignisfenster Media Player
- Currentmediaitemavailable-Ereignis, Windows Media Player, Player-Klasse
- Windows Media Player Player-Klasse, currentmediaitemavailable-Ereignis
topic_type:
- apiref
api_name:
- Player.CurrentMediaItemAvailable
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7f25d085c354cf18966ec37f822a080db56cf16
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368363"
---
# <a name="playercurrentmediaitemavailable-event"></a><span data-ttu-id="1b1d9-107">Player. currentmediaitemavailable-Ereignis</span><span class="sxs-lookup"><span data-stu-id="1b1d9-107">Player.CurrentMediaItemAvailable event</span></span>

<span data-ttu-id="1b1d9-108">Das **currentmediaitemavailable** -Ereignis tritt auf, wenn ein grafisches Metadatenelement im aktuellen Medien Element verfügbar wird.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-108">The **CurrentMediaItemAvailable** event occurs when a graphic metadata item in the current media item becomes available.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b1d9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b1d9-109">Syntax</span></span>


```JScript
Player.CurrentMediaItemAvailable(
  bstrItemName
)
```



## <a name="parameters"></a><span data-ttu-id="1b1d9-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b1d9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b1d9-111">*bstritemname*</span><span class="sxs-lookup"><span data-stu-id="1b1d9-111">*bstrItemName*</span></span> 
</dt> <dd>

<span data-ttu-id="1b1d9-112">**Zeichenfolge** , die den Namen des aktuellen Medien Elements enthält.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-112">**String** containing the name of the current media item.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b1d9-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b1d9-113">Return value</span></span>

<span data-ttu-id="1b1d9-114">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-114">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b1d9-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b1d9-115">Remarks</span></span>

<span data-ttu-id="1b1d9-116">Da die Wiedergabe beginnen kann, bevor ein Medien Element vollständig heruntergeladen wird, sind alle im Medien Element enthaltenen metadatengrafiken (z. b. Albumcover Art) möglicherweise nicht verfügbar, wenn die Wiedergabe gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-116">Because playback can begin before a media item is fully downloaded, any metadata graphics contained in the media item (such as album cover art) may not be available when it starts to play.</span></span> <span data-ttu-id="1b1d9-117">Dieses Ereignis warnt Sie, wenn ein metadatengrafieelement den Download abgeschlossen hat.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-117">This event alerts you when a metadata graphic item is finished downloading.</span></span> <span data-ttu-id="1b1d9-118">Sie können dann das **Medien** Objekt abrufen, indem Sie den Wert von *bstritemname* an *mediacollection* übergeben. **getByName** -Methode, nach der Sie auf das metadatengrafieelement mithilfe von *Medien* zugreifen können. **getItemInfoByType** und Angeben von **WM/Bild** für den Attributnamen.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-118">You can then retrieve the **Media** object by passing the value of *bstrItemName* to the *MediaCollection*.**getByName** method, after which you can access the metadata graphic item by using *Media*.**getItemInfoByType** and specifying **WM/Picture** for the attribute name.</span></span>

<span data-ttu-id="1b1d9-119">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-119">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file using the parameter name given.</span></span> <span data-ttu-id="1b1d9-120">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-120">This parameter name must be typed exactly as shown, including capitalization.</span></span>

<span data-ttu-id="1b1d9-121">**Windows Media Player 10 Mobile:** Dieses Ereignis wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-121">**Windows Media Player 10 Mobile:** This event is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="1b1d9-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b1d9-122">Requirements</span></span>



| <span data-ttu-id="1b1d9-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b1d9-123">Requirement</span></span> | <span data-ttu-id="1b1d9-124">Wert</span><span class="sxs-lookup"><span data-stu-id="1b1d9-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1b1d9-125">Version</span><span class="sxs-lookup"><span data-stu-id="1b1d9-125">Version</span></span><br/> | <span data-ttu-id="1b1d9-126">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="1b1d9-126">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="1b1d9-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1b1d9-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="1b1d9-128"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b1d9-128"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b1d9-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b1d9-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b1d9-130">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="1b1d9-130">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1b1d9-131">**Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="1b1d9-131">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="1b1d9-132">**Mediacollection. getByName**</span><span class="sxs-lookup"><span data-stu-id="1b1d9-132">**MediaCollection.getByName**</span></span>](mediacollection-getbyname.md)
</dt> <dt>

[<span data-ttu-id="1b1d9-133">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="1b1d9-133">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





