---
title: ListBox. fontface
description: Das fontface-Attribut gibt die Schriftart für das Listenfeld-Steuerelement an oder ruft diese ab.
ms.assetid: 15e3180a-6e1e-4654-a0bb-164d66a86a26
keywords:
- ListBox. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- LISTBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c03c367001b307dd8bd5059ec7e3f4a0b364e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373750"
---
# <a name="listboxfontface"></a><span data-ttu-id="1c1ce-104">ListBox. fontface</span><span class="sxs-lookup"><span data-stu-id="1c1ce-104">LISTBOX.fontFace</span></span>

<span data-ttu-id="1c1ce-105">Das **fontface** -Attribut gibt die Schriftart für das Listenfeld-Steuerelement an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-105">The **fontFace** attribute specifies or retrieves the font for the list box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="1c1ce-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="1c1ce-106">Possible Values</span></span>

<span data-ttu-id="1c1ce-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c1ce-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-108">Remarks</span></span>

<span data-ttu-id="1c1ce-109">Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die in Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="1c1ce-110">Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="1c1ce-111">Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird im Listenfeld-Steuerelement standardmäßig die Schriftart des Windows-Systems angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-111">If the **fontFace** specified is not available on the user's system, the list box control defaults to the Windows system font.</span></span> <span data-ttu-id="1c1ce-112">Der Standardwert für englischsprachige Systeme ist "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="1c1ce-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="1c1ce-113">Bei internationalen Systemen wird der Standardwert aus einer Ressourcen Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="1c1ce-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c1ce-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c1ce-114">Requirements</span></span>



| <span data-ttu-id="1c1ce-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c1ce-115">Requirement</span></span> | <span data-ttu-id="1c1ce-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1c1ce-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="1c1ce-117">Version</span><span class="sxs-lookup"><span data-stu-id="1c1ce-117">Version</span></span><br/> | <span data-ttu-id="1c1ce-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="1c1ce-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c1ce-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c1ce-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c1ce-120">**ListBox-Element**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-120">**LISTBOX Element**</span></span>](listbox-element.md)
</dt> <dt>

[<span data-ttu-id="1c1ce-121">**ListBox. FontSize**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-121">**LISTBOX.fontSize**</span></span>](listbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="1c1ce-122">**ListBox. FontStyle**</span><span class="sxs-lookup"><span data-stu-id="1c1ce-122">**LISTBOX.fontStyle**</span></span>](listbox-fontstyle.md)
</dt> </dl>

 

 





