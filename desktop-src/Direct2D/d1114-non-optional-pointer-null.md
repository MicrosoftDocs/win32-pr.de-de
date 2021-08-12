---
title: D1114 Non Optional Pointer NULL
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: Der Parameter für interface::method ist nicht optional. Ein NULL-Zeiger wurde übergeben. Dies verursacht einen Absturz von Direct2D.
keywords:
- D1114 Nicht optionaler Zeiger NULL Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: fa5213eabfb4b22b9a37927495f5058cbfeb0b86b0f1f8b8f3a4ba1a2a2bdbb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666209"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114: Nicht optionaler Zeiger NULL

Der \[ *Parameterparameter* \] für die *Schnittstelle*::*-Methode* ist nicht optional. Ein **NULL-Zeiger** wurde übergeben. Dies verursacht einen Absturz von Direct2D.

### <a name="placeholders"></a>Platzhalter

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*Parameter*
</dt> <dd>

Der Name des Parameters, der den **NULL-Zeiger** enthält.

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*Schnittstelle*
</dt> <dd>

Der Name der Schnittstelle, zu der *die Methode* gehört.

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*Methode*
</dt> <dd>

Der Name der Methode, die den ungültigen Parameter empfangen hat.

</dd> </dl> 




 

### <a name="examples"></a>Beispiele

Das folgende Beispiel zeigt, dass die [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) einen NULL-Zeiger für den nicht optionalen *geometry-Parameter* empfängt.


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



In diesem Beispiel wird die folgende Debugmeldung erzeugt:

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>Mögliche Ursachen

Für einen nicht optionalen Parameter wurde ein NULL-Zeiger übergeben.

## <a name="fixes"></a>Fehlerbehebungen

Stellen Sie sicher, dass ein nicht optionaler Parameter keinen NULL-Zeiger aufgibt.

 

 
