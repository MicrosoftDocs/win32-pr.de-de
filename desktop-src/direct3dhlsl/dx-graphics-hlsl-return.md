---
title: return-Anweisung
description: Eine return-Anweisung signalisiert das Ende einer Funktion.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- return Statement HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 876c69f3ecfcf1ee1c8391ccc503b2316056b37a
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119585"
---
# <a name="return-statement"></a>return-Anweisung

Eine return-Anweisung signalisiert das Ende einer Funktion.

Rückgabewert \[ \] ;



 

Die einfachste return-Anweisung gibt die Steuerung von der Funktion an das aufrufende Programm zurück. gibt keinen Wert zurück.


```
void main()
{
    return ;
}
```



Eine return-Anweisung kann jedoch einen oder mehrere Werte zurückgeben. In diesem Beispiel wird ein Literalwert zurückgegeben:


```
float main( float input : COLOR0) : COLOR0
{
    return 0;
}
```



In diesem Beispiel wird das skalare Ergebnis eines Ausdrucks zurückgegeben.


```
return  light.enabled = true ;
```



In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus einer lokalen Variablen und einem Literal erstellt wird.


```
return  float4(color.rgb, 1) ;
```



In diesem Beispiel wird ein Vierkomponentenvektor zurückgegeben, der aus dem Ergebnis erstellt wird, das von einer systeminternen Funktion zusammen mit Literalwerten zurückgegeben wird.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



In diesem Beispiel wird eine -Struktur zurückgegeben, die einen oder mehrere Member enthält.


```
float4x4 WorldViewProj;

struct VS_OUTPUT
{
    float4 Pos  : POSITION;
};

VS_OUTPUT VertexShader_Tutorial_1(float4 inPos : POSITION )
{
    VS_OUTPUT out;
    out.Pos = mul(inPos, WorldViewProj );
    return out;
};
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Funktionen (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




