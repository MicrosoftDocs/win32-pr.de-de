---
title: Media. durationString
description: Die durationString-Eigenschaft ruft einen Zeichen folgen Wert ab, der die Dauer des aktuellen Medien Elements im hh mm ss-Format angibt.
ms.assetid: dfcb4c2e-c62c-4c3e-a9f4-fd147fb5b28c
keywords:
- Media. durationString-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.durationString
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f1bbb89716ab1d06b176754396611ab22980659
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368689"
---
# <a name="mediadurationstring"></a><span data-ttu-id="5bfa0-104">Media. durationString</span><span class="sxs-lookup"><span data-stu-id="5bfa0-104">Media.durationString</span></span>

<span data-ttu-id="5bfa0-105">Die **durationString** -Eigenschaft ruft einen **Zeichen** folgen Wert ab, der die Dauer des aktuellen Medien Elements im Format hh: mm: SS angibt.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-105">The **durationString** property retrieves a **String** value indicating the duration of the current media item in HH:MM:SS format.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bfa0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5bfa0-106">Syntax</span></span>

<span data-ttu-id="5bfa0-107">*Player*. *currentMedia*. **durationString**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-107">*player*.*currentMedia*.**durationString**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5bfa0-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="5bfa0-108">Possible Values</span></span>

<span data-ttu-id="5bfa0-109">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5bfa0-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bfa0-110">Remarks</span></span>

<span data-ttu-id="5bfa0-111">, Wenn diese Eigenschaft mit einem anderen als dem in *Player* angegebenen Medien Element verwendet wird. **currentMedia** kann keinen gültigen Wert enthalten.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-111">If this property is used with a media item other than the one specified in *Player*.**currentMedia**, it may not contain a valid value.</span></span> <span data-ttu-id="5bfa0-112">Wenn das Medien Element weniger als eine Stunde lang ist, wird der HH:-Teil des Rückgabewerts ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-112">If the media item is less than an hour long, the HH: portion of the return value is omitted.</span></span>

<span data-ttu-id="5bfa0-113">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5bfa0-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5bfa0-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5bfa0-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5bfa0-115">Examples</span></span>

<span data-ttu-id="5bfa0-116">Im folgenden JScript-Beispiel werden *Medien* verwendet. **durationString** , um die Dauer des aktuellen Medien Elements als formatierten Text anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-116">The following JScript example uses *Media*.**durationString** to display the duration of the current media item as formatted text.</span></span> <span data-ttu-id="5bfa0-117">Ein HTML div-Element mit dem Namen MediaInfo zeigt die Dauer Informationen an.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-117">An HTML DIV element named MediaInfo displays the duration information.</span></span> <span data-ttu-id="5bfa0-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler to update the display when
 the current media item changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Write the formatted duration string to the DIV region.
   MediaInfo.innerHTML = "Duration: " + Player.currentMedia.durationString;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="5bfa0-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5bfa0-119">Requirements</span></span>



| <span data-ttu-id="5bfa0-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5bfa0-120">Requirement</span></span> | <span data-ttu-id="5bfa0-121">Wert</span><span class="sxs-lookup"><span data-stu-id="5bfa0-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5bfa0-122">Version</span><span class="sxs-lookup"><span data-stu-id="5bfa0-122">Version</span></span><br/> | <span data-ttu-id="5bfa0-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5bfa0-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5bfa0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="5bfa0-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="5bfa0-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5bfa0-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bfa0-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bfa0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bfa0-127">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5bfa0-128">**Media. Duration**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-128">**Media.duration**</span></span>](media-duration.md)
</dt> <dt>

[<span data-ttu-id="5bfa0-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="5bfa0-130">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5bfa0-131">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5bfa0-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





