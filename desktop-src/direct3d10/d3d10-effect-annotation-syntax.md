---
description: Eine Anmerkung ist eine benutzerdefinierte Information, die mit der folgenden Syntax deklariert wird.
ms.assetid: 9178e61e-05a4-441c-a9f1-e05e23ab48a5
title: Anmerkungssyntax (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0c02e250438f25a22f8ba6d059a723299f1ee1fa175b51ce2ffe87b07c5f87
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120120000"
---
# <a name="annotation-syntax-direct3d-10"></a>Anmerkungssyntax (Direct3D 10)

Eine Anmerkung ist eine benutzerdefinierte Information, die mit der folgenden Syntax deklariert wird.



| <*DataType* *Name*  =  *Value*; ... ; > |
|--------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                   | Beschreibung                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datatype*<br/> | \[in \] Der Datentyp, der alle [skalaren HLSL-Typen](../direct3dhlsl/dx-graphics-hlsl-scalar.md) sowie den [Zeichenfolgentyp](../direct3dhlsl/dx-graphics-hlsl-scalar.md)enthält.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Namen*<br/>                 | \[in \] Eine ASCII-Zeichenfolge, die den Anmerkungsnamen darstellt.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Wert*<br/>             | \[in \] Der Anfangswert der Anmerkung.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[in \] Zusätzliche Anmerkungen (Name-Wert-Paare).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Hinweise

Sie können innerhalb der spitzen Klammern mehrere Anmerkungen hinzufügen, die jeweils durch ein Semikolon getrennt sind. Die Effektframework-APIs erkennen Anmerkungen zu globalen Variablen. alle anderen Anmerkungen werden ignoriert.

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

[Syntax der Effect-Variablen](d3d10-effect-variable-syntax.md)
</dt> </dl>

 

 
