---
title: Design. loadpreference
description: Die loadpreference-Methode lädt eine bevorzugte Einstellung aus der Registrierung.
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- Design. loadpreference-Windows-Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365436"
---
# <a name="themeloadpreference"></a><span data-ttu-id="c2ad5-104">Design. loadpreference</span><span class="sxs-lookup"><span data-stu-id="c2ad5-104">THEME.loadPreference</span></span>

<span data-ttu-id="c2ad5-105">Die **loadpreference** -Methode lädt eine bevorzugte Einstellung aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="c2ad5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2ad5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c2ad5-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*der Schlüssel*</span><span class="sxs-lookup"><span data-stu-id="c2ad5-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="c2ad5-108">Eine **Zeichenfolge** , die den Schlüssel des zu ladenden Einstellungs Werts angibt.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c2ad5-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c2ad5-109">Return Value</span></span>

<span data-ttu-id="c2ad5-110">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c2ad5-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2ad5-111">Remarks</span></span>

<span data-ttu-id="c2ad5-112">Eine Bevorzugung ist ein Schlüssel-Wert-Paar, das in der Registrierung gespeichert werden kann, um Informationen über den Status der Windows-Media Player zwischen den Ausführungen zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="c2ad5-113">Diese Funktion kann z. b. verwendet werden, um Anpassungs Einstellungen zu speichern, sodass Sie nicht jedes Mal neu eingegeben werden müssen, wenn Windows Media Player gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="c2ad5-114">Die Einstellungen werden nicht verschlüsselt und sind daher keine sichere Methode zum Speichern von Daten.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="c2ad5-115">Verwenden Sie keine Einstellungen, um private Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c2ad5-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="c2ad5-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c2ad5-116">Requirements</span></span>



| <span data-ttu-id="c2ad5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c2ad5-117">Requirement</span></span> | <span data-ttu-id="c2ad5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="c2ad5-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="c2ad5-119">Version</span><span class="sxs-lookup"><span data-stu-id="c2ad5-119">Version</span></span><br/> | <span data-ttu-id="c2ad5-120">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="c2ad5-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c2ad5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2ad5-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c2ad5-122">**Design-Element**</span><span class="sxs-lookup"><span data-stu-id="c2ad5-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="c2ad5-123">**Design. savepreference**</span><span class="sxs-lookup"><span data-stu-id="c2ad5-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





