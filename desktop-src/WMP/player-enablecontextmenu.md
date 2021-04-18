---
title: Player. enablecontextmenu
description: Mit der enablecontextmenu-Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird.
ms.assetid: 736c8714-5650-4912-9e97-914a20137b91
keywords:
- Player. enablecontextmenu-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.enableContextMenu
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 324ab0f14b83621651869e715c1fd4a882ceb650
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371995"
---
# <a name="playerenablecontextmenu"></a><span data-ttu-id="b7bf5-104">Player. enablecontextmenu</span><span class="sxs-lookup"><span data-stu-id="b7bf5-104">Player.enableContextMenu</span></span>

<span data-ttu-id="b7bf5-105">Mit der **enablecontextmenu** -Eigenschaft wird ein Wert angegeben oder abgerufen, der angibt, ob das Kontextmenü aktiviert werden soll, das angezeigt wird, wenn mit der rechten Maustaste geklickt wird.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-105">The **enableContextMenu** property specifies or retrieves a value indicating whether to enable the context menu, which appears when the right mouse button is clicked.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7bf5-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7bf5-106">Syntax</span></span>

<span data-ttu-id="b7bf5-107">*Player*. **enablecontextmenu**</span><span class="sxs-lookup"><span data-stu-id="b7bf5-107">*player*.**enableContextMenu**</span></span>

## <a name="possible-values"></a><span data-ttu-id="b7bf5-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b7bf5-108">Possible Values</span></span>

<span data-ttu-id="b7bf5-109">Diese Eigenschaft ist ein boolescher Wert mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-109">This property is a read/write Boolean.</span></span>



| <span data-ttu-id="b7bf5-110">Wert</span><span class="sxs-lookup"><span data-stu-id="b7bf5-110">Value</span></span> | <span data-ttu-id="b7bf5-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7bf5-111">Description</span></span>                       |
|-------|-----------------------------------|
| <span data-ttu-id="b7bf5-112">true</span><span class="sxs-lookup"><span data-stu-id="b7bf5-112">true</span></span>  | <span data-ttu-id="b7bf5-113">Standard.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-113">Default.</span></span> <span data-ttu-id="b7bf5-114">Aktivieren Sie das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-114">Enable the context menu.</span></span> |
| <span data-ttu-id="b7bf5-115">false</span><span class="sxs-lookup"><span data-stu-id="b7bf5-115">false</span></span> | <span data-ttu-id="b7bf5-116">Aktivieren Sie nicht das Kontextmenü.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-116">Do not enable the context menu.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="b7bf5-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b7bf5-117">Remarks</span></span>

<span data-ttu-id="b7bf5-118">Während der Vollbildwiedergabe blendet Windows Media Player den Mauszeiger aus, wenn **enablecontextmenu** den Wert false hat und **uiMode** den Wert "None" hat.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-118">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="b7bf5-119">**Windows Media Player 10 Mobile:** Diese Eigenschaft wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-119">**Windows Media Player 10 Mobile:** This property is not supported.</span></span>

## <a name="requirements"></a><span data-ttu-id="b7bf5-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b7bf5-120">Requirements</span></span>



| <span data-ttu-id="b7bf5-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b7bf5-121">Requirement</span></span> | <span data-ttu-id="b7bf5-122">Wert</span><span class="sxs-lookup"><span data-stu-id="b7bf5-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b7bf5-123">Version</span><span class="sxs-lookup"><span data-stu-id="b7bf5-123">Version</span></span><br/> | <span data-ttu-id="b7bf5-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b7bf5-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b7bf5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b7bf5-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="b7bf5-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7bf5-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b7bf5-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7bf5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7bf5-128">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b7bf5-128">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





