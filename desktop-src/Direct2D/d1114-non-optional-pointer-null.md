---
title: D1114 nicht optionaler Zeiger NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: 'Der-Parameter für die Interface:: method ist nicht optional. Ein NULL-Zeiger wurde übermittelt. Dadurch stürzt Direct2D ab.'
keywords:
- D1114 nicht optionaler Zeiger NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/27/2021
ms.locfileid: "106368698"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: nicht optionaler Zeiger NULL

Der Parameter \[ *Parameter* \] für die *Interface*::*method* ist nicht optional. Ein **null** -Zeiger wurde übermittelt. Dadurch stürzt Direct2D ab.

### <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parame*
</dt> <dd>

Der Name des Parameters, der den **null** -Zeiger enthält.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*berfläche*
</dt> <dd>

Der Name der Schnittstelle, zu der die *Methode* gehört.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*anzuwenden*
</dt> <dd>

Der Name der Methode, die den ungültigen Parameter empfangen hat.

</dd> </dl> 




 

### <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, dass die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode einen NULL-Zeiger für den nicht optionalen *Geometry* -Parameter erhält.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



Dieses Beispiel erzeugt die folgende Debugmeldung:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Ein NULL-Zeiger wurde für einen nicht optionalen Parameter übergeben.

## <a name="fixes"></a>Fehlerbehebungen

Stellen Sie sicher, dass ein nicht optionaler Parameter keinen NULL-Zeiger hat.

 

 
