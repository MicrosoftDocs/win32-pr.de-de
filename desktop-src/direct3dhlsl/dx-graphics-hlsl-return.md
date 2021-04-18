---
title: return-Anweisung
description: Eine Return-Anweisung signalisiert das Ende einer Funktion.
ms.assetid: e6c097af-ba0b-4abc-8099-69882ced1e18
keywords:
- Return-Anweisung HLSL
topic_type:
- apiref
api_name:
- return Statement
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 525abf6d815d2073ee39a6bc6a5a81120cf652ee
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104976193"
---
# <a name="return-statement"></a>return-Anweisung

Eine Return-Anweisung signalisiert das Ende einer Funktion.



|                   |
|-------------------|
| Rückgabe \[ Wert \] ; |



 

Die einfachste Return-Anweisung gibt die Steuerung von der Funktion an das aufrufenden Programm zurück. Es wird kein Wert zurückgegeben.


```
void main()
{
    return ;
}
```



Eine Return-Anweisung kann jedoch einen oder mehrere Werte zurückgeben. In diesem Beispiel wird ein Literalwert zurückgegeben:


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



In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus einer lokalen Variablen und einem Literalelement erstellt wird.


```
return  float4(color.rgb, 1) ;
```



In diesem Beispiel wird ein Vektor mit vier Komponenten zurückgegeben, der aus dem Ergebnis erstellt wird, das von einer intrinsischen Funktion zurückgegeben wird, sowie Literalwerte.


```
float4 func(float2 a: POSITION): COLOR
{
    return float4(sin(length(a) * 100.0) * 0.5 + 0.5, sin(a.y * 50.0), 0, 1);
}
```



Dieses Beispiel gibt eine-Struktur zurück, die mindestens ein-Element enthält.


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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Funktionen (DirectX HLSL)](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




