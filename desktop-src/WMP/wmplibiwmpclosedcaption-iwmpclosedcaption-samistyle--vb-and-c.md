---
title: Iwmpclosedcaption samistyle (Eigenschaft)
description: Die samistyle-Eigenschaft ruft den Untertitel Stil ab oder legt ihn fest.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Samistyle-Eigenschaften Fenster Media Player
- Samistyle-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samistyle (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365650"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a><span data-ttu-id="37fd2-106">Iwmpclosedcaption:: samistyle (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="37fd2-106">IWMPClosedCaption::SAMIStyle property</span></span>

<span data-ttu-id="37fd2-107">Die **samistyle** -Eigenschaft ruft den Untertitel Stil ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="37fd2-107">The **SAMIStyle** property gets or sets the closed captioning style.</span></span>

## <a name="syntax"></a><span data-ttu-id="37fd2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="37fd2-108">Syntax</span></span>


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a><span data-ttu-id="37fd2-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="37fd2-109">Property value</span></span>

<span data-ttu-id="37fd2-110">Der **System. String** -Wert, der dem Namen entspricht, der im Stil Bezeichner einer Sami-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="37fd2-110">The **System.String** that is the name specified in the style identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="37fd2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="37fd2-111">Remarks</span></span>

<span data-ttu-id="37fd2-112">Eine Sami-Datei kann mehrere Format Definitionen enthalten.</span><span class="sxs-lookup"><span data-stu-id="37fd2-112">A SAMI file can contain several format style definitions.</span></span> <span data-ttu-id="37fd2-113">Sami-Stile werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="37fd2-113">SAMI styles are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="37fd2-114">Ein Stil wird mit einer Text Zeichenfolge mit vorangestelltem \# Zeichen definiert.</span><span class="sxs-lookup"><span data-stu-id="37fd2-114">A style is defined with a text string preceded by a \# character.</span></span> <span data-ttu-id="37fd2-115">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="37fd2-115">For example:</span></span>


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



<span data-ttu-id="37fd2-116">Gibt einen Stil an, der eine bestimmte Schriftart erzeugt.</span><span class="sxs-lookup"><span data-stu-id="37fd2-116">This specifies a style that produces a particular font.</span></span>

<span data-ttu-id="37fd2-117">Wenn kein Sami-Format angegeben ist, wird standardmäßig das erste Format verwendet, das in der Sami-Datei definiert ist.</span><span class="sxs-lookup"><span data-stu-id="37fd2-117">If no SAMI style is specified, the first style defined in the SAMI file is used by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="37fd2-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37fd2-118">Requirements</span></span>



| <span data-ttu-id="37fd2-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37fd2-119">Requirement</span></span> | <span data-ttu-id="37fd2-120">Wert</span><span class="sxs-lookup"><span data-stu-id="37fd2-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37fd2-121">Version</span><span class="sxs-lookup"><span data-stu-id="37fd2-121">Version</span></span><br/>   | <span data-ttu-id="37fd2-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="37fd2-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="37fd2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="37fd2-123">Namespace</span></span><br/> | <span data-ttu-id="37fd2-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="37fd2-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="37fd2-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="37fd2-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="37fd2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="37fd2-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37fd2-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37fd2-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37fd2-128">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="37fd2-128">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="37fd2-129">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="37fd2-129">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="37fd2-130">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="37fd2-130">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





