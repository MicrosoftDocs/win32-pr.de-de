---
title: Signaturen
description: Bei einer shadersignatur handelt es sich um eine Liste der Parameter, bei denen es sich entweder um Eingaben oder Ausgaben aus einer shaderfunktion handelt.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 37906222ec674c2c1bb5e1cdfea1cb2de2e1df3d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104992855"
---
# <a name="signatures"></a>Signaturen

Bei einer shadersignatur handelt es sich um eine Liste der Parameter, bei denen es sich entweder um Eingaben oder Ausgaben aus einer shaderfunktion handelt. In Direct3D 10 Teilen angrenzende Stufen effektiv ein Register Array, bei dem der ausgabeshader (oder die Pipeline Phase) Daten an bestimmte Speicherorte im Register Array schreibt, und der Eingabe-Shader muss von denselben Speicherorten gelesen werden. Die API verwendet shadersignaturen, um shaderausgaben ohne den Aufwand der semantischen Auflösung mit Eingaben zu binden.

In Direct3D 10 werden Eingabe Signaturen aus einer Shader-Input-Deklaration generiert, und die Ausgabe Signatur wird aus einer Shader-Output-Deklaration generiert. Eine Eingabe Signatur ist mit einer Ausgabe Signatur kompatibel, wenn die Ausgabe Signatur eine strikte Teilmenge (Argumenttyp und Reihenfolge Übereinstimmung) der Eingabe Signatur ist. Die einfachste Möglichkeit, dies zu erreichen, besteht darin, entsprechende shadereingaben und-Ausgaben mit dem gleichen Strukturtyp zu verknüpfen.

Im folgenden finden Sie ein Beispiel für kompatible Signaturen.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInWorks
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
}
```



Im folgenden finden Sie ein Beispiel für inkompatible Signaturen: die Reihenfolge der Parameter in der Eingabe Signatur entspricht nicht der Reihenfolge in der Ausgabe Signatur.


```
// Vertex Shader Output Signature
Struct VSOut
{
  float4 Pos: SV_Position;
  float3 MyNormal: Normal;
  float2 MyTex : Texcoord0;
}

// Pixel Shader Input Signature
Struct PSInFails
{
  float3 MyNormal: Normal;
  float4 Pos: SV_Position;
}
```



Psinworks ist eine kompatible Teilmenge von vsout (die ersten beiden Einträge entsprechen sowohl Typ als auch Order mit den ersten beiden Einträgen in vsout). Psinmisslungen ist jedoch nicht kompatibel, da die Reihenfolge nicht mit vsout identisch ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




