---
title: Player. currentMedia
description: Die currentMedia-Eigenschaft gibt das aktuelle Medienobjekt an oder ruft es ab.
ms.assetid: 5cf45a10-9d0d-435e-97f1-d2c9c51f4b47
keywords:
- Player. currentMedia-Fenster Media Player
topic_type:
- apiref
api_name:
- Player.currentMedia
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea90b7be72bcb10a8ec0d3c49116f3effceb9a93
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366696"
---
# <a name="playercurrentmedia"></a><span data-ttu-id="4f3c3-104">Player. currentMedia</span><span class="sxs-lookup"><span data-stu-id="4f3c3-104">Player.currentMedia</span></span>

<span data-ttu-id="4f3c3-105">Die **currentMedia** -Eigenschaft gibt das aktuelle Medienobjekt an oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-105">The **currentMedia** property specifies or retrieves the current Media object.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f3c3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f3c3-106">Syntax</span></span>

<span data-ttu-id="4f3c3-107">*Player* . **currentMedia**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-107">*player* .**currentMedia**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4f3c3-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4f3c3-108">Possible Values</span></span>

<span data-ttu-id="4f3c3-109">Diese Eigenschaft ist ein Medienobjekt mit Lese-/Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-109">This property is a read/write Media object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f3c3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f3c3-110">Remarks</span></span>

<span data-ttu-id="4f3c3-111">Wenn die *Einstellungen*. die **Autostart** -Eigenschaft ist "true". die Wiedergabe beginnt automatisch, wenn Sie **currentMedia** festlegen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-111">If the *Settings*.**autoStart** property is true, playback begins automatically whenever you set **currentMedia**.</span></span>

<span data-ttu-id="4f3c3-112">Diese Eigenschaft nimmt ein Medienobjekt an, das über die *Wiedergabeliste* abgerufen werden kann. **Element**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-112">This property takes a Media object, which can be acquired by using *Playlist*.**item**.</span></span> <span data-ttu-id="4f3c3-113">Wenn Sie ein **Medien** Element mithilfe eines Datei namens laden möchten, legen Sie die URL-Eigenschaft fest, oder verwenden Sie **newmedia**.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-113">To load a **Media** item using a file name, set the URL property or use **newMedia**.</span></span>

## <a name="examples"></a><span data-ttu-id="4f3c3-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f3c3-114">Examples</span></span>

<span data-ttu-id="4f3c3-115">Im folgenden JScript-Beispiel wird das erste Medien Element in der Bibliothek abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-115">The following JScript example retrieves the first media item in the library.</span></span> <span data-ttu-id="4f3c3-116">Anschließend wird **currentMedia** verwendet, um das abgerufene Medien Element zum aktuellen Medien Element zu machen, und dann den Namen des aktuellen Medien Elements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-116">It then uses **currentMedia** to make the retrieved media item the current media item, and then to display the name of the current media item.</span></span> <span data-ttu-id="4f3c3-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Retrieve the first media item from the library.
var firstMedia = Player.mediaCollection.getAll().item(0);

// Make the retrieved media item the current media item.
Player.currentMedia = firstMedia;

// Display the name of the current media item.
document.write("Found first media item. Name = " + Player.currentMedia.name);
```



## <a name="requirements"></a><span data-ttu-id="4f3c3-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f3c3-118">Requirements</span></span>



| <span data-ttu-id="4f3c3-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f3c3-119">Requirement</span></span> | <span data-ttu-id="4f3c3-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4f3c3-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4f3c3-121">Version</span><span class="sxs-lookup"><span data-stu-id="4f3c3-121">Version</span></span><br/> | <span data-ttu-id="4f3c3-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4f3c3-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4f3c3-123">DLL</span><span class="sxs-lookup"><span data-stu-id="4f3c3-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="4f3c3-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f3c3-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f3c3-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f3c3-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f3c3-126">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="4f3c3-127">**Player-Objekt**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-127">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="4f3c3-128">**Player. newmedia**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-128">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="4f3c3-129">**Wiedergabeliste. Element**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-129">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="4f3c3-130">**Einstellungen. Autostart**</span><span class="sxs-lookup"><span data-stu-id="4f3c3-130">**Settings.autoStart**</span></span>](settings-autostart.md)
</dt> </dl>

 

 





