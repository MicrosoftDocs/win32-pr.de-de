---
title: glgetmapfv-Funktion (GL. h)
description: Die Funktionen "glgetmapdv", "glgetmapfv" und "glgetmapiv" geben auswertungsparameter zurück. | glgetmapfv-Funktion (GL. h)
ms.assetid: dc93e468-7b76-4b5d-a46c-63920ed05568
keywords:
- glgetmapfv-Funktion OpenGL
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
ms.openlocfilehash: 02129e9637333fb36265ce9f7b631d6cb3377d0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106365035"
---
# <a name="glgetmapfv-function"></a>glgetmapfv-Funktion

Die Funktionen " [**glgetmapdv**](glgetmapdv.md)", " **glgetmapfv**" und " [**glgetmapiv**](glgetmapiv.md) " geben auswertungsparameter zurück.

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

Der symbolische Name einer Karte. Folgende Werte sind zulässig: GL \_ zuordnung1 \_ Color \_ 4, GL \_ zuordnung1 \_ Index, GL \_ zuordnung1 \_ Normal, GL \_ zuordnung1 \_ Texture \_ coord \_ 1, GL \_ zuordnung1 \_ Texture \_ coord \_ 2, GL \_ zuordnung1 \_ Texture \_ coord \_ 3, GL \_ zuordnung1 \_ Textur \_ coord \_ 4, GL \_ zuordnung1 \_ Vertex \_ 3, GL \_ zuordnung1 \_ Vertex \_ 4, GL \_ map2 \_ Color \_ 4, GL \_ map2 \_ Index, GL \_ map2 \_ Normal, GL \_ map2 \_ Texture \_ coord \_ 1, GL \_ map2 \_ Texture \_ coord \_ 2, GL \_ map2 \_ Texture \_ coord \_ 3, GL \_ map2 \_ Texture \_ coord \_ 4, GL \_ map2 \_ Vertex \_ 3 und GL \_ map2 \_ Vertex \_ 4.

</dd> <dt>

*query* 
</dt> <dd>

Gibt an, welcher Parameter zurückgegeben werden soll. Die folgenden symbolischen Namen werden akzeptiert.



| Wert                                                                                                                                             | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GL_COEFF"></span><span id="gl_coeff"></span><dl> <dt>**GL. \_ coeff**</dt> </dl>    | Der *v* -Parameter gibt die Kontrollpunkte für die auswerterfunktion zurück. Eindimensionale Evaluatoren geben *Reihen* folgen Kontrollpunkte zurück, und zweidimensionale Evaluatoren geben *uorder* *x* *Vorder* Steuerungs Punkte zurück. Jeder Kontrollpunkt besteht aus einem, zwei, drei oder vier ganzzahligen Gleit Komma Werten mit einfacher Genauigkeit oder Gleit Komma Werten mit doppelter Genauigkeit, abhängig vom Typ der Auswertung. Zweidimensionale Steuerpunkte werden in der Reihenfolge der Zeilen zurückgegeben, wobei der *uorder* -Index schnell erhöht wird, und der *Vorder* -Index nach jeder Zeile. Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.<br/> |
| <span id="GL_ORDER"></span><span id="gl_order"></span><dl> <dt>**GL- \_ Bestellung**</dt> </dl>    | Der *v* -Parameter gibt die Reihenfolge der evaluatorfunktion zurück. Eindimensionale Evaluatoren geben einen einzelnen Wert zurück, *Order*. Zweidimensionale Evaluatoren geben zwei Werte zurück: *uorder* und *Vorder*.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="GL_DOMAIN"></span><span id="gl_domain"></span><dl> <dt>**GL- \_ Domäne**</dt> </dl> | Der *v* -Parameter gibt die linearen *u* -und *v* -Mapping-Parameter zurück. Eindimensionale Evaluatoren geben zwei Werte zurück, *u* 1 und *u* 2, wie von [**glMap1**](glmap1.md)angegeben. Zweidimensionale Evaluatoren geben gemäß [**glMap2**](glmap2.md)-Angabe vier Werte (*U1*, *U2*, *v1* und *v2*) zurück. Ganzzahlige Werte werden, wenn angefordert, berechnet, indem die internen Gleit Komma Werte auf die nächstgelegenen ganzzahligen Werte gerundet werden.<br/>                                                                                                                                                                                                                                                  |



 

</dd> <dt>

*Ramelow* 
</dt> <dd>

Gibt die angeforderten Daten zurück.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="error-codes"></a>Fehlercodes

Die folgenden Fehlercodes können von der Funktion " [**glgeterror**](glgeterror.md) " abgerufen werden.



| Name                                                                                                  | Bedeutung                                                                                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**GL \_ ungültige Aufzählung. \_**</dt> </dl>      | Das *Ziel* oder die *Abfrage* war kein akzeptierter Wert.<br/>                                                                             |
| <dl> <dt>**\_ungültiger \_ Vorgang**</dt> </dl> | Die Funktion wurde zwischen einem Aufruf von [**glBegin**](glbegin.md) und dem entsprechenden Aufruf von [**glEnd**](glend.md)aufgerufen.<br/> |



## <a name="remarks"></a>Bemerkungen

Die **glgetmap** -Funktion gibt evaluatorparameter zurück. (Die **glMap1** -Funktion und die **glMap2** -Funktion definieren Evaluatoren.) Der *Ziel* Parameter gibt eine Karte an, die *Abfrage* wählt einen bestimmten Parameter aus, und *v* verweist auf den Speicher, in den die Werte zurückgegeben werden.

Die zulässigen Werte für den *Ziel* Parameter werden in [**glMap1**](glmap1.md) und [**glMap2**](glmap2.md)beschrieben.

Wenn ein Fehler generiert wird, wird keine Änderung am Inhalt von *v* vorgenommen.

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
</dt> <dt>

[**glevalcoord**](glevalcoord-functions.md)
</dt> <dt>

[**glMap1**](glmap1.md)
</dt> <dt>

[**glMap2**](glmap2.md)
</dt> </dl>

 

 





