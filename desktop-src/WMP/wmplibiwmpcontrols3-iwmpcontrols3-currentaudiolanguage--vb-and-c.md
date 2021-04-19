---
title: IWMPControls3 currentaudiolanguage (Eigenschaft)
description: Die currentaudiolanguage-Eigenschaft ruft den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt ihn fest.
ms.assetid: 4adf26c7-077a-483e-8a76-accf871eca4c
keywords:
- currentaudiolanguage-Eigenschaft, Windows Media Player
- currentaudiolanguage-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentaudiolanguage-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguage
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c4621b5eace56cb883a6c8b14c3b1f082b12d3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367794"
---
# <a name="iwmpcontrols3currentaudiolanguage-property"></a><span data-ttu-id="e7857-106">IWMPControls3:: currentaudiolanguage (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7857-106">IWMPControls3::currentAudioLanguage property</span></span>

<span data-ttu-id="e7857-107">Die **currentaudiolanguage** -Eigenschaft ruft den Gebiets Schema Bezeichner (LCID) der Audiosprache für die Wiedergabe ab oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e7857-107">The **currentAudioLanguage** property gets or sets the locale identifier (LCID) of the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7857-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7857-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguage {get; set;}
```


```VB

Public Property currentAudioLanguage As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e7857-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7857-109">Property value</span></span>

<span data-ttu-id="e7857-110">Ein **System. Int32** -Wert, der die LCID der Audiosprache ist.</span><span class="sxs-lookup"><span data-stu-id="e7857-110">A **System.Int32** that is the LCID of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7857-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7857-111">Remarks</span></span>

<span data-ttu-id="e7857-112">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="e7857-112">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="e7857-113">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e7857-113">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="e7857-114">Beim Arbeiten mit DVD-Inhalten bewirkt die Angabe einer LCID, dass die erste verfügbare Audiospur mit der angegebenen Sprach-ID ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="e7857-114">When working with DVD content, specifying an LCID will cause the first available audio track having the specified language ID to be selected.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7857-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7857-115">Requirements</span></span>



| <span data-ttu-id="e7857-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7857-116">Requirement</span></span> | <span data-ttu-id="e7857-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e7857-117">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7857-118">Version</span><span class="sxs-lookup"><span data-stu-id="e7857-118">Version</span></span><br/>   | <span data-ttu-id="e7857-119">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e7857-119">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e7857-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7857-120">Namespace</span></span><br/> | <span data-ttu-id="e7857-121">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e7857-121">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e7857-122">Assembly</span><span class="sxs-lookup"><span data-stu-id="e7857-122">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e7857-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e7857-123"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7857-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7857-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7857-125">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-125">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7857-126">**IWMPControls3. audiolanguagecount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-126">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7857-127">**IWMPControls3. currentaudiolanguageindex (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-127">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7857-128">**IWMPControls3. getaudiolanguagedescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-128">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7857-129">**IWMPControls3. getaudiolanguageid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-129">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7857-130">**IWMPControls3. getlanguagename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7857-130">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





