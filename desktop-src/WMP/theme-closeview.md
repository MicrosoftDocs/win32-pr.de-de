---
title: Design. CloseView
description: Die CloseView-Methode schließt eine geöffnete Ansicht.
ms.assetid: 37b56a7d-8031-4055-95ad-0510105e1c1f
keywords:
- Design. CloseView-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.closeView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b39083979809fc2e747c54569db8d03298a951c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371081"
---
# <a name="themecloseview"></a><span data-ttu-id="f9c5e-104">Design. CloseView</span><span class="sxs-lookup"><span data-stu-id="f9c5e-104">THEME.closeView</span></span>

<span data-ttu-id="f9c5e-105">Die **CloseView** -Methode schließt eine geöffnete **Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="f9c5e-105">The **closeView** method closes an open **VIEW**.</span></span>

``` syntax
        theme.closeView(theView)
```

## <a name="parameters"></a><span data-ttu-id="f9c5e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9c5e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9c5e-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*der Ansicht*</span><span class="sxs-lookup"><span data-stu-id="f9c5e-107"><span id="theView"></span><span id="theview"></span><span id="THEVIEW"></span>*theView*</span></span>
</dt> <dd>

<span data-ttu-id="f9c5e-108">Eine **Zeichenfolge** , die die **ID** der **Sicht** angibt, die geschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9c5e-108">A **String** specifying the **id** of the **VIEW** to close.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9c5e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9c5e-109">Return Value</span></span>

<span data-ttu-id="f9c5e-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f9c5e-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="f9c5e-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9c5e-111">Examples</span></span>


```C++
<THEME>
  <VIEW>
    <TEXT value="open" 
        onclick="jscript:theme.openView('newView')"/>
    <TEXT top="30" value="close"
        onclick="jscript:theme.closeView('newView')"/>
  </VIEW>
  <VIEW id="newView"/>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="f9c5e-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9c5e-112">Requirements</span></span>



| <span data-ttu-id="f9c5e-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9c5e-113">Requirement</span></span> | <span data-ttu-id="f9c5e-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f9c5e-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="f9c5e-115">Version</span><span class="sxs-lookup"><span data-stu-id="f9c5e-115">Version</span></span><br/> | <span data-ttu-id="f9c5e-116">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="f9c5e-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f9c5e-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9c5e-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9c5e-118">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="f9c5e-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="f9c5e-119">**Design. OpenView**</span><span class="sxs-lookup"><span data-stu-id="f9c5e-119">**THEME.openView**</span></span>](theme-openview.md)
</dt> </dl>

 

 





