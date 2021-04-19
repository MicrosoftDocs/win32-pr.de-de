---
title: Media. imagesourceheight
description: Die imagesourceheight-Eigenschaft ruft die Höhe des aktuellen Medien Elements in Pixel ab.
ms.assetid: fa98ec62-4c58-46ab-98f3-8017096d46d8
keywords:
- Media. imagesourceheight Windows Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceHeight
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de364243e71c6653085b4c9c9ff81f148dc299d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368622"
---
# <a name="mediaimagesourceheight"></a><span data-ttu-id="43168-104">Media. imagesourceheight</span><span class="sxs-lookup"><span data-stu-id="43168-104">Media.imageSourceHeight</span></span>

<span data-ttu-id="43168-105">Die **imagesourceheight** -Eigenschaft ruft die Höhe des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="43168-105">The **ImageSourceHeight** property retrieves the height of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="43168-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43168-106">Syntax</span></span>

<span data-ttu-id="43168-107">*Player*. *currentMedia*. **imagesourceheight**</span><span class="sxs-lookup"><span data-stu-id="43168-107">*player*.*currentMedia*.**imageSourceHeight**</span></span>

## <a name="possible-values"></a><span data-ttu-id="43168-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="43168-108">Possible Values</span></span>

<span data-ttu-id="43168-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="43168-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="43168-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="43168-110">Remarks</span></span>

<span data-ttu-id="43168-111">Wenn das Medien Element nicht das aktuelle ist, gibt diese Eigenschaft 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="43168-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="43168-112">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="43168-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="43168-113">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="43168-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="43168-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43168-114">Examples</span></span>

<span data-ttu-id="43168-115">Im folgenden JScript-Beispiel wird *Media*. imagesourceheight verwendet, um die Bildgröße des aktuellen Medien Elements in Pixel anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="43168-115">The following JScript example uses *Media*.imageSourceHeight to display the image size, in pixels, of the current media item.</span></span> <span data-ttu-id="43168-116">Die Informationen werden in einem HTML-TEXTAREA-Element namens videosize gedruckt.</span><span class="sxs-lookup"><span data-stu-id="43168-116">The information is printed to an HTML TEXTAREA element named VideoSize.</span></span> <span data-ttu-id="43168-117">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="43168-117">The **Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = Player  EVENT = OpenStateChange(NewState)>

// Test whether the new media item is open.
if (NewState == 13){

   // Store the height and width of the new media item.
   var Height = Player.currentMedia.imageSourceHeight;
   var Width =  Player.currentMedia.imageSourceWidth;

   // Erase the information in the text area.
   VideoSize.value = "";

   // Test whether an image is visible.
   if (Height != 0 && Width != 0)

      // Display the image size information.
      VideoSize.value = Width + " x " + Height;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="43168-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="43168-118">Requirements</span></span>



| <span data-ttu-id="43168-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="43168-119">Requirement</span></span> | <span data-ttu-id="43168-120">Wert</span><span class="sxs-lookup"><span data-stu-id="43168-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43168-121">Version</span><span class="sxs-lookup"><span data-stu-id="43168-121">Version</span></span><br/> | <span data-ttu-id="43168-122">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="43168-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="43168-123">DLL</span><span class="sxs-lookup"><span data-stu-id="43168-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="43168-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43168-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43168-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="43168-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43168-126">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="43168-126">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="43168-127">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="43168-127">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="43168-128">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="43168-128">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="43168-129">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="43168-129">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





