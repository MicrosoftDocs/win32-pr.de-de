---
title: Design. currentViewID
description: Das currentViewID-Attribut gibt die aktuell angezeigte Ansicht an oder ruft Sie ab.
ms.assetid: 94f23da9-cfda-4dc4-9804-b7daff5ebb8f
keywords:
- Design. currentViewID Windows Media Player
topic_type:
- apiref
api_name:
- THEME.currentViewID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c0c1b52ffdc35abf846987ed459565904938d4e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372408"
---
# <a name="themecurrentviewid"></a><span data-ttu-id="d0714-104">Design. currentViewID</span><span class="sxs-lookup"><span data-stu-id="d0714-104">THEME.currentViewID</span></span>

<span data-ttu-id="d0714-105">Das **currentViewID** -Attribut gibt die aktuell angezeigte **Ansicht** an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="d0714-105">The **currentViewID** attribute specifies or retrieves the currently displayed **VIEW**.</span></span>

``` syntax
theme.currentViewID
```

## <a name="possible-values"></a><span data-ttu-id="d0714-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d0714-106">Possible Values</span></span>

<span data-ttu-id="d0714-107">Dieses Attribut ist eine Lese-/schreibzeichenfolge, die die **ID** der aktuellen **Ansicht** angibt. </span><span class="sxs-lookup"><span data-stu-id="d0714-107">This attribute is a read/write **String** specifying the **id** of the current **VIEW**.</span></span> <span data-ttu-id="d0714-108">Er besitzt keinen Standardwert.</span><span class="sxs-lookup"><span data-stu-id="d0714-108">It has no default value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0714-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0714-109">Remarks</span></span>

<span data-ttu-id="d0714-110">Durch Angeben von **currentViewID** wird die vorhandene **CurrentView** (auf die durch das **View** Global-Attribut verwiesen wird) automatisch geschlossen, und die angegebene **Ansicht** wird geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d0714-110">Specifying **currentViewID** automatically closes the existing **currentView** (pointed to by the **view** global attribute) and opens the specified **VIEW**.</span></span>

## <a name="examples"></a><span data-ttu-id="d0714-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d0714-111">Examples</span></span>


```C++
<THEME currentViewID="startView">
  <VIEW>
    <TEXT value="this would have been the default view"/>
  </VIEW>
  <VIEW id="startView">
    <TEXT value="go to new view"
        onclick="jscript:theme.currentViewID='newView'"/>
  </VIEW>
  <VIEW id="newView">
    <TEXT value="new view"/>
  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="d0714-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d0714-112">Requirements</span></span>



| <span data-ttu-id="d0714-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d0714-113">Requirement</span></span> | <span data-ttu-id="d0714-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d0714-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="d0714-115">Version</span><span class="sxs-lookup"><span data-stu-id="d0714-115">Version</span></span><br/> | <span data-ttu-id="d0714-116">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="d0714-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d0714-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0714-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0714-118">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="d0714-118">**THEME Element**</span></span>](theme-element.md)
</dt> </dl>

 

 





