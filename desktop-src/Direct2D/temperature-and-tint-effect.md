---
title: Temperature and Tönungseffekt
description: Temperatur- und Tönungseffekt
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096638"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="fcf4d-103">Temperatur- und Tönungseffekt</span><span class="sxs-lookup"><span data-stu-id="fcf4d-103">Temperature and tint effect</span></span>

<span data-ttu-id="fcf4d-104">Die CLSID für diesen Effekt ist CLSID \_ D2D1TemperatureTint.</span><span class="sxs-lookup"><span data-stu-id="fcf4d-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="fcf4d-105">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="fcf4d-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="fcf4d-106">Effect-Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="fcf4d-106">Effect properties</span></span>

<span data-ttu-id="fcf4d-107">Die Eigenschaften für den Temperatur- und Tönungseffekt werden durch die [**D2D1 \_ TEMPERATUREANDTINT \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) definiert.</span><span class="sxs-lookup"><span data-stu-id="fcf4d-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fcf4d-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcf4d-108">Requirements</span></span>



| <span data-ttu-id="fcf4d-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fcf4d-109">Requirement</span></span> | <span data-ttu-id="fcf4d-110">Wert</span><span class="sxs-lookup"><span data-stu-id="fcf4d-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="fcf4d-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fcf4d-111">Minimum supported client</span></span> | <span data-ttu-id="fcf4d-112">Windows 10 desktop \[ apps \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcf4d-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fcf4d-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fcf4d-113">Minimum supported server</span></span> | <span data-ttu-id="fcf4d-114">Windows 10 desktop \[ apps \| Windows Store-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fcf4d-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="fcf4d-115">Header</span><span class="sxs-lookup"><span data-stu-id="fcf4d-115">Header</span></span>                   | <span data-ttu-id="fcf4d-116">d2d1effects \_ 2.h</span><span class="sxs-lookup"><span data-stu-id="fcf4d-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="fcf4d-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fcf4d-117">Library</span></span>                  | <span data-ttu-id="fcf4d-118">d2d1.lib, dxguid.lib</span><span class="sxs-lookup"><span data-stu-id="fcf4d-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="fcf4d-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="fcf4d-119">Related topics</span></span>

* [<span data-ttu-id="fcf4d-120">ID2D1Effect-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="fcf4d-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
