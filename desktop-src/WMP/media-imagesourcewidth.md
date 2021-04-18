---
title: Media. imagesourcewidth
description: Die imagesourcewidth-Eigenschaft ruft die Breite des aktuellen Medien Elements in Pixel ab.
ms.assetid: 6559bd51-cec2-4fc6-aab8-f2fdd1d59bae
keywords:
- Media. imagesourcewidth-Windows-Media Player
topic_type:
- apiref
api_name:
- Media.imageSourceWidth
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff2a3fef7b74a3d033b058f0afd1f6eece007bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358632"
---
# <a name="mediaimagesourcewidth"></a><span data-ttu-id="5ddcf-104">Media. imagesourcewidth</span><span class="sxs-lookup"><span data-stu-id="5ddcf-104">Media.imageSourceWidth</span></span>

<span data-ttu-id="5ddcf-105">Die **imagesourcewidth** -Eigenschaft ruft die Breite des aktuellen Medien Elements in Pixel ab.</span><span class="sxs-lookup"><span data-stu-id="5ddcf-105">The **imageSourceWidth** property retrieves the width of the current media item in pixels.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ddcf-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ddcf-106">Syntax</span></span>

<span data-ttu-id="5ddcf-107">*Player*. *currentMedia*. **imagesourcewidth**</span><span class="sxs-lookup"><span data-stu-id="5ddcf-107">*player*.*currentMedia*.**imageSourceWidth**</span></span>

## <a name="possible-values"></a><span data-ttu-id="5ddcf-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="5ddcf-108">Possible Values</span></span>

<span data-ttu-id="5ddcf-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="5ddcf-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="5ddcf-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ddcf-110">Remarks</span></span>

<span data-ttu-id="5ddcf-111">Wenn das Medien Element nicht das aktuelle ist, gibt diese Eigenschaft 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="5ddcf-111">If the media item is not the current one, this property returns zero.</span></span>

<span data-ttu-id="5ddcf-112">Zum Abrufen des Werts dieser Eigenschaft ist Lesezugriff auf die Bibliothek erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5ddcf-112">To retrieve the value of this property, read access to the library is required.</span></span> <span data-ttu-id="5ddcf-113">Weitere Informationen finden Sie unter [Bibliotheks Zugriff](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="5ddcf-113">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="5ddcf-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ddcf-114">Examples</span></span>

<span data-ttu-id="5ddcf-115">Im folgenden JScript-Beispiel werden *Medien* verwendet. **imagesourcewidth** zum Anzeigen der Bildgröße des **aktuellen Medien Elements in Pixel. Die Informationen werden in einem HTML-TEXTAREA-Element namens videosize gedruckt. Das Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="5ddcf-115">The following JScript example uses *Media*.**imageSourceWidth** to display the image size, in pixels, of the **current media item. The information is printed to an HTML TEXTAREA element named VideoSize. The Player** object was created with ID = "player".</span></span>


```JScript
<!-- Create an event handler to refresh the information when the current media changes. -->
<SCRIPT LANGUAGE = "JScript"  FOR = "Player"  EVENT = OpenStateChange(NewState)>

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



## <a name="requirements"></a><span data-ttu-id="5ddcf-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ddcf-116">Requirements</span></span>



| <span data-ttu-id="5ddcf-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ddcf-117">Requirement</span></span> | <span data-ttu-id="5ddcf-118">Wert</span><span class="sxs-lookup"><span data-stu-id="5ddcf-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="5ddcf-119">Version</span><span class="sxs-lookup"><span data-stu-id="5ddcf-119">Version</span></span><br/> | <span data-ttu-id="5ddcf-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="5ddcf-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="5ddcf-121">DLL</span><span class="sxs-lookup"><span data-stu-id="5ddcf-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="5ddcf-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ddcf-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ddcf-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ddcf-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ddcf-124">**Medienobjekt**</span><span class="sxs-lookup"><span data-stu-id="5ddcf-124">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="5ddcf-125">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="5ddcf-125">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="5ddcf-126">**Settings. mediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5ddcf-126">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="5ddcf-127">**Settings. requestmediaaccessrights**</span><span class="sxs-lookup"><span data-stu-id="5ddcf-127">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





