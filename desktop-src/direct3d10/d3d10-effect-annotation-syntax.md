---
description: Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der folgenden Syntax deklariert wird.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Syntax Syntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 303065e9c49c380a5accba6faadbc641ec0f528a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861767"
---
# <a name="annotation-syntax-direct3d-10"></a>Syntax Syntax (Direct3D 10)

Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der folgenden Syntax deklariert wird.



| <Wert des *DataType* - *namens*  =  ;...; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                   | BESCHREIBUNG                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datentyp*<br/> | \[im- \] Datentyp, der einen beliebigen [skalaren HLSL](../direct3dhlsl/dx-graphics-hlsl-scalar.md) -Typ und den [Zeichen Folgentyp](../direct3dhlsl/dx-graphics-hlsl-scalar.md)enthält.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*<br/>                 | \[in \] einer ASCII-Zeichenfolge, die den Namen der Anmerkung darstellt.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Wert*<br/>             | \[im \] Anfangswert der Anmerkung.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[in \] zusätzlichen Anmerkungen (Name-Wert-Paare).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Sie können mehr als eine Anmerkung in den spitzen Klammern hinzufügen, die jeweils durch ein Semikolon voneinander getrennt sind. Die Effekt-Framework-APIs erkennen Anmerkungen für globale Variablen. alle anderen Anmerkungen werden ignoriert.

## <a name="example"></a>Beispiel

Beispiele:


```
       
int i <int blabla=27; string blacksheep="Hello There";>;

int j <int bambam=30; string blacksheep="Goodbye There";> = 5 ;

float y <float y=2.3;> = 2.3, z <float y=1.3;> = 1.3 ;

half w <half GlobalW = 3.62;>;

float4 main(float4 pos : SV_POSITION ) : SV_POSITION
{
    pos.y = pos.x > 0 ? pos.w * 1.3 : pos.z * .032;
    for (int x = i; x < j ; x++) 
    {
        pos.w = pos.w * pos.y + x + j - y * w;
    } 

return pos;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Syntax der Effekt Variablen](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
