---
title: glColor4us-Funktion (GL. h)
description: Legt die aktuelle Farbe fest. | glColor4us-Funktion (GL. h)
ms.assetid: 800ab5f7-bf42-4df6-8f3f-64df651240bd
keywords:
- glColor4us-Funktion OpenGL
topic_type:
- apiref
api_name:
- glColor4us
api_location:
- opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be59d11c944febe7149c78d0abc7444cd11d146
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363099"
---
# <a name="glcolor4us-function"></a>glColor4us-Funktion

Legt die aktuelle Farbe fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glColor4us(
   GLushort red,
   GLushort green,
   GLushort blue,
   GLushort alpha
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Red* 
</dt> <dd>

Der neue rote Wert für die aktuelle Farbe.

</dd> <dt>

*Grünbuchs* 
</dt> <dd>

Der neue grüne Wert für die aktuelle Farbe.

</dd> <dt>

*blauen* 
</dt> <dd>

Der neue blaue Wert für die aktuelle Farbe.

</dd> <dt>

*alpha* 
</dt> <dd>

Der neue Alpha-Wert für die aktuelle Farbe.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der GL speichert sowohl einen aktuellen einwertigen Farbindex als auch eine aktuelle vier wertige RGBA-Farbe. mit **glcolor** wird eine neue vier wertige RGBA-Farbe festgelegt. **glcolor** hat zwei Hauptvarianten: **glcolor3** und **glcolor4**. **glcolor3** -Varianten geben die neuen roten, grünen und blauen Werte explizit an und legen den aktuellen Alpha-Wert implizit auf 1,0 (volle Intensität) fest. **glcolor4** Varianten geben alle vier Farbkomponenten explizit an.

**glcolor3b**, **glcolor4b**, **glcolor3s**, **glcolor4s**, **glcolor3i** und **glcolor4i** nehmen drei oder vier signierte Byte-, kurzoder lange ganze Zahlen als Argumente an. Wenn v an den Namen angefügt wird, können die Farb Befehle einen Zeiger auf ein Array solcher Werte annehmen.

Aktuelle Farbwerte werden im Gleit Komma Format mit nicht spezifizierten Mantisse-und Exponent-Größen gespeichert. Ganzzahlige Farbkomponenten ohne Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der größte darstellbare Wert 1,0 (volle Intensität) und 0 dem Wert 0,0 (keine Intensität) zugeordnet wird. Ganzzahlige Farbkomponenten mit Vorzeichen werden bei Angabe von Gleit Komma Werten linear zugeordnet, sodass der positivste darstellbare Wert 1,0 und der negativste darstellbare Wert-1,0 zugeordnet wird. (Beachten Sie, dass diese Zuordnung nicht 0 genau in 0,0 konvertiert.) Gleit Komma Werte werden direkt zugeordnet.

Weder Gleit Komma Werte noch ganzzahlige ganzzahlige Werte werden an den Bereich \[ 0, 1, \] vor dem Aktualisieren der aktuellen Farbe gebunden. Farbkomponenten werden jedoch an diesen Bereich gebunden, bevor Sie interpoliert oder in einen Farb Puffer geschrieben werden.

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

[**glgetbooleanv, glgetdoublev, glgetfloatv, glgetintegerv**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md)
</dt> <dt>

[**glindex**](glindexd.md)
</dt> </dl>

 

 





