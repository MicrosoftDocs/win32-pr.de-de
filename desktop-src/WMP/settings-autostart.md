---
title: Einstellungen. Autostart
description: Mit der Autostart-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.
ms.assetid: 553f8534-9e3e-4fdc-bfc1-551939969289
keywords:
- Einstellungen. Autostart-Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.autoStart
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d08b8f84f4a0b51225ed5692a25fa41cab809ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364816"
---
# <a name="settingsautostart"></a><span data-ttu-id="7afeb-104">Einstellungen. Autostart</span><span class="sxs-lookup"><span data-stu-id="7afeb-104">Settings.autoStart</span></span>

<span data-ttu-id="7afeb-105">Mit der **Autostart** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das aktuelle Medien Element automatisch wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7afeb-105">The **autoStart** property specifies or retrieves a value indicating whether the current media item begins playing automatically.</span></span>

## <a name="syntax"></a><span data-ttu-id="7afeb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="7afeb-106">Syntax</span></span>

<span data-ttu-id="7afeb-107">Player. Settings. Autostart</span><span class="sxs-lookup"><span data-stu-id="7afeb-107">player.settings.autoStart</span></span>

## <a name="possible-values"></a><span data-ttu-id="7afeb-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7afeb-108">Possible Values</span></span>

<span data-ttu-id="7afeb-109">Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="7afeb-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="7afeb-110">Wert</span><span class="sxs-lookup"><span data-stu-id="7afeb-110">Value</span></span> | <span data-ttu-id="7afeb-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7afeb-111">Description</span></span>                                                         |
|-------|---------------------------------------------------------------------|
| <span data-ttu-id="7afeb-112">true</span><span class="sxs-lookup"><span data-stu-id="7afeb-112">true</span></span>  | <span data-ttu-id="7afeb-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="7afeb-113">Default.</span></span> <span data-ttu-id="7afeb-114">Das Medien Element beginnt automatisch (siehe Hinweise).</span><span class="sxs-lookup"><span data-stu-id="7afeb-114">The media item begins playing automatically (see Remarks).</span></span> |
| <span data-ttu-id="7afeb-115">false</span><span class="sxs-lookup"><span data-stu-id="7afeb-115">false</span></span> | <span data-ttu-id="7afeb-116">Das Medien Element beginnt nicht automatisch mit der Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="7afeb-116">The media item does not begin playing automatically.</span></span>                |



 

## <a name="remarks"></a><span data-ttu-id="7afeb-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7afeb-117">Remarks</span></span>

<span data-ttu-id="7afeb-118">Wenn **Autostart** auf true festgelegt ist, beginnt das Medien Element mit der Wiedergabe beim *Player*. **URL**, *Player*. **currentwiedergabe**, oder *Player*. **currentMedia** wird festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7afeb-118">If **autoStart** is set to true, the media item will begin playing when *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** is set.</span></span> <span data-ttu-id="7afeb-119">Andernfalls wird die Wiedergabe bis zu den Steuer *Elementen* nicht gestartet. die **Play** -Methode wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="7afeb-119">Otherwise, it will not start playing until the *Controls*.**play** method is called.</span></span>

<span data-ttu-id="7afeb-120">Da die **Autostart** -Eigenschaft für den vollständigen Modus von Windows Media Player Global durch externe Ereignisse (z. b. das Laden einer CD) festgelegt werden kann, gibt es keinen zuverlässigen Standardwert für Skins und Remote Player-Steuerelemente.</span><span class="sxs-lookup"><span data-stu-id="7afeb-120">Because the **autoStart** property for the full mode of Windows Media Player can be set globally by external events (such as loading a CD), there is no reliable default value for skins and remoted Player controls.</span></span> <span data-ttu-id="7afeb-121">Dies liegt daran, dass die Wiedergabe-Engine des vollmodusplayers in beiden Fällen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7afeb-121">This is because the playback engine of the full mode Player is used in both cases.</span></span>

<span data-ttu-id="7afeb-122">Legen Sie **Autostart** direkt vor dem Festlegen von *Player* auf false fest. **URL**, *Player*. **currentwiedergabe**, oder *Player*. **currentMedia** in Skins und Remote Windows Media Player-Steuerelemente, wenn Sie sicherstellen möchten, dass das Medien Element nicht sofort wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7afeb-122">You should set **autoStart** to false immediately before you set *Player*.**URL**, *Player*.**currentPlaylist**, or *Player*.**currentMedia** in skins and remoted Windows Media Player controls if you want to ensure that the media item does not start playing immediately.</span></span> <span data-ttu-id="7afeb-123">Außerdem sollten Sie diese Einstellung nicht als Ersatz für die Verwendung der Steuer *Elemente* verwenden, es sei denn, Sie legen **Autostart** direkt vor der Angabe eines Medien Elements auf true fest. **Wiedergabe** Methode.</span><span class="sxs-lookup"><span data-stu-id="7afeb-123">Also, unless you set **autostart** to true immediately before specifying a media item, you should not rely on this setting as a substitute for using the *Controls*.**play** method.</span></span>

## <a name="examples"></a><span data-ttu-id="7afeb-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7afeb-124">Examples</span></span>

<span data-ttu-id="7afeb-125">Im folgenden Beispiel wird ein HTML-Checkbox-Element erstellt, mit dem der Benutzer angeben kann, ob das aktuelle Medien Element vom Player-Steuerelement automatisch abgespielt wird.</span><span class="sxs-lookup"><span data-stu-id="7afeb-125">The following example creates an HTML CHECKBOX element that allows the user to specify whether the Player control plays the current media item automatically.</span></span> <span data-ttu-id="7afeb-126">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="7afeb-126">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML CHECKBOX control. -->
<INPUT  TYPE = "CHECKBOX" ID = AS
              onClick = "
    /* Use the CHECKBOX state to specify the value 
       of the autoStart property. */
    Player.settings.autoStart = AS.checked;
"> 

```



## <a name="requirements"></a><span data-ttu-id="7afeb-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7afeb-127">Requirements</span></span>



| <span data-ttu-id="7afeb-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7afeb-128">Requirement</span></span> | <span data-ttu-id="7afeb-129">Wert</span><span class="sxs-lookup"><span data-stu-id="7afeb-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7afeb-130">Version</span><span class="sxs-lookup"><span data-stu-id="7afeb-130">Version</span></span><br/> | <span data-ttu-id="7afeb-131">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="7afeb-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="7afeb-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7afeb-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="7afeb-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7afeb-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7afeb-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7afeb-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7afeb-135">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="7afeb-135">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="7afeb-136">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="7afeb-136">**Player.URL**</span></span>](player-url.md)
</dt> <dt>

[<span data-ttu-id="7afeb-137">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="7afeb-137">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





