---
title: Iwmpsettings getMode-Methode
description: Die getMode-Methode gibt einen Wert zurück, der angibt, ob der Schleifen-oder Shuffle-Modus aktiv ist.
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- getMode-Methode, Windows-Media Player
- getMode-Methode, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, getMode-Methode
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359346"
---
# <a name="iwmpsettingsgetmode-method"></a><span data-ttu-id="fbd06-106">Iwmpsettings:: getMode-Methode</span><span class="sxs-lookup"><span data-stu-id="fbd06-106">IWMPSettings::getMode method</span></span>

<span data-ttu-id="fbd06-107">Die **getMode** -Methode gibt einen Wert zurück, der angibt, ob der Schleifen-oder Shuffle-Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="fbd06-107">The **getMode** method returns a value indicating whether loop mode or shuffle mode is active.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbd06-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbd06-108">Syntax</span></span>


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a><span data-ttu-id="fbd06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbd06-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbd06-110">*bstraumode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fbd06-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fbd06-111">Ein **System. String** -Wert, der einem der folgenden Werte entspricht.</span><span class="sxs-lookup"><span data-stu-id="fbd06-111">A **System.String** that is one of the following values.</span></span>



| <span data-ttu-id="fbd06-112">Wert</span><span class="sxs-lookup"><span data-stu-id="fbd06-112">Value</span></span>      | <span data-ttu-id="fbd06-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbd06-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd06-114">autorewind</span><span class="sxs-lookup"><span data-stu-id="fbd06-114">autoRewind</span></span> | <span data-ttu-id="fbd06-115">Die Nachverfolgung wird von Anfang an neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="fbd06-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="fbd06-116">loop</span><span class="sxs-lookup"><span data-stu-id="fbd06-116">loop</span></span>       | <span data-ttu-id="fbd06-117">Die Reihenfolge der Spuren wird wiederholt.</span><span class="sxs-lookup"><span data-stu-id="fbd06-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="fbd06-118">showframe</span><span class="sxs-lookup"><span data-stu-id="fbd06-118">showFrame</span></span>  | <span data-ttu-id="fbd06-119">Der nächste Keyframe wird angezeigt, wenn er nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fbd06-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="fbd06-120">Dieser Modus ist für Audiospuren nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="fbd06-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="fbd06-121">Shuffle</span><span class="sxs-lookup"><span data-stu-id="fbd06-121">shuffle</span></span>    | <span data-ttu-id="fbd06-122">Spuren werden in zufälliger Reihenfolge wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="fbd06-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fbd06-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fbd06-123">Return value</span></span>

<span data-ttu-id="fbd06-124">Ein **System. Boolean** -Wert, der angibt, ob der angegebene Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="fbd06-124">A **System.Boolean** value indicating whether the specified mode is active.</span></span>

## <a name="requirements"></a><span data-ttu-id="fbd06-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbd06-125">Requirements</span></span>



| <span data-ttu-id="fbd06-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fbd06-126">Requirement</span></span> | <span data-ttu-id="fbd06-127">Wert</span><span class="sxs-lookup"><span data-stu-id="fbd06-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fbd06-128">Version</span><span class="sxs-lookup"><span data-stu-id="fbd06-128">Version</span></span><br/>   | <span data-ttu-id="fbd06-129">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="fbd06-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="fbd06-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbd06-130">Namespace</span></span><br/> | <span data-ttu-id="fbd06-131">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="fbd06-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="fbd06-132">Assembly</span><span class="sxs-lookup"><span data-stu-id="fbd06-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="fbd06-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="fbd06-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fbd06-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbd06-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fbd06-135">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fbd06-135">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="fbd06-136">**Iwmpsettings. SetMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="fbd06-136">**IWMPSettings.setMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





