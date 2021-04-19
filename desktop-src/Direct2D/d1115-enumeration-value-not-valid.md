---
title: D1115-Enumerationswert ist ungültig.
description: D1115-Enumerationswert ist ungültig.
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- D1115-Enumerationswert ungültig Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: edcfe70c67e61a3b8bfc435adfdaa017a1c62b22
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106360469"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115: der Enumerationswert ist ungültig.

Der Parameter Parameter mit dem Wert "Value" für die " \[  \] \[  \] *Interface*::*method* " ist kein gültiger Enumerationswert.

## <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parame*
</dt> <dd>

Der Name des Parameters, der den unerwarteten Typ empfangen hat.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Wert*
</dt> <dd>

Der ungültige Enumerationswert.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*berfläche*
</dt> <dd>

Der Name der Schnittstelle, zu der die *Methode* gehört.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*anzuwenden*
</dt> <dd>

Der Name der Methode, die den ungültigen Enumerationswert empfangen hat.

</dd> </dl> 




 

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird der Enumerationswert " [**D2D1 \_ Rendering \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) " von 30 angegeben, der außerhalb des erwarteten Bereichs liegt.


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Ein Parameter hat einen ungültigen Enumerationswert verwendet.

## <a name="fixes"></a>Fehlerbehebungen

Verwenden Sie einen gültigen-Enumerationswert.

> [!Note]  
> Die debugschicht überprüft derzeit nur die einzelnen Enumerationswerte. Es wird nicht überprüft, ob eine bitweise Kombination gültig ist.

 

 

 
