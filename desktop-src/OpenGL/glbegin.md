---
title: glBegin-Funktion (Gl.h)
description: Die funktionen glBegin und primitived begrenzen die Scheitelzeichen eines Primitivs oder einer Gruppe von primitiven Typen. | glBegin-Funktion (Gl.h)
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

Die **funktionen glBegin** und [**primitived**](glend.md) begrenzen die Scheitelzeichen eines Primitivs oder einer Gruppe von primitiven Typen.

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

Die primitiven oder primitiven Typen, die aus Scheitelungen erstellt werden, die zwischen **glBegin** und dem nachfolgenden [**-Typ dargestellt werden.**](glend.md) Im Folgenden werden symbolische Konstanten und ihre Bedeutungen akzeptiert:



| Wert                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_POINTS"></span><span id="gl_points"></span><dl> <dt>**GL \_ POINTS**</dt> </dl>                          | Behandelt jeden Scheitelpunkt als einen einzelnen Punkt. *Scheitelpunkt n* definiert Punkt *n.* *N Punkte* werden gezeichnet.<br/>                                                                                                                                                                                                                                                                                                      |
| <span id="GL_LINES"></span><span id="gl_lines"></span><dl> <dt>**GL \_ LINES**</dt> </dl>                             | Behandelt jedes Vertices-Paar als unabhängiges Liniensegment. Vertices *2n - 1 und* *2n definieren* Zeile *n*. *N/2 Linien* werden gezeichnet.<br/>                                                                                                                                                                                                                                                                |
| <span id="GL_LINE_STRIP"></span><span id="gl_line_strip"></span><dl> <dt>**GL \_ LINE \_ STRIP**</dt> </dl>             | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Scheitelpunkt zum letzten. *Scheitelstriche n* und *n+1* definieren Zeile *n.* *N – 1* Linien werden gezeichnet.<br/>                                                                                                                                                                                                                                                   |
| <span id="GL_LINE_LOOP"></span><span id="gl_line_loop"></span><dl> <dt>**GL \_ LINE \_ LOOP**</dt> </dl>                | Zeichnet eine verbundene Gruppe von Liniensegmenten vom ersten Scheitelpunkt zum letzten und dann zurück zum ersten. *Scheitelstriche n* und *n + 1 definieren* Zeile *n.* Die letzte Zeile wird jedoch durch die Scheitelstriche *N* und *1 definiert.* *N Linien* werden gezeichnet.<br/>                                                                                                                                                                 |
| <span id="GL_TRIANGLES"></span><span id="gl_triangles"></span><dl> <dt>**\_GL-DREIECKE**</dt> </dl>                 | Behandelt jedes Triplet von Scheitelten als unabhängiges Dreieck. Die Scheitelungen *3n – 2*, *3n – 1* und *3n definieren* das Dreieck *n*. *N/3 Dreiecke* werden gezeichnet.<br/>                                                                                                                                                                                                                                              |
| <span id="GL_TRIANGLE_STRIP"></span><span id="gl_triangle_strip"></span><dl> <dt>**GL \_ TRIANGLE \_ STRIP**</dt> </dl> | Zeichnet eine verbundene Gruppe von Dreiecken. Ein Dreieck wird für jeden Scheitelpunkt definiert, der nach den ersten beiden Scheitelpunkte dargestellt wird. Für *ungerade n* definieren *Scheitelungen n*, *n + 1* und *n + 2* das Dreieck *n*. Für *n definieren* Scheitelungen *n + 1,* *n* und *n + 2* das Dreieck *n*. *N – 2* Dreiecke werden gezeichnet.<br/>                                                                                                  |
| <span id="GL_TRIANGLE_FAN"></span><span id="gl_triangle_fan"></span><dl> <dt>**GL \_ TRIANGLE \_ FAN**</dt> </dl>       | Zeichnet eine verbundene Gruppe von Dreiecken. Ein Dreieck wird für jeden Scheitelpunkt definiert, der nach den ersten beiden Scheitelpunkte dargestellt wird. Scheitelungen *1,* *n + 1,* *n + 2 definieren* das Dreieck *n*. *N – 2* Dreiecke werden gezeichnet.<br/>                                                                                                                                                                                         |
| <span id="GL_QUADS"></span><span id="gl_quads"></span><dl> <dt>**GL \_ QUADS**</dt> </dl>                             | Behandelt jede Gruppe von vier Scheitelungen als unabhängige Quadraktion. Vertices *4n - 3*, *4n - 2*, *4n - 1* und *4n definieren* quadrierenateral *n*. *N/4-Quadriertateralen* werden gezeichnet.<br/>                                                                                                                                                                                                                  |
| <span id="GL_QUAD_STRIP"></span><span id="gl_quad_strip"></span><dl> <dt>**GL \_ QUAD \_ STRIP**</dt> </dl>             | Zeichnet eine verbundene Gruppe von Quadrierten. Für jedes Scheitelungspaar, das nach dem ersten Paar dargestellt wird, wird eine quadrierend definiert. Die *Scheitelungen 2n – 1*, *2n*, *2n + 2* und *2n + 1* definieren quadrierentral *n*. *N/2 – 1* Quadriertateral werden gezeichnet. Beachten Sie, dass sich die Reihenfolge, in der Scheiteltices verwendet werden, um ein Quadrokatral aus Stripdaten zu erstellen, von der reihenfolge abgrenzt, die mit unabhängigen Daten verwendet wird.<br/> |
| <span id="GL_POLYGON"></span><span id="gl_polygon"></span><dl> <dt>**GL \_ POLYGON**</dt> </dl>                       | Zeichnet ein einzelnes, konvexes Polygon. Vertices *1* bis *N* definieren dieses Polygon.<br/>                                                                                                                                                                                                                                                                                                                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *mode* wurde auf einen nicht unterstützten Wert festgelegt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Eine andere Funktion als [glVertex](glvertex-functions.md), [glColor](glcolor-functions.md), [glIndex](glindex-functions.md), [glNormal](glnormal-functions.md), [glTexCoord](gltexcoord-functions.md), [glEvalCoord](glevalcoord-functions.md), [glEvalPoint](glevalpoint.md), [glMaterial](glmaterial-functions.md), [glEdgeFlag](gledgeflag-functions.md), [**glCallList**](glcalllist.md)oder [**glCallLists**](glcalllists.md) wurde zwischen **glBegin** und dem entsprechenden - [**aufgerufen.**](glend.md) Die Funktion **wurde aufgerufen,** bevor die entsprechende **glBegin** aufgerufen wurde, oder **glBegin** wurde innerhalb einer **glBegin-Sequenz** /  aufgerufen. <br/> |



## <a name="remarks"></a>Hinweise

Die **glBegin-Funktion** [**und die -Funktion begrenzen**](glend.md) die Scheitelzeichen, die einen Primitiven oder eine Gruppe von primitiven Typen definieren. Die **glBegin-Funktion** akzeptiert ein einzelnes Argument, das angibt, welche von zehn Primitiven die Scheitelungen bilden. Wenn *n* als ganzzahlige Anzahl beginnend bei 1 und *N* als Gesamtzahl der angegebenen Scheitelzeichen verwendet wird, lauten die Interpretationen wie folgt:

-   Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin und** [**der -Datei verwenden.**](glend.md) Sie können die folgenden Funktionen verwenden:

    [**glVertex**](glvertex-functions.md)

     

    [**glColor**](glcolor-functions.md)

     

    [**glIndex**](glindex-functions.md)

     

    [**glNormal**](glnormal-functions.md)

     

    [**glTexCoord**](gltexcoord-functions.md)

     

    [**glEvalCoord**](glevalcoord-functions.md)

     

    [**glEvalPoint**](glevalpoint.md)

     

    [**glMaterial**](glmaterial-functions.md)

     

    [**glEdgeFlag**](gledgeflag-functions.md)

    Sie können auch [**glCallList oder**](glcalllist.md) [**glCallLists**](glcalllists.md) verwenden, um Anzeigelisten auszuführen, die nur die vorherigen Funktionen enthalten. Wenn eine andere OpenGL-Funktion zwischen **glBegin** und [**dem**](glend.md)-Flag aufgerufen wird, wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.

-   Unabhängig vom für den -Modus *in* **glBegin** ausgewählten Wert gibt es keine Beschränkung für die Anzahl der Scheitelzeichen, die Sie zwischen **glBegin** und [**gez. definieren können.**](glend.md) Zeilen, Dreiecke, Quadrieren und Polygone, die unvollständig angegeben sind, werden nicht gezeichnet. Unvollständige Spezifikationsergebnisse, wenn entweder zu wenige Scheitelungen bereitgestellt werden, um auch nur einen einzelnen Primitiv anzugeben, oder wenn ein falsches Vielfaches von Scheitelungen angegeben wird. Der unvollständige Primitive wird ignoriert. die vollständigen Primitiven werden gezeichnet.
-   Die Mindestspezifikation der Scheiteltices für die einzelnen Primitiven ist: 

    | Mindestanzahl von Scheitelzeichen | Typ des Primitivs |
    |----------------------------|-------------------|
    | 1                          | point             |
    | 2                          | line              |
    | 3                          | Dreieck          |
    | 4                          | Viereck     |
    | 3                          | polygon           |

    

     

-   Modi, die ein bestimmtes Vielfaches von Scheitellinien erfordern, sind GL \_ LINES (2), GL \_ TRIANGLES (3), GL \_ QUADS (4) und GL \_ QUAD STRIP \_ (2).

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

 

