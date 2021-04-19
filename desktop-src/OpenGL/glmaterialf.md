---
title: glmaterialf-Funktion (GL. h)
description: Die glmaterialf-Funktion gibt Materialparameter für das Beleuchtungsmodell an.
ms.assetid: c6d183c4-2d1f-4fb9-b24f-c132ebfc708d
keywords:
- glmaterialf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glMaterialf
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c77cb1be5595f4a872988bbc6480d4cd6f65aae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342483"
---
# <a name="glmaterialf-function"></a>glmaterialf-Funktion

Die **glmaterialf** -Funktion gibt Materialparameter für das Beleuchtungsmodell an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glMaterialf(
   GLenum  face,
   GLenum  pname,
   GLfloat param
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

Der einwertige Materialparameter der Gesichts-oder Gesichter, die aktualisiert werden. Muss ein GL- \_ Glanz sein.



| Wert                                                                                                                                                      | Bedeutung                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_SHININESS"></span><span id="gl_shininess"></span><dl> <dt>**GL \_ .**</dt> </dl> | Der Parameter *param* ist ein einzelner Gleit Komma Wert, der den glänzenden RGBA-Exponent des Materials angibt. Ganzzahlige Werte werden direkt zugeordnet. Nur Werte im Bereich von \[ 0, 128 \] werden akzeptiert. Der standardmäßige Glanz Exponent für die Vorder-und Hintergrundmaterialien ist 0. <br/> |



 

</dd> <dt>

*param* 
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

Die Funktion " **glmaterialf** " weist Materialparametern Werte zu. Es gibt zwei übereinstimmende Sätze von Materialparametern. Eine, die *Front-End-* Gruppe, wird zum Schattieren von Punkten, Linien, Bitmaps und allen Polygonen verwendet (wenn die zweiseitige Beleuchtung deaktiviert ist), oder nur mit Front-End-Polygonen (bei aktivierter zweiseitiger Beleuchtung). Der andere Satz, mit dem *Hintergrund*, wird verwendet, um nur rückwärts gerichtete Polygone zu schattieren, wenn die zweiseitige Beleuchtung aktiviert ist. Ausführliche Informationen zu einseitigen und zweiseitigen Beleuchtungsberechnungen finden Sie unter " [**gllightmodel**](gllightmodel-functions.md) ".

Die **glmaterialf** -Funktion erfordert drei Argumente. *Mit* dem ersten, dem Vordergrund, wird angegeben, ob die GL \_ -Front-Materialien, die GL \_ -Back-Materialien oder die \_ Vorder \_ -und \_ Hintergrundmaterialien von GL geändert werden. Der zweite Wert, *PName*, gibt an, welche von mehreren Parametern in einem oder beiden Sätzen geändert werden. Der dritte Parameter gibt *an, welcher* Wert dem angegebenen Parameter zugewiesen wird.

Material Parameter werden in der Beleuchtungs Gleichung verwendet, die optional auf jeden Scheitelpunkt angewendet wird. Die Gleichung wird in " [**gllightmodel**](gllightmodel-functions.md)" erläutert.

Die Materialparameter können jederzeit aktualisiert werden. Insbesondere kann **glmaterialf** zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen werden. Wenn nur ein einzelner Materialparameter pro Scheitelpunkt geändert werden soll, wird [**glcolormaterial**](glcolormaterial.md) gegenüber **glmaterialf** bevorzugt.

Die folgende Funktion Ruft Informationen im Zusammenhang mit **glmaterialf** ab:

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

 

 





