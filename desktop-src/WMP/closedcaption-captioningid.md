---
title: Closedcaption. captioningid
description: Die captioningid-Eigenschaft gibt den Namen des Elements an, das die Untertitel anzeigt, oder ruft ihn ab.
ms.assetid: 99d4aae3-485f-4c86-9130-101b1ca968e9
keywords:
- Fenster "closedcaption. captioningid" Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.captioningID
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faadae626dd5ac0314c4140e3f9d82ab645ef9b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365364"
---
# <a name="closedcaptioncaptioningid"></a><span data-ttu-id="b9c50-104">Closedcaption. captioningid</span><span class="sxs-lookup"><span data-stu-id="b9c50-104">ClosedCaption.captioningID</span></span>

<span data-ttu-id="b9c50-105">Die **captioningid** -Eigenschaft gibt den Namen des Elements an, das die Untertitel anzeigt, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="b9c50-105">The **captioningID** property specifies or retrieves the name of the element displaying the captioning.</span></span>

``` syntax
player.closedCaption.captioningID
```

## <a name="possible-values"></a><span data-ttu-id="b9c50-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="b9c50-106">Possible Values</span></span>

<span data-ttu-id="b9c50-107">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="b9c50-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="b9c50-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b9c50-108">Remarks</span></span>

<span data-ttu-id="b9c50-109">Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange es das innerHTML-Attribut unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b9c50-109">The element name specified can be any HTML element in the webpage as long as it supports the innerHTML attribute.</span></span> <span data-ttu-id="b9c50-110">Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im gleichen Frame wie das Player-Steuerelement verweisen.</span><span class="sxs-lookup"><span data-stu-id="b9c50-110">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Player control.</span></span>

<span data-ttu-id="b9c50-111">**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="b9c50-111">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="b9c50-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b9c50-112">Examples</span></span>

<span data-ttu-id="b9c50-113">Im folgenden Microsoft JScript-Beispiel wird *closedcaption* verwendet. **captioningid** zum Auswählen des Bereichs einer Webseite, in der Beschriftungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b9c50-113">The following Microsoft JScript example uses *ClosedCaption*.**captioningID** to choose the area of a webpage used to display captions.</span></span> <span data-ttu-id="b9c50-114">Es wurden zwei HTML-div-Elemente mit ID = CC1 bzw. ID = cc2 erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c50-114">Two HTML DIV elements were created, with ID = CC1 and ID = CC2, respectively.</span></span> <span data-ttu-id="b9c50-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="b9c50-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create two HTML BUTTON elements to allow the user to choose a display region. -->
<INPUT TYPE = "BUTTON"  NAME = "SET1"  VALUE = "Move Caption to CC1"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC2.innerHTML = 'This is the CC2 DIV';

           /* Show the captions in the DIV named CC1. */ 
           Player.ClosedCaption.captioningID = 'CC1';
          ">

<INPUT TYPE = "BUTTON" NAME = "SET2" VALUE = "Move Caption to CC2"
       OnClick = "
           /* Clear the caption text from the other DIV */
           CC1.innerHTML = 'This is the CC1 DIV';

           /* Show the captions in the DIV named CC2. */
           Player.ClosedCaption.captioningID = 'CC2';
          ">

```



## <a name="requirements"></a><span data-ttu-id="b9c50-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9c50-116">Requirements</span></span>



| <span data-ttu-id="b9c50-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9c50-117">Requirement</span></span> | <span data-ttu-id="b9c50-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b9c50-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c50-119">Version</span><span class="sxs-lookup"><span data-stu-id="b9c50-119">Version</span></span><br/> | <span data-ttu-id="b9c50-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="b9c50-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b9c50-121">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c50-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="b9c50-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c50-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c50-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9c50-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c50-124">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="b9c50-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="b9c50-125">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="b9c50-125">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





