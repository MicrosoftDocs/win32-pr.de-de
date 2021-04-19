---
title: Equalizersettings. nextvoreinstellung
description: Die nextvoreinstellung-Methode wendet die nächste Voreinstellung für den equaliausgleich an.
ms.assetid: 67d40ec9-2744-4d63-aa56-0ee20496e896
keywords:
- Fenster "equalizersettings. nextvoreinstellung" Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.nextPreset
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b464c0fca9b38a14a65a24185e51813e4520eee0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372727"
---
# <a name="equalizersettingsnextpreset"></a><span data-ttu-id="6ef6d-104">Equalizersettings. nextvoreinstellung</span><span class="sxs-lookup"><span data-stu-id="6ef6d-104">EQUALIZERSETTINGS.nextPreset</span></span>

<span data-ttu-id="6ef6d-105">Die **nextvoreinstellung** -Methode wendet die nächste Voreinstellung für den equaliausgleich an.</span><span class="sxs-lookup"><span data-stu-id="6ef6d-105">The **nextPreset** method applies the next equalizer preset.</span></span>

``` syntax
        elementID.nextPreset()
```

## <a name="parameters"></a><span data-ttu-id="6ef6d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ef6d-106">Parameters</span></span>

<span data-ttu-id="6ef6d-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6ef6d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6ef6d-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6ef6d-108">Return Value</span></span>

<span data-ttu-id="6ef6d-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="6ef6d-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6ef6d-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ef6d-110">Remarks</span></span>

<span data-ttu-id="6ef6d-111">Wenn es sich bei der aktuellen Voreinstellung um die letzte verfügbare Voreinstellung handelt, wird die erste Voreinstellung als aktuell festgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ef6d-111">If the current preset is the last one available, the first preset is made current.</span></span>

## <a name="examples"></a><span data-ttu-id="6ef6d-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ef6d-112">Examples</span></span>


```JScript
<SUBVIEW id="eqtray">
  <EQUALIZERSETTINGS id="eq"/>
  <BUTTON
    id="nextPreset" 
    onClick="eq.nextPreset();"
  />
  <BUTTON
    id="prevPreset" 
    onClick="eq.previousPreset();"
  />
  <TEXT
    id="currentPreset" 
    value="wmpprop:eq.currentPresetTitle" 
  />
</SUBVIEW>
```



## <a name="requirements"></a><span data-ttu-id="6ef6d-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6ef6d-113">Requirements</span></span>



| <span data-ttu-id="6ef6d-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6ef6d-114">Requirement</span></span> | <span data-ttu-id="6ef6d-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6ef6d-115">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="6ef6d-116">Version</span><span class="sxs-lookup"><span data-stu-id="6ef6d-116">Version</span></span><br/> | <span data-ttu-id="6ef6d-117">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="6ef6d-117">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6ef6d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ef6d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ef6d-119">**Equalizersettings-Element**</span><span class="sxs-lookup"><span data-stu-id="6ef6d-119">**EQUALIZERSETTINGS Element**</span></span>](equalizersettings-element.md)
</dt> <dt>

[<span data-ttu-id="6ef6d-120">**Equalizersettings. previouationsset**</span><span class="sxs-lookup"><span data-stu-id="6ef6d-120">**EQUALIZERSETTINGS.previousPreset**</span></span>](equalizersettings-previouspreset.md)
</dt> </dl>

 

 





