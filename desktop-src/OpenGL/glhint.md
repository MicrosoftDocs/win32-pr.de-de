---
title: glhint-Funktion (GL. h)
description: Die Funktion "glhint" gibt Implementierungs spezifische Hinweise an.
ms.assetid: 6d03e107-321a-45ee-9ce7-25fa9cab32d9
keywords:
- glhint-Funktion OpenGL
topic_type:
- apiref
api_name:
- glHint
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2772c76868c741660486184e5ab51bd193d3667a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103198"
---
# <a name="glhint-function"></a>glhint-Funktion

Die Funktion " **glhint** " gibt Implementierungs spezifische Hinweise an.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glHint(
   GLenum target,
   GLenum mode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Eine symbolische Konstante, die das zu kontrollier Ende Verhalten angibt. Die folgenden symbolischen Konstanten, zusammen mit der vorgeschlagenen Semantik, werden akzeptiert.



| Wert                                                                                                                                                                                                              | Bedeutung                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_FOG_HINT"></span><span id="gl_fog_hint"></span><dl> <dt>**GL- \_ Nebel \_ Hinweis**</dt> </dl>                                                           | Gibt die Genauigkeit der Nebel Berechnung an. Wenn die Berechnung pro Pixel-Nebel von der OpenGL-Implementierung nicht effizient unterstützt wird, kann das Hinweise von GL nicht \_ \_ Care oder GL \_ schnellste zu einer pro-Vertex-Berechnung von Nebeleffekten führen.<br/>                                                                          |
| <span id="GL_LINE_SMOOTH_HINT"></span><span id="gl_line_smooth_hint"></span><dl> <dt>**GL- \_ Linien- \_ Smooth- \_ Hinweis**</dt> </dl>                                  | Gibt die Stichproben Qualität von Zeilen mit Antialiasing an. Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                               |
| <span id="GL_PERSPECTIVE_CORRECTION_HINT"></span><span id="gl_perspective_correction_hint"></span><dl> <dt>**GL \_ Perspective- \_ Korrektur \_ Hinweis**</dt> </dl> | Gibt die Qualität der Farb-und Texturkoordinaten Interpolations an. Wenn die parameterinterpolung von Perspektiven korrigiert nicht effizient von der OpenGL-Implementierung unterstützt wird, kann das Hinweise von GL nicht \_ \_ Care oder GL \_ schnellste zu einer einfachen linearen interpolung von Farben und/oder Texturkoordinaten führen.<br/> |
| <span id="GL_POINT_SMOOTH_HINT"></span><span id="gl_point_smooth_hint"></span><dl> <dt>**GL \_ Point \_ Smooth- \_ Hinweis**</dt> </dl>                               | Gibt die Stichproben Qualität von Antialiasing Punkten an. Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                              |
| <span id="GL_POLYGON_SMOOTH_HINT"></span><span id="gl_polygon_smooth_hint"></span><dl> <dt>**GL- \_ Polygon- \_ Smooth- \_ Hinweis**</dt> </dl>                         | Gibt die Stichproben Qualität von Polygonen mit antialigwerten an. Hinting GL \_ schönste kann dazu führen, dass während der rasterisierung mehr Pixel Fragmente generiert werden, wenn eine größere Filterfunktion angewendet wird.<br/>                                                                                                            |



 

</dd> <dt>

*mode* 
</dt> <dd>

Eine symbolische Konstante, die das gewünschte Verhalten angibt. Die folgenden symbolischen Konstanten werden akzeptiert.



| Wert                                                                                                                                                       | Bedeutung                                                                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <span id="GL_FASTEST"></span><span id="gl_fastest"></span><dl> <dt>**GL \_ schnellste**</dt> </dl>        | Die effizienteste Option sollte ausgewählt werden.<br/>                    |
| <span id="GL_NICEST"></span><span id="gl_nicest"></span><dl> <dt>**GL am \_ schönsten**</dt> </dl>           | Die am besten geeignete Option oder höchste Qualität sollte ausgewählt werden.<br/> |
| <span id="GL_DONT_CARE"></span><span id="gl_dont_care"></span><dl> <dt>**GL ist nicht \_ \_ wichtig**</dt> </dl> | Der Client hat keine bevorzugte Einstellung.<br/>                          |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | der *Ziel* -oder *Modus* war kein akzeptierter Wert.<br/>                                                                              |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn es Raum für die Interpretation gibt, können Sie bestimmte Aspekte des OpenGL-Verhaltens mit Hinweisen steuern. Sie geben einen Hinweis mit zwei Argumenten an. Der *Ziel* Parameter ist eine symbolische Konstante, die das Verhalten angibt, das gesteuert werden soll, und der *Modus* ist eine weitere symbolische Konstante, die das gewünschte Verhalten angibt.

Obwohl die Implementierungsaspekte, die angegeben werden können, wohl definiert sind, hängt die Interpretation der Hinweise von der Implementierung ab.

Die **glhint** -Funktion kann ignoriert werden.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> </dl>

 

 





