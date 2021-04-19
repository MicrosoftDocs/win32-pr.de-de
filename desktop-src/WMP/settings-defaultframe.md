---
title: Settings. defaultframe
description: Die defaultframe-Eigenschaft gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem ScriptCommand-Ereignis empfangen wird.
ms.assetid: c2edb253-a545-4820-85aa-8fb7badf4d81
keywords:
- Settings. defaultframe-Fenster Media Player
topic_type:
- apiref
api_name:
- Settings.defaultFrame
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a6182a635e4bd73a946c3cf85efb7d39966c0007
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369695"
---
# <a name="settingsdefaultframe"></a><span data-ttu-id="785bd-104">Settings. defaultframe</span><span class="sxs-lookup"><span data-stu-id="785bd-104">Settings.defaultFrame</span></span>

<span data-ttu-id="785bd-105">Die **defaultframe** -Eigenschaft gibt den Namen des Frames an oder ruft ihn ab, der zum Anzeigen einer URL verwendet wird, die in einem **ScriptCommand** -Ereignis empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="785bd-105">The **defaultFrame** property specifies or retrieves the name of the frame used to display a URL that is received in a **ScriptCommand** event.</span></span>

## <a name="syntax"></a><span data-ttu-id="785bd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="785bd-106">Syntax</span></span>

<span data-ttu-id="785bd-107">Player. Settings. defaultframe</span><span class="sxs-lookup"><span data-stu-id="785bd-107">player.settings.defaultFrame</span></span>

## <a name="possible-values"></a><span data-ttu-id="785bd-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="785bd-108">Possible Values</span></span>

<span data-ttu-id="785bd-109">Diese Eigenschaft ist eine Lese-/schreibzeichenfolge, die dem Wert des **Name** -Attributs des Target Frame-Elements entspricht. </span><span class="sxs-lookup"><span data-stu-id="785bd-109">This property is a read/write **String** corresponding to the value of the **name** attribute of the target FRAME element.</span></span>

## <a name="remarks"></a><span data-ttu-id="785bd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="785bd-110">Remarks</span></span>

<span data-ttu-id="785bd-111">Wenn ein Zielframe im **ScriptCommand** -Ereignis selbst angegeben wird, wird diese Eigenschaft ignoriert.</span><span class="sxs-lookup"><span data-stu-id="785bd-111">If a target frame is specified in the **ScriptCommand** event itself, this property is ignored.</span></span>

<span data-ttu-id="785bd-112">Diese Eigenschaft wird ignoriert, wenn das Applet "Netscape Navigator Java" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="785bd-112">This property is ignored when using the Netscape Navigator Java applet.</span></span> <span data-ttu-id="785bd-113">Im Navigator zeigt jeder empfangene URL-Skript Befehl die URL in einem neuen Browserfenster an, unabhängig vom Wert der *Einstellungen*. **defaultframe**.</span><span class="sxs-lookup"><span data-stu-id="785bd-113">In Navigator, each URL script command received displays the URL in a new browser window, regardless of the value of *Settings*.**defaultFrame**.</span></span>

<span data-ttu-id="785bd-114">**Windows Media Player 10 Mobile**: Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="785bd-114">**Windows Media Player 10 Mobile**: This property is read only, and always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="785bd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="785bd-115">Requirements</span></span>



| <span data-ttu-id="785bd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="785bd-116">Requirement</span></span> | <span data-ttu-id="785bd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="785bd-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="785bd-118">Version</span><span class="sxs-lookup"><span data-stu-id="785bd-118">Version</span></span><br/> | <span data-ttu-id="785bd-119">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="785bd-119">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="785bd-120">DLL</span><span class="sxs-lookup"><span data-stu-id="785bd-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="785bd-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="785bd-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="785bd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="785bd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="785bd-123">**Player. ScriptCommand-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="785bd-123">**Player.ScriptCommand Event**</span></span>](player-player-scriptcommand.md)
</dt> <dt>

[<span data-ttu-id="785bd-124">**Einstellungs Objekt**</span><span class="sxs-lookup"><span data-stu-id="785bd-124">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="785bd-125">**Verwenden von Windows Media Player mit Netscape 7.1**</span><span class="sxs-lookup"><span data-stu-id="785bd-125">**Using Windows Media Player with Netscape 7.1**</span></span>](using-windows-media-player-with-netscape-7-1.md)
</dt> </dl>

 

 





