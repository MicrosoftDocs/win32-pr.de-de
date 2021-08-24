---
title: Signaturen
description: Eine Shadersignatur ist eine Liste der Parameter, die entweder in eine Shaderfunktion eingegeben oder von dieser ausgegeben werden.
ms.assetid: c73a4f3e-e6fa-4e49-9ee8-4e200269dba7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5631dbe473b2e3eea0abb525e58621faf9c5137dd5dc3d743bde53b0ae258f25
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789580"
---
# <a name="signatures"></a>Signaturen

Eine Shadersignatur ist eine Liste der Parameter, die entweder in eine Shaderfunktion eingegeben oder von dieser ausgegeben werden. In Direct3D 10 teilen sich angrenzende Phasen effektiv ein Registerarray, in dem der Ausgabe-Shader (oder die Pipelinephase) Daten an bestimmte Speicherorte im Registerarray schreibt und der Eingabe-Shader von den gleichen Speicherorten lesen muss. Die API verwendet Shadersignaturen, um Shaderausgaben ohne den Mehraufwand der semantischen Auflösung an Eingaben zu binden.

In Direct3D 10 werden Eingabesignaturen aus einer shader-input-Deklaration generiert, und die Ausgabesignatur wird aus einer Shader-Ausgabedeklaration generiert. Eine Eingabesignatur wird als kompatibel mit einer Ausgabesignatur bezeichnet, wenn es sich bei der Ausgabesignatur um eine strikte Teilmenge (Übereinstimmung von Argumenttyp und Reihenfolge) der Eingabesignatur handelt. Die einfachste Möglichkeit, dies zu erreichen, besteht darin, entsprechende Shadereingaben und -ausgaben mit demselben Strukturtyp zu verknüpfen.

Hier ist ein Beispiel für kompatible Signaturen.


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



Hier sehen Sie ein Beispiel für inkompatible Signaturen: Die Reihenfolge der Parameter in der Eingabesignatur stimmt nicht mit der Reihenfolge in der Ausgabesignatur überein.


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



PSInWorks ist eine kompatible Teilmenge von VSOut (die ersten beiden Einträge entsprechen sowohl Typ als auch Reihenfolge mit den ersten beiden Einträgen in VSOut). PSInFails ist jedoch inkompatibel, da die Reihenfolge nicht mit VSOut übereinstimmt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Funktionen](dx-graphics-hlsl-functions.md)
</dt> </dl>

 

 




