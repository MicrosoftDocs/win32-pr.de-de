---
title: glColor3iv-Funktion (Gl.h)
description: Legt die aktuelle Farbe aus einem bereits vorhandenen Array von Farbwerten fest. | glColor3iv-Funktion (Gl.h)
ms.assetid: b083fd09-fe92-4afa-bcb7-f36e9eeffbab
keywords:
- glColor3iv-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor3iv
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d47354f812ebcd89b88170d78669309e13843645073d5580ed1aa0b935f5539
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120081880"
---
# <a name="glcolor3iv-function"></a>glColor3iv-Funktion

Legt die aktuelle Farbe aus einem bereits vorhandenen Array von Farbwerten fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColor3iv(
   const GLint *v
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

 

 





