---
title: Iwmpclosedcaption-captioningid (Eigenschaft)
description: Die iwmpclosedcaption-Eigenschaft ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt diesen fest.
ms.assetid: b09bb7c7-c3b6-4e0d-962f-24b06a04f6d1
keywords:
- captioningid-Eigenschaft, Fenster Media Player
- captioningid-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, captioningid (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.captioningId
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 343234fce2b93ac02255731a38025f6d7b9fac6f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358601"
---
# <a name="iwmpclosedcaptioncaptioningid-property"></a><span data-ttu-id="6b855-106">Iwmpclosedcaption:: captioningid (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6b855-106">IWMPClosedCaption::captioningId property</span></span>

<span data-ttu-id="6b855-107">Die **iwmpclosedcaption** -Eigenschaft ruft den Namen des HTML-Elements ab, das die Beschriftung anzeigt, oder legt diesen fest.</span><span class="sxs-lookup"><span data-stu-id="6b855-107">The **IWMPClosedCaption** property gets or sets the name of the HTML element displaying the captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b855-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b855-108">Syntax</span></span>


```CSharp
public System.String captioningId {get; set;}
```


```VB

Public Property captioningId As System.String
```





## <a name="property-value"></a><span data-ttu-id="6b855-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6b855-109">Property value</span></span>

<span data-ttu-id="6b855-110">Die **System. String** -ID, die die ID des HTML-Elements ist.</span><span class="sxs-lookup"><span data-stu-id="6b855-110">The **System.String** that is the ID of the HTML element.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b855-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6b855-111">Remarks</span></span>

<span data-ttu-id="6b855-112">Der angegebene Elementname kann ein beliebiges HTML-Element auf der Webseite sein, solange es das **InnerHtml** -Attribut unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6b855-112">The element name specified can be any HTML element in the webpage as long as it supports the **innerHTML** attribute.</span></span> <span data-ttu-id="6b855-113">Wenn die Webseite mehrere Frames enthält, kann der Elementname nur auf ein Element im gleichen Frame wie das Windows Media Player-Steuerelement verweisen.</span><span class="sxs-lookup"><span data-stu-id="6b855-113">If the webpage contains multiple frames, the element name can only refer to an element in the same frame as the Windows Media Player control.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b855-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6b855-114">Requirements</span></span>



| <span data-ttu-id="6b855-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6b855-115">Requirement</span></span> | <span data-ttu-id="6b855-116">Wert</span><span class="sxs-lookup"><span data-stu-id="6b855-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b855-117">Version</span><span class="sxs-lookup"><span data-stu-id="6b855-117">Version</span></span><br/>   | <span data-ttu-id="6b855-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="6b855-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6b855-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="6b855-119">Namespace</span></span><br/> | <span data-ttu-id="6b855-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="6b855-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6b855-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="6b855-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6b855-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6b855-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b855-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b855-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b855-124">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="6b855-124">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="6b855-125">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6b855-125">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6b855-126">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="6b855-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





