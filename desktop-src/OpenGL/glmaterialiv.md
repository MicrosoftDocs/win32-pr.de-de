---
title: glMaterialiv-Funktion (Gl.h)
description: Die glMaterialiv-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: 9d045202-e565-4cf7-946a-60299e1bc1b1
keywords:
- glMaterialfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMaterialfv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 922fd0cd90b848f0d5c324451f502faa8fa6b961686b209cb881c752b992a6df
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128210"
---
# <a name="glmaterialiv-function"></a>glMaterialiv-Funktion

Die **glMaterialiv-Funktion** gibt Materialparameter für das Beleuchtungsmodell an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMaterialfv(
         GLenum face,
         GLenum pname,
   const GLint  *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Das Gesicht oder die Gesichter, die aktualisiert werden. Muss einer der folgenden Sein: GL \_ FRONT, GL \_ BACK oder GL FRONT und GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Der Materialparameter des Gesichts oder der Gesichter, die aktualisiert werden. Die Parameter, die mit [**glMaterialiv**](glmaterialfv.md)und ihren Interpretationen durch die Beleuchtungsgleichung angegeben werden können, sind wie folgt.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                       | Der parameter-Parameter enthält vier ganzzahlige Werte, die die RGBA-Reflektion des Materials in der Umgebung angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige Werte noch Gleitkommawerte werden geklammern. Die Standardmäßige Umgebungsreflektion für materialien mit Vorder- und Hintergrund ist (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                       | Der parameter-Parameter enthält vier ganzzahlige Werte, die die diffuse RGBA-Reflexion des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige Werte noch Gleitkommawerte werden geklammern. Die standardmäßige diffuse Reflektion für vordere und hintere Materialien ist (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                    | Der parameter-Parameter enthält vier ganzzahlige Werte, die die specular RGBA-Reflexion des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige Werte noch Gleitkommawerte werden geklammern. Die Standardmäßige spiegelungsbasierte Reflektion für vordere und hintere Materialien ist (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ AUSGABE**</dt> </dl>                                    | Der parameter -Parameter enthält vier ganzzahlige Werte, die die RGBA-Ausgabe der Lichtstärke des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige Werte noch Gleitkommawerte werden geklammern. Die Standardmäßige Intensität der Ausgabe für materialien mit vorderer und hinterer Richtung ist (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-VERTRAUENSWÜRDIGKEIT**</dt> </dl>                                 | Der *Parameter param* ist eine einzelne ganze Zahl, die den RGBA-Glanz exponenten des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. Der Standardspekular exponent für vordere und hintere Materialien ist 0. <br/>                                                                                                                                                                                                     |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**GL \_ AMBIENT \_ UND \_ DIFFUSE**</dt> </dl> | Entspricht dem zweimalen Aufrufen von [**glMaterial**](glmaterial-functions.md) mit den gleichen Parameterwerten, einmal mit GL \_ AMBIENT und einmal mit GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                            |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL \_ COLOR \_ INDEXES**</dt> </dl>                    | Der Parameter params enthält drei ganzzahlige Werte, die die Farbindizes für Umgebungs-, Diffuse- und Glanzlicht angeben. Diese drei Werte und GL \_ CABINESS sind die einzigen Materialwerte, die von der Farbindexmodus-Beleuchtungsgleichung verwendet werden. Eine Erläuterung der Farbindexbeleuchtung finden Sie unter [**glLightModel.**](gllightmodel-functions.md)<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Der Wert, auf den der Parameter GL \_ CABINESS festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                              | Bedeutung                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | Entweder *face* oder *pname* war kein akzeptierter Wert.<br/>                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | Ein Glanz exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.<br/> |



## <a name="remarks"></a>Hinweise

Die [**glMaterialiv-Funktion**](glmaterialf.md) weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine , die *vordere* Gruppe, wird verwendet, um Punkte, Linien, Bitmaps und alle Polygone (wenn die zweiseitige Beleuchtung deaktiviert ist) oder einfach frontseitige Polygone (wenn die zweiseitige Beleuchtung aktiviert ist) zu beschatten. Der andere Satz, *rückwärts gerichtet,* wird nur verwendet, um rückwärts gerichtete Polygone zu schatten, wenn die zweiseitige Beleuchtung aktiviert ist. Ausführliche Informationen zu ein- und zweiseitigen Beleuchtungsberechnungen finden Sie unter [**glLightModel.**](gllightmodel-functions.md)

Die [**glMaterialiv-Funktion**](glmaterialf.md) verwendet drei Argumente. Die erste , *face*, gibt an, ob die GL \_ FRONT-Materialien, die GL \_ BACK-Materialien oder beide GL \_ FRONT AND \_ \_ BACK-Materialien geändert werden. Die zweite , *pname*, gibt an, welcher von mehreren Parametern in einem oder beiden Sätzen geändert wird. Der dritte *Parameter* gibt an, welcher Wert dem angegebenen Parameter zugewiesen wird.

Materialparameter werden in der Beleuchtungsgleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in [**glLightModel**](gllightmodel-functions.md)erläutert.

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann [**glMaterialiv**](glmaterialf.md) zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden. Wenn jedoch nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glColorMaterial**](glcolormaterial.md) gegenüber **glMaterialiv** bevorzugt.

Die folgende Funktion ruft Informationen im Zusammenhang mit [**glMaterialiv**](glmaterialf.md)ab:

[**glGetMaterial**](glgetmaterial.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                              |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Gl.h</dt> </dl>         |
| Bibliothek<br/>                  | <dl> <dt>Opengl32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Opengl32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





