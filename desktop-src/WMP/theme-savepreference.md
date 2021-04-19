---
title: Design. savepreference
description: Die savepreference-Methode speichert eine bevorzugte Einstellung in der Registrierung.
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- Design. savepreference-Fenster Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373929"
---
# <a name="themesavepreference"></a><span data-ttu-id="4a06d-104">Design. savepreference</span><span class="sxs-lookup"><span data-stu-id="4a06d-104">THEME.savePreference</span></span>

<span data-ttu-id="4a06d-105">Die **savepreference** -Methode speichert eine bevorzugte Einstellung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="4a06d-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="4a06d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4a06d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4a06d-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*der Schlüssel*</span><span class="sxs-lookup"><span data-stu-id="4a06d-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="4a06d-108">Eine **Zeichenfolge** , die den Schlüssel des zu speichernden Einstellungs Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="4a06d-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="4a06d-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*Parallelitätstyp*</span><span class="sxs-lookup"><span data-stu-id="4a06d-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="4a06d-110">Eine **Zeichenfolge** , die den zu speichernden Wert angibt.</span><span class="sxs-lookup"><span data-stu-id="4a06d-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4a06d-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4a06d-111">Return Value</span></span>

<span data-ttu-id="4a06d-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="4a06d-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="4a06d-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a06d-113">Remarks</span></span>

<span data-ttu-id="4a06d-114">Eine Bevorzugung ist ein Schlüssel-Wert-Paar, das in der Registrierung gespeichert werden kann, um Informationen über den Status der Windows-Media Player zwischen den Ausführungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4a06d-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="4a06d-115">Diese Funktion kann z. b. verwendet werden, um Anpassungs Einstellungen zu speichern, sodass Sie nicht jedes Mal neu eingegeben werden müssen, wenn Windows Media Player gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="4a06d-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="4a06d-116">Die Einstellungen werden nicht verschlüsselt und sind daher keine sichere Methode zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="4a06d-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="4a06d-117">Verwenden Sie keine Einstellungen, um private Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="4a06d-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="4a06d-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4a06d-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="4a06d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4a06d-119">Requirements</span></span>



| <span data-ttu-id="4a06d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4a06d-120">Requirement</span></span> | <span data-ttu-id="4a06d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="4a06d-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="4a06d-122">Version</span><span class="sxs-lookup"><span data-stu-id="4a06d-122">Version</span></span><br/> | <span data-ttu-id="4a06d-123">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="4a06d-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4a06d-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4a06d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a06d-125">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="4a06d-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="4a06d-126">**Design. loadpreference**</span><span class="sxs-lookup"><span data-stu-id="4a06d-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





