---
title: Stream-Output-Objekt
description: Ein Stream-Output-Objekt ist ein Vorlagen Objekt, das Daten aus der Geometrie-Shader-Stufe streamt. Verwenden Sie die folgende Syntax, um ein Stream-Output-Objekt zu deklarieren.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 98063ddb45633dda6c897abf0f82f29a394c3f95
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390469"
---
# <a name="stream-output-object"></a>Stream-Output-Objekt

Ein Stream-Output-Objekt ist ein Vorlagen Objekt, das Daten aus der [Geometrie-Shader-Stufe](/previous-versions//bb205146(v=vs.85))streamt. Verwenden Sie die folgende Syntax, um ein Stream-Output-Objekt zu deklarieren.



| INOUT *streamoutputobject* < *DataType* >  *Name;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*Streamoutputobject*  <  *DataType*  >    *Name*
</dt> <dd>

Die Deklaration des Stream-Output-Objekts (so).



| Stream-Output von Objekttypen | BESCHREIBUNG                       |
|----------------------------|-----------------------------------|
| *Pointstream*              | Eine Sequenz von Punkt primitiven    |
| *LineStream*               | Eine Sequenz von Zeilen primitiven     |
| *"Test-Stream"*           | Eine Sequenz von Dreiecks primitiven |



 

*DataType* -Output-Datentyp; kann ein beliebiger [HLSL-Datentyp](dx-graphics-hlsl-data-types.md)sein. Muss von den spitzen Klammern umgeben sein.

*Name* : Variablenname; eine ASCII-Zeichenfolge, die das-Objekt eindeutig identifiziert.

</dd> </dl>

## <a name="example"></a>Beispiel

Dies ist ein Beispiel für eine Datenstrom Ausgabe-Objekt Deklaration, die Dreiecks primitive ausgibt, deren Daten durch die PS- \_ cubemap in der Struktur definiert werden \_ . Der Geometry-Shader ist auf das Erstellen von 18 Vertices beschränkt.


```
struct PS_CUBEMAP_IN
{
    float4 Pos : SV_POSITION;     // Projection coord
    float2 Tex : TEXCOORD0;       // Texture coord
    uint RTIndex : SV_RenderTargetArrayIndex;
};

[maxvertexcount(18)]
void main( inout TriangleStream<PS_CUBEMAP_IN> CubeMapStream, triangle PS_CUBEMAP_INT[3] )
{
    ...
}
```



Dies ist ein Code Ausschnitt aus dem [cubemapgs-Beispiel](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx).

## <a name="stream-output-object-methods"></a>Stream-Output-Objektmethoden

Verwenden Sie die folgende Syntax, um Stream-Output-Object-Methoden aufzurufen.


```
Object.Method
```



Die folgenden Methoden werden implementiert.



| Methoden                                              | BESCHREIBUNG                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md)             | Anfügen von Ausgabedaten an einen vorhandenen Datenstrom.                        |
| [Restartstrip](dx-graphics-hlsl-so-restartstrip.md) | Beenden Sie den aktuellen primitiven Bereich, und starten Sie einen neuen primitiven Strip. |



 

## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 