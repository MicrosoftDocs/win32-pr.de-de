---
title: Closedcaption. samilang
description: Die samilang-Eigenschaft gibt die für Untertitel angezeigte Sprache an oder ruft Sie ab.
ms.assetid: 990fb180-cb37-4022-b236-03f5acfd3ad3
keywords:
- Closedcaption. samilang-Fenster Media Player
topic_type:
- apiref
api_name:
- ClosedCaption.SAMILang
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae99b9a164e29b4adeb2fd7b23a1b79945dcb26e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370635"
---
# <a name="closedcaptionsamilang"></a><span data-ttu-id="0470c-104">Closedcaption. samilang</span><span class="sxs-lookup"><span data-stu-id="0470c-104">ClosedCaption.SAMILang</span></span>

<span data-ttu-id="0470c-105">Die **samilang** -Eigenschaft gibt die für Untertitel angezeigte Sprache an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="0470c-105">The **SAMILang** property specifies or retrieves the language displayed for closed captioning.</span></span>

``` syntax
player.closedCaption.SAMILang
```

## <a name="possible-values"></a><span data-ttu-id="0470c-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="0470c-106">Possible Values</span></span>

<span data-ttu-id="0470c-107">Diese Eigenschaft ist eine Lese- **/schreibzeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="0470c-107">This property is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="0470c-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0470c-108">Remarks</span></span>

<span data-ttu-id="0470c-109">Eine Sami-Datei kann Text für eine oder mehrere Sprachen enthalten.</span><span class="sxs-lookup"><span data-stu-id="0470c-109">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="0470c-110">Die Sprachen, die für Untertitel verfügbar sind, werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="0470c-110">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="0470c-111">Eine Sprach-ID wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Zeitraum (.) vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="0470c-111">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="0470c-112">Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="0470c-112">The name specified for a language can be any string.</span></span> <span data-ttu-id="0470c-113">Beispielsweise könnte Folgendes zum Definieren von US-Englisch verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="0470c-113">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}

```



<span data-ttu-id="0470c-114">Wenn keine Sami-Sprache angegeben ist, wird standardmäßig die erste in der Sami-Datei definierte Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="0470c-114">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="0470c-115">Der Wert, den Sie mithilfe von *closedcaption* übergeben. **Samilang** muss mit dem **Name** -Attribut im sprachspezifizierer identisch sein.</span><span class="sxs-lookup"><span data-stu-id="0470c-115">The value you pass using *ClosedCaption*.**SAMILang** must match the **Name** attribute in the language specifier.</span></span>

<span data-ttu-id="0470c-116">**Windows Media Player 10 Mobile:** Diese Eigenschaft ist schreibgeschützt und gibt immer eine leere Zeichenfolge zurück.</span><span class="sxs-lookup"><span data-stu-id="0470c-116">**Windows Media Player 10 Mobile:** This property is read only, and always returns an empty string.</span></span>

## <a name="examples"></a><span data-ttu-id="0470c-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0470c-117">Examples</span></span>

<span data-ttu-id="0470c-118">Im folgenden JScript-Beispiel wird *closedcaption* verwendet. **Samilang** in einem HTML-SELECT-Element, um die Closed Caption-Sprache anzugeben.</span><span class="sxs-lookup"><span data-stu-id="0470c-118">The following JScript example uses *ClosedCaption*.**SAMILang** in an HTML SELECT element to specify the closed caption language.</span></span> <span data-ttu-id="0470c-119">Das **Player** -Objekt wurde mit ID = "Player" erstellt.</span><span class="sxs-lookup"><span data-stu-id="0470c-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create the SELECT element. -->
<SELECT ID = CCLANG  NAME = "CCLANG"  LANGUAGE = "JScript"

     /* Set the closed caption language when the SELECT element changes. */
        onChange = "Player.closedCaption.SAMILang = CCLANG.value;
        ">

        /* Fill in the SELECT element options. */
           <OPTION VALUE = "'Spanish Captions'">Spanish
           <OPTION VALUE = "'Japanese Captions'">Japanese
           <OPTION VALUE = "'English Captions'">English
           <OPTION VALUE = "'French Captions'">French
           <OPTION VALUE = "'German Captions'" SELECTED>German
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="0470c-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0470c-120">Requirements</span></span>



| <span data-ttu-id="0470c-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0470c-121">Requirement</span></span> | <span data-ttu-id="0470c-122">Wert</span><span class="sxs-lookup"><span data-stu-id="0470c-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0470c-123">Version</span><span class="sxs-lookup"><span data-stu-id="0470c-123">Version</span></span><br/> | <span data-ttu-id="0470c-124">Windows Media Player Version 7,0 oder höher.</span><span class="sxs-lookup"><span data-stu-id="0470c-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="0470c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0470c-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="0470c-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0470c-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0470c-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0470c-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0470c-128">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="0470c-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="0470c-129">**Closedcaption-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0470c-129">**ClosedCaption Object**</span></span>](closedcaption-object.md)
</dt> </dl>

 

 





