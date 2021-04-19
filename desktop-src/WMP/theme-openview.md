---
title: Design. OpenView
description: Die OpenView-Methode öffnet eine Ansicht in einem neuen Fenster.
ms.assetid: 2aa63c29-dafe-4942-a010-076f1503862b
keywords:
- Design. OpenView-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.openView
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d66ff2cf47004c7687a37f1f22a87bdeb534d344
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373770"
---
# <a name="themeopenview"></a><span data-ttu-id="fe2d6-104">Design. OpenView</span><span class="sxs-lookup"><span data-stu-id="fe2d6-104">THEME.openView</span></span>

<span data-ttu-id="fe2d6-105">Die **OpenView** -Methode öffnet eine **Ansicht** in einem neuen Fenster.</span><span class="sxs-lookup"><span data-stu-id="fe2d6-105">The **openView** method opens a **VIEW** in a new window.</span></span>

``` syntax
        theme.openView(view)
```

## <a name="parameters"></a><span data-ttu-id="fe2d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fe2d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe2d6-107"><span id="view"></span><span id="VIEW"></span>*Anschauung*</span><span class="sxs-lookup"><span data-stu-id="fe2d6-107"><span id="view"></span><span id="VIEW"></span>*view*</span></span>
</dt> <dd>

<span data-ttu-id="fe2d6-108">Eine **Zeichenfolge** , die die **ID** der zu öffnenden **Ansicht** angibt.</span><span class="sxs-lookup"><span data-stu-id="fe2d6-108">A **String** specifying the **id** of the **VIEW** to open.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe2d6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fe2d6-109">Return Value</span></span>

<span data-ttu-id="fe2d6-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fe2d6-110">This method does not return a value.</span></span>

## <a name="examples"></a><span data-ttu-id="fe2d6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fe2d6-111">Examples</span></span>


```JScript
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



## <a name="requirements"></a><span data-ttu-id="fe2d6-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fe2d6-112">Requirements</span></span>



| <span data-ttu-id="fe2d6-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fe2d6-113">Requirement</span></span> | <span data-ttu-id="fe2d6-114">Wert</span><span class="sxs-lookup"><span data-stu-id="fe2d6-114">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="fe2d6-115">Version</span><span class="sxs-lookup"><span data-stu-id="fe2d6-115">Version</span></span><br/> | <span data-ttu-id="fe2d6-116">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="fe2d6-116">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe2d6-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fe2d6-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe2d6-118">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="fe2d6-118">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="fe2d6-119">**Design. CloseView**</span><span class="sxs-lookup"><span data-stu-id="fe2d6-119">**THEME.closeView**</span></span>](theme-closeview.md)
</dt> <dt>

[<span data-ttu-id="fe2d6-120">**Design. openviewrelative**</span><span class="sxs-lookup"><span data-stu-id="fe2d6-120">**THEME.openViewRelative**</span></span>](theme-openviewrelative.md)
</dt> </dl>

 

 





