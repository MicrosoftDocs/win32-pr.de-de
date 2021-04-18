---
title: IWMPClosedCaption2 samilangcount (Eigenschaft)
description: Die samilangcount-Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.
ms.assetid: e3c7203d-66cb-49e2-9204-795c0f27248f
keywords:
- Samilangcount-Eigenschaften Fenster Media Player
- Samilangcount-Eigenschaft, Windows Media Player, IWMPClosedCaption2-Schnittstelle
- IWMPClosedCaption2 Interface Windows Media Player, samilangcount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPClosedCaption2.SAMILangCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea01357de508dea319389cd14ab85ebafe0329e6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354773"
---
# <a name="iwmpclosedcaption2samilangcount-property"></a><span data-ttu-id="ee912-106">IWMPClosedCaption2:: samilangcount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="ee912-106">IWMPClosedCaption2::SAMILangCount property</span></span>

<span data-ttu-id="ee912-107">Die **samilangcount** -Eigenschaft ruft die Anzahl der Sprachen ab, die von der aktuellen Sami-Datei unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="ee912-107">The **SAMILangCount** property gets the number of languages supported by the current SAMI file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee912-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee912-108">Syntax</span></span>


```CSharp
public System.Int32 SAMILangCount {get; set;}
```


```VB

Public ReadOnly Property SAMILangCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="ee912-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ee912-109">Property value</span></span>

<span data-ttu-id="ee912-110">Ein **System. Int32** -Wert, der die Anzahl der unterstützten Sprachen ist.</span><span class="sxs-lookup"><span data-stu-id="ee912-110">A **System.Int32** that is the number of languages supported.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee912-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee912-111">Remarks</span></span>

<span data-ttu-id="ee912-112">Diese Eigenschaft gibt 0 (null) zurück, es sei denn, eine digitale Mediendatei ist geöffnet (AxWindowsMediaPlayer. openstate ist gleich 13).</span><span class="sxs-lookup"><span data-stu-id="ee912-112">This property returns 0 unless a digital media file is open (AxWindowsMediaPlayer.openState is equal to 13).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee912-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee912-113">Requirements</span></span>



| <span data-ttu-id="ee912-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee912-114">Requirement</span></span> | <span data-ttu-id="ee912-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ee912-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee912-116">Version</span><span class="sxs-lookup"><span data-stu-id="ee912-116">Version</span></span><br/>   | <span data-ttu-id="ee912-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="ee912-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="ee912-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee912-118">Namespace</span></span><br/> | <span data-ttu-id="ee912-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="ee912-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="ee912-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="ee912-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="ee912-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="ee912-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee912-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee912-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee912-123">**Hinzufügen von Untertiteln zu digitalen Medien**</span><span class="sxs-lookup"><span data-stu-id="ee912-123">**Adding Closed Captions to Digital Media**</span></span>](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[<span data-ttu-id="ee912-124">**Iwmpclosedcaption-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee912-124">**IWMPClosedCaption Interface (VB and C#)**</span></span>](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee912-125">**Iwmpclosedcaption. samilang (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee912-125">**IWMPClosedCaption.SAMILang (VB and C#)**</span></span>](wmplibiwmpclosedcaption-iwmpclosedcaption-samilang--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee912-126">**IWMPClosedCaption2-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee912-126">**IWMPClosedCaption2 Interface (VB and C#)**</span></span>](iwmpclosedcaption2--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="ee912-127">**IWMPClosedCaption2. getsamilangname (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="ee912-127">**IWMPClosedCaption2.getSAMILangName (VB and C#)**</span></span>](wmplibiwmpclosedcaption2-iwmpclosedcaption2-getsamilangname--vb-and-c.md)
</dt> </dl>

 

 





