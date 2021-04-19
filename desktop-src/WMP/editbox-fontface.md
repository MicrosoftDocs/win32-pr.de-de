---
title: EditBox. fontface
description: Das fontface-Attribut gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft diese ab.
ms.assetid: 5fb5e6d2-8535-402e-9ca1-d43e334e94e3
keywords:
- EditBox. fontface-Fenster Media Player
topic_type:
- apiref
api_name:
- EDITBOX.fontFace
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c5794da93821db840a48facbba45540da9249a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362064"
---
# <a name="editboxfontface"></a><span data-ttu-id="3823e-104">EditBox. fontface</span><span class="sxs-lookup"><span data-stu-id="3823e-104">EDITBOX.fontFace</span></span>

<span data-ttu-id="3823e-105">Das **fontface** -Attribut gibt die Schriftart für Text im Bearbeitungsfeld-Steuerelement an oder ruft diese ab.</span><span class="sxs-lookup"><span data-stu-id="3823e-105">The **fontFace** attribute specifies or retrieves the font for text in the edit box control.</span></span>

``` syntax
        elementID.fontFace
```

## <a name="possible-values"></a><span data-ttu-id="3823e-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="3823e-106">Possible Values</span></span>

<span data-ttu-id="3823e-107">Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="3823e-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="3823e-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3823e-108">Remarks</span></span>

<span data-ttu-id="3823e-109">Dieses Attribut kann der Name einer beliebigen gültigen Schriftart sein, die in Windows verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="3823e-109">This attribute can be the name of any valid font available in Windows.</span></span> <span data-ttu-id="3823e-110">Das Installieren von Schriftarten wird von Windows Media Player nicht unterstützt. Wählen Sie also eine Schriftart aus, die Sie auf dem vorgesehenen System kennen.</span><span class="sxs-lookup"><span data-stu-id="3823e-110">Windows Media Player will not support installing fonts, so choose a font that you know will be on the intended system.</span></span>

<span data-ttu-id="3823e-111">Wenn die angegebene **fontface** nicht auf dem System des Benutzers verfügbar ist, wird für das Steuerelement "Bearbeitungsfeld" standardmäßig die Schriftart des Windows-Systems verwendet.</span><span class="sxs-lookup"><span data-stu-id="3823e-111">If the **fontFace** specified is not available on the user's system, the edit box control defaults to the Windows system font.</span></span> <span data-ttu-id="3823e-112">Der Standardwert für englischsprachige Systeme ist "Tahoma".</span><span class="sxs-lookup"><span data-stu-id="3823e-112">The default value for English-language systems is "Tahoma".</span></span> <span data-ttu-id="3823e-113">Bei internationalen Systemen wird der Standardwert aus einer Ressourcen Datei geladen.</span><span class="sxs-lookup"><span data-stu-id="3823e-113">For international systems, the default is loaded from a resource file.</span></span>

## <a name="requirements"></a><span data-ttu-id="3823e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3823e-114">Requirements</span></span>



| <span data-ttu-id="3823e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3823e-115">Requirement</span></span> | <span data-ttu-id="3823e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3823e-116">Value</span></span> |
|--------------------|---------------------------------------------------------|
| <span data-ttu-id="3823e-117">Version</span><span class="sxs-lookup"><span data-stu-id="3823e-117">Version</span></span><br/> | <span data-ttu-id="3823e-118">Windows Media Player für Windows XP oder höher</span><span class="sxs-lookup"><span data-stu-id="3823e-118">Windows Media Player for Windows XP or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3823e-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3823e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3823e-120">**EditBox-Element**</span><span class="sxs-lookup"><span data-stu-id="3823e-120">**EDITBOX Element**</span></span>](editbox-element.md)
</dt> <dt>

[<span data-ttu-id="3823e-121">**EditBox. FontSize**</span><span class="sxs-lookup"><span data-stu-id="3823e-121">**EDITBOX.fontSize**</span></span>](editbox-fontsize.md)
</dt> <dt>

[<span data-ttu-id="3823e-122">**EditBox. FontStyle**</span><span class="sxs-lookup"><span data-stu-id="3823e-122">**EDITBOX.fontStyle**</span></span>](editbox-fontstyle.md)
</dt> </dl>

 

 





