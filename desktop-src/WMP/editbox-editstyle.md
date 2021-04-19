---
title: EditBox. editstyle
description: Das editstyle-Attribut gibt den Stil des Steuer Elements "Bearbeitungsfeld" an oder ruft ihn ab.
ms.assetid: 1b3052c4-3087-4d41-af03-d7758680cc3b
keywords:
- EditBox. editstyle-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.editStyle
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229f225dfca0ec00dd4f45a4eb63f6b2503d5df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366771"
---
# <a name="editboxeditstyle"></a><span data-ttu-id="2efed-104">EditBox. editstyle</span><span class="sxs-lookup"><span data-stu-id="2efed-104">EDITBOX.editStyle</span></span>

<span data-ttu-id="2efed-105">Das **editstyle** -Attribut gibt den Stil des Steuer Elements "Bearbeitungsfeld" an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="2efed-105">The **editStyle** attribute specifies or retrieves the style of the edit box control.</span></span>

``` syntax
        elementID.editStyle
```

## <a name="possible-values"></a><span data-ttu-id="2efed-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="2efed-106">Possible Values</span></span>

<span data-ttu-id="2efed-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="2efed-107">This attribute is a read/write **String** containing one of the following values.</span></span>



| <span data-ttu-id="2efed-108">Wert</span><span class="sxs-lookup"><span data-stu-id="2efed-108">Value</span></span>     | <span data-ttu-id="2efed-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2efed-109">Description</span></span>                                                                     |
|-----------|---------------------------------------------------------------------------------|
| <span data-ttu-id="2efed-110">normal</span><span class="sxs-lookup"><span data-stu-id="2efed-110">normal</span></span>    | <span data-ttu-id="2efed-111">Standard.</span><span class="sxs-lookup"><span data-stu-id="2efed-111">Default.</span></span> <span data-ttu-id="2efed-112">Zeigt den normalen Text in einer einzelnen Zeile an.</span><span class="sxs-lookup"><span data-stu-id="2efed-112">Displays normal text on a single line.</span></span>                                 |
| <span data-ttu-id="2efed-113">password</span><span class="sxs-lookup"><span data-stu-id="2efed-113">password</span></span>  | <span data-ttu-id="2efed-114">Zeigt Sternchen ( \* ) anstelle von Text an.</span><span class="sxs-lookup"><span data-stu-id="2efed-114">Displays asterisks (\*) in place of text.</span></span> <span data-ttu-id="2efed-115">Kann nur zur Entwurfszeit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2efed-115">Can only be specified at design time.</span></span> |
| <span data-ttu-id="2efed-116">Großbuchstaben</span><span class="sxs-lookup"><span data-stu-id="2efed-116">uppercase</span></span> | <span data-ttu-id="2efed-117">Zeigt Text als Großbuchstaben an.</span><span class="sxs-lookup"><span data-stu-id="2efed-117">Displays text as all uppercase.</span></span>                                                 |
| <span data-ttu-id="2efed-118">Kleinbuchstaben</span><span class="sxs-lookup"><span data-stu-id="2efed-118">lowercase</span></span> | <span data-ttu-id="2efed-119">Zeigt Text in Kleinbuchstaben an.</span><span class="sxs-lookup"><span data-stu-id="2efed-119">Displays text as all lowercase.</span></span>                                                 |
| <span data-ttu-id="2efed-120">number</span><span class="sxs-lookup"><span data-stu-id="2efed-120">number</span></span>    | <span data-ttu-id="2efed-121">Zeigt nur Zahlen an.</span><span class="sxs-lookup"><span data-stu-id="2efed-121">Only displays numbers.</span></span>                                                          |
| <span data-ttu-id="2efed-122">mehrzeiligen</span><span class="sxs-lookup"><span data-stu-id="2efed-122">multiline</span></span> | <span data-ttu-id="2efed-123">Zeigt mehrere Textzeilen an.</span><span class="sxs-lookup"><span data-stu-id="2efed-123">Displays multiple lines of text.</span></span> <span data-ttu-id="2efed-124">Kann nur zur Entwurfszeit angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2efed-124">Can only be specified at design time.</span></span>          |



 

## <a name="remarks"></a><span data-ttu-id="2efed-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2efed-125">Remarks</span></span>

<span data-ttu-id="2efed-126">Dieses Attribut kann zur Entwurfszeit nur auf "Password" oder "Multiline" festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="2efed-126">This attribute can only be set to "password" or "multiline" at design time.</span></span> <span data-ttu-id="2efed-127">Wenn Sie auf "Multiline" festgelegt ist, kann der Wert zur Laufzeit nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="2efed-127">If it is set to "multiline", the value cannot be changed at run time.</span></span>

## <a name="requirements"></a><span data-ttu-id="2efed-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2efed-128">Requirements</span></span>



| <span data-ttu-id="2efed-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2efed-129">Requirement</span></span> | <span data-ttu-id="2efed-130">Wert</span><span class="sxs-lookup"><span data-stu-id="2efed-130">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="2efed-131">Version</span><span class="sxs-lookup"><span data-stu-id="2efed-131">Version</span></span><br/> | <span data-ttu-id="2efed-132">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="2efed-132">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2efed-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2efed-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2efed-134">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="2efed-134">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> </dl>

 

 





