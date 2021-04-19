---
title: Media. getmarkername-Methode
description: Die getmarkername-Methode ruft den Namen des Markers am angegebenen Index ab.
ms.assetid: 142438b7-88d1-4523-829f-52dafbf0a7a6
keywords:
- getmarkername-Methode, Windows Media Player
- getmarkername-Methode, Windows Media Player, Medienklasse
- Media Class Windows Media Player, getmarkername-Methode
topic_type:
- apiref
api_name:
- Media.getMarkerName
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69b923408432f76525b2dcf8cab046703fb76f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361695"
---
# <a name="mediagetmarkername-method"></a><span data-ttu-id="e256c-106">Media. getmarkername-Methode</span><span class="sxs-lookup"><span data-stu-id="e256c-106">Media.getMarkerName method</span></span>

<span data-ttu-id="e256c-107">Die **getmarkername** -Methode ruft den Namen des Markers am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="e256c-107">The **getMarkerName** method retrieves the name of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="e256c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e256c-108">Syntax</span></span>


```JScript
strRetVal = Media.getMarkerName(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="e256c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e256c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e256c-110">*markernum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e256c-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e256c-111">**Zahl** (**Long**), die einen MarkerIndex angibt.</span><span class="sxs-lookup"><span data-stu-id="e256c-111">**Number** (**long**) specifying a marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e256c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e256c-112">Return value</span></span>

<span data-ttu-id="e256c-113">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="e256c-113">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e256c-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e256c-114">Remarks</span></span>

<span data-ttu-id="e256c-115">Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e256c-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="e256c-116">Einige digitale Medienelemente enthalten keine Marker.</span><span class="sxs-lookup"><span data-stu-id="e256c-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="e256c-117">Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Clip angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e256c-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="e256c-118">Markerindexnummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="e256c-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="e256c-119">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e256c-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="e256c-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="e256c-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e256c-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e256c-121">Examples</span></span>

<span data-ttu-id="e256c-122">Im folgenden JScript-Beispiel werden *Medien* verwendet. " **getmarkername** ", um ein HTML-TEXTAREA-Element mit dem Namen "mNames" mit den Namen der Marker im aktuellen Medien Element auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="e256c-122">The following JScript example uses *Media*.**getMarkerName** to fill an HTML TEXTAREA element named MNAMES with the names of the markers in the current media item.</span></span> <span data-ttu-id="e256c-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="e256c-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="e256c-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e256c-124">Requirements</span></span>



| <span data-ttu-id="e256c-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e256c-125">Requirement</span></span> | <span data-ttu-id="e256c-126">Wert</span><span class="sxs-lookup"><span data-stu-id="e256c-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e256c-127">Version</span><span class="sxs-lookup"><span data-stu-id="e256c-127">Version</span></span><br/> | <span data-ttu-id="e256c-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="e256c-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e256c-129">DLL</span><span class="sxs-lookup"><span data-stu-id="e256c-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="e256c-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e256c-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e256c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e256c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e256c-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="e256c-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e256c-133">**Media. getmarkertime**</span><span class="sxs-lookup"><span data-stu-id="e256c-133">**Media.getMarkerTime**</span></span>](media-getmarkertime.md)
</dt> <dt>

[<span data-ttu-id="e256c-134">**Media. markercount**</span><span class="sxs-lookup"><span data-stu-id="e256c-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="e256c-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e256c-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="e256c-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="e256c-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





