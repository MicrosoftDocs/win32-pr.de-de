---
title: D1115-Enumerationswert ungültig
description: D1115-Enumerationswert ungültig
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- D1115-Enumerationswert Ungültiges Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11800acaae350b5289b339738448300c91db32a16c0d3f3d9224f08b6079fba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758120"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: Enumerationswert ungültig

Der \[ *Parameterparameter* \] mit dem \[ *Wertwert* für die \] *Schnittstelle*::*-Methode* ist kein gültiger Enumerationswert.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parameter*
</dt> <dd>

Der Name des Parameters, der den unerwarteten Typ empfangen hat.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Der ungültige Enumerationswert.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Der Name der Schnittstelle, zu der die *Methode* gehört.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Methode*
</dt> <dd>

Der Name der Methode, die den ungültigen Enumerationswert empfangen hat.

</dd> </dl> 




 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der [**D2D1 \_ RENDER \_ TARGET \_ TYPE-Enumerationswert**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 30 angegeben, der außerhalb des erwarteten Bereichs liegt.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



In diesem Beispiel wird die folgende Debugmeldung erzeugt:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Ein Parameter hat einen ungültigen Enumerationswert verwendet.

## <a name="fixes"></a>Fehlerbehebungen

Verwenden Sie einen gültigen Enumerationswert.

> [!Note]  
> Die Debugebene überprüft derzeit nur die einzelnen Enumerationswerte. es überprüft nicht, ob eine bitweise Kombination gültig ist.

 

 

 
