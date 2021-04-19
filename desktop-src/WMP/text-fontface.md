---
title: Text. fontface
description: Das fontface-Attribut gibt die Schriftart für das Text Steuerelement an oder ruft Sie ab.
ms.assetid: 3b39e245-139a-4361-b678-0f9e962996b7
keywords:
- Text. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 183b25547e456cb90cac4d2137354679e13d8a96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369119"
---
# <a name="textfontface"></a><span data-ttu-id="e9732-104">Text. fontface</span><span class="sxs-lookup"><span data-stu-id="e9732-104">TEXT.fontFace</span></span>

<span data-ttu-id="e9732-105">Das **fontface** -Attribut gibt die Schriftart für das Text Steuerelement an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="e9732-105">The **fontFace** attribute specifies or retrieves the typeface for the Text control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="e9732-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="e9732-106">Possible Values</span></span>

<span data-ttu-id="e9732-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="e9732-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9732-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e9732-108">Remarks</span></span>

<span data-ttu-id="e9732-109">Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die unter Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="e9732-109">This attribute can be the name of any valid font available on Windows.</span></span> <span data-ttu-id="e9732-110">Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.</span><span class="sxs-lookup"><span data-stu-id="e9732-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="e9732-111">Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird das Text Steuerelement standardmäßig auf die Schriftart des Windows-Systems festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e9732-111">If the **fontFace** specified is not available on the user's system, the Text control defaults to the Windows system font.</span></span>

<span data-ttu-id="e9732-112">Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9732-112">See the [value](text-value.md) attribute for a sample illustrating how the attributes of the **TEXT** element are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9732-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e9732-113">Requirements</span></span>



| <span data-ttu-id="e9732-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e9732-114">Requirement</span></span> | <span data-ttu-id="e9732-115">Wert</span><span class="sxs-lookup"><span data-stu-id="e9732-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="e9732-116">Version</span><span class="sxs-lookup"><span data-stu-id="e9732-116">Version</span></span><br/> | <span data-ttu-id="e9732-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="e9732-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e9732-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9732-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9732-119">**Text-Element**</span><span class="sxs-lookup"><span data-stu-id="e9732-119">**TEXT Element**</span></span>](text-element.md)
</dt> <dt>

[<span data-ttu-id="e9732-120">**Text. FontSize**</span><span class="sxs-lookup"><span data-stu-id="e9732-120">**TEXT.fontSize**</span></span>](text-fontsize.md)
</dt> </dl>

 

 





