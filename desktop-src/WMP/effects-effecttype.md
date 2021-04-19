---
title: Effects. EffectType
description: Die EffectType-Methode ruft den Registrierungs Namen der Visualisierung mit dem angegebenen Registrierungs Index ab. Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.
ms.assetid: 47da4f3f-8552-4404-ad46-5dc6afca849a
keywords:
- Effekte. EffectType-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.effectType
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3eda9cbd1a4634062683536f1f132393a2874691
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366700"
---
# <a name="effectseffecttype"></a><span data-ttu-id="7a0e8-105">Effects. EffectType</span><span class="sxs-lookup"><span data-stu-id="7a0e8-105">EFFECTS.effectType</span></span>

<span data-ttu-id="7a0e8-106">Die **EffectType** -Methode ruft den Registrierungs Namen der Visualisierung mit dem angegebenen Registrierungs Index ab.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-106">The **effectType** method retrieves the registry name of the visualization with the specified registry index.</span></span> <span data-ttu-id="7a0e8-107">Dieser Name ist eine eindeutige ID, die vom Visualisierungs Autor definiert wurde.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-107">This name is a unique ID defined by the visualization author.</span></span>

``` syntax
        elementID.effectType(index)
```

## <a name="parameters"></a><span data-ttu-id="7a0e8-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a0e8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a0e8-109"><span id="index"></span><span id="INDEX"></span>*Sin*</span><span class="sxs-lookup"><span data-stu-id="7a0e8-109"><span id="index"></span><span id="INDEX"></span>*index*</span></span>
</dt> <dd>

<span data-ttu-id="7a0e8-110">**Zahl** (**Long**), die den Registrierungs Index einer Visualisierung enthält.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-110">**Number** (**long**) containing the registry index of a visualization.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a0e8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a0e8-111">Return Value</span></span>

<span data-ttu-id="7a0e8-112">Diese Methode gibt eine **Zeichenfolge** zurück.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-112">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a0e8-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a0e8-113">Remarks</span></span>

<span data-ttu-id="7a0e8-114">Diese Methode ist hilfreich für den Wechsel zwischen Visualisierungen im Skript.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-114">This method is useful for switching between visualizations in script.</span></span> <span data-ttu-id="7a0e8-115">Eine Benutzeroberfläche könnte den Satz von Titeln anzeigen. wenn der Benutzer jedoch eine solche Tabelle auswählt, muss das Skript für die Visualisierung von Visualisierungen die Verwendung von " **einstellerffecttype** " verwenden.</span><span class="sxs-lookup"><span data-stu-id="7a0e8-115">A user interface could display the set of titles, but when the user selects one, the script must use **currentEffectType** to switch visualizations.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a0e8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a0e8-116">Requirements</span></span>



| <span data-ttu-id="7a0e8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a0e8-117">Requirement</span></span> | <span data-ttu-id="7a0e8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7a0e8-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="7a0e8-119">Version</span><span class="sxs-lookup"><span data-stu-id="7a0e8-119">Version</span></span><br/> | <span data-ttu-id="7a0e8-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="7a0e8-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7a0e8-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a0e8-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a0e8-122">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="7a0e8-122">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="7a0e8-123">**Effekte. Currency-ffecttype**</span><span class="sxs-lookup"><span data-stu-id="7a0e8-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





