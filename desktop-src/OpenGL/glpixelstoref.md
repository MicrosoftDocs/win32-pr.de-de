---
title: glpixelstoref-Funktion (GL. h)
description: Legt die Pixel Speicher Modi fest. | glpixelstoref-Funktion (GL. h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- glpixelstoref-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelStoref
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc35613be68bb142b14a7e8278d6e0b89f05d78e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104552957"
---
# <a name="glpixelstoref-function"></a>glpixelstoref-Funktion

Legt die Pixel Speicher Modi fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Der symbolische Name des festzulegenden Parameters. Sechs der Speicher Parameter beeinflussen, wie Pixeldaten an den Client Speicher zurückgegeben werden, und sind daher nur für [**glread Pixels**](glreadpixels.md) -Befehle von Bedeutung. Dies sind:



| Storage-Parameter                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auslagerungs Bytes von GL \_ Pack \_ \_                                       | True gibt an, dass die Byte Reihenfolge für multibytefarbkomponenten, tiefen Komponenten, Farbindizes oder Schablonen Indizes umgekehrt wird. Das heißt, wenn eine 4-Byte-Komponente aus den Bytes *b* 0, *b* 1, *b* 2, *b* 3 besteht, wird Sie im Arbeitsspeicher als *b* 3, *b* 2, *b* 1, *b* 0 gespeichert, wenn die Auslagerungs Bytes von GL Pack den Wert \_ true haben \_ \_ . Die Auslagerungs \_ \_ Bytes von GL Pack wirken sich \_ nicht auf die Speicher Reihenfolge von Komponenten innerhalb eines Pixels aus, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten oder Indizes. So werden z. b. die drei Komponenten eines Formats des PS \_ RGB-Formats immer mit "Red First", "Green Second" und "Blue Third" gespeichert, unabhängig vom Wert der Auslagerungs Bytes des GL- \_ Pakets \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                               |
| \_zuerst GL Pack- \_ lsb \_                                        | True gibt an, dass Bits innerhalb eines Bytes von der geringsten Bedeutung bis zu den wichtigsten Zeichen geordnet sind. Andernfalls ist das erste Bit in jedem Byte das wichtigste. Dieser Parameter ist nur für Bitmapdaten wichtig.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Länge der GL- \_ Paket \_ Zeile \_                                       | Wenn der Wert größer als 0 (null) ist, wird \_ \_ \_ die Anzahl der Pixel in einer Zeile mit der Zeilenlänge von GL Wenn sich das erste Pixel einer Zeile an Position p im Speicher befindet, wird der Speicherort des ersten Pixels der nächsten Zeile durch übersprungen der Gleichung abgerufen, ![ die den Speicherort des ersten Pixels der nächsten Zeile in GL_PACK_ROW_LENGTH anzeigt. ](images/pix01.png) \[ neueinzeilige \] Komponenten oder Indizes, wobei *n* die Anzahl der Komponenten oder Indizes in einem Pixel ist, *l* ist die Anzahl der Pixel in einer Zeile (bei einem \- \- \- Wert größer als 0 (null), das width-Argument der Pixel Routine andernfalls), *a* ist der Wert der \- GL \- -Paket Ausrichtung, und *s* ist die Größe (in Bytes) einer einzelnen Komponente (wenn *ein*  <  *s*-Wert ist, dann ist Sie so, als ob *ein*  =  *s*). im Fall von 1-Bit-Werten wird der Speicherort der nächsten Zeile durch übersprungen der Gleichung abgerufen, ![ die den Speicherort der nächsten Zeile in GL_PACK_ROW_LENGTH anzeigt.](images/pix02.png)<br/> Komponenten oder Indizes. Die Word- *Komponente* in dieser Beschreibung verweist auf die nicht-Index-Werte rot, grün, blau, Alpha und Tiefe. Das Speicherformat "GL RGB" hat z. b. \_ drei Komponenten pro Pixel: zuerst rot, dann grün und schließlich blau.<br/> |
| GL. über \_ \_ springen von \_ Pixeln und <br/> GL- \_ Paket, \_ Zeilen überspringen \_ | Diese Werte werden dem Programmierer als praktische Hilfe bereitgestellt. Sie stellen keine Funktionen bereit, die nicht dupliziert werden können, indem Sie den an [**glread Pixel**](glreadpixels.md)übergebenen Zeiger inkrementieren. Das Festlegen \_ von GL- \_ \_ Überspringen von 1 bis *i* ist äquivalent zum Inkrementieren des Zeigers durch *i n* Komponenten oder Indizes, wobei *n* die Anzahl der Komponenten oder Indizes in jedem Pixel ist. Das Festlegen \_ von GL Pack \_ zum Überspringen \_ von Zeilen an *j* entspricht dem Inkrementieren des Zeigers durch *j k* -Komponenten oder-Indizes, wobei " *k* " die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im Abschnitt "GL \_ \_ . Row length" berechnet \_ .                                                                                                                                                                                                                                                                                                                                                                                                   |
| GL- \_ Paket \_ Ausrichtung                                         | Gibt die Ausrichtungs Anforderungen für den Start jeder Pixel Zeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byte-Ausrichtung), 2 (Zeilen ausgerichtet auf gleichmäßig nummerierte Bytes), 4 (Wort Ausrichtung) und 8 (Zeilen werden an doppelten Wortgrenzen gestartet).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Die anderen sechs Speicher Parameter beeinflussen, wie Pixeldaten aus dem Client Speicher gelesen werden. Diese Werte sind wichtig für [**gldrawpixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glbitmap**](glbitmap.md)und [**glpolygonstippel**](glpolygonstipple.md). Dies sind:



| Storage-Parameter                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Auslagerungs Bytes von GL \_ Entpacken \_ \_                                         | True gibt an, dass die Byte Reihenfolge für multibytefarbkomponenten, tiefen Komponenten, Farbindizes oder Schablonen Indizes umgekehrt wird. Das heißt, wenn eine 4-Byte-Komponente aus den Bytes *b* 0, *b* 1, *b* 2, *b* 3 besteht, wird Sie im Arbeitsspeicher als *b* 3, *b* 2, *b* 1, *b* 0 gespeichert, wenn die Auslagerungs Bytes von GL \_ Entpack den Wert true haben \_ \_ . Die Auslagerungs \_ Bytes von GL Entpack \_ wirken sich \_ nicht auf die Speicher Reihenfolge von Komponenten innerhalb eines Pixels aus, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten oder Indizes. So werden z. b. die drei Komponenten eines Formats des PS \_ RGB-Formats immer mit der roten ersten, grünen Sekunde und blauen dritten gespeichert, unabhängig vom Wert der Auslagerungs Bytes von GL \_ Entpack \_ \_ .                                                                                                                                                                                                                                                                                                                                                                                           |
| \_zuerst GL Entpacken von \_ lsb \_                                          | True gibt an, dass Bits innerhalb eines Bytes von der geringsten Bedeutung bis zu den wichtigsten Zeichen geordnet sind. Andernfalls ist das erste Bit in jedem Byte das wichtigste. Dies ist nur für Bitmapdaten von Bedeutung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| \_ \_ Zeilenlänge von GL entpacken \_                                         | Wenn der Wert größer als 0 (null) ist, wird \_ \_ \_ die Anzahl der Pixel in einer Zeile mit der Zeilenlänge von GL entpackt Wenn sich das erste Pixel einer Zeile an Position p im Speicher befindet, wird der Speicherort des ersten Pixels der nächsten Zeile durch übersprungen der Gleichung abgerufen, ![ die den Speicherort des ersten Pixels der nächsten Zeile in GL_UNPACK_ROW_LENGTH anzeigt. ](images/pix01.png) \[ neueinzeilige \] Komponenten oder Indizes, wobei *n* die Anzahl der Komponenten oder Indizes in einem Pixel ist, *l* ist die Anzahl der Pixel in einer Zeile (bei einem \- \- \- Wert größer als 0 (null), das width-Argument der Pixel Routine andernfalls), *a* ist der Wert der \- GL \- -Paket Ausrichtung, und *s* ist die Größe (in Bytes) einer einzelnen Komponente (wenn *ein*  <  *s*-Wert ist, dann ist Sie so, als ob *ein*  =  *s*). im Fall von 1-Bit-Werten wird der Speicherort der nächsten Zeile durch übersprungen der Gleichung abgerufen, ![ die den Speicherort der nächsten Zeile in GL_UNPACK_ROW_LENGTH anzeigt.](images/pix02.png)<br/> Komponenten oder Indizes. Die Word- *Komponente* in dieser Beschreibung verweist auf die nicht-Index-Werte rot, grün, blau, Alpha und Tiefe. Das Speicherformat "GL RGB" hat z. b. \_ drei Komponenten pro Pixel: zuerst rot, dann grün und schließlich blau.<br/> |
| GL \_ entpackt \_ die \_ Pixel und <br/> GL \_ Entpacken \_ von \_ Zeilen überspringen | Diese Werte werden dem Programmierer als praktische Hilfe bereitgestellt. Sie stellen keine Funktionen bereit, die nicht dupliziert werden können, indem Sie den Zeiger erhöhen, der an [**gldrawpixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glbitmap**](glbitmap.md)oder [**glpolygonstiple**](glpolygonstipple.md)übergeben wird. Das Festlegen \_ von "GL Unpack- \_ überspringen" \_ auf " *i* " entspricht dem Inkrementieren des Zeigers durch *i n* Komponenten oder Indizes, wobei " *n* " die Anzahl der Komponenten oder Indizes in jedem Pixel ist. Das Festlegen \_ von GL Unpack \_ zum Überspringen \_ von Zeilen an *j* entspricht dem Inkrementieren des Zeigers durch *j k* -Komponenten oder-Indizes, wobei " *k* " die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im Abschnitt "GL \_ unpack- \_ Zeilenlänge" berechnet \_ .                                                                                                                                                                                                                                    |
| Ausrichtung des GL- \_ entpakets \_                                           | Gibt die Ausrichtungs Anforderungen für den Start jeder Pixel Zeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byte-Ausrichtung), 2 (Zeilen ausgerichtet auf gleichmäßig nummerierte Bytes), 4 (Wort Ausrichtung) und 8 (Zeilen werden an doppelten Wortgrenzen gestartet).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *PName* festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit der **glpixelstore** -Funktion werden Pixel Speicher Modi festgelegt, die sich auf den Vorgang der nachfolgenden [**gldrawpixels**](gldrawpixels.md) und [**glread Pixel**](glreadpixels.md) auswirken, sowie das Entpacken von Polygon-stippingmustern (siehe [**glpolygonstippel**](glpolygonstipple.md)), Bitmaps (siehe [**glbitmap**](glbitmap.md)) und Textur Muster (siehe [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md)).

In der folgenden Tabelle sind der Typ, der Anfangswert und der Bereich gültiger Werte für jeden der Speicher Parameter angegeben, die mit **glpixelstore** festgelegt werden können.



| PName                    | type    | Anfangswert | Gültiger Bereich   |
|--------------------------|---------|---------------|---------------|
| Auslagerungs Bytes von GL \_ Pack \_ \_    | Boolean | false         | true oder false |
| Auslagerungs Bytes von GL \_ Pack \_ \_    | Boolean | false         | true oder false |
| Länge der GL- \_ Paket \_ Zeile \_    | integer | 0             | \[0,?)        |
| GL- \_ Paket, \_ Zeilen überspringen \_     | integer | 0             | \[0,?)        |
| GL. über \_ \_ springen von \_ Pixeln   | integer | 0             | \[0,?)        |
| GL- \_ Paket \_ Ausrichtung      | integer | 4             | 1, 2, 4 oder 8 |
| Auslagerungs Bytes von GL \_ Entpacken \_ \_  | Boolean | false         | true oder false |
| \_zuerst GL Entpacken von \_ lsb \_   | Boolean | false         | true oder false |
| \_ \_ Zeilenlänge von GL entpacken \_  | integer | 0             | \[0,?)        |
| GL \_ Entpacken \_ von \_ Zeilen überspringen   | integer | 0             | \[0,?)        |
| Entpacken von GL- \_ Entpacken \_ \_ | integer | 0             | \[0,?)        |
| Ausrichtung des GL- \_ entpakets \_    | integer | 4             | 1, 2, 4 oder 8 |



 

Die **glpixelstoref** -Funktion kann verwendet werden, um einen beliebigen Pixel Speicher Parameter festzulegen. Wenn der Parametertyp Boolean ist, und wenn *param* 0,0 ist, dann ist der-Parameter false. Andernfalls wird Sie auf "true" festgelegt. Wenn " *PName* " ein ganzzahliger Typparameter ist, wird *param* auf die nächste ganze Zahl gerundet.

Ebenso kann die **glpixelstorei** -Funktion auch verwendet werden, um beliebige Pixel Speicher Parameter festzulegen. Boolesche Parameter werden auf false festgelegt, wenn *param* den Wert 0 hat, andernfalls true. Der Parameter *param* wird in den Gleit Komma Wert konvertiert, bevor er den Real-Wert-Parametern zugewiesen wird.

Die Pixel Speicher Modi, die in Kraft treten, wenn " [**gldrawpixels**](gldrawpixels.md)", " [**glread Pixels**](glreadpixels.md)", " [**glTexImage1D**](glteximage1d.md)", " [**glTexImage2D**](glteximage2d.md)", " [**glbitmap**](glbitmap.md)" oder " [**glpolygonstipple**](glpolygonstipple.md) " in einer Anzeigeliste platziert werden, steuern die Interpretation Die Pixel Speicher Modi, die beim Ausführen einer Anzeigeliste wirksam sind, sind nicht signifikant.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpixelstore** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL \_ Pack \_ Swap \_ Bytes

**glget** mit dem Argument GL \_ Pack \_ lsb \_ First

**glget** mit Argument, GL \_ Pack, \_ Zeilen \_ Länge

**glget** mit dem Argument \_ GL \_ Pack \_ Zeilen überspringen

**glget** mit dem Argument GL \_ Pack \_ Skip \_ Pixels

**glget** mit der "Argument GL Pack"- \_ \_ Ausrichtung

**glget** mit dem Argument GL Entpack-Auslagerungs \_ \_ \_ Bytes

**glget** mit dem Argument GL \_ Entpack \_ lsb \_ First

**glget** mit Argument GL \_ Entpacken der \_ Zeilen \_ Länge

**glget** mit dem Argument GL \_ Entpacken von \_ Zeilen überspringen \_

**glget** mit dem Argument GL \_ unpack \_ Skip \_ Pixels

**glget** mit Argument GL \_ Entpacken der \_ Ausrichtung

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

[**glbitmap**](glbitmap.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glpixelmap**](glpixelmap.md)
</dt> <dt>

[**glpixeltransfer**](glpixeltransfer.md)
</dt> <dt>

[**glpixelzoom**](glpixelzoom.md)
</dt> <dt>

[**glpolygonstippel**](glpolygonstipple.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





