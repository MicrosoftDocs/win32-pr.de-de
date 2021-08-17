---
title: glBegin-Funktion (Gl.h)
description: Die GlBegin- und die glBegin-Funktion begrenzen die Scheitelpunkte eines Primitiven oder einer Gruppe von ähnlichen Primitiven. | glBegin-Funktion (Gl.h)
ms.assetid: 8e8e98f8-89e8-40f5-89c1-492c9e3bbd74
keywords:
- glBegin-Funktion OpenGL
topic_type:
- apiref
api_name:
- glBegin
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c497542e345b412bdc7955870405e6ee6cfe0503cee22f9320a031e835853345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361155"
---
# <a name="glbegin-function"></a>glBegin-Funktion

Die **GlBegin-** und die [**glBegin-Funktion**](glend.md) begrenzen die Scheitelpunkte eines Primitiven oder einer Gruppe von ähnlichen Primitiven.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glBegin(
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*mode* 
</dt> <dd>

Die primitiven oder primitiven Typen, die aus Scheitelpunkten erstellt werden, die zwischen **glBegin** und dem nachfolgenden [**gezierten**](glend.md)dargestellt werden. Die folgenden symbolischen Konstanten und ihre Bedeutung werden akzeptiert:



| Wert                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**GL \_ POINTS**</dt> </dl>                          | Behandelt jeden Scheitelpunkt als einen einzelnen Punkt. Vertex *n* definiert Punkt *n.* *N* Punkte werden gezeichnet.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**GL \_ LINES**</dt> </dl>                             | Behandelt jedes Scheitelpunktpaar als unabhängiges Liniensegment. Die Scheitelpunkte *2n bis 1* und *2n* definieren Zeile *n*. Es werden *N/2* Linien gezeichnet.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**GL \_ LINE \_ STRIP**</dt> </dl>             | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten bis zum letzten Scheitelpunkt. Die Scheitelpunkte *n* und *n+1* definieren Zeile *n*. *N – 1* Linien werden gezeichnet.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**GL \_ LINE \_ LOOP**</dt> </dl>                | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Scheitelpunkt bis zum letzten und dann zurück zum ersten. Die Scheitelpunkte *n* und *n + 1* definieren Zeile *n*. Die letzte Zeile wird jedoch durch die Scheitelpunkte *N* und *1* definiert. *N* Linien werden gezeichnet.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**GL \_ TRIANGLES**</dt> </dl>                 | Behandelt jedes Triplet von Scheitelpunkten als unabhängiges Dreieck. Die Scheitelpunkte *3n - 2*, *3n - 1* und *3n* definieren das Dreieck *n*. *N/3* Dreiecke werden gezeichnet.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**GL \_ TRIANGLE \_ STRIP**</dt> </dl> | Zeichnet eine verbundene Gruppe von Dreiecken. Für jeden Scheitelpunkt, der nach den ersten beiden Scheitelpunkten angezeigt wird, wird ein Dreieck definiert. Definieren Sie für ungerade *n* die Scheitelpunkte *n*, *n + 1* und *n + 2* das Dreieck *n*. Für sogar *n* definieren die Scheitelpunkte *n + 1*, *n* und *n + 2* das Dreieck *n*. *N – 2* Dreiecke werden gezeichnet.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**GL \_ TRIANGLE \_ FAN**</dt> </dl>       | Zeichnet eine verbundene Gruppe von Dreiecken. Für jeden Scheitelpunkt, der nach den ersten beiden Scheitelpunkten angezeigt wird, wird ein Dreieck definiert. Die Scheitelpunkte *1,* *n + 1,* *n + 2* definieren das Dreieck *n*. *N – 2* Dreiecke werden gezeichnet.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ QUADS**</dt> </dl>                             | Behandelt jede Gruppe von vier Scheitelpunkten als unabhängiges Quadernatral. Die Scheitelpunkte *4n - 3*, *4n - 2*, *4n - 1* und *4n* definieren quadquaquarale *n*. *N/4* Quaderale werden gezeichnet.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ QUAD \_ STRIP**</dt> </dl>             | Zeichnet eine verbundene Gruppe von Quadernatralen. Für jedes Vertices-Paar, das nach dem ersten Paar angezeigt wird, wird ein Quaderatral definiert. Die Scheitelpunkte *2n – 1*, *2n*, *2n + 2* und *2n + 1* definieren quadquarale *n*. *N/2 - 1* Quadquaraterale werden gezeichnet. Beachten Sie, dass sich die Reihenfolge, in der Scheitelpunkte zum Erstellen eines Quaderatrals aus Stripdaten verwendet werden, von der Reihenfolge unterscheidet, die mit unabhängigen Daten verwendet wird.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**\_GL-POLYGON**</dt> </dl>                       | Zeichnet ein einzelnes konvexes Polygon. Die Scheitelpunkte *1* bis *N* definieren dieses Polygon.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* wurde auf einen nicht akzeptierten Wert festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Eine andere Funktion als [glVertex,](glvertex-functions.md) [glColor,](glcolor-functions.md) [glIndex,](glindex-functions.md) [glNormal,](glnormal-functions.md) [glTexCoord,](gltexcoord-functions.md) [glEvalCoord,](glevalcoord-functions.md) [glEvalPoint,](glevalpoint.md) [glMaterial,](glmaterial-functions.md) [glEdgeFlag,](gledgeflag-functions.md) [**glCallList**](glcalllist.md)oder [**glCallLists**](glcalllists.md) wurde zwischen **glBegin** und dem entsprechenden [**geleerten**](glend.md)aufgerufen. Die Funktion **wurde** aufgerufen, bevor die entsprechende **glBegin** aufgerufen wurde, oder **glBegin** wurde innerhalb einer **glBegin-Sequenz** /  aufgerufen. <br/> |



## <a name="remarks"></a>Hinweise

Die **GlBegin-** und die [**glBegind-Funktion**](glend.md) begrenzen die Scheitelpunkte, die einen Primitiven oder eine Gruppe von ähnlichen Primitiven definieren. Die **glBegin-Funktion** akzeptiert ein einzelnes Argument, das angibt, welche von zehn Primitiven die Scheitelpunkte bilden. Wenn *n* als ganzzahlige Anzahl beginnend bei 1 und *N* als Gesamtzahl der angegebenen Scheitelpunkte verwendet wird, sind die Interpretationen wie folgt:

-   Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und [**dem -Ausschnitt**](glend.md)verwenden. Sie können folgende Funktionen verwenden:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    Sie können [**auch glCallList**](glcalllist.md) oder [**glCallLists**](glcalllists.md) verwenden, um Anzeigelisten auszuführen, die nur die vorherigen Funktionen enthalten. Wenn eine andere OpenGL-Funktion zwischen **glBegin** und soll aufgerufen [**werden,**](glend.md)wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.

-   Unabhängig vom Wert, der für den *Modus* in **glBegin** ausgewählt wurde, gibt es keine Beschränkung für die Anzahl der Scheitelpunkte, die Sie zwischen **glBegin** und [**dem gepunkteten**](glend.md)definieren können. Unvollständig angegebene Linien, Dreiecke, Quadquaraterale und Polygone werden nicht gezeichnet. Unvollständige Spezifikationsergebnisse, wenn entweder zu wenige Scheitelpunkte bereitgestellt werden, um sogar einen einzelnen Primitiven anzugeben, oder wenn ein falsches Vielfaches von Scheitelpunkten angegeben wird. Der unvollständige Primitive wird ignoriert. die vollständigen Primitive werden gezeichnet.
-   Die Mindestspezifikation von Scheitelpunkten für jedes Primitive ist: 

    | Mindestanzahl von Scheitelpunkten | Typ des Primitiven |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | Dreieck          |
    | 4                          | Viereck     |
    | 3                          | polygon           |

    

     

-   Modi, die ein bestimmtes Vielfaches von Scheitelpunkten erfordern, sind GL \_ LINES (2), GL \_ TRIANGLES (3), GL \_ QUADS (4) und GL \_ QUAD STRIP \_ (2).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glEvalPoint**](glevalpoint.md)
</dt> <dt>

[**glIndex**](glindex-functions.md)
</dt> <dt>

[**glMaterial**](glmaterial-functions.md)
</dt> <dt>

[**glNormal**](glnormal-functions.md)
</dt> <dt>

[**glTexCoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

