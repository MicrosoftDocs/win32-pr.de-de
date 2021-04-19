---
title: Settings. invokeurls
description: Die invokeurls-Eigenschaft gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft ihn ab.
ms.assetid: 3a28d949-96b7-4c21-97c5-2442c2f7baa5
keywords:
- Settings. invokeurls-Windows-Media Player
topic_type:
- apiref
api_name:
- Settings.invokeURLs
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb55bb61243e6905a51a943a26adc120511335c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352956"
---
# <a name="settingsinvokeurls"></a><span data-ttu-id="a854f-104">Settings. invokeurls</span><span class="sxs-lookup"><span data-stu-id="a854f-104">Settings.invokeURLs</span></span>

<span data-ttu-id="a854f-105">Die **invokeurls** -Eigenschaft gibt einen Wert an, der angibt, ob URL-Ereignisse einen Webbrowser starten sollen, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="a854f-105">The **invokeURLs** property specifies or retrieves a value indicating whether URL events should launch a Web browser.</span></span>

## <a name="syntax"></a><span data-ttu-id="a854f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a854f-106">Syntax</span></span>

<span data-ttu-id="a854f-107">Player. Settings. invokeurls</span><span class="sxs-lookup"><span data-stu-id="a854f-107">player.settings.invokeURLs</span></span>

## <a name="possible-values"></a><span data-ttu-id="a854f-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a854f-108">Possible Values</span></span>

<span data-ttu-id="a854f-109">Diese Eigenschaft ist ein **boolescher** Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="a854f-109">This property is a read/write **Boolean**.</span></span>



| <span data-ttu-id="a854f-110">Wert</span><span class="sxs-lookup"><span data-stu-id="a854f-110">Value</span></span> | <span data-ttu-id="a854f-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a854f-111">Description</span></span>                                  |
|-------|----------------------------------------------|
| <span data-ttu-id="a854f-112">true</span><span class="sxs-lookup"><span data-stu-id="a854f-112">true</span></span>  | <span data-ttu-id="a854f-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="a854f-113">Default.</span></span> <span data-ttu-id="a854f-114">Mit URL-Ereignissen sollte ein Browser gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a854f-114">URL events should launch a browser.</span></span> |
| <span data-ttu-id="a854f-115">false</span><span class="sxs-lookup"><span data-stu-id="a854f-115">false</span></span> | <span data-ttu-id="a854f-116">Bei URL-Ereignissen sollte kein Browser gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="a854f-116">URL events should not launch a browser.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="a854f-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a854f-117">Remarks</span></span>

<span data-ttu-id="a854f-118">Mediendateien können URLs enthalten.</span><span class="sxs-lookup"><span data-stu-id="a854f-118">Media files can contain URLs.</span></span> <span data-ttu-id="a854f-119">Wenn eine URL an das Windows Media Player-Steuerelement gesendet wird, wird Sie unabhängig vom Wert in **invokeurls** zuerst an den **ScriptCommand** -Ereignishandler übergeben.</span><span class="sxs-lookup"><span data-stu-id="a854f-119">When a URL is sent to the Windows Media Player control, it is passed first to the **ScriptCommand** event handler regardless of the value in **invokeURLs**.</span></span> <span data-ttu-id="a854f-120">Nachdem **ScriptCommand** beendet wurde, prüft Windows Media Player **invokeurls** , ob der Standard Internet Browser mit der URL gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="a854f-120">After **ScriptCommand** exits, Windows Media Player checks **invokeURLs** to determine whether to launch the default Internet browser with the URL.</span></span> <span data-ttu-id="a854f-121">Sie können URLs selektiv anzeigen, indem Sie Sie in **ScriptCommand** überprüfen und **invokeurls** wie gewünscht festlegen.</span><span class="sxs-lookup"><span data-stu-id="a854f-121">You can selectively display URLs by checking them in **ScriptCommand** and setting **invokeURLs** as desired.</span></span>

<span data-ttu-id="a854f-122">**Windows Media Player 10 Mobile**: Diese Eigenschaft akzeptiert nur "false" oder gibt "false" zurück.</span><span class="sxs-lookup"><span data-stu-id="a854f-122">**Windows Media Player 10 Mobile**: This property only accepts or returns false.</span></span>

## <a name="requirements"></a><span data-ttu-id="a854f-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a854f-123">Requirements</span></span>



| <span data-ttu-id="a854f-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a854f-124">Requirement</span></span> | <span data-ttu-id="a854f-125">Wert</span><span class="sxs-lookup"><span data-stu-id="a854f-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a854f-126">Version</span><span class="sxs-lookup"><span data-stu-id="a854f-126">Version</span></span><br/> | <span data-ttu-id="a854f-127">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a854f-127">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a854f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a854f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="a854f-129"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a854f-129"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a854f-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a854f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a854f-131">**Player. ScriptCommand-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="a854f-131">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="a854f-132">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="a854f-132">**Settings Object**</span></span>](settings-object.md)
</dt> </dl>

 

 





