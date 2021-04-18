---
title: IWMPControls3 getlanguagename-Methode
description: Die getlanguagename-Methode gibt den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) zurück.
ms.assetid: a0651e8d-0ba1-4fff-93f0-fe097231723e
keywords:
- getlanguagename-Methode, Windows-Media Player
- getlanguagename-Methode, Windows Media Player, IWMPControls3-Schnittstelle
- IWMPControls3 Interface, Windows Media Player, getlanguagename-Methode
topic_type:
- apiref
api_name:
- IWMPControls3.getLanguageName
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d93bf97c7b5213e3d196897de1c3ebcfa6e6d2c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371745"
---
# <a name="iwmpcontrols3getlanguagename-method"></a><span data-ttu-id="0517a-106">IWMPControls3:: getlanguagename-Methode</span><span class="sxs-lookup"><span data-stu-id="0517a-106">IWMPControls3::getLanguageName method</span></span>

<span data-ttu-id="0517a-107">Die **getlanguagename** -Methode gibt den Namen der Audiosprache mit dem angegebenen Gebiets Schema Bezeichner (LCID) zurück.</span><span class="sxs-lookup"><span data-stu-id="0517a-107">The **getLanguageName** method returns the name of the audio language with the specified locale identifier (LCID).</span></span>

## <a name="syntax"></a><span data-ttu-id="0517a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="0517a-108">Syntax</span></span>


```CSharp
public System.String getLanguageName(
  System.Int32 lLangID
);
```


```VB

Public Function getLanguageName( _
  ByVal lLangID As System.Int32 _
) As System.String
Implements IWMPControls3.getLanguageName
```





## <a name="parameters"></a><span data-ttu-id="0517a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0517a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0517a-110">*llangid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0517a-110">*lLangID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0517a-111">Ein **System. Int32** -Wert, der die LCID ist.</span><span class="sxs-lookup"><span data-stu-id="0517a-111">A **System.Int32** that is the LCID.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0517a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0517a-112">Return value</span></span>

<span data-ttu-id="0517a-113">Ein **System. String** -Wert, der der Name der Audiosprache ist.</span><span class="sxs-lookup"><span data-stu-id="0517a-113">A **System.String** that is the name of the audio language.</span></span>

## <a name="remarks"></a><span data-ttu-id="0517a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0517a-114">Remarks</span></span>

<span data-ttu-id="0517a-115">Eine LCID identifiziert eindeutig einen bestimmten Sprach Dialekt, der als Gebiets Schema bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="0517a-115">An LCID uniquely identifies a particular language dialect, called a locale.</span></span>

<span data-ttu-id="0517a-116">Bei Windows Media-basierten Inhalten unterstützen Eigenschaften und Methoden im Zusammenhang mit der Sprachauswahl nur eine einzige Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0517a-116">For Windows Media-based content, properties and methods related to language selection support only a single output.</span></span>

## <a name="requirements"></a><span data-ttu-id="0517a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0517a-117">Requirements</span></span>



| <span data-ttu-id="0517a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0517a-118">Requirement</span></span> | <span data-ttu-id="0517a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="0517a-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0517a-120">Version</span><span class="sxs-lookup"><span data-stu-id="0517a-120">Version</span></span><br/>   | <span data-ttu-id="0517a-121">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="0517a-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0517a-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="0517a-122">Namespace</span></span><br/> | <span data-ttu-id="0517a-123">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="0517a-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0517a-124">Assembly</span><span class="sxs-lookup"><span data-stu-id="0517a-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0517a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0517a-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0517a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0517a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0517a-127">**IWMPControls3-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-127">**IWMPControls3 Interface (VB and C#)**</span></span>](iwmpcontrols3--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0517a-128">**IWMPControls3. audiolanguagecount (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-128">**IWMPControls3.audioLanguageCount (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-audiolanguagecount--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0517a-129">**IWMPControls3. currentaudiolanguage (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-129">**IWMPControls3.currentAudioLanguage (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguage--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0517a-130">**IWMPControls3. currentaudiolanguageindex (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-130">**IWMPControls3.currentAudioLanguageIndex (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-currentaudiolanguageindex--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0517a-131">**IWMPControls3. getaudiolanguagedescription (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-131">**IWMPControls3.getAudioLanguageDescription (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguagedescription--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0517a-132">**IWMPControls3. getaudiolanguageid (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="0517a-132">**IWMPControls3.getAudioLanguageID (VB and C#)**</span></span>](wmplibiwmpcontrols3-iwmpcontrols3-getaudiolanguageid--vb-and-c.md)
</dt> </dl>

 

 





