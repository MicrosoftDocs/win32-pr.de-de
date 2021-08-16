---
title: glMaterialfv-Funktion (Gl.h)
description: Die funktion glMaterialfv gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
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
ms.openlocfilehash: 05c4d8fc3f1e141f9913fe997da0b9982200f6be77edc5e4ef190970ee2fca87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118358948"
---
# <a name="glmaterialfv-function"></a>glMaterialfv-Funktion

Die **funktion glMaterialfv** gibt Materialparameter für das Beleuchtungsmodell an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMaterialfv(
         GLenum  face,
         GLenum  pname,
   const GLfloat *params
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Gesicht* 
</dt> <dd>

Das oder die Gesichter, die aktualisiert werden. Dies muss einer der folgenden Sein: GL \_ FRONT, GL \_ BACK oder GL FRONT und GL \_ \_ BACK.

</dd> <dt>

*pname* 
</dt> <dd>

Der Materialparameter des oder der Gesichter, die aktualisiert werden. Die Parameter, die mit **glMaterialfv** angegeben werden können, und ihre Interpretationen durch die Beleuchtungsgleichung lauten wie folgt.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL \_ AMBIENT**</dt> </dl>                                       | Der Parameter params enthält vier Gleitkommawerte, die die RGBA-Umgebungsreflektoranz des Materials angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die Standard-Ambient-Reflektor für vordere und hintere Materialien ist (0.2, 0.2, 0.2, 1.0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL \_ DIFFUSE**</dt> </dl>                                       | Der Parameter params enthält vier Gleitkommawerte, die die diffuse RGBA-Reflektoranz des Materials angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die standardmäßige diffuse Reflektoranz für vordere und zurück gerichtete Materialien ist (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ SPECULAR**</dt> </dl>                                    | Der Parameter params enthält vier Gleitkommawerte, die die rgba-Spiegelung des Materials angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die Standardmäßige Glanzreflektor für vordere und hintere Materialien ist (0.0, 0.0, 0.0, 1.0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**\_GL-FEHLER**</dt> </dl>                                    | Der Parameter params enthält vier Gleitkommawerte, die die RGBA-Lichtstärke des Materials angeben. Ganzzahlwerte werden linear zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. Gleitkommawerte werden direkt zugeordnet. Weder ganzzahlige werte noch Gleitkommawerte werden an die Klammern klammern. Die Standardausgabestärke für vordere und zurück gerichtete Materialien ist (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**\_GL-GL-SCHLÄFRIGKEIT**</dt> </dl>                                 | Der *Parameter param* ist ein einzelner ganzzahliger Wert, der den RGBA-Exponenten des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich \[ 0, 128 \] werden akzeptiert. Der Standardspezifikations exponent für front- und back-facing materials ist 0. <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**GL \_ AMBIENT \_ UND \_ DIFFUSE**</dt> </dl> | Entspricht dem [**zweimalen Aufrufen von glMaterial**](glmaterial-functions.md) mit den gleichen Parameterwerten, einmal mit GL \_ AMBIENT und einmal mit GL \_ DIFFUSE. <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**\_ \_ GL-FARBINDIZES**</dt> </dl>                    | Der Parameter params enthält drei Gleitkommawerte, die die Farbindizes für umgebungsbasierte, diffuse und speculare Beleuchtung angeben. Diese drei Werte und GL KERNELINESS sind die einzigen Materialwerte, die von der \_ Farbindexmodus-Beleuchtungsgleichung verwendet werden. Eine Erörterung der Farbindexbeleuchtung finden Sie unter [**glLightModel.**](gllightmodel-functions.md)<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Der Wert, auf den der Parameter \_ GLINESS festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                              | Bedeutung                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>  | Entweder *face* oder *pname* war kein akzeptierter Wert.<br/>                |
| <dl> <dt>**GL \_ UNGÜLTIGER \_ WERT**</dt> </dl> | Ein specular-Exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.<br/> |



## <a name="remarks"></a>Hinweise

Die [**funktion glMaterialfv**](glmaterialf.md) weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine,  die frontseitige Gruppe, wird verwendet, um Punkte, Linien, Bitmaps und alle Polygone (wenn die zweiseitige Beleuchtung deaktiviert ist) oder einfach frontseitige Polygone zu schattigen (wenn die zweiseitige Beleuchtung aktiviert ist). Die andere Gruppe, *die nach* hinten gerichtet ist, wird nur verwendet, um nach hinten gerichtete Polygone zu beschatten, wenn die zweiseitige Beleuchtung aktiviert ist. Details zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter [**glLightModel.**](gllightmodel-functions.md)

Die [**glMaterialfv-Funktion**](glmaterialf.md) verwendet drei Argumente. Die erste, *die Gesichtserkennung,* gibt an, ob die GL FRONT-Materialien, die GL BACK-Materialien oder beide \_ GL FRONT AND \_ \_ \_ \_ BACK-Materialien geändert werden. Der zweite Parameter , *pname,* gibt an, welcher von mehreren Parametern in einer oder beiden Sätzen geändert wird. Der dritte Parameter *( param*) gibt an, welcher Wert dem angegebenen Parameter zugewiesen wird.

Materialparameter werden in der Beleuchtungsgleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in [**glLightModel erläutert.**](gllightmodel-functions.md)

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann [**glMaterialfv**](glmaterialf.md) zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen werden.**](glend.md) Wenn jedoch nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glColorMaterial**](glcolormaterial.md) gegenüber **glMaterialfv bevorzugt.**

Die folgende Funktion ruft Informationen im Zusammenhang mit [**glMaterialfv ab:**](glmaterialf.md)

[**glGetMaterial**](glgetmaterial.md)

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

[**glColorMaterial**](glcolormaterial.md)
</dt> <dt>

[**glLight**](gllight-functions.md)
</dt> <dt>

[**glLightModel**](gllightmodel-functions.md)
</dt> </dl>

 

 





