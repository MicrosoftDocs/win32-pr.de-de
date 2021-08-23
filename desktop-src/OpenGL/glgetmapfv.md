---
title: glGetMapfv-Funktion (Gl.h)
description: Die Funktionen glGetMapdv, glGetMapfv und glGetMapiv geben Auswertungsparameter zurück. | glGetMapfv-Funktion (Gl.h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- glGetMapfv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMapfv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1bedb1b5ff07b7331eb740c46392e80ad324c6cef7f843978d9a5a41edf8da1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119741590"
---
# <a name="glgetmapfv-function"></a>glGetMapfv-Funktion

Die [**Funktionen glGetMapdv,**](glgetmapdv.md) **glGetMapfv** und [**glGetMapiv**](glgetmapiv.md) geben Auswertungsparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetMapfv(
   GLenum  target,
   GLenum  query,
   GLfloat *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Der symbolische Name einer Karte. Folgende Werte sind akzeptiert: GL \_ MAP1 \_ COLOR \_ 4, GL \_ MAP1 \_ INDEX, GL \_ MAP1 \_ NORMAL, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP1 \_ VERTEX \_ 3, GL \_ MAP1 \_ VERTEX \_ 4, GL \_ MAP2 COLOR \_ \_ 4, GL \_ MAP2 \_ INDEX, GL \_ \_ MAP2 NORMAL, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 \_ VERTEX 3 und \_ GL \_ MAP2 \_ VERTEX \_ 4.

</dd> <dt>

*Frage* 
</dt> <dd>

Gibt an, welcher Parameter zurückgibt. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | Der *v-Parameter* gibt die Kontrollpunkte für die Auswertungsfunktion zurück. Eindimensionale Auswertungen geben Steuerungspunkte *für* die Reihenfolge zurück, und zweidimensionale Auswertungen geben *uorder* *x* *vordere Kontrollpunkte* zurück. Jeder Kontrollpunkt besteht je nach Typ der Auswertung aus einem, zwei, drei oder vier ganzen Zahlen, Gleitkommawerten mit einzelner Genauigkeit oder Gleitkommawerten mit doppelter Genauigkeit. Zweidimensionale Kontrollpunkte werden in zeilenweiser Reihenfolge zurückgegeben und erhöhen den *uorder-Index* schnell und den *vorderen* Index nach jeder Zeile. Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**GL \_ ORDER**</dt> </dl>    | Der *v-Parameter* gibt die Reihenfolge der Auswertungsfunktion zurück. Eindimensionale Auswertungen geben einen einzelnen Wert in der Reihenfolge *zurück.* Zweidimensionale Auswertungen geben zwei Werte zurück: *uorder* und *vorder.*<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**GL \_ DOMAIN**</dt> </dl> | Der *v-Parameter* gibt die linearen *u-* und *v-Zuordnungsparameter* zurück. Eindimensionale Auswertungen geben zwei Werte zurück, *u* 1 und *u* 2, wie von [**glMap1 angegeben.**](glmap1.md) Zweidimensionale Auswertungen geben vier Werte zurück (*u1*, *u2*, *v1* und *v2*), wie von [**glMap2 angegeben.**](glmap2.md) Ganzzahlige Werte werden, wenn sie angefordert werden, berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*V* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion abgerufen**](glgeterror.md) werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *query* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**UNGÜLTIGER \_ \_ GL-VORGANG**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd aufgerufen.**](glend.md)<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetMap-Funktion** gibt Auswertungsparameter zurück. (Die **Funktionen glMap1** und **glMap2 definieren** Auswertungen.) Der *Zielparameter* gibt eine Zuordnung *an,* die Abfrage wählt einen bestimmten Parameter aus, und *v* zeigt auf den Speicher, an dem die Werte zurückgegeben werden.

Die zulässigen Werte für *den Zielparameter* werden in [**glMap1 und**](glmap1.md) [**glMap2 beschrieben.**](glmap2.md)

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *v vorgenommen.*

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glEvalCoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





