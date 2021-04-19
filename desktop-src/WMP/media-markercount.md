---
title: Media. markercount
description: Die markercount-Eigenschaft ruft die Anzahl der Marker im Medien Element ab.
ms.assetid: 48313395-b225-4008-b0e8-82fa22d6aaef
keywords:
- Media. markercount-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.markerCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c97a874211c0c00ebf9f242887d4314ec490b552
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354227"
---
# <a name="mediamarkercount"></a><span data-ttu-id="67ca7-104">Media. markercount</span><span class="sxs-lookup"><span data-stu-id="67ca7-104">Media.markerCount</span></span>

<span data-ttu-id="67ca7-105">Die **markercount** -Eigenschaft ruft die Anzahl der Marker im Medien Element ab.</span><span class="sxs-lookup"><span data-stu-id="67ca7-105">The **markerCount** property retrieves the number of markers in the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="67ca7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="67ca7-106">Syntax</span></span>

<span data-ttu-id="67ca7-107">*Player*. *currentMedia*. **markercount**</span><span class="sxs-lookup"><span data-stu-id="67ca7-107">*player*.*currentMedia*.**markerCount**</span></span>

## <a name="possible-values"></a><span data-ttu-id="67ca7-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="67ca7-108">Possible Values</span></span>

<span data-ttu-id="67ca7-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**), die die Anzahl der Marker in der Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="67ca7-109">This property is a read-only **Number** (**long**) specifying the number of markers in the file.</span></span>

## <a name="remarks"></a><span data-ttu-id="67ca7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67ca7-110">Remarks</span></span>

<span data-ttu-id="67ca7-111">Diese Eigenschaft gibt 0 (null) zurück, wenn eine Datei keine Marker enthält, oder wenn das Medien Element nicht mit dem *Player* übereinstimmt. **currentMedia**.</span><span class="sxs-lookup"><span data-stu-id="67ca7-111">This property returns zero if a file has no markers, or if the media item is not the same as *Player*.**currentMedia**.</span></span>

<span data-ttu-id="67ca7-112">Markernummern beginnen bei 1.</span><span class="sxs-lookup"><span data-stu-id="67ca7-112">Marker numbers start at 1.</span></span>

<span data-ttu-id="67ca7-113">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="67ca7-113">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="67ca7-114">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="67ca7-114">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="67ca7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67ca7-115">Examples</span></span>

<span data-ttu-id="67ca7-116">Im folgenden JScript-Beispiel werden *Medien* verwendet. **markercount** , um die Anzahl der Marker im aktuellen Medien Element abzurufen.</span><span class="sxs-lookup"><span data-stu-id="67ca7-116">The following JScript example uses *Media*.**markerCount** to retrieve the number of markers in the current media item.</span></span> <span data-ttu-id="67ca7-117">Dieser Wert wird dann als obere Grenze für eine Schleifen Struktur verwendet, die die markerliste durchläuft, um die einzelnen Markernamen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="67ca7-117">That value is then used as the upper boundary for a looping structure, which iterates through the marker list to retrieve each marker name.</span></span> <span data-ttu-id="67ca7-118">Ein HTML-TEXTAREA-Element mit dem Namen mNames zeigt die Namen der Marker im aktuellen Medien Element an.</span><span class="sxs-lookup"><span data-stu-id="67ca7-118">An HTML TEXTAREA element named MNAMES displays the names of the markers in the current media item.</span></span> <span data-ttu-id="67ca7-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="67ca7-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Get the number of markers in the current media item.
var mcount = Player.currentMedia.markerCount;

// Verify that at least one marker exists in the current media item.
if (mcount > 0){

// Loop through the marker list.
for (var i = 1; i < mcount + 1; i++){

   // Print the marker name to the text area.
   MNAMES.value += Player.currentMedia.getMarkerName(i);
   MNAMES.value += "\n";
}

```



## <a name="requirements"></a><span data-ttu-id="67ca7-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67ca7-120">Requirements</span></span>



| <span data-ttu-id="67ca7-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67ca7-121">Requirement</span></span> | <span data-ttu-id="67ca7-122">Wert</span><span class="sxs-lookup"><span data-stu-id="67ca7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="67ca7-123">Version</span><span class="sxs-lookup"><span data-stu-id="67ca7-123">Version</span></span><br/> | <span data-ttu-id="67ca7-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="67ca7-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="67ca7-125">DLL</span><span class="sxs-lookup"><span data-stu-id="67ca7-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="67ca7-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67ca7-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67ca7-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67ca7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67ca7-128">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="67ca7-128">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="67ca7-129">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="67ca7-129">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="67ca7-130">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="67ca7-130">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="67ca7-131">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="67ca7-131">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





