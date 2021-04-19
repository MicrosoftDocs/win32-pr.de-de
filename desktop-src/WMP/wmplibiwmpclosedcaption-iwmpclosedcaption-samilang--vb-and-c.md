---
title: Iwmpclosedcaption samilang-Eigenschaft
description: Die samilang-Eigenschaft ruft die für Untertitel angezeigte Sprache ab oder legt diese fest.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Samilang-Eigenschaften Fenster Media Player
- Samilang-Eigenschaft, Windows Media Player, iwmpclosedcaption-Schnittstelle
- Iwmpclosedcaption-Schnittstelle, Windows Media Player, samilang (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe29defa3736795c88613ee7ab2ef11a914a3f80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369249"
---
# <a name="iwmpclosedcaptionsamilang-property"></a><span data-ttu-id="235be-106">Iwmpclosedcaption:: samilang-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="235be-106">IWMPClosedCaption::SAMILang property</span></span>

<span data-ttu-id="235be-107">Die **samilang** -Eigenschaft ruft die für Untertitel angezeigte Sprache ab oder legt diese fest.</span><span class="sxs-lookup"><span data-stu-id="235be-107">The **SAMILang** property gets or sets the language displayed for closed captioning.</span></span>

## <a name="syntax"></a><span data-ttu-id="235be-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="235be-108">Syntax</span></span>


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a><span data-ttu-id="235be-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="235be-109">Property value</span></span>

<span data-ttu-id="235be-110">Der **System. String** -Wert, der dem Namen entspricht, der in der Sprach-ID einer Sami-Datei angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="235be-110">The **System.String** that is the name specified in the language identifier of a SAMI file.</span></span>

## <a name="remarks"></a><span data-ttu-id="235be-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="235be-111">Remarks</span></span>

<span data-ttu-id="235be-112">Eine Sami-Datei kann Text für eine oder mehrere Sprachen enthalten.</span><span class="sxs-lookup"><span data-stu-id="235be-112">A SAMI file can contain text for one or many languages.</span></span> <span data-ttu-id="235be-113">Die Sprachen, die für Untertitel verfügbar sind, werden zwischen den Tags und in der Sami <STYLE> - </STYLE> Datei definiert.</span><span class="sxs-lookup"><span data-stu-id="235be-113">The languages available for closed captioning are defined between the <STYLE> and </STYLE> tags in the SAMI file.</span></span> <span data-ttu-id="235be-114">Eine Sprach-ID wird mit einer eindeutigen alphanumerischen Zeichenfolge angegeben, der ein Zeitraum (.) vorangestellt ist.</span><span class="sxs-lookup"><span data-stu-id="235be-114">A language identifier is specified with a unique alphanumeric string that is preceded by a period (.).</span></span> <span data-ttu-id="235be-115">Der für eine Sprache angegebene Name kann eine beliebige Zeichenfolge sein.</span><span class="sxs-lookup"><span data-stu-id="235be-115">The name specified for a language can be any string.</span></span> <span data-ttu-id="235be-116">Beispielsweise könnte Folgendes zum Definieren von US-Englisch verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="235be-116">For example, the following could be used to define US English:</span></span>


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



<span data-ttu-id="235be-117">Wenn keine Sami-Sprache angegeben ist, wird standardmäßig die erste in der Sami-Datei definierte Sprache verwendet.</span><span class="sxs-lookup"><span data-stu-id="235be-117">If no SAMI language is specified, the first language defined in the SAMI file is used by default.</span></span>

<span data-ttu-id="235be-118">Die Zeichenfolge, die Sie mit **samilang** festlegen, muss mit dem **Name** -Attribut im sprachspezifizierer identisch sein.</span><span class="sxs-lookup"><span data-stu-id="235be-118">The string you set using **SAMILang** must match the **Name** attribute in the language specifier.</span></span>

## <a name="requirements"></a><span data-ttu-id="235be-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="235be-119">Requirements</span></span>



| <span data-ttu-id="235be-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="235be-120">Requirement</span></span> | <span data-ttu-id="235be-121">Wert</span><span class="sxs-lookup"><span data-stu-id="235be-121">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="235be-122">Version</span><span class="sxs-lookup"><span data-stu-id="235be-122">Version</span></span><br/>   | <span data-ttu-id="235be-123">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="235be-123">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="235be-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="235be-124">Namespace</span></span><br/> | <span data-ttu-id="235be-125">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="235be-125">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="235be-126">Assembly</span><span class="sxs-lookup"><span data-stu-id="235be-126">Assembly</span></span><br/>  | <dl> <span data-ttu-id="235be-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="235be-127"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="235be-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="235be-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="235be-129">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="235be-129">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="235be-130">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="235be-130">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="235be-131">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="235be-131">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





