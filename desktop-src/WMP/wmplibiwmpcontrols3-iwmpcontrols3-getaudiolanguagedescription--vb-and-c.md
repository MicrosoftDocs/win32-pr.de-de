---
title: IWMPControls3 getaudiolanguagedescription-Methode
description: Die getaudiolanguagedescription-Methode gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen 1-basierten Index entspricht.
ms.assetid: bf3db27f-ba14-409e-8942-fe863d6f3670
keywords:
- getaudiolanguagedescription-Methode, Windows Media Player
- getaudiolanguagedescription-Methode, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, getaudiolanguagedescription-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageDescription
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb45ceb166ca9c948823e516029569e457f35e27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367092"
---
# <a name="iwmpcontrols3getaudiolanguagedescription-method"></a><span data-ttu-id="0d6b8-106">IWMPControls3:: getaudiolanguagedescription-Methode</span><span class="sxs-lookup"><span data-stu-id="0d6b8-106">IWMPControls3::getAudioLanguageDescription method</span></span>

<span data-ttu-id="0d6b8-107">Die **getaudiolanguagedescription** -Methode gibt die Beschreibung für die Audiosprache zurück, die dem angegebenen 1-basierten Index entspricht.</span><span class="sxs-lookup"><span data-stu-id="0d6b8-107">The **getAudioLanguageDescription** method returns the description for the audio language corresponding to the specified one-based index.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d6b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0d6b8-108">Syntax</span></span>


```CSharp
public System.String getAudioLanguageDescription(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageDescription( _
  ByVal lIndex As System.Int32 _
) As System.String
Implements IWMPControls3.getAudioLanguageDescription
```





## <a name="parameters"></a><span data-ttu-id="0d6b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0d6b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d6b8-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0d6b8-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d6b8-111">Ein **System. Int32** -Wert, der der einbasierte audiosprachindex ist.</span><span class="sxs-lookup"><span data-stu-id="0d6b8-111">A **System.Int32** that is the one-based audio language index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d6b8-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0d6b8-112">Return value</span></span>

<span data-ttu-id="0d6b8-113">Ein **System. String** -Wert, der die Beschreibung der Audiosprache ist.</span><span class="sxs-lookup"><span data-stu-id="0d6b8-113">A **System.String** that is the description of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d6b8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0d6b8-114">Remarks</span></span>

<span data-ttu-id="0d6b8-115">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0d6b8-115">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="0d6b8-116">Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann einzeln mithilfe eines 1-basierten Indexes auf eine Audiosprache zu.</span><span class="sxs-lookup"><span data-stu-id="0d6b8-116">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d6b8-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0d6b8-117">Requirements</span></span>



| <span data-ttu-id="0d6b8-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0d6b8-118">Requirement</span></span> | <span data-ttu-id="0d6b8-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0d6b8-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d6b8-120">Version</span><span class="sxs-lookup"><span data-stu-id="0d6b8-120">Version</span></span><br/>   | <span data-ttu-id="0d6b8-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0d6b8-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0d6b8-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d6b8-122">Namespace</span></span><br/> | <span data-ttu-id="0d6b8-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0d6b8-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="0d6b8-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0d6b8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0d6b8-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d6b8-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d6b8-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d6b8-127">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d6b8-128">**IWMPControls3. audiolanguagecount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d6b8-129">**IWMPControls3. currentaudiolanguageindex (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-129">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d6b8-130">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d6b8-131">**IWMPControls3. getaudiolanguageid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-131">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0d6b8-132">**IWMPControls3. getlanguagename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0d6b8-132">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





