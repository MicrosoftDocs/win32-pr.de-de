---
title: Media. Duration
description: Die Duration-Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.
ms.assetid: d7d36858-812d-471b-84ce-fe2ab96b86b3
keywords:
- Media. Duration Windows Media Player
topic_type:
- apiref
api_name:
- Media.duration
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71586f6aa37401d56a9e9537bfbea6c5af23f318
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368690"
---
# <a name="mediaduration"></a><span data-ttu-id="03bab-104">Media. Duration</span><span class="sxs-lookup"><span data-stu-id="03bab-104">Media.duration</span></span>

<span data-ttu-id="03bab-105">Die **Duration** -Eigenschaft ruft die Dauer des aktuellen Medien Elements in Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="03bab-105">The **duration** property retrieves the duration of the current media item in seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="03bab-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="03bab-106">Syntax</span></span>

<span data-ttu-id="03bab-107">*Player*. *currentMedia*. **Dauer**</span><span class="sxs-lookup"><span data-stu-id="03bab-107">*player*.*currentMedia*.**duration**</span></span>

## <a name="possible-values"></a><span data-ttu-id="03bab-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="03bab-108">Possible Values</span></span>

<span data-ttu-id="03bab-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** ( **Double**).</span><span class="sxs-lookup"><span data-stu-id="03bab-109">This property is a read-only **Number** ( **double**).</span></span>

## <a name="remarks"></a><span data-ttu-id="03bab-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="03bab-110">Remarks</span></span>

<span data-ttu-id="03bab-111">, Wenn diese Eigenschaft mit einem anderen als dem in *Player* angegebenen Medien Element verwendet wird. **currentMedia** kann keinen gültigen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="03bab-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span>

<span data-ttu-id="03bab-112">Zum Abrufen der Dauer für Dateien, die sich nicht in der Bibliothek des Benutzers befinden, müssen Sie auf das Öffnen der Datei durch Windows Media Player warten. Das heißt, dass der aktuelle openstate-Wert "mediaopen" entsprechen muss.</span><span class="sxs-lookup"><span data-stu-id="03bab-112">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current OpenState must equal MediaOpen.</span></span> <span data-ttu-id="03bab-113">Sie können dies überprüfen, indem Sie den *Player* verarbeiten. **OpenStateChange** -Ereignis oder durch regelmäßiges Überprüfen des Werts von *Player*. **openstate**.</span><span class="sxs-lookup"><span data-stu-id="03bab-113">You can verify this by handling the *Player*.**OpenStateChange** event or by periodically checking the value of *Player*.**openState**.</span></span>

<span data-ttu-id="03bab-114">Bei Wiedergabelisten kann die Dauer der einzelnen Medienelemente abgerufen werden, wenn das einzelne Medien Element geöffnet wird, anstatt beim Öffnen der Wiedergabeliste.</span><span class="sxs-lookup"><span data-stu-id="03bab-114">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="03bab-115">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="03bab-115">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="03bab-116">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="03bab-116">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="03bab-117">Im folgenden JScript-Beispiel werden *Medien* verwendet. **Dauer** , mit der die verbleibende Zeit im aktuellen Medien Element angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="03bab-117">The following JScript example uses *Media*.**duration** to display the time remaining in the current media item.</span></span> <span data-ttu-id="03bab-118">Ein HTML div-Element namens remtime zeigt die Informationen an.</span><span class="sxs-lookup"><span data-stu-id="03bab-118">An HTML DIV element named RemTime displays the information.</span></span> <span data-ttu-id="03bab-119">Ein HTML-Timer aktualisiert den Text im div-Element jede Sekunde.</span><span class="sxs-lookup"><span data-stu-id="03bab-119">An HTML timer updates the text in the DIV element every second.</span></span>

<span data-ttu-id="03bab-120">Mit dem folgenden JScript-Code wird der Timer gestartet:</span><span class="sxs-lookup"><span data-stu-id="03bab-120">The following JScript code starts the timer:</span></span>


```JScript
// Execute the update() function at one-second intervals.
idTmr = window.setInterval("update()",1000);
```



<span data-ttu-id="03bab-121">Mit dem folgenden JScript-Code wird der Timer beendet:</span><span class="sxs-lookup"><span data-stu-id="03bab-121">The following JScript code stops the timer:</span></span>


```JScript
window.clearInterval(idTmr);
```



<span data-ttu-id="03bab-122">Verwenden Sie den *Player*. **PlayStateChange** -Ereignis mit einer **Switch** -Anweisung, um zu bestimmen, wann der Timer gestartet und angehalten werden soll.</span><span class="sxs-lookup"><span data-stu-id="03bab-122">Use the *Player*.**PlayStateChange** event with a **switch** statement to determine when to start and stop the timer.</span></span>

<span data-ttu-id="03bab-123">Der folgende JScript-Code wird jedes Mal ausgeführt, wenn der Timer die Update-Funktion aufruft:</span><span class="sxs-lookup"><span data-stu-id="03bab-123">The following JScript code executes each time the timer calls the update function:</span></span>


```JScript
// Store the current position of the current media item.
var TimeNow = Player.controls.currentPosition;

// Display the time remaining information.
RemTime.innerHTML = "Seconds remaining: ";

// Subtract the current position from the duration of the current media.
// Use the Math.floor method to round the result down to the nearest integer.
RemTime.innerHTML += Math.floor(Player.currentMedia.duration - TimeNow);
```



## <a name="requirements"></a><span data-ttu-id="03bab-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03bab-124">Requirements</span></span>



| <span data-ttu-id="03bab-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03bab-125">Requirement</span></span> | <span data-ttu-id="03bab-126">Wert</span><span class="sxs-lookup"><span data-stu-id="03bab-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="03bab-127">Version</span><span class="sxs-lookup"><span data-stu-id="03bab-127">Version</span></span><br/> | <span data-ttu-id="03bab-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="03bab-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="03bab-129">DLL</span><span class="sxs-lookup"><span data-stu-id="03bab-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="03bab-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03bab-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="03bab-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03bab-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03bab-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="03bab-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="03bab-133">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="03bab-133">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="03bab-134">**Player. PlayStateChange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="03bab-134">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> <dt>

[<span data-ttu-id="03bab-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="03bab-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="03bab-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="03bab-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





