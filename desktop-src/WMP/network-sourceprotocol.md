---
title: Network. sourceprotocol
description: Die sourceprotocol-Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.
ms.assetid: f09bbcd0-9c34-49d1-8080-247aed2548d5
keywords:
- Network. sourceprotocol-Windows-Media Player
topic_type:
- apiref
api_name:
- Network.sourceProtocol
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29e3f0ad63827605eb79a89325877e4bb83bfc62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370617"
---
# <a name="networksourceprotocol"></a><span data-ttu-id="d47d3-104">Network. sourceprotocol</span><span class="sxs-lookup"><span data-stu-id="d47d3-104">Network.sourceProtocol</span></span>

<span data-ttu-id="d47d3-105">Die **sourceprotocol** -Eigenschaft ruft das Quell Protokoll ab, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d47d3-105">The **sourceProtocol** property retrieves the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="d47d3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d47d3-106">Syntax</span></span>

<span data-ttu-id="d47d3-107">*Player*. *Netzwerk*. **sourceprotocol**</span><span class="sxs-lookup"><span data-stu-id="d47d3-107">*player*.*network*.**sourceProtocol**</span></span>

## <a name="possible-values"></a><span data-ttu-id="d47d3-108">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d47d3-108">Possible Values</span></span>

<span data-ttu-id="d47d3-109">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="d47d3-109">This property is a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d47d3-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d47d3-110">Remarks</span></span>

<span data-ttu-id="d47d3-111">Diese Eigenschaft wird auf "" (leere Zeichenfolge) festgelegt, wenn Medien von einer CD oder DVD abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="d47d3-111">This property is set to "" (empty string) when playing media from a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="d47d3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d47d3-112">Examples</span></span>

<span data-ttu-id="d47d3-113">Im folgenden JScript-Beispiel wird *Network* verwendet. **sourceprotocol** zum Anzeigen des Quell Protokolls, das zum Empfangen von Daten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d47d3-113">The following JScript example uses *Network*.**sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="d47d3-114">Die Informationen werden in einem mit ID = "SP" erstellten HTML-div angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d47d3-114">The information is displayed in an HTML DIV created with ID = "SP".</span></span> <span data-ttu-id="d47d3-115">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="d47d3-115">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   if (3 == NewState){
     SP.innerHTML = "Source protocol: " + Player.network.sourceProtocol;
   }
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="d47d3-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d47d3-116">Requirements</span></span>



| <span data-ttu-id="d47d3-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d47d3-117">Requirement</span></span> | <span data-ttu-id="d47d3-118">Wert</span><span class="sxs-lookup"><span data-stu-id="d47d3-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d47d3-119">Version</span><span class="sxs-lookup"><span data-stu-id="d47d3-119">Version</span></span><br/> | <span data-ttu-id="d47d3-120">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="d47d3-120">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="d47d3-121">DLL</span><span class="sxs-lookup"><span data-stu-id="d47d3-121">DLL</span></span><br/>     | <dl> <span data-ttu-id="d47d3-122"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d47d3-122"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d47d3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d47d3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d47d3-124">**Netzwerk Objekt**</span><span class="sxs-lookup"><span data-stu-id="d47d3-124">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





