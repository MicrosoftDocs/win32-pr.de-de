---
title: Closedcaption. samistyle
description: Die samistyle-Eigenschaft gibt den Beschriftungs Stil an oder ruft ihn ab.
ms.assetid: 5535fb31-f1c0-49c4-b758-df74964b1e67
keywords:
- Fenster "closedcaption. samistyle" Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMIStyle
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebe81c2c2c4f4504d6167abe538c52ab769550a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359309"
---
# <a name="closedcaptionsamistyle"></a><span data-ttu-id="63b64-104">Closedcaption. samistyle</span><span class="sxs-lookup"><span data-stu-id="63b64-104">ClosedCaption.SAMIStyle</span></span>

<span data-ttu-id="63b64-105">Die **samistyle** -Eigenschaft gibt den Beschriftungs Stil an oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="63b64-105">The **SAMIStyle** property specifies or retrieves the closed captioning style.</span></span>

``` syntax
player.closedCaption.SAMIStyle
```

## <a name="possible-values"></a><span data-ttu-id="63b64-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="63b64-106">Possible Values</span></span>

<span data-ttu-id="63b64-107">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="63b64-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="63b64-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="63b64-108">Remarks</span></span>

<span data-ttu-id="63b64-109">Eine Sami-Datei kann mehrere Format Definitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="63b64-109">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="63b64-110">Sami-Stile werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="63b64-110">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="63b64-111">Ein Stil wird mit einer Text Zeichenfolge mit vorangestelltem \# Zeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="63b64-111">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="63b64-112">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="63b64-112">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}

```



<span data-ttu-id="63b64-113">Gibt einen Stil an, der eine bestimmte Schriftart erzeugt.</span><span class="sxs-lookup"><span data-stu-id="63b64-113">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="63b64-114">Wenn kein Sami-Format angegeben ist, wird standardmäßig das erste Format verwendet, das in der Sami-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="63b64-114">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="63b64-115">**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="63b64-115">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="63b64-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="63b64-116">Examples</span></span>

<span data-ttu-id="63b64-117">Im folgenden JScript-Beispiel wird ein HTML-SELECT-Element erstellt, das *closedcaption* verwendet. **Samistyle** , um die Darstellung des geschlossenen Beschriftungs Texts zu ändern.</span><span class="sxs-lookup"><span data-stu-id="63b64-117">The following JScript example creates an HTML SELECT element that uses *closedCaption*.**SAMIStyle** to change the appearance of the closed caption text.</span></span> <span data-ttu-id="63b64-118">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="63b64-118">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCMode  NAME = "CCMode"  LANGUAGE = "JScript"

       /* Change the text style when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMIStyle = CCMode.value;
        ">

       /* Fill the SELECT list with options, set the default to Strong. */
        <OPTION VALUE = "Normal">Normal
        <OPTION VALUE = "Small">Small 
        <OPTION VALUE = "Big Bold Italic" SELECTED>Strong
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="63b64-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="63b64-119">Requirements</span></span>



| <span data-ttu-id="63b64-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="63b64-120">Requirement</span></span> | <span data-ttu-id="63b64-121">Wert</span><span class="sxs-lookup"><span data-stu-id="63b64-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="63b64-122">Version</span><span class="sxs-lookup"><span data-stu-id="63b64-122">Version</span></span><br/> | <span data-ttu-id="63b64-123">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="63b64-123">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="63b64-124">DLL</span><span class="sxs-lookup"><span data-stu-id="63b64-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="63b64-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63b64-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63b64-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63b64-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63b64-127">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="63b64-127">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="63b64-128">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="63b64-128">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





