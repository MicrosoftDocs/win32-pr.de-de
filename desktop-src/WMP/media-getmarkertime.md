---
title: Media. getmarkertime-Methode
description: Die getmarkertime-Methode ruft die Zeit des Markers am angegebenen Index ab.
ms.assetid: c3e6bead-2831-4d84-9d13-dcb865efe472
keywords:
- getmarkertime-Methode, Windows-Media Player
- getmarkertime-Methode, Windows Media Player, Medienklasse
- Medienklasse Windows Media Player, getmarkertime-Methode
topic_type:
- apiref
api_name:
- Media.getMarkerTime
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4398f89055a1996acb3f921d33c7675e52100ddd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358726"
---
# <a name="mediagetmarkertime-method"></a><span data-ttu-id="5ea18-106">Media. getmarkertime-Methode</span><span class="sxs-lookup"><span data-stu-id="5ea18-106">Media.getMarkerTime method</span></span>

<span data-ttu-id="5ea18-107">Die **getmarkertime** -Methode ruft die Zeit des Markers am angegebenen Index ab.</span><span class="sxs-lookup"><span data-stu-id="5ea18-107">The **getMarkerTime** method retrieves the time of the marker at the specified index.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ea18-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ea18-108">Syntax</span></span>


```JScript
retVal = Media.getMarkerTime(
  markerNum
)
```



## <a name="parameters"></a><span data-ttu-id="5ea18-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ea18-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ea18-110">*markernum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5ea18-110">*markerNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ea18-111">**Zahl** (**Long**), die den MarkerIndex angibt.</span><span class="sxs-lookup"><span data-stu-id="5ea18-111">**Number** (**long**) specifying the marker index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ea18-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ea18-112">Return value</span></span>

<span data-ttu-id="5ea18-113">Diese Methode gibt eine **Zahl** (**Double**) zurück, die den Speicherort der Markierung in Sekunden ab dem Anfang des Clips angibt.</span><span class="sxs-lookup"><span data-stu-id="5ea18-113">This method returns a **Number** (**double**) specifying the location of the marker in seconds from the beginning of the clip.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ea18-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ea18-114">Remarks</span></span>

<span data-ttu-id="5ea18-115">Diese Methode gibt **null** zurück, wenn der angegebene Marker nicht vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="5ea18-115">This method returns **NULL** if the specified marker does not exist.</span></span>

<span data-ttu-id="5ea18-116">Einige digitale Medienelemente enthalten keine Marker.</span><span class="sxs-lookup"><span data-stu-id="5ea18-116">Some digital media items do not contain markers.</span></span> <span data-ttu-id="5ea18-117">Verwenden Sie **markercount** , um herauszufinden, wie viele Marker im aktuellen Clip angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="5ea18-117">Use **markerCount** to find out how many markers are in the current clip.</span></span>

<span data-ttu-id="5ea18-118">Markerindexnummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="5ea18-118">Marker index numbers start at 1.</span></span>

<span data-ttu-id="5ea18-119">Um diese Methode verwenden zu können, ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ea18-119">To use this method, read access to the library is required.</span></span> <span data-ttu-id="5ea18-120">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5ea18-120">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5ea18-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ea18-121">Examples</span></span>

<span data-ttu-id="5ea18-122">Im folgenden JScript-Beispiel werden *Medien* verwendet. **getmarkertime** zum Ausfüllen eines HTML-TEXTAREA-Elements mit dem Namen "mtimes" mit dem Speicherort der einzelnen Marker.</span><span class="sxs-lookup"><span data-stu-id="5ea18-122">The following JScript example uses *Media*.**getMarkerTime** to fill an HTML TEXTAREA element named MTIMES with the location of each marker.</span></span> <span data-ttu-id="5ea18-123">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ea18-123">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1;i < mcount + 1; i++){

   // Print the message to the text area.
   MTIMES.value += "Marker number " + i + " occurs at ";
   MTIMES.value += Player.currentMedia.getMarkerTime(i);
   MTIMES.value += " second(s).";
   MTIMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="5ea18-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ea18-124">Requirements</span></span>



| <span data-ttu-id="5ea18-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ea18-125">Requirement</span></span> | <span data-ttu-id="5ea18-126">Wert</span><span class="sxs-lookup"><span data-stu-id="5ea18-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ea18-127">Version</span><span class="sxs-lookup"><span data-stu-id="5ea18-127">Version</span></span><br/> | <span data-ttu-id="5ea18-128">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5ea18-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ea18-129">DLL</span><span class="sxs-lookup"><span data-stu-id="5ea18-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ea18-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ea18-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ea18-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ea18-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ea18-132">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="5ea18-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5ea18-133">**Media. getmarkername**</span><span class="sxs-lookup"><span data-stu-id="5ea18-133">**Media.getMarkerName**</span></span>](media-getmarkername.md)
</dt> <dt>

[<span data-ttu-id="5ea18-134">**Media. markercount**</span><span class="sxs-lookup"><span data-stu-id="5ea18-134">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="5ea18-135">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5ea18-135">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5ea18-136">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5ea18-136">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





