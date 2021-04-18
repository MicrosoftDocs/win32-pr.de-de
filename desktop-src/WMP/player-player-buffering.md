---
title: Player. buffereing-Ereignis
description: Das bufferingereignis tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet. | Player. buffereing-Ereignis
ms.assetid: a0a09bf7-19bc-4838-a403-924e8d83b48d
keywords:
- Media Player für die Pufferung von Ereignis Fenstern
- Puffer Ereignis Windows Media Player, Player-Klasse
- Player-Klasse, Windows Media Player, pufferungsereignis
topic_type:
- apiref
api_name:
- Player.Buffering
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a73ac77f9b8e81162a6cc0f9220562caba26eae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358044"
---
# <a name="playerbuffering-event"></a><span data-ttu-id="fbaa3-107">Player. buffereing-Ereignis</span><span class="sxs-lookup"><span data-stu-id="fbaa3-107">Player.Buffering event</span></span>

<span data-ttu-id="fbaa3-108">Das **bufferingereignis** tritt auf, wenn das Windows Media Player-Steuerelement die Pufferung oder den Download beendet.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-108">The **Buffering** event occurs when the Windows Media Player control begins or ends buffering or downloading.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbaa3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbaa3-109">Syntax</span></span>


```JScript
Player.Buffering(
  Start
)
```



## <a name="parameters"></a><span data-ttu-id="fbaa3-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbaa3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbaa3-111">*Starten*</span><span class="sxs-lookup"><span data-stu-id="fbaa3-111">*Start*</span></span> 
</dt> <dd>

<span data-ttu-id="fbaa3-112">**Boolescher** Wert, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-112">**Boolean** containing one of the following values.</span></span>



| <span data-ttu-id="fbaa3-113">Wert</span><span class="sxs-lookup"><span data-stu-id="fbaa3-113">Value</span></span> | <span data-ttu-id="fbaa3-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbaa3-114">Description</span></span>            |
|-------|------------------------|
| <span data-ttu-id="fbaa3-115">true</span><span class="sxs-lookup"><span data-stu-id="fbaa3-115">true</span></span>  | <span data-ttu-id="fbaa3-116">Die Pufferung wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-116">Buffering has started.</span></span> |
| <span data-ttu-id="fbaa3-117">false</span><span class="sxs-lookup"><span data-stu-id="fbaa3-117">false</span></span> | <span data-ttu-id="fbaa3-118">Die Pufferung wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-118">Buffering has ended.</span></span>   |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbaa3-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbaa3-119">Return value</span></span>

<span data-ttu-id="fbaa3-120">Dieses Ereignis gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-120">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbaa3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fbaa3-121">Remarks</span></span>

<span data-ttu-id="fbaa3-122">Verwenden Sie dieses Ereignis, um zu bestimmen, wann ein-oder herunterladen gestartet oder beendet wird.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-122">Use this event to determine when buffering or downloading starts or stops.</span></span> <span data-ttu-id="fbaa3-123">Sie können den gleichen Ereignisblock für beide Fälle und das Test *Netzwerk* verwenden. **BufferingProgress** und *Network*. **Download Progress** , um zu bestimmen, ob der Inhalt von Windows Media Player derzeit gepuffert oder heruntergeladen wird.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-123">You can use the same event block for both cases and test *Network*.**bufferingProgress** and *Network*.**downloadProgress** to determine whether Windows Media Player is currently buffering or downloading content.</span></span>

<span data-ttu-id="fbaa3-124">Der Wert von Ereignis Parametern wird von Windows Media Player festgelegt, und der Zugriff auf und die Übergabe an eine Methode in einer importierten JScript-Datei mithilfe des angegebenen Parameter namens ist möglich.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-124">The value of event parameters is specified by Windows Media Player, and can be accessed or passed to a method in an imported JScript file by using the parameter name given.</span></span> <span data-ttu-id="fbaa3-125">Dieser Parameter Name muss genau wie gezeigt eingegeben werden, einschließlich der Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-125">This parameter name must be typed exactly as shown, including capitalization.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbaa3-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbaa3-126">Requirements</span></span>



| <span data-ttu-id="fbaa3-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbaa3-127">Requirement</span></span> | <span data-ttu-id="fbaa3-128">Wert</span><span class="sxs-lookup"><span data-stu-id="fbaa3-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fbaa3-129">Version</span><span class="sxs-lookup"><span data-stu-id="fbaa3-129">Version</span></span><br/> | <span data-ttu-id="fbaa3-130">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-130">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="fbaa3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="fbaa3-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="fbaa3-132"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fbaa3-132"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbaa3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbaa3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbaa3-134">**Network. BufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="fbaa3-134">**Network.bufferingProgress**</span></span>](network-bufferingprogress.md)
</dt> <dt>

[<span data-ttu-id="fbaa3-135">**Network. Download Progress**</span><span class="sxs-lookup"><span data-stu-id="fbaa3-135">**Network.downloadProgress**</span></span>](network-downloadprogress.md)
</dt> <dt>

[<span data-ttu-id="fbaa3-136">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="fbaa3-136">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





