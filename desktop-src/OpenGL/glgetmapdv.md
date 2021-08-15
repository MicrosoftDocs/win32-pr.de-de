---
title: glGetMapdv-Funktion (Gl.h)
description: Die Funktionen glGetMapdv, glGetMapfv und glGetMapiv geben Auswertungsparameter zurück. | glGetMapdv-Funktion (Gl.h)
ms.assetid: 3b4fc03b-ada4-4f4a-a234-fa6439f2e5c8
keywords:
- glGetMapdv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glGetMapdv
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1603d87004e9b97e635e5fa6a52efa97c5e760ccd9010aa6f86fc62eb3ee7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118360308"
---
# <a name="glgetmapdv-function"></a>glGetMapdv-Funktion

Die Funktionen **glGetMapdv,** [**glGetMapfv**](glgetmapfv.md)und [**glGetMapiv**](glgetmapiv.md) geben Auswertungsparameter zurück.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glGetMapdv(
   GLenum   target,
   GLenum   query,
   GLdouble *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Ziel* 
</dt> <dd>

Der symbolische Name einer Zuordnung. Folgende Werte werden akzeptiert: GL \_ MAP1 \_ COLOR \_ 4, GL \_ MAP1 \_ INDEX, GL \_ MAP1 \_ NORMAL, GL \_ MAP1 \_ TEXTURE \_ COORD \_ 1, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP1 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP1 \_ VERTEX \_ 3, GL \_ MAP1 \_ VERTEX \_ 4, GL \_ MAP2 COLOR \_ \_ 4, GL \_ MAP2 \_ INDEX, GL \_ MAP2 \_ NORMAL, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 1, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 2, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 3, GL \_ MAP2 TEXTURE \_ \_ COORD \_ 4, GL \_ MAP2 \_ VERTEX \_ 3 UND GL \_ MAP2 \_ VERTEX \_ 4.

</dd> <dt>

*Frage* 
</dt> <dd>

Gibt an, welcher Parameter zurückgegeben werden soll. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL \_ COEFF**</dt> </dl>    | Der *v-Parameter* gibt die Steuerungspunkte für die Auswertungsfunktion zurück. Eindimensionale Auswertungen geben *Kontrollpunkte* für die Reihenfolge zurück, und zweidimensionale Auswertungen geben *uorder* *x* *vorder-Kontrollpunkte* zurück. Jeder Steuerungspunkt besteht je nach Typ der Auswertung aus einem, zwei, drei oder vier ganzzahligen Gleitkommawerten mit einfacher Genauigkeit oder Gleitkommawerten mit doppelter Genauigkeit. Zweidimensionale Kontrollpunkte werden in Zeilen-Hauptreihenfolge zurückgegeben, wodurch der *UORDER-Index* schnell erhöht wird, und der *vordere* Index nach jeder Zeile. Ganzzahlige Werte werden bei Anforderung berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**GL \_ ORDER**</dt> </dl>    | Der *v-Parameter* gibt die Reihenfolge der Auswertungsfunktion zurück. Eindimensionale Auswertungen geben einen einzelnen Wert in *der Reihenfolge* zurück. Zweidimensionale Auswertungen geben zwei Werte zurück: *uorder* und *vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**GL \_ DOMAIN**</dt> </dl> | Der *v-Parameter* gibt die linearen *u-* und v-Zuordnungsparameter zurück.  Eindimensionale Auswertungen geben zwei Werte zurück, *u* 1 und *u* 2, wie durch [**glMap1**](glmap1.md)angegeben. Zweidimensionale Auswertungen geben vier Werte zurück (*u1*, *u2*, *v1* und *v2*), wie von [**glMap2**](glmap2.md)angegeben. Ganzzahlige Werte werden bei Anforderung berechnet, indem die internen Gleitkommawerte auf die nächsten ganzzahligen Werte gerundet werden.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*V* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der [**glGetError-Funktion**](glgeterror.md) abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ INVALID \_ ENUM**</dt> </dl>      | *target* oder *query* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**GL \_ INVALID \_ OPERATION**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Hinweise

Die **glGetMap-Funktion** gibt Auswertungsparameter zurück. (Die Funktionen **glMap1** und **glMap2** definieren Auswertungen.) Der *Zielparameter* gibt eine Zuordnung an, *die Abfrage* wählt einen bestimmten Parameter aus und zeigt *auf* den Speicher, in dem die Werte zurückgegeben werden.

Die zulässigen Werte für den *Zielparameter* werden in [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)beschrieben.

Wenn ein Fehler generiert wird, werden keine Änderungen am Inhalt von *v* vorgenommen.

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

 

 





