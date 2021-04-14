---
title: glmaterialfv-Funktion (GL. h)
description: Die glmaterialfv-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: cd357686-4d6f-49fd-a111-308b5485ac21
keywords:
- glmaterialfv-Funktion OpenGL
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
ms.openlocfilehash: b44b200abe0588a657f770902a9a897329e1942a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391504"
---
# <a name="glmaterialfv-function"></a>glmaterialfv-Funktion

Die **glmaterialfv** -Funktion gibt Materialparameter für das Beleuchtungsmodell an.

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

*mit* 
</dt> <dd>

Die Gesichter oder Gesichter, die aktualisiert werden. Muss eines der folgenden sein: GL \_ Front, GL \_ Back, GL \_ Front und GL \_ Back.

</dd> <dt>

*pName* 
</dt> <dd>

Der Materialparameter der Gesichts-oder Gesichter, die aktualisiert werden. Die Parameter, die mit **glmaterialfv** angegeben werden können, und ihre Interpretationen durch die Beleuchtungs Gleichung lauten wie folgt.



| Wert                                                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_AMBIENT"></span><span id="gl_ambient"></span><dl> <dt>**GL- \_ AMBIENT**</dt> </dl>                                       | Der Parameter Parameters enthält vier Gleit Komma Werte, die die Ambiente-RGBA-Reflektion des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige Umgebungs Reflektion für die Vorder-und Hintergrundmaterialien ist (0,2, 0,2, 0,2, 1,0). <br/>    |
| <span id="GL_DIFFUSE"></span><span id="gl_diffuse"></span><dl> <dt>**GL- \_ diffuses**</dt> </dl>                                       | Der Parameter Parameters enthält vier Gleit Komma Werte, die die diffuse RGBA-Reflektion des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige diffuse Reflektion für die Vorder-und Hintergrundmaterialien ist (0,8, 0,8, 0,8, 1,0). <br/>    |
| <span id="GL_SPECULAR"></span><span id="gl_specular"></span><dl> <dt>**GL \_ Glanz**</dt> </dl>                                    | Der Parameter Parameters enthält vier Gleit Komma Werte, die die Glanz Bare RGBA-Reflektion des Materials angeben. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige Glanz Reflektion für die Vorder-und Hintergrundmaterialien lautet (0,0, 0,0, 0,0, 1,0). <br/>  |
| <span id="GL_EMISSION"></span><span id="gl_emission"></span><dl> <dt>**GL \_ -Ausgabe**</dt> </dl>                                    | Der Parameter Parameters enthält vier Gleit Komma Werte, die angeben, dass RGBA die helle Intensität des Materials ausgegeben hat. Ganzzahlige Werte werden linear zugeordnet, sodass der positivste darstellbare Wert 1,0 zugeordnet wird, und der negativere darstellbare Wert ist-1,0. Gleit Komma Werte werden direkt zugeordnet. Keine ganzzahligen oder Gleit Komma Werte werden geklammert. Die standardmäßige Ausgabe Intensität für die Vorder-und Hintergrundmaterialien ist (0,0, 0,0, 0,0, 1,0). <br/> |
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ .**</dt> </dl>                                 | Der Parameter *param* ist ein einzelner ganzzahliger Wert, der den glänzenden RGBA-Exponent des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert. Der standardmäßige Glanz Exponent für die Vorder-und Hintergrundmaterialien ist 0. <br/>                                                                                                                                                                                                      |
| <span id="GL_AMBIENT_AND_DIFFUSE"></span><span id="gl_ambient_and_diffuse"></span><dl> <dt>**GL \_ AMBIENT \_ und \_ diffuse**</dt> </dl> | Äquivalent zum doppelten Aufrufen von [**glmaterial**](glmaterial-functions.md) mit denselben Parameterwerten, einmal mit GL \_ AMBIENT und Once mit GL \_ diffus. <br/>                                                                                                                                                                                                                                                                                                                                   |
| <span id="GL_COLOR_INDEXES"></span><span id="gl_color_indexes"></span><dl> <dt>**GL- \_ Farb \_ Indizes**</dt> </dl>                    | Der Parameter Parameters enthält drei Gleit Komma Werte, die die Farbindizes für Ambient, diffuse und Glanz Beleuchtung angeben. Diese drei Werte und GL \_ -Glanz sind die einzigen materiellen Werte, die von der Farb Index Modus-Beleuchtungs Gleichung verwendet werden. Eine Erläuterung der Farb Index Beleuchtung finden Sie unter [**gllightmodel**](gllightmodel-functions.md) .<br/>                                                                                                                                  |



 

</dd> <dt>

*params* 
</dt> <dd>

Der Wert, auf den der Parameter GL- \_ Glanz festgelegt wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                              | Bedeutung                                                                       |
|---------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>  | Entweder *Face* oder *PName* war kein akzeptierter Wert.<br/>                |
| <dl> <dt>**\_Ungültiger GL- \_ Wert**</dt> </dl> | Ein Glanz Exponent außerhalb des Bereichs von \[ 0, 128 \] wurde angegeben.<br/> |



## <a name="remarks"></a>Bemerkungen

Die Funktion " [**glmaterialfv**](glmaterialf.md) " weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine, die *Front-End-* Gruppe, wird zum Schattieren von Punkten, Linien, Bitmaps und allen Polygonen verwendet (wenn die zweiseitige Beleuchtung deaktiviert ist), oder nur mit Front-End-Polygonen (bei aktivierter zweiseitiger Beleuchtung). Der andere Satz, mit dem *Hintergrund*, wird verwendet, um nur rückwärts gerichtete Polygone zu schattieren, wenn die zweiseitige Beleuchtung aktiviert ist. Ausführliche Informationen zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter " [**gllightmodel**](gllightmodel-functions.md) ".

Die [**glmaterialfv**](glmaterialf.md) -Funktion erfordert drei Argumente. *Mit* dem ersten, dem Vordergrund, wird angegeben, ob die GL \_ -Front-Materialien, die GL \_ -Back-Materialien oder die \_ Vorder \_ -und \_ Hintergrundmaterialien von GL geändert werden. Der zweite Wert, *PName*, gibt an, welche von mehreren Parametern in einem oder beiden Sätzen geändert werden. Der dritte Parameter gibt *an, welcher* Wert dem angegebenen Parameter zugewiesen wird.

Material Parameter werden in der Beleuchtungs Gleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in " [**gllightmodel**](gllightmodel-functions.md)" erläutert.

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann [**glmaterialfv**](glmaterialf.md) zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden. Wenn nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glcolormaterial**](glcolormaterial.md) gegenüber **glmaterialfv** bevorzugt.

Die folgende Funktion Ruft Informationen im Zusammenhang mit [**glmaterialfv**](glmaterialf.md)ab:

[**glgetmaterial**](glgetmaterial.md)

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

[**glcolormaterial**](glcolormaterial.md)
</dt> <dt>

[**gllight**](gllight-functions.md)
</dt> <dt>

[**gllightmodel**](gllightmodel-functions.md)
</dt> </dl>

 

 





