---
title: Geometry-Shader-Objekt
description: Ein Geometry-Shader-Objekt verarbeitet ganze primitive. Verwenden Sie die folgende Syntax, um ein Geometry-Shader-Objekt zu deklarieren.
ms.assetid: d5c1c22b-6fa6-40a8-900f-6d74f74468c1
keywords:
- maxvertexcount (DirectX HLSL)
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: dadb0e8bb3ddda16305ac701b34523668bd9c1a5
ms.sourcegitcommit: 477b1efe7d9c2f91d5f2ac588a20edf348b1c734
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2019
ms.locfileid: "103719752"
---
# <a name="geometry-shader-object"></a>Geometry-Shader-Objekt

Ein Geometry-Shader-Objekt verarbeitet ganze primitive. Verwenden Sie die folgende Syntax, um ein Geometry-Shader-Objekt zu deklarieren.



|                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------|
| \[maxvertexcount (*numverts*) \] void *shadername* ( *PrimitiveType DataType Name \[ numElements \]*, INOUT *streamoutputobject* ); |



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount (*numverts*)\]
</dt> <dd>

\[in \] der Deklaration für die maximale Anzahl der zu erstellenden Scheitel Punkte.

-   \[maxvertexcount () \] : Erforderliches Schlüsselwort; eckige Klammern und Klammer sind erforderliche Zeichen für die korrekte Syntax.
-   *Numverts* -eine ganzzahlige Zahl, die die Anzahl der Vertices darstellt.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*Shadername*
</dt> <dd>

\[in \] einer ASCII-Zeichenfolge, die einen eindeutigen Namen für die Geometry-Shader-Funktion enthält.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ numElements \]*
</dt> <dd>

*PrimitiveType* : primitiver Typ, der die Reihenfolge der primitiven Daten bestimmt.



| Primitiver Typ | BESCHREIBUNG                                                   |
|----------------|---------------------------------------------------------------|
| *Punkt*        | Punkt Liste                                                    |
| *Stimmen*         | Zeilen-oder Zeilen Streifen                                       |
| *Triangle*     | Dreiecks Liste oder Dreiecks Leiste                               |
| *lineadj*      | Zeilen Liste mit der Nähe oder dem Zeilen Streifen mit der Nähe         |
| *"-adangleadj"*  | Dreiecks Liste mit der Nähe oder dem Dreiecks Streifen mit der Nähe |



 

*DataType*  -  \[ in \] einem Eingabe Datentyp kann ein beliebiger [HLSL-Datentyp](dx-graphics-hlsl-data-types.md)sein.

*Name* : Argument Name; Dies ist eine ASCII-Zeichenfolge.

*NumElements* : Array Größe der Eingabe, die von *PrimitiveType* abhängig ist, wie in der folgenden Tabelle gezeigt.

| Primitiver Typ | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Punkt*        | \[1\]<br/> Sie arbeiten jeweils nur auf einem Punkt.<br/>                                         |
| *Stimmen*         | \[2\]<br/> Eine Zeile erfordert zwei Vertices.<br/>                                                    |
| *Triangle*     | \[3\]<br/> Ein Dreieck erfordert drei Vertices.<br/>                                              |
| *lineadj*      | \[4\]<br/> Ein lineadj hat zwei Ende. Daher sind vier Vertices erforderlich.<br/>                    |
| *"-adangleadj"*  | \[6\]<br/> Ein "dreiangleadj"-Rahmen drei weitere Dreiecke Daher sind sechs Vertices erforderlich.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*Streamoutputobject*
</dt> <dd>

Die Deklaration des [Stream-Output-Objekts](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Das folgende Diagramm zeigt die verschiedenen primitiven Typen für ein Geometry-Shader-Objekt.

![Darstellung der verschiedenen primitiven Typen für ein Geometry-Shader-Objekt](images/d3d11-gsinputs1.png)

Das folgende Diagramm zeigt die Geometrie-Shader-Aufrufe.

![Abbildung der Geometrie-Shader-Aufrufe](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Beispiele

Dieses Beispiel basiert auf Übung 1 aus dem [Direct3D 10-Shader Model 4,0-Workshop](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx).


```
[maxvertexcount(3)]
void GSScene( triangleadj GSSceneIn input[6], inout TriangleStream<PSSceneIn> OutputStream )
{   
    PSSceneIn output = (PSSceneIn)0;

    for( uint i=0; i<6; i+=2 )
    {
        output.Pos = input[i].Pos;
        output.Norm = input[i].Norm;
        output.Tex = input[i].Tex;
        
        OutputStream.Append( output );
    }
    
    OutputStream.RestartStrip();
}
```



## <a name="minimum-shader-model"></a>Minimaler Shader-Modell

Dieses Objekt wird in den folgenden shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shader Model 4](dx-graphics-hlsl-sm4.md) und höhere shadermodelle | ja       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





