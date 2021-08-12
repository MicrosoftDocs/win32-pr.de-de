---
title: glColor3ui-Funktion (Gl.h)
description: Legt die aktuelle Farbe fest. | glColor3ui-Funktion (Gl.h)
ms.assetid: 4a04ad4d-91a8-4d70-93e5-9c8f4ec4d9d2
keywords:
- glColor3ui-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor3ui
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 062ec8fbbcb135c28c3bb7454ad3ca2782c7d60068b9da82dcd980cf9cfb20a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118617412"
---
# <a name="glcolor3ui-function"></a>glColor3ui-Funktion

Legt die aktuelle Farbe fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColor3ui(
   GLuint red,
   GLuint green,
   GLuint blue
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Rot* 
</dt> <dd>

Der neue rote Wert für die aktuelle Farbe.

</dd> <dt>

*Grün* 
</dt> <dd>

Der neue grüne Wert für die aktuelle Farbe.

</dd> <dt>

*Blau* 
</dt> <dd>

Der neue blaue Wert für die aktuelle Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vierwertige RGBA-Farbe. **glcolor** legt eine neue vierwertige RGBA-Farbe fest. **glcolor** verfügt über zwei Hauptvarianten: **glcolor3** und **glcolor4**. **Glcolor3-Varianten** geben neue rote, grüne und blaue Werte explizit an und legen den aktuellen Alphawert implizit auf 1,0 (volle Intensität) fest. **glcolor4-Varianten** geben alle vier Farbkomponenten explizit an.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** nehmen drei oder vier ganze Zahlen mit Vorzeichen, kurze oder lange Ganze Zahlen als Argumente an. Wenn v an den Namen angefügt wird, können die Farbbefehle einen Zeiger auf ein Array solcher Werte verwenden.

Aktuelle Farbwerte werden im Gleitkommaformat mit nicht angegebenen Mantisse- und Exponentengrößen gespeichert. Ganzzahlige Farbkomponenten ohne Vorzeichen werden, wenn angegeben, linear Gleitkommawerten zugeordnet, damit der größte darstellbare Wert 1,0 (volle Intensität) und 0 0 (Intensität 0) zugeordnet wird. Ganzzahlige Farbkomponenten mit Vorzeichen werden, wenn angegeben, linear Gleitkommawerten zugeordnet, damit der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert -1,0 zugeordnet wird. (Beachten Sie, dass diese Zuordnung 0 nicht genau in 0,0 konvertiert.) Gleitkommawerte werden direkt zugeordnet.

Weder Gleitkommawerte noch ganzzahlige Werte mit Vorzeichen werden an den Bereich \[ 0,1 klammert, \] bevor die aktuelle Farbe aktualisiert wird. Farbkomponenten werden jedoch an diesen Bereich klammert, bevor sie interpoliert oder in einen Farbpuffer geschrieben werden.

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

[**glGetBooleanv, glGetDoublev, glGetFloatv, glGetIntegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glIndex**](glindexd.md)
</dt> </dl>

 

 





