---
title: Stream-Output-Objekt
description: Ein Streamausgabeobjekt ist ein Vorlagenobjekt, das Daten aus der Geometry-Shader-Phase streamt. Verwenden Sie die folgende Syntax, um ein Streamausgabeobjekt zu deklarieren.
ms.assetid: 07a5489c-c238-4466-9282-5b168448aff7
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 79e0247b424ebb6f72622565845c17b622ab715cd8860a83ce24ae58ac7420c6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789480"
---
# <a name="stream-output-object"></a>Stream-Output-Objekt

Ein Streamausgabeobjekt ist ein Vorlagenobjekt, das Daten aus der [Geometry-Shader-Phase streamt.](/previous-versions//bb205146(v=vs.85)) Verwenden Sie die folgende Syntax, um ein Streamausgabeobjekt zu deklarieren.



| inout *StreamOutputObject* < *DataType* >  *Name;* |
|------------------------------------------------------|



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="StreamOutputObject___________________________DataType_________________________________________Name"></span><span id="streamoutputobject___________________________datatype_________________________________________name"></span><span id="STREAMOUTPUTOBJECT___________________________DATATYPE_________________________________________NAME"></span>*StreamOutputObject*  <  *DataType*  >    *Name*
</dt> <dd>

Die Stream-Output-Objektdeklaration (SO).



| Stream-Output Objekttypen | Beschreibung                       |
|----------------------------|-----------------------------------|
| *PointStream*              | Eine Sequenz von Punktprimitiven    |
| *LineStream*               | Eine Sequenz von Linienprimitiven     |
| *TriangleStream*           | Eine Sequenz von Dreiecksprimitiven |



 

*DataType :* Ausgabedatentyp; kann ein [beliebiger HLSL-Datentyp sein.](dx-graphics-hlsl-data-types.md) Muss von den eckigen Klammern umgeben sein.

*Name* – Variablenname; Eine ASCII-Zeichenfolge, die das Objekt eindeutig identifiziert.

</dd> </dl>

## <a name="example"></a>Beispiel

Dies ist ein Beispiel für eine Streamausgabe-Objektdeklaration, die Dreiecksprimitiven ausstreamt, deren Daten von der PS \_ CUBEMAP \_ IN-Struktur definiert werden. Der geometry-shader ist auf das Generieren von 18 Scheiteltices beschränkt.


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



Dies ist ein Codeausschnitt aus dem [CubeMapGS-Beispiel.](https://msdn.microsoft.com/library/Ee416398(v=VS.85).aspx)

## <a name="stream-output-object-methods"></a>Stream-Output Objektmethoden

Verwenden Sie die folgende Syntax zum Aufrufen von stream-output-object-Methoden.


```
Object.Method
```



Die folgenden Methoden werden implementiert.



| Methoden                                              | BESCHREIBUNG                                                      |
|------------------------------------------------------|------------------------------------------------------------------|
| [Append](dx-graphics-hlsl-so-append.md) (Anfügen)             | Fügen Sie Ausgabedaten an einen vorhandenen Stream an.                        |
| [RestartStrip](dx-graphics-hlsl-so-restartstrip.md) | Beenden Sie den aktuellen primitiven Strip, und starten Sie einen neuen primitiven Strip. |



 

## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höhere Shadermodelle | Ja       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 