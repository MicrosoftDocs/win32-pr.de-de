---
title: Network. Framerate
description: Die Framerate-Eigenschaft ruft die aktuelle Video Frame Rate in Frames pro hundert Sekunden ab. Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde an.
ms.assetid: ee30dce5-a42e-4be5-ab4b-0d5f8869d23a
keywords:
- Network. Framerate-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.frameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30ec6e16a3cef86a385525a793d73a50c3124e21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361315"
---
# <a name="networkframerate"></a><span data-ttu-id="a9899-105">Network. Framerate</span><span class="sxs-lookup"><span data-stu-id="a9899-105">Network.frameRate</span></span>

<span data-ttu-id="a9899-106">Die **Framerate** -Eigenschaft ruft die aktuelle Video Frame Rate in Frames pro hundert Sekunden ab.</span><span class="sxs-lookup"><span data-stu-id="a9899-106">The **frameRate** property retrieves the current video frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="a9899-107">Der Wert 2998 gibt z. b. 29,98 Frames pro Sekunde an.</span><span class="sxs-lookup"><span data-stu-id="a9899-107">For example, a value of 2998 indicates 29.98 frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9899-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9899-108">Syntax</span></span>

<span data-ttu-id="a9899-109">*Player*. *Netzwerk*. **Framerate**</span><span class="sxs-lookup"><span data-stu-id="a9899-109">*player*.*network*.**frameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a9899-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="a9899-110">Possible Values</span></span>

<span data-ttu-id="a9899-111">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="a9899-111">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="a9899-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9899-112">Examples</span></span>

<span data-ttu-id="a9899-113">Im folgenden JScript-Beispiel wird *Network* verwendet. **Framerate** , um die aktuelle Framerate anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a9899-113">The following JScript example uses *Network*.**frameRate** to display the current frame rate.</span></span> <span data-ttu-id="a9899-114">Die Informationen werden in einem HTML-div-Code angezeigt, der mit ID = "fr" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="a9899-114">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="a9899-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="a9899-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the current frame rate.
          FR.innerHTML = "Frame Rate: ";
          FR.innerHTML += Player.network.frameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a9899-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a9899-116">Requirements</span></span>



| <span data-ttu-id="a9899-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a9899-117">Requirement</span></span> | <span data-ttu-id="a9899-118">Wert</span><span class="sxs-lookup"><span data-stu-id="a9899-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a9899-119">Version</span><span class="sxs-lookup"><span data-stu-id="a9899-119">Version</span></span><br/> | <span data-ttu-id="a9899-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="a9899-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a9899-121">DLL</span><span class="sxs-lookup"><span data-stu-id="a9899-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="a9899-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9899-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9899-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9899-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9899-124">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="a9899-124">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a9899-125">**Network. Encode dframerate**</span><span class="sxs-lookup"><span data-stu-id="a9899-125">**Network.encodedFrameRate**</span></span>](network-encodedframerate.md)
</dt> </dl>

 

 





