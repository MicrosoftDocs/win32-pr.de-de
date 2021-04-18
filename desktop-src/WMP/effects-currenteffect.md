---
title: Effekte. Currency-ffect
description: Das Attribut "attributeffect" gibt die aktuelle Visualisierung an oder ruft Sie ab.
ms.assetid: d6b0e77d-2872-420a-b5f5-36fd23243648
keywords:
- Effekte. Currency-ffect-Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.currentEffect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19398946906fb6c6ea43234c110383b27b16ede
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372279"
---
# <a name="effectscurrenteffect"></a><span data-ttu-id="9ed85-104">Effekte. Currency-ffect</span><span class="sxs-lookup"><span data-stu-id="9ed85-104">EFFECTS.currentEffect</span></span>

<span data-ttu-id="9ed85-105">Das Attribut " **attributeffect** " gibt die aktuelle Visualisierung an oder ruft Sie ab.</span><span class="sxs-lookup"><span data-stu-id="9ed85-105">The **currentEffect** attribute specifies or retrieves the current visualization.</span></span>

``` syntax
        elementID.currentEffect
```

## <a name="possible-values"></a><span data-ttu-id="9ed85-106">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="9ed85-106">Possible Values</span></span>

<span data-ttu-id="9ed85-107">Dieses Attribut ist ein Lese- **/schreibjekt**.</span><span class="sxs-lookup"><span data-stu-id="9ed85-107">This attribute is a read/write **object**.</span></span> <span data-ttu-id="9ed85-108">Der Standardwert ist die erste Visualisierung in der Erstellungs Reihenfolge.</span><span class="sxs-lookup"><span data-stu-id="9ed85-108">The default value is the first visualization in the authoring order.</span></span> <span data-ttu-id="9ed85-109">Wenn keine Visualisierungen in der Skin erstellt wurden, ist der Standardwert die erste Visualisierung in der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="9ed85-109">If there are no visualizations authored in the skin, the default is the first visualization in the registry.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ed85-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ed85-110">Remarks</span></span>

<span data-ttu-id="9ed85-111">Mit diesem Objekt können Sie auf benutzerdefinierte Visualisierungen zugreifen, die Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9ed85-111">You can use this object to access custom visualizations you have created.</span></span> <span data-ttu-id="9ed85-112">Beispielsweise können Sie eine Eigenschaft über die **IDispatch** -Schnittstelle in der Visualisierung verfügbar machen.</span><span class="sxs-lookup"><span data-stu-id="9ed85-112">For example, you could expose a property through the **IDispatch** interface in your visualization.</span></span> <span data-ttu-id="9ed85-113">Anschließend können Sie den Eigenschafts Wert aus der Skin ändern, indem Sie die Visualisierung auf den aktuellen Effekt festlegen, und dann das Objekt " **setobffect** " verwenden, um einen neuen Wert für die Eigenschaft festzulegen.</span><span class="sxs-lookup"><span data-stu-id="9ed85-113">You can then change the property value from your skin by making your visualization the current effect, and then using the **currentEffect** object to set a new value for the property.</span></span> <span data-ttu-id="9ed85-114">Wenn Ihre Visualisierung z. b. eine Eigenschaft mit dem Namen BackgroundColor verfügbar macht, gibt der folgende JScript-Code einen neuen Wert an:</span><span class="sxs-lookup"><span data-stu-id="9ed85-114">For example, if your visualization exposes a property named backgroundColor, the following JScript code specifies a new value:</span></span>


```JScript
// The EFFECTS element ID is MyEffects.
MyEffects.currentEffect.backgroundColor = "blue";
```



## <a name="requirements"></a><span data-ttu-id="9ed85-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ed85-115">Requirements</span></span>



| <span data-ttu-id="9ed85-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ed85-116">Requirement</span></span> | <span data-ttu-id="9ed85-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9ed85-117">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="9ed85-118">Version</span><span class="sxs-lookup"><span data-stu-id="9ed85-118">Version</span></span><br/> | <span data-ttu-id="9ed85-119">Windows Media Player, Version 7,0 oder höher</span><span class="sxs-lookup"><span data-stu-id="9ed85-119">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9ed85-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ed85-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ed85-121">**Effects-Element**</span><span class="sxs-lookup"><span data-stu-id="9ed85-121">**EFFECTS Element**</span></span>](effects-element.md)
</dt> <dt>

[<span data-ttu-id="9ed85-122">**Effekte. Currency-ffecttitle**</span><span class="sxs-lookup"><span data-stu-id="9ed85-122">**EFFECTS.currentEffectTitle**</span></span>](effects-currenteffecttitle.md)
</dt> <dt>

[<span data-ttu-id="9ed85-123">**Effekte. Currency-ffecttype**</span><span class="sxs-lookup"><span data-stu-id="9ed85-123">**EFFECTS.currentEffectType**</span></span>](effects-currenteffecttype.md)
</dt> </dl>

 

 





