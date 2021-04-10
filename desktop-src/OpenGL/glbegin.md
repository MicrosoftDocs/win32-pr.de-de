---
title: glBegin-Funktion (GL. h)
description: Die Funktionen "glBegin" und "glEnd" begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven. | glBegin-Funktion (GL. h)
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
ms.openlocfilehash: 8227d30adf97bf27fecc19603a5e5e32e4f44822
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "103961424"
---
# <a name="glbegin-function"></a>glBegin-Funktion

Die Funktionen " **glBegin** " und " [**glEnd**](glend.md) " begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven.

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

Die primitiven oder primitiven, die aus Scheitel Punkten erstellt werden, die zwischen **glBegin** und dem nachfolgenden [**glEnd**](glend.md)dargestellt werden. Die folgenden symbolischen Konstanten und ihre Bedeutung sind zulässig:



| Wert                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**GL- \_ Punkte**</dt> </dl>                          | Behandelt jeden Scheitelpunkt als einen einzelnen Punkt. Scheitel *Punkt n definiert* Punkt *n*. *N* Punkte werden gezeichnet.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**GL- \_ Zeilen**</dt> </dl>                             | Behandelt jedes Paar von Scheitel Punkten als unabhängiges Liniensegment. Die Scheitel Punkte *2n-1* und *2N* definieren Zeile *n*. *N/2* Zeilen werden gezeichnet.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**GL- \_ Zeilen \_ Streifen**</dt> </dl>             | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Scheitelpunkt bis zum letzten. Die Scheitel Punkte *n* und *n + 1* definieren Zeile *n*. *N-1* Zeilen werden gezeichnet.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**GL- \_ Zeilen \_ Schleife**</dt> </dl>                | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Vertex bis zum letzten und dann zurück zum ersten. Die Scheitel Punkte *n* und *n + 1* definieren Zeile *n*. Die letzte Zeile wird jedoch durch Vertices *N* und *1* definiert. *N* Zeilen werden gezeichnet.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**GL- \_ Dreiecke**</dt> </dl>                 | Behandelt jedes tripleder Scheitel Punkte als unabhängiges Dreieck. Die Scheitel Punkte *3N-2*, *3N-1* und *3N* definieren das Dreieck *n*. *N/3-* Dreiecke werden gezeichnet.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**GL- \_ Dreiecks \_ Streifen**</dt> </dl> | Zeichnet eine verbundene Gruppe von Dreiecken. Für jeden Scheitelpunkt, der nach den ersten beiden Scheitel Punkten dargestellt wird, wird ein Dreieck definiert. Für ungerade *n*, Vertices *n*, *n + 1* und *n + 2* definieren Sie das Dreieck *n*. Für gerade *n* werden die Scheitel Punkte *n + 1*, *n* und *n + 2* das Dreieck *n* definieren. *N-2* Dreiecke werden gezeichnet.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**GL- \_ Dreiecks \_ Lüfter**</dt> </dl>       | Zeichnet eine verbundene Gruppe von Dreiecken. für jeden Scheitelpunkt, der nach den ersten beiden Scheitel Punkten dargestellt wird, wird ein Dreieck definiert. Die Scheitel Punkte *1*, *n + 1*, *n + 2* definieren das Dreieck *n*. *N-2* Dreiecke werden gezeichnet.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ .**</dt> </dl>                             | Behandelt jede Gruppe von vier Scheitel Punkten als unabhängige vier Vertices. Vertices *4N-3*, *4N-2*, *4N-1* und *4N* definieren vierseitiges *n*. *N/4* viereckale werden gezeichnet.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ Quad \_ Strip**</dt> </dl>             | Zeichnet eine verbundene Gruppe von viereckalen. Für jedes Paar von Vertices, die nach dem ersten paar dargestellt werden, ist ein Viereck definiert. Die Scheitel Punkte *2n-1*, *2N*, *2N + 2* und *2n + 1* definieren vierseitige *n*. *N/2-1* viereckale werden gezeichnet. Beachten Sie, dass die Reihenfolge, in der die Scheitel Punkte verwendet werden, um ein vierseitiges aus den Bereichs Daten zu erstellen, von dem mit unabhängigen Daten verwendeten abweicht<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**GL- \_ Polygon**</dt> </dl>                       | Zeichnet ein einzelnes, zusammen gemitteles Polygon. In den Scheitel Punkten *1* bis *N* wird dieses Polygon definiert.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Modus* wurde auf einen nicht akzeptierten Wert festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion " [glVertex](glvertex-functions.md)", " [glcolor](glcolor-functions.md)", " [glindex](glindex-functions.md)", " [glnormal](glnormal-functions.md)", " [gltexcoord](gltexcoord-functions.md)", " [glevalcoord](glevalcoord-functions.md)", " [glevalpoint](glevalpoint.md)", " [glmaterial](glmaterial-functions.md)", " [gledgeflag](gledgeflag-functions.md)", " [**glCallList**](glcalllist.md)" und " [**glcalllists**](glcalllists.md) " wurde zwischen **glBegin** und [**dem entsprechenden**](glend.md) Die Funktion " **glEnd** " wurde aufgerufen, bevor die entsprechende " **glBegin** " aufgerufen wurde, oder " **glBegin** " wurde innerhalb einer **glBegin**- / **glEnd** -Sequenz aufgerufen. <br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktionen " **glBegin** " und " [**glEnd**](glend.md) " begrenzen die Scheitel Punkte, die eine primitive oder eine Gruppe von ähnlichen primitiven definieren. Die **glBegin** -Funktion akzeptiert ein einzelnes Argument, das angibt, welche von zehn primitiven die Scheitel Punkte bilden. Wenn *n* als ganzzahlige Anzahl beginnend bei eins und *n* als Gesamtzahl der angegebenen Scheitel Punkte übernommen wird, lauten die Interpretationen wie folgt:

-   Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und [**glEnd**](glend.md)verwenden. Die Funktionen, die Sie verwenden können, sind:

    [**glVertex**](glvertex-functions.md)

     

    [**glcolor**](glcolor-functions.md)

     

    [**glindex**](glindex-functions.md)

     

    [**glnormal**](glnormal-functions.md)

     

    [**gltexcoord**](gltexcoord-functions.md)

     

    [**glevalcoord**](glevalcoord-functions.md)

     

    [**glevalpoint**](glevalpoint.md)

     

    [**glmaterial**](glmaterial-functions.md)

     

    [**gledgeflag**](gledgeflag-functions.md)

    Sie können auch " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) " verwenden, um Anzeigelisten auszuführen, die nur die vorangehenden Funktionen enthalten. Wenn eine andere OpenGL-Funktion zwischen **glBegin** und [**glEnd**](glend.md)aufgerufen wird, wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.

-   Unabhängig von dem Wert, der für den- *Modus* in **glBegin** ausgewählt ist, gibt es keine Beschränkung für die Anzahl der Scheitel Punkte, die Sie zwischen **glBegin** und [**glEnd**](glend.md)definieren können. Zeilen, Dreiecke, vier eckale und Polygone, die nicht vollständig angegeben sind, werden nicht gezeichnet. Unvollständige Spezifikations Ergebnisse, wenn zu wenig Scheitel Punkte bereitgestellt werden, um auch einen einzelnen primitiven anzugeben, oder wenn ein falsches Vielfaches von Vertices angegeben wird. Der unvollständige primitive wird ignoriert. die gesamten primitiven werden gezeichnet.
-   Die minimale Spezifikation der Scheitel Punkte für die einzelnen primitiven ist: 

    | Mindestanzahl von Vertices | Primitiver Typ |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | Dreieck          |
    | 4                          | vierseitigen     |
    | 3                          | polygon           |

    

     

-   Modi, die ein bestimmtes Vielfaches von Vertices erfordern, sind GL- \_ Linien (2), GL \_ -Dreiecke (3), GL \_ -Quad (4) und GL \_ Quad \_ Strip (2).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>GL. h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glcalllists**](glcalllists.md)
</dt> <dt>

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**gledgeflag**](gledgeflag-functions.md)
</dt> <dt>

[**glEnd**](/windows/desktop/OpenGL/glend)
</dt> <dt>

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[**glevalpoint**](glevalpoint.md)
</dt> <dt>

[**glindex**](glindex-functions.md)
</dt> <dt>

[**glmaterial**](glmaterial-functions.md)
</dt> <dt>

[**glnormal**](glnormal-functions.md)
</dt> <dt>

[**gltexcoord**](gltexcoord-functions.md)
</dt> <dt>

[**glVertex**](glvertex-functions.md)
</dt> </dl>

 

