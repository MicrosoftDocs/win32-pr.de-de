---
title: Geometry-Shader-Objekt
description: Ein geometry-shader-Objekt verarbeitet ganze Primitive. Verwenden Sie die folgende Syntax, um ein geometry-shader-Objekt zu deklarieren.
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
ms.openlocfilehash: e06bbc184a4b5f82d5edaaf7fdbfbd55f1906f12
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120615"
---
# <a name="geometry-shader-object"></a>Geometry-Shader-Objekt

Ein geometry-shader-Objekt verarbeitet ganze Primitive. Verwenden Sie die folgende Syntax, um ein geometry-shader-Objekt zu deklarieren.

\[maxvertexcount(*NumVerts*) \] void *ShaderName* ( *PrimitiveType DataType Name \[ NumElements \]*, inout *StreamOutputObject* );



 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="_maxvertexcount_NumVerts__"></span><span id="_maxvertexcount_numverts__"></span><span id="_MAXVERTEXCOUNT_NUMVERTS__"></span>\[maxvertexcount(*NumVerts*)\]
</dt> <dd>

\[in \] Deklaration für die maximale Anzahl der zu erstellenden Scheitelzeichen.

-   \[maxvertexcount() \] – erforderliches Schlüsselwort; Klammern und Klammern sind erforderliche Zeichen für die richtige Syntax.
-   *NumVerts:* Eine ganzzahlige Zahl, die die Anzahl der Scheitelzeichen darstellt.

</dd> <dt>

<span id="ShaderName"></span><span id="shadername"></span><span id="SHADERNAME"></span>*ShaderName*
</dt> <dd>

\[in \] Eine ASCII-Zeichenfolge, die einen eindeutigen Namen für die geometry-shader-Funktion enthält.

</dd> <dt>

<span id="PrimitiveType_DataType_Name___NumElements__"></span><span id="primitivetype_datatype_name___numelements__"></span><span id="PRIMITIVETYPE_DATATYPE_NAME___NUMELEMENTS__"></span>*PrimitiveType DataType Name \[ NumElements \]*
</dt> <dd>

*PrimitiveType:* Primitiver Typ, der die Reihenfolge der primitiven Daten bestimmt.



| Primitiver Typ | Beschreibung                                                   |
|----------------|---------------------------------------------------------------|
| *Punkt*        | Punktliste                                                    |
| *Linie*         | Zeilenliste oder Linienstreifen                                       |
| *Dreieck*     | Dreiecksliste oder Dreiecksstreifen                               |
| *lineadj*      | Zeilenliste mit Adjacency oder Zeilenstreifen mit Adjacency         |
| *triangleadj*  | Dreiecksliste mit Adjacency oder Dreiecksstreifen mit Adjacency |



 

*DataType*  -  \[ in \] Ein Eingabedatentyp; kann ein beliebiger [HLSL-Datentyp sein.](dx-graphics-hlsl-data-types.md)

*Name* – Argumentname; dies ist eine ASCII-Zeichenfolge.

*NumElements:* Arraygröße der Eingabe, die vom *PrimitiveType* abhängt, wie in der folgenden Tabelle gezeigt.

| Primitiver Typ | NumElements                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------|
| *Punkt*        | \[1\]<br/> Sie arbeiten nur an einem Punkt nach dem anderen.<br/>                                         |
| *Linie*         | \[2\]<br/> Eine Zeile erfordert zwei Scheitellinien.<br/>                                                    |
| *Dreieck*     | \[3\]<br/> Ein Dreieck erfordert drei Scheitelungen.<br/>                                              |
| *lineadj*      | \[4\]<br/> Ein lineadj hat zwei Enden; daher sind vier Scheitelungen erforderlich.<br/>                    |
| *triangleadj*  | \[6\]<br/> Ein Dreieckadj grenzt an drei weitere Dreiecke; daher sind sechs Scheiteltices erforderlich.<br/> |



 

</dd> <dt>

<span id="StreamOutputObject"></span><span id="streamoutputobject"></span><span id="STREAMOUTPUTOBJECT"></span>*StreamOutputObject*
</dt> <dd>

Die Deklaration des [Streamausgabeobjekts](dx-graphics-hlsl-so-type.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Keine

## <a name="remarks"></a>Bemerkungen

Das folgende Diagramm zeigt die verschiedenen primitiven Typen für ein Geometrie-Shaderobjekt.

![Abbildung der verschiedenen primitiven Typen für ein Geometrie-Shaderobjekt](images/d3d11-gsinputs1.png)

Das folgende Diagramm zeigt Geometry-Shaderaufrufe.

![Abbildung von Geometry-Shaderaufrufen](images/d3d11-gsinputs2.png)

## <a name="examples"></a>Beispiele

Dieses Beispiel ist aus Übung 1 des [Direct3D 10 Shader Model 4.0 Workshop.](https://msdn.microsoft.com/library/Ee416554(v=VS.85).aspx)


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



## <a name="minimum-shader-model"></a>Minimales Shadermodell

Dieses Objekt wird in den folgenden Shadermodellen unterstützt.



| Shadermodell                                                        | Unterstützt |
|---------------------------------------------------------------------|-----------|
| [Shadermodell 4](dx-graphics-hlsl-sm4.md) und höher– Shadermodelle | Ja       |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Shadermodell 4](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 





