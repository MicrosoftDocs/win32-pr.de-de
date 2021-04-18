---
title: IWMPControls3 audiolanguagecount (Eigenschaft)
description: Die audiolanguagecount-Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.
ms.assetid: 92e2093f-435b-4427-9f85-8c8ae76e0e2d
keywords:
- audiolanguagecount-Eigenschaften Fenster Media Player
- audiolanguagecount-Eigenschaft, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, audiolanguagecount (Eigenschaft)
topic_type:
- apiref
api_name:
- IWMPControls3.audioLanguageCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd397dec80a5ccb5f2085e3231782555efde8e39
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365779"
---
# <a name="iwmpcontrols3audiolanguagecount-property"></a><span data-ttu-id="2cdcc-106">IWMPControls3:: audiolanguagecount (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="2cdcc-106">IWMPControls3::audioLanguageCount property</span></span>

<span data-ttu-id="2cdcc-107">Die **audiolanguagecount** -Eigenschaft ruft die Anzahl der unterstützten Audiosprachen ab.</span><span class="sxs-lookup"><span data-stu-id="2cdcc-107">The **audioLanguageCount** property gets the count of supported audio languages.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cdcc-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cdcc-108">Syntax</span></span>


```CSharp
public System.Int32 audioLanguageCount {get; set;}
```


```VB

Public ReadOnly Property audioLanguageCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2cdcc-109">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="2cdcc-109">Property value</span></span>

<span data-ttu-id="2cdcc-110">Ein **System. Int32** -Wert, der die Anzahl unterstützter Audiosprachen ist.</span><span class="sxs-lookup"><span data-stu-id="2cdcc-110">A **System.Int32** that is the count of supported audio languages.</span></span>

## <a name="remarks"></a><span data-ttu-id="2cdcc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2cdcc-111">Remarks</span></span>

<span data-ttu-id="2cdcc-112">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="2cdcc-112">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="2cdcc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2cdcc-113">Requirements</span></span>



| <span data-ttu-id="2cdcc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2cdcc-114">Requirement</span></span> | <span data-ttu-id="2cdcc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2cdcc-115">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2cdcc-116">Version</span><span class="sxs-lookup"><span data-stu-id="2cdcc-116">Version</span></span><br/>   | <span data-ttu-id="2cdcc-117">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="2cdcc-117">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2cdcc-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="2cdcc-118">Namespace</span></span><br/> | <span data-ttu-id="2cdcc-119">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-119">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2cdcc-120">Assembly</span><span class="sxs-lookup"><span data-stu-id="2cdcc-120">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2cdcc-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2cdcc-121"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2cdcc-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2cdcc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2cdcc-123">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-123">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cdcc-124">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-124">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cdcc-125">**IWMPControls3. currentaudiolanguageindex (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-125">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cdcc-126">**IWMPControls3. getaudiolanguagedescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-126">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cdcc-127">**IWMPControls3. getaudiolanguageid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-127">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2cdcc-128">**IWMPControls3. getlanguagename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="2cdcc-128">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





