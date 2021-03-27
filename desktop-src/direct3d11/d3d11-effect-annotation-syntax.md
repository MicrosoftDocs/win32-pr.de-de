---
title: Syntax Syntax (Direct3D 11)
description: Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.
ms.assetid: a81198d2-c4d7-47b5-b3b8-2de11a9ee9a3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9583dafd3e1fb314ae6ac9e53d609bebc74a030
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948769"
---
# <a name="annotation-syntax-direct3d-11"></a>Syntax Syntax (Direct3D 11)

Eine Anmerkung ist ein benutzerdefiniertes Informationselement, das mit der in diesem Abschnitt beschriebenen Syntax deklariert wird.



| <*DataType* - *namens*  =  *Wert*; *...* ; > |
|----------------------------------------------|



 

## <a name="parameters"></a>Parameter



| Element                                                                                                   | BESCHREIBUNG                                                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DataType"></span><span id="datatype"></span><span id="DATATYPE"></span>*Datentyp*<br/> | \[im- \] Datentyp, der einen beliebigen [skalaren HLSL](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar) -Typ und den [Zeichen Folgentyp](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-scalar)enthält.<br/> |
| <span id="Name"></span><span id="name"></span><span id="NAME"></span>*Benennen*<br/>                 | \[in \] einer ASCII-Zeichenfolge, die den Namen der Anmerkung darstellt.<br/>                                                                                                          |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>*Wert*<br/>             | \[im \] Anfangswert der Anmerkung.<br/>                                                                                                                           |
| <span id="..."></span>*...*<br/>                                                                 | \[in \] zusätzlichen Anmerkungen (Name-Wert-Paare).<br/>                                                                                                                     |



 

## <a name="remarks"></a>Bemerkungen

Sie können mehr als eine Anmerkung in den spitzen Klammern hinzufügen, die jeweils durch ein Semikolon voneinander getrennt sind. Die Effekt-Framework-APIs erkennen Anmerkungen für globale Variablen. alle anderen Anmerkungen werden ignoriert.

## <a name="example"></a>Beispiel

Hier einige Beispiele.


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

[Effekt Format](d3d11-effect-format.md)
</dt> <dt>

[Syntax der Effekt Variablen](d3d11-effect-variable-syntax.md)
</dt> </dl>

 

