---
title: attribute_onchange
description: Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann. Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und \ 0034; OnChange \ 0034;, z. b. \ 0034; Value \_ OnChange \ 0034;.
ms.assetid: 783b686c-d56c-4036-9af4-97b9b246ef7e
keywords:
- attribute_onchange Windows Media Player
topic_type:
- apiref
api_name:
- attribute_onchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 45c4955193507e258d055a3399fc565c569fd291
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370236"
---
# <a name="attribute_onchange"></a><span data-ttu-id="05297-105">Attribut \_ OnChange</span><span class="sxs-lookup"><span data-stu-id="05297-105">attribute\_onchange</span></span>

<span data-ttu-id="05297-106">Wenn ein Skin-Attribut den Wert ändert, tritt ein Ereignis auf, das von einem Ereignishandler behandelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="05297-106">When a skin attribute changes value, an event occurs that can be handled by an event handler.</span></span> <span data-ttu-id="05297-107">Der Name des Ereignis Handlers ist der Name des Attributs, gefolgt von einem Unterstrich und "OnChange", z. b. "Value \_ OnChange".</span><span class="sxs-lookup"><span data-stu-id="05297-107">The name of the event handler is the name of the attribute followed by an underscore and "onchange", such as "value\_onchange".</span></span>

``` syntax
        attribute_onchange
```

## <a name="examples"></a><span data-ttu-id="05297-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05297-108">Examples</span></span>


```JScript
<SLIDER 
  thumbImage = "thumb.gif"
  value_onchange = "JScript: if (value == 100) backgroundColor = 'green';"
/>

```



## <a name="requirements"></a><span data-ttu-id="05297-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="05297-109">Requirements</span></span>



| <span data-ttu-id="05297-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="05297-110">Requirement</span></span> | <span data-ttu-id="05297-111">Wert</span><span class="sxs-lookup"><span data-stu-id="05297-111">Value</span></span> |
|--------------------|-----------------------------------------------------|
| <span data-ttu-id="05297-112">Version</span><span class="sxs-lookup"><span data-stu-id="05297-112">Version</span></span><br/> | <span data-ttu-id="05297-113">Windows Media Player, Version 70 oder höher</span><span class="sxs-lookup"><span data-stu-id="05297-113">Windows Media Player version 70 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05297-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05297-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05297-115">**Ambient-Ereignishandler**</span><span class="sxs-lookup"><span data-stu-id="05297-115">**Ambient Event Handlers**</span></span>](ambient-event-handlers.md)
</dt> </dl>

 

 





