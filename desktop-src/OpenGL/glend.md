---
title: glEnd-Funktion (GL. h)
description: Die Funktionen "glBegin" und "glEnd" begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven. | glEnd-Funktion (GL. h)
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
ms.openlocfilehash: d9bb41395b3ed2e38a64094506e07e2a69ad1d52
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365253"
---
# <a name="glend-function"></a>glEnd-Funktion

Die Funktionen " [**glBegin**](glbegin.md) " und " **glEnd** " begrenzen die Scheitel Punkte eines primitiven oder einer Gruppe von ähnlichen primitiven.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glEnd(void);
```



## <a name="parameters"></a>Parameter

Diese Funktion besitzt keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Der folgende Fehlercode kann von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion " **glVertex**", " **glcolor**", " **glindex**", " **glnormal**", " **gltexcoord**", " **glevalcoord**", " **glevalpoint**", " **glmaterial**", " **gledgeflag**", " **glCallList**" und " **glcalllists** " wurde zwischen **glBegin** und **dem entsprechenden** Die Funktion " **glEnd** " wurde aufgerufen, bevor die entsprechende " **glBegin** " aufgerufen wurde, oder " **glBegin** " wurde innerhalb einer **glBegin**- / **glEnd** -Sequenz aufgerufen. <br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktionen " [**glBegin**](glbegin.md) " und " **glEnd** " begrenzen die Scheitel Punkte, die eine primitive oder eine Gruppe von ähnlichen primitiven definieren. Die **glBegin** -Funktion akzeptiert ein einzelnes Argument, das angibt, welche von zehn primitiven die Scheitel Punkte bilden. Wenn *n* als ganzzahlige Anzahl beginnend bei eins und *n* als Gesamtzahl der angegebenen Scheitel Punkte übernommen wird, lauten die Interpretationen wie folgt:

-   Sie können nur eine Teilmenge der OpenGL-Funktionen zwischen **glBegin** und **glEnd** verwenden. Die Funktionen, die Sie verwenden können, sind:

    -   [**glVertex**](glvertex-functions.md)
    -   [**glcolor**](glcolor-functions.md)
    -   [**glindex**](glindex-functions.md)
    -   [**glnormal**](glnormal-functions.md)
    -   [**gltexcoord**](gltexcoord-functions.md)
    -   [**glevalcoord**](glevalcoord-functions.md)
    -   [**glevalpoint**](glevalpoint.md)
    -   [**glmaterial**](glmaterial-functions.md)
    -   [**gledgeflag**](gledgeflag-functions.md)

    Sie können auch " [**glCallList**](glcalllist.md) " oder " [**glcalllists**](glcalllists.md) " verwenden, um Anzeigelisten auszuführen, die nur die vorangehenden Funktionen enthalten. Wenn eine andere OpenGL-Funktion zwischen **glBegin** und **glEnd** aufgerufen wird, wird das Fehlerflag festgelegt, und die Funktion wird ignoriert.

-   Unabhängig von dem Wert, der für den- *Modus* in **glBegin** ausgewählt ist, gibt es keine Beschränkung für die Anzahl der Scheitel Punkte, die Sie zwischen **glBegin** und **glEnd** definieren können. Zeilen, Dreiecke, vier eckale und Polygone, die nicht vollständig angegeben sind, werden nicht gezeichnet. Unvollständige Spezifikations Ergebnisse, wenn zu wenig Scheitel Punkte bereitgestellt werden, um auch einen einzelnen primitiven anzugeben, oder wenn ein falsches Vielfaches von Vertices angegeben wird. Der unvollständige primitive wird ignoriert. die gesamten primitiven werden gezeichnet.
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

[**glBegin**](/windows/desktop/OpenGL/glbegin)
</dt> <dt>

[**glcalllists**](glcalllists.md)
</dt> <dt>

[**glcolor**](glcolor-functions.md)
</dt> <dt>

[**gledgeflag**](gledgeflag-functions.md)
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

 

