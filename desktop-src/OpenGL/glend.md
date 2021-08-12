---
title: glEnd-Funktion (Gl.h)
description: Die glBegin-Funktion und die -Funktion begrenzen die Scheitelzeichen eines Primitiven oder einer Gruppe von primitiven Typen. | glEnd-Funktion (Gl.h)
ms.assetid: 040f8573-683c-4a8a-ae51-66abb0541ac4
keywords:
- glEnd-Funktion OpenGL
topic_type:
- apiref
api_name:
- glEnd
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0817bec7874b9a3a58e28653ff10497eb1e3f5e5170c57dbe2c26a6b20b64460
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118616552"
---
# <a name="glend-function"></a>glEnd-Funktion

Die [**glBegin-Funktion**](glbegin.md) **und die -Funktion begrenzen** die Scheitelzeichen eines Primitiven oder einer Gruppe von primitiven Typen.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Eine andere Funktion als **glVertex**, **glColor**, **glIndex**, **glNormal**, **glTexCoord**, **glEvalCoord**, **glEvalPoint**, **glMaterial**, **glEdgeFlag**, **glCallList** oder **glCallLists** wurde zwischen **glBegin** und dem entsprechenden **glEnd aufgerufen.** Die **Funktion glEnd** wurde aufgerufen, bevor die entsprechende **glBegin** aufgerufen wurde, oder **glBegin** wurde innerhalb einer **glBegin** / **glEnd-Sequenz** aufgerufen. <br/> |



## <a name="remarks"></a>Hinweise

Die [**glBegin-**](glbegin.md) **und die gegrenzte** Funktion begrenzen die Scheitelzeichen, die einen Primitiv oder eine Gruppe von primitiven Typen definieren. Die **glBegin-Funktion** akzeptiert ein einzelnes Argument, das angibt, welche von zehn Primitiven die Scheitelungen bilden. Wenn *n* als ganzzahlige Anzahl beginnend bei 1 und *N* als Gesamtzahl der angegebenen Scheitelzeichen verwendet wird, lauten die Interpretationen wie folgt:

-   Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und **glEnd verwenden.** Sie können die folgenden Funktionen verwenden:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glColor**](glcolor-functions.md)
    -   [**glIndex**](glindex-functions.md)
    -   [**glNormal**](glnormal-functions.md)
    -   [**glTexCoord**](gltexcoord-functions.md)
    -   [**glEvalCoord**](glevalcoord-functions.md)
    -   [**glEvalPoint**](glevalpoint.md)
    -   [**glMaterial**](glmaterial-functions.md)
    -   [**glEdgeFlag**](gledgeflag-functions.md)

    Sie können auch [**glCallList oder**](glcalllist.md) [**glCallLists**](glcalllists.md) verwenden, um Anzeigelisten auszuführen, die nur die vorherigen Funktionen enthalten. Wenn eine andere OpenGL-Funktion zwischen **glBegin** und **glEnd** aufgerufen wird, wird das Fehlerflag festgelegt und die Funktion ignoriert.

-   Unabhängig vom für den Modus *in* **glBegin** ausgewählten Wert gibt es keine Beschränkung für die Anzahl von Scheitelzeichen, die Sie zwischen **glBegin** und **glEnd definieren können.** Zeilen, Dreiecke, Quadrieren und Polygone, die unvollständig angegeben sind, werden nicht gezeichnet. Unvollständige Spezifikationsergebnisse, wenn entweder zu wenige Scheitelungen bereitgestellt werden, um auch nur einen einzelnen Primitiv anzugeben, oder wenn ein falsches Vielfaches von Scheitelungen angegeben wird. Der unvollständige Primitive wird ignoriert. die vollständigen Primitive werden gezeichnet.
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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glCallLists**](glcalllists.md)
</dt> <dt>

[**glColor**](glcolor-functions.md)
</dt> <dt>

[**glEdgeFlag**](gledgeflag-functions.md)
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

 

