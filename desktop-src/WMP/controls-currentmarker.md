---
title: Controls. currentmarker
description: Die currentmarker-Eigenschaft gibt die aktuelle Markernummer an oder ruft Sie ab.
ms.assetid: 4b4eacd4-3df0-4e11-8755-1ac326fad027
keywords:
- Steuerelemente. currentmarker-Fenster Media Player
topic_type:
- apiref
api_name:
- Controls.currentMarker
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aae8af226b62550b3faae9389385d321bf10aad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354671"
---
# <a name="controlscurrentmarker"></a><span data-ttu-id="261e2-104">Controls. currentmarker</span><span class="sxs-lookup"><span data-stu-id="261e2-104">Controls.currentMarker</span></span>

<span data-ttu-id="261e2-105">Die **currentmarker** -Eigenschaft gibt die aktuelle Markernummer an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="261e2-105">The **currentMarker** property specifies or retrieves the current marker number.</span></span>

``` syntax
player.controls.currentMarker
      
```

## <a name="possible-values"></a><span data-ttu-id="261e2-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="261e2-106">Possible Values</span></span>

<span data-ttu-id="261e2-107">Diese Eigenschaft ist eine Lese-/schreibzahl (**Long**) mit einem Standardwert von 0 (null). </span><span class="sxs-lookup"><span data-stu-id="261e2-107">This property is a read/write **Number** (**long**) with a default value of zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="261e2-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="261e2-108">Remarks</span></span>

<span data-ttu-id="261e2-109">Das Festlegen von **currentmarker** bewirkt, dass die Wiedergabe vom angegebenen Marker gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="261e2-109">Setting **currentMarker** causes playback to start from the specified marker.</span></span> <span data-ttu-id="261e2-110">Bevor Sie versuchen, **currentmarker** festzulegen, stellen Sie fest, ob eine Datei Marker hat und wie viele Sie mit **markercount** haben.</span><span class="sxs-lookup"><span data-stu-id="261e2-110">Before attempting to set **currentMarker**, determine whether a file has markers and how many it has by using **markerCount**.</span></span> <span data-ttu-id="261e2-111">Wenn eine Datei keine Marker hat, führt die Festlegung von **currentmarker** auf alles, aber auf 0 (null) zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="261e2-111">If a file has no markers, setting **currentMarker** to anything but zero results in an error.</span></span> <span data-ttu-id="261e2-112">Wenn **currentmarker** auf eine Zahl höher als **markercount** festgelegt wird, führt dies ebenfalls zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="261e2-112">Setting **currentMarker** to a number higher than **markerCount** also results in an error.</span></span>

<span data-ttu-id="261e2-113">Die **currentmarker** -Eigenschaft gibt immer den aktuellen oder den letzten Marker zurück. Dies bedeutet, dass sich die tatsächliche Dateiposition entweder am aktuellen Marker oder vor dem nächsten Marker befinden kann.</span><span class="sxs-lookup"><span data-stu-id="261e2-113">The **currentMarker** property always returns the current or last marker, which means the actual file position can be either at the current marker or before the next marker.</span></span> <span data-ttu-id="261e2-114">Marker werden beginnend mit 1 nummeriert. Wenn also eine Datei Marker enthält, können Sie **currentmarker** auf NULL festlegen, um die Dateiposition in NULL zu ändern.</span><span class="sxs-lookup"><span data-stu-id="261e2-114">Markers are numbered beginning at 1, so if a file has markers, you can set **currentMarker** to zero to change the file position to zero.</span></span>

<span data-ttu-id="261e2-115">Bis zum Festlegen des aktuellen Medien Elements (mithilfe von *Player*).**URL** oder *Player*. **currentMedia**), **currentmarker** gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="261e2-115">Until the current media item is set (using *Player*.**URL** or *Player*.**currentMedia**), **currentMarker** returns zero.</span></span>

## <a name="examples"></a><span data-ttu-id="261e2-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="261e2-116">Examples</span></span>

<span data-ttu-id="261e2-117">Im folgenden JScript-Beispiel wird **currentmarker** verwendet, um die Videowiedergabe aus dem Marker zu starten, der der **SelectedIndex** -Eigenschaft eines HTML SELECT-Elements entspricht.</span><span class="sxs-lookup"><span data-stu-id="261e2-117">The following JScript example uses **currentMarker** to start video playback from the marker that corresponds to the **selectedIndex** property of an HTML SELECT element.</span></span> <span data-ttu-id="261e2-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="261e2-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<SELECT ID = "markers"  NAME = "markers"  LANGUAGE = "JScript"

    /* Seek to the marker number that corresponds to the SELECT element
       selectedIndex value when the list selection changes. */
    onChange = "Player.controls.currentMarker = markers.selectedIndex + 1;
">

    /* Fill the SELECT element with the marker identifiers. */
    <OPTION SELECTED>Sunrise
    <OPTION>Car chase 
    <OPTION>Happy ending
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="261e2-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="261e2-119">Requirements</span></span>



| <span data-ttu-id="261e2-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="261e2-120">Requirement</span></span> | <span data-ttu-id="261e2-121">Wert</span><span class="sxs-lookup"><span data-stu-id="261e2-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="261e2-122">Version</span><span class="sxs-lookup"><span data-stu-id="261e2-122">Version</span></span><br/> | <span data-ttu-id="261e2-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="261e2-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="261e2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="261e2-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="261e2-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="261e2-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="261e2-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="261e2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="261e2-127">**Controls-Objekt**</span><span class="sxs-lookup"><span data-stu-id="261e2-127">**Controls Object**</span></span>](controls-object.md)
</dt> <dt>

[<span data-ttu-id="261e2-128">**Media. markercount**</span><span class="sxs-lookup"><span data-stu-id="261e2-128">**Media.markerCount**</span></span>](media-markercount.md)
</dt> <dt>

[<span data-ttu-id="261e2-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="261e2-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="261e2-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="261e2-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





