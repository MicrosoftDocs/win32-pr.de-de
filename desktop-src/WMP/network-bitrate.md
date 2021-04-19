---
title: Network. Bitrate
description: Die Bitrate-Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.
ms.assetid: e970a43a-1773-4dc0-ac2f-115f698bc1f4
keywords:
- Windows-Media Player "Network. Bitrate"
topic_type:
- apiref
api_name:
- Network.bitRate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4373d667ea41d55b5b0e12f1a47289f15d7b115b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370013"
---
# <a name="networkbitrate"></a><span data-ttu-id="2d102-104">Network. Bitrate</span><span class="sxs-lookup"><span data-stu-id="2d102-104">Network.bitRate</span></span>

<span data-ttu-id="2d102-105">Die **Bitrate** -Eigenschaft ruft die aktuelle Bitrate ab, die empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="2d102-105">The **bitRate** property retrieves the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d102-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="2d102-106">Syntax</span></span>

<span data-ttu-id="2d102-107">*Player*. *Netzwerk*. **Bitrate**</span><span class="sxs-lookup"><span data-stu-id="2d102-107">*player*.*network*.**bitRate**</span></span>

## <a name="possible-values"></a><span data-ttu-id="2d102-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2d102-108">Possible Values</span></span>

<span data-ttu-id="2d102-109">Diese Eigenschaft ist eine schreibgeschützte **Zahl** (**Long**).</span><span class="sxs-lookup"><span data-stu-id="2d102-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="2d102-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2d102-110">Remarks</span></span>

<span data-ttu-id="2d102-111">Dieser Wert ist eine Kombination aus den Bitraten der aktuellen Video-und Audiodatenströme.</span><span class="sxs-lookup"><span data-stu-id="2d102-111">This value is a combination of the bit rates of both the current video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="2d102-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2d102-112">Examples</span></span>

<span data-ttu-id="2d102-113">Im folgenden JScript-Beispiel wird *Network* verwendet. **Bitrate** zum Anzeigen der aktuellen Medien Bitrate.</span><span class="sxs-lookup"><span data-stu-id="2d102-113">The following JScript example uses *Network*.**bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="2d102-114">Die Informationen werden in einem mit ID = "br" erstellten HTML-div angezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d102-114">The information is displayed in an HTML DIV created with ID = "BR".</span></span> <span data-ttu-id="2d102-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="2d102-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!<entity type="mdash"/>-Create an event handler. -->
<SCRIPT FOR = Player EVENT = PlayStateChange()>
   switch (Player.playState){

      case 3:

         if (Player.network.bitRate){

            BR.innerHTML = "Current Bit Rate: " + Player.network.bitRate;
            BR.innerHTML += " K bits/second";
          }

         break;

      default:
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="2d102-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2d102-116">Requirements</span></span>



| <span data-ttu-id="2d102-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2d102-117">Requirement</span></span> | <span data-ttu-id="2d102-118">Wert</span><span class="sxs-lookup"><span data-stu-id="2d102-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2d102-119">Version</span><span class="sxs-lookup"><span data-stu-id="2d102-119">Version</span></span><br/> | <span data-ttu-id="2d102-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="2d102-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="2d102-121">DLL</span><span class="sxs-lookup"><span data-stu-id="2d102-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="2d102-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d102-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2d102-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2d102-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d102-124">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="2d102-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





