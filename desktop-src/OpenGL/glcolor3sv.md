---
title: glColor3sv-Funktion (Gl.h)
description: Legt die aktuelle Farbe aus einem bereits vorhandenen Array von Farbwerten fest. | glColor3sv-Funktion (Gl.h)
ms.assetid: b1be5f7b-4c5f-4d4e-8898-3621dc7a503f
keywords:
- glColor3sv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor3sv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cd76121885dfe5dba3bdb794caa86bb6d539e2af1638208ae0ec374100630a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119061868"
---
# <a name="glcolor3sv-function"></a>glColor3sv-Funktion

Legt die aktuelle Farbe aus einem bereits vorhandenen Array von Farbwerten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColor3sv(
   const GLshort *v
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*V* 
</dt> <dd>

Ein Zeiger auf ein Array, das rote, grüne und blaue Werte enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vierwertige RGBA-Farbe. **glcolor** legt eine neue vierwertige RGBA-Farbe fest. **glcolor** verfügt über zwei Hauptvarianten: **glcolor3** und **glcolor4**. **Glcolor3-Varianten** geben explizit neue Werte für Rot, Grün und Blau an und legen den aktuellen Alphawert implizit auf 1,0 (vollständige Intensität) fest. **Glcolor4-Varianten** geben alle vier Farbkomponenten explizit an.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** verwenden drei oder vier byte-, short- oder long-Ganzzahlen mit Vorzeichen als Argumente. Wenn v an den Namen angefügt wird, können die Farbbefehle einen Zeiger auf ein Array solcher Werte annehmen.

Aktuelle Farbwerte werden im Gleitkommaformat mit nicht angegebenen Mantisse- und Exponentengrößen gespeichert. Ganzzahlige Farbkomponenten ohne Vorzeichen werden, sofern angegeben, linear Gleitkommawerten zugeordnet, sodass der größte darstellbare Wert 1,0 (vollständige Intensität) und 0 0,0 (Null-Intensität) zugeordnet wird. Ganzzahlige Farbkomponenten mit Vorzeichen werden, sofern angegeben, linear Gleitkommawerten zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. (Beachten Sie, dass diese Zuordnung 0 nicht genau in 0,0 konvertiert.) Gleitkommawerte werden direkt zugeordnet.

Weder Gleitkomma- noch ganzzahlige Werte mit Vorzeichen werden an den Bereich \[ 0,1 klammern, \] bevor die aktuelle Farbe aktualisiert wird. Farbkomponenten werden jedoch an diesen Bereich klammert, bevor sie interpoliert oder in einen Farbpuffer geschrieben werden.

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

[**glBegin**](glbegin.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





