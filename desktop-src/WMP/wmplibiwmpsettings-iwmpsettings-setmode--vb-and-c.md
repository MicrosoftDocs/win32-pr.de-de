---
title: Iwmpsettings setmode-Methode
description: Die setmode-Methode legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setmode-Methode, Windows-Media Player
- setmode-Methode, Windows Media Player, iwmpsettings-Schnittstelle
- Iwmpsettings-Schnittstelle, Windows Media Player, setmode-Methode
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365394"
---
# <a name="iwmpsettingssetmode-method"></a><span data-ttu-id="29439-106">Iwmpsettings:: setmode-Methode</span><span class="sxs-lookup"><span data-stu-id="29439-106">IWMPSettings::setMode method</span></span>

<span data-ttu-id="29439-107">Die **setmode** -Methode legt den Schleifen Modus oder den Shuffle-Modus auf aktiv oder inaktiv fest.</span><span class="sxs-lookup"><span data-stu-id="29439-107">The **setMode** method sets the loop mode or shuffle mode to active or inactive.</span></span>

## <a name="syntax"></a><span data-ttu-id="29439-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29439-108">Syntax</span></span>


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a><span data-ttu-id="29439-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29439-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29439-110">*bstraumode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29439-110">*bstrMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29439-111">Ein **System. String** -Wert, der der Name des geänderten Modus ist, der einen der folgenden Werte enthält.</span><span class="sxs-lookup"><span data-stu-id="29439-111">A **System.String** that is the name of the mode being changed, containing one of the following values.</span></span>



| <span data-ttu-id="29439-112">Wert</span><span class="sxs-lookup"><span data-stu-id="29439-112">Value</span></span>      | <span data-ttu-id="29439-113">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29439-113">Description</span></span>                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29439-114">autorewind</span><span class="sxs-lookup"><span data-stu-id="29439-114">autoRewind</span></span> | <span data-ttu-id="29439-115">Die Nachverfolgung wird von Anfang an neu gestartet.</span><span class="sxs-lookup"><span data-stu-id="29439-115">Tracks are restarted from the beginning after playing to the end.</span></span>                                |
| <span data-ttu-id="29439-116">loop</span><span class="sxs-lookup"><span data-stu-id="29439-116">loop</span></span>       | <span data-ttu-id="29439-117">Die Reihenfolge der Spuren wird wiederholt.</span><span class="sxs-lookup"><span data-stu-id="29439-117">The sequence of tracks repeats itself.</span></span>                                                           |
| <span data-ttu-id="29439-118">showframe</span><span class="sxs-lookup"><span data-stu-id="29439-118">showFrame</span></span>  | <span data-ttu-id="29439-119">Der nächste Keyframe wird angezeigt, wenn er nicht wiedergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="29439-119">The nearest key frame is displayed when not playing.</span></span> <span data-ttu-id="29439-120">Dieser Modus ist für Audiospuren nicht relevant.</span><span class="sxs-lookup"><span data-stu-id="29439-120">This mode is not relevant for audio tracks.</span></span> |
| <span data-ttu-id="29439-121">Shuffle</span><span class="sxs-lookup"><span data-stu-id="29439-121">shuffle</span></span>    | <span data-ttu-id="29439-122">Spuren werden in zufälliger Reihenfolge wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="29439-122">Tracks are played in random order.</span></span>                                                               |



 

</dd> <dt>

<span data-ttu-id="29439-123">*varf-Modus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="29439-123">*varfMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="29439-124">Ein **System. Boolean** -Wert, der angibt, ob der neue angegebene Modus aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="29439-124">A **System.Boolean** value specifying whether the new specified mode is active.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29439-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29439-125">Return value</span></span>

<span data-ttu-id="29439-126">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29439-126">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29439-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29439-127">Remarks</span></span>

<span data-ttu-id="29439-128">Wenn der showframe-Modus aktiv ist, muss Windows Media Player auf den Inhalt der Nachverfolgung zugreifen, um den Videoframe abzurufen.</span><span class="sxs-lookup"><span data-stu-id="29439-128">When the showFrame mode is active, Windows Media Player must access the track content to retrieve the video frame.</span></span> <span data-ttu-id="29439-129">Verwenden Sie diesen Modus bei der Wiedergabe von Inhalten, die nicht lokal sind, vorsichtig.</span><span class="sxs-lookup"><span data-stu-id="29439-129">Use this mode cautiously when playing content that is not local.</span></span>

## <a name="requirements"></a><span data-ttu-id="29439-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29439-130">Requirements</span></span>



| <span data-ttu-id="29439-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29439-131">Requirement</span></span> | <span data-ttu-id="29439-132">Wert</span><span class="sxs-lookup"><span data-stu-id="29439-132">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="29439-133">Version</span><span class="sxs-lookup"><span data-stu-id="29439-133">Version</span></span><br/>   | <span data-ttu-id="29439-134">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="29439-134">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="29439-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="29439-135">Namespace</span></span><br/> | <span data-ttu-id="29439-136">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="29439-136">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="29439-137">Assembly</span><span class="sxs-lookup"><span data-stu-id="29439-137">Assembly</span></span><br/>  | <dl> <span data-ttu-id="29439-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="29439-138"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29439-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29439-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29439-140">**Iwmpsettings-Schnittstelle (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="29439-140">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="29439-141">**Iwmpsettings. getMode (VB und c#)**</span><span class="sxs-lookup"><span data-stu-id="29439-141">**IWMPSettings.getMode (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





