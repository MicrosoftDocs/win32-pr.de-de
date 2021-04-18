---
title: Network. Encode dframerate
description: Die encoabdframerate-Eigenschaft ruft die vom Inhalts Autor angegebene Videoframerate in Frames pro Sekunde ab.
ms.assetid: 7dad5c90-f750-48d7-9dda-3fc07394edcc
keywords:
- Network. encodedframerate-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.encodedFrameRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0008eb5d648dc7d3f51b40329ca3d830c3590c49
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365533"
---
# <a name="networkencodedframerate"></a><span data-ttu-id="4a687-104">Network. Encode dframerate</span><span class="sxs-lookup"><span data-stu-id="4a687-104">Network.encodedFrameRate</span></span>

<span data-ttu-id="4a687-105">Die **encoabdframerate** -Eigenschaft ruft die vom Inhalts Autor angegebene Videoframerate in Frames pro Sekunde ab.</span><span class="sxs-lookup"><span data-stu-id="4a687-105">The **encodedFrameRate** property retrieves the video frame rate specified by the content author in frames per second.</span></span>

## <a name="syntax"></a><span data-ttu-id="4a687-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4a687-106">Syntax</span></span>

<span data-ttu-id="4a687-107">*Player*. *Netzwerk*. **encodframerate**</span><span class="sxs-lookup"><span data-stu-id="4a687-107">*player*.*network*.**encodedFrameRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="4a687-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="4a687-108">Possible Values</span></span>

<span data-ttu-id="4a687-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="4a687-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="examples"></a><span data-ttu-id="4a687-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a687-110">Examples</span></span>

<span data-ttu-id="4a687-111">Im folgenden JScript-Beispiel wird *Network* verwendet. **encodedframerate** , um die beim Codieren der Datei angegebene Framerate anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="4a687-111">The following JScript example uses *Network*.**encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="4a687-112">Die Informationen werden in einem HTML-div-Code angezeigt, der mit ID = "fr" erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4a687-112">The information is displayed in an HTML DIV created with ID = "FR".</span></span> <span data-ttu-id="4a687-113">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4a687-113">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   switch (NewState){
      case 3:
          // Display the encoded frame rate.
          FR.innerHTML = "Encoded Frame Rate: ";
          FR.innerHTML += Player.network.encodedFrameRate;
          break;

      default:
      }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="4a687-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a687-114">Requirements</span></span>



| <span data-ttu-id="4a687-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a687-115">Requirement</span></span> | <span data-ttu-id="4a687-116">Wert</span><span class="sxs-lookup"><span data-stu-id="4a687-116">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="4a687-117">Version</span><span class="sxs-lookup"><span data-stu-id="4a687-117">Version</span></span><br/> | <span data-ttu-id="4a687-118">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="4a687-118">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="4a687-119">DLL</span><span class="sxs-lookup"><span data-stu-id="4a687-119">DLL</span></span><br/>     | <dl> <span data-ttu-id="4a687-120"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4a687-120"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a687-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a687-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a687-122">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="4a687-122">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="4a687-123">**Network. Framerate**</span><span class="sxs-lookup"><span data-stu-id="4a687-123">**Network.frameRate**</span></span>](network-framerate.md)
</dt> </dl>

 

 





