---
title: IWMPControls3 currentaudiolanguageindex (Eigenschaft)
description: Die currentaudiolanguageindex-Eigenschaft ruft den 1-basierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt ihn fest.
ms.assetid: 3ed60827-c4e9-4455-b95e-b6eebf7a9a08
keywords:
- currentaudiolanguageindex-Eigenschaft, Fenster Media Player
- currentaudiolanguageindex-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface Windows Media Player, currentaudiolanguageindex (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls3.currentAudioLanguageIndex
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4fb36eea4038322cacd7f233892151ab77e5eea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369245"
---
# <a name="iwmpcontrols3currentaudiolanguageindex-property"></a><span data-ttu-id="e7866-106">IWMPControls3:: currentaudiolanguageindex (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="e7866-106">IWMPControls3::currentAudioLanguageIndex property</span></span>

<span data-ttu-id="e7866-107">Die **currentaudiolanguageindex** -Eigenschaft ruft den 1-basierten Index ab, der der Audiosprache für die Wiedergabe entspricht, oder legt ihn fest.</span><span class="sxs-lookup"><span data-stu-id="e7866-107">The **currentAudioLanguageIndex** property gets or sets the one-based index that corresponds to the audio language for playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7866-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7866-108">Syntax</span></span>


```CSharp
public System.Int32 currentAudioLanguageIndex {get; set;}
```


```VB

Public Property currentAudioLanguageIndex As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e7866-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="e7866-109">Property value</span></span>

<span data-ttu-id="e7866-110">Ein **System. Int32** -Wert, der der einbasierte Index der Sprache ist.</span><span class="sxs-lookup"><span data-stu-id="e7866-110">A **System.Int32** that is the one-based index of the language.</span></span>

## <a name="remarks"></a><span data-ttu-id="e7866-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e7866-111">Remarks</span></span>

<span data-ttu-id="e7866-112">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="e7866-112">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="e7866-113">Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e7866-113">Use the **audioLanguageCount** property to get the number of supported audio languages.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7866-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e7866-114">Requirements</span></span>



| <span data-ttu-id="e7866-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e7866-115">Requirement</span></span> | <span data-ttu-id="e7866-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e7866-116">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7866-117">Version</span><span class="sxs-lookup"><span data-stu-id="e7866-117">Version</span></span><br/>   | <span data-ttu-id="e7866-118">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="e7866-118">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e7866-119">Namespace</span><span class="sxs-lookup"><span data-stu-id="e7866-119">Namespace</span></span><br/> | <span data-ttu-id="e7866-120">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="e7866-120">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e7866-121">Assembly</span><span class="sxs-lookup"><span data-stu-id="e7866-121">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e7866-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e7866-122"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7866-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e7866-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7866-124">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-124">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7866-125">**IWMPControls3. audiolanguagecount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-125">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7866-126">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-126">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7866-127">**IWMPControls3. getaudiolanguagedescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-127">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7866-128">**IWMPControls3. getaudiolanguageid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-128">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e7866-129">**IWMPControls3. getlanguagename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="e7866-129">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





