---
title: IWMPControls3 getaudiolanguageid-Methode
description: Die getaudiolanguageid-Methode gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex zurück.
ms.assetid: 880bbfca-6f69-41ce-a078-467c1939fae5
keywords:
- getaudiolanguageid-Methode, Windows Media Player
- getaudiolanguageid-Methode, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, getaudiolanguageid-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getAudioLanguageID
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb8112eafec018b12012d20b37bfe30f7b464377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370803"
---
# <a name="iwmpcontrols3getaudiolanguageid-method"></a><span data-ttu-id="a8095-106">IWMPControls3:: getaudiolanguageid-Methode</span><span class="sxs-lookup"><span data-stu-id="a8095-106">IWMPControls3::getAudioLanguageID method</span></span>

<span data-ttu-id="a8095-107">Die **getaudiolanguageid** -Methode gibt den Gebiets Schema Bezeichner (Locale Identifier, LCID) für einen angegebenen audiosprachindex zurück.</span><span class="sxs-lookup"><span data-stu-id="a8095-107">The **getAudioLanguageID** method returns the locale identifier (LCID) for a specified audio language index.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8095-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8095-108">Syntax</span></span>


```CSharp
public System.Int32 getAudioLanguageID(
  System.Int32 lIndex
);
```


```VB

Public Function getAudioLanguageID( _
  ByVal lIndex As System.Int32 _
) As System.Int32
Implements IWMPControls3.getAudioLanguageID
```





## <a name="parameters"></a><span data-ttu-id="a8095-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8095-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a8095-110">*Lindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a8095-110">*lIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a8095-111">Ein **System. Int32** -Wert, der der einbasierte Index der Audiosprache ist.</span><span class="sxs-lookup"><span data-stu-id="a8095-111">A **System.Int32** that is the one-based index of the audio language.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a8095-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a8095-112">Return value</span></span>

<span data-ttu-id="a8095-113">Ein **System. Int32** -Wert, der die LCID ist.</span><span class="sxs-lookup"><span data-stu-id="a8095-113">A **System.Int32** that is the LCID.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8095-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8095-114">Remarks</span></span>

<span data-ttu-id="a8095-115">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="a8095-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="a8095-116">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="a8095-116">For Windows Media based content, properties and methods related to language selection support only a single output.</span></span>

<span data-ttu-id="a8095-117">Verwenden Sie die Eigenschaft **audiolanguagecount** , um die Anzahl der unterstützten Audiosprachen abzurufen, und greifen Sie dann einzeln mithilfe eines 1-basierten Indexes auf eine Audiosprache zu.</span><span class="sxs-lookup"><span data-stu-id="a8095-117">Use the **audioLanguageCount** property to get the number of supported audio languages, and then access an audio language individually by using a one-based index.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8095-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a8095-118">Requirements</span></span>



| <span data-ttu-id="a8095-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a8095-119">Requirement</span></span> | <span data-ttu-id="a8095-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a8095-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8095-121">Version</span><span class="sxs-lookup"><span data-stu-id="a8095-121">Version</span></span><br/>   | <span data-ttu-id="a8095-122">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="a8095-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="a8095-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8095-123">Namespace</span></span><br/> | <span data-ttu-id="a8095-124">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="a8095-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="a8095-125">Assembly</span><span class="sxs-lookup"><span data-stu-id="a8095-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="a8095-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="a8095-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8095-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8095-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8095-128">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-128">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8095-129">**IWMPControls3. audiolanguagecount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-129">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8095-130">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-130">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8095-131">**IWMPControls3. currentaudiolanguageindex (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-131">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8095-132">**IWMPControls3. getaudiolanguagedescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-132">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="a8095-133">**IWMPControls3. getlanguagename (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="a8095-133">**IWMPControls3.getLanguageName (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getlanguagename--vb-and-c.md)
</dt> </dl>

 

 





