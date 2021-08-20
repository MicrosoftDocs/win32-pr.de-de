---
title: glPixelStoref-Funktion (Gl.h)
description: Legt die Pixelspeichermodi fest. | glPixelStoref-Funktion (Gl.h)
ms.assetid: 8d5055d7-3ea4-40b7-9447-2a005129da58
keywords:
- glPixelStoref-Funktion OpenGL
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
ms.openlocfilehash: 928cf7ccc054a94840e146e0e2ce6a7afdb74f7cde5f59569ec1cf71acbb3dfa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128080"
---
# <a name="glpixelstoref-function"></a>glPixelStoref-Funktion

Legt die Pixelspeichermodi fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelStoref(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Der symbolische Name des festzulegenden Parameters. Sechs der Speicherparameter beeinflussen die Rückgabe von Pixeldaten an den Clientspeicher und sind daher nur für [**glReadPixels-Befehle**](glreadpixels.md) von Bedeutung. Dies sind:



| Storage Parameter                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ PACK \_ SWAP \_ BYTES                                       | True gibt an, dass die Bytereihenfolge für Multibyte-Farbkomponenten, Tiefenkomponenten, Farbindizes oder Schablonenindizes umgekehrt wird. Das heißt, wenn eine 4-Byte-Komponente aus bytes *b* 0 , *b* 1 , *b* 2 , *b* 3 besteht, wird sie im Arbeitsspeicher als *b* 3 , *b* 2 , *b* 1 , *b* 0 gespeichert, wenn GL \_ PACK SWAP BYTES true \_ \_ ist. GL \_ PACK SWAP BYTES hat keine Auswirkungen auf die \_ \_ Speicherreihenfolge von Komponenten innerhalb eines Pixels, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten oder Indizes. Beispielsweise werden die drei Komponenten eines GL \_ RGB-Formatpixels unabhängig vom Wert von GL PACK SWAP BYTES immer mit roter, grüner sekunde und blauer Dritter \_ \_ \_ gespeichert.                                                                                                                                                                                                                                                                                                                                                                                               |
| GL \_ PACK \_ LSB \_ FIRST                                        | True gibt an, dass Bits innerhalb eines Byte von der geringsten bis zur höchsten Bedeutung sortiert werden. Andernfalls ist das erste Bit in jedem Byte das wichtigste. Dieser Parameter ist nur für Bitmapdaten von Bedeutung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| GL \_ PACK \_ ROW \_ LENGTH                                       | Wenn größer als 0 (null) ist, definiert GL \_ PACK ROW LENGTH die Anzahl der Pixel in einer \_ \_ Zeile. Wenn das erste Pixel einer Zeile an Position p im Arbeitsspeicher platziert wird, wird die Position des ersten Pixels der nächsten Zeile abgerufen, indem die Gleichung übersprungen wird, ![ die die Position des ersten Pixels der nächsten Zeile in GL_PACK_ROW_LENGTH anzeigt. ](images/pix01.png) \[ \]Zeilenneuzeilenkomponenten oder -indizes, wobei *n* die Anzahl der Komponenten oder Indizes in einem Pixel ist, *l* die Anzahl der Pixel in einer Zeile (gl \- pack row \- \- length, wenn sie größer als 0 ist, das Width-Argument für die Pixelroutine andernfalls ), *ein* der Wert der Gl \- \- pack-Ausrichtung und *s* die Größe einer einzelnen Komponente in Bytes ist (wenn *ein*  <  *s* ist, dann ist es wie *ein*  =  *s*). Bei 1-Bit-Werten wird die Position der nächsten Zeile abgerufen, indem die Gleichung übersprungen wird, ![ die die Position der nächsten Zeile in GL_PACK_ROW_LENGTH anzeigt.](images/pix02.png)<br/> -Komponenten oder -Indizes. Die *Wortkomponente* in dieser Beschreibung bezieht sich auf die Nichtindexwerte Rot, Grün, Blau, Alpha und Tiefe. Storage Format GL \_ RGB enthält z. B. drei Komponenten pro Pixel: zuerst rot, dann grün und schließlich blau.<br/> |
| GL \_ PACK SKIP PIXELS \_ \_ und <br/> GL \_ PACK \_ SKIP \_ ROWS | Diese Werte werden dem Programmierer zur Vereinfachung bereitgestellt. sie bieten keine Funktionalität, die nicht einfach durch Erhöhen des an [**glReadPixels übergebenen Zeigers**](glreadpixels.md)dupliziert werden kann. Das Festlegen von GL \_ PACK SKIP PIXELS auf \_ \_ *i* entspricht dem Erhöhen des Zeigers um *i n* Komponenten oder Indizes, wobei *n* die Anzahl der Komponenten oder Indizes in jedem Pixel ist. Das Festlegen von GL \_ PACK SKIP ROWS auf \_ \_ *j* entspricht dem Erhöhen des Zeigers um *j k* Komponenten oder Indizes, wobei *k* die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im Abschnitt GL PACK ROW \_ LENGTH \_ \_ berechnet.                                                                                                                                                                                                                                                                                                                                                                                                   |
| GL \_ \_ PACK-AUSRICHTUNG                                         | Gibt die Ausrichtungsanforderungen für den Anfang jeder Pixelzeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byteausrichtung), 2 (Zeilen, die an gerade nummerierten Bytes ausgerichtet sind), 4 (Wortausrichtung) und 8 (Zeilen beginnen bei Doppelwortgrenzen).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Die anderen sechs Speicherparameter beeinflussen, wie Pixeldaten aus dem Clientspeicher gelesen werden. Diese Werte sind für [**glDrawPixels,**](gldrawpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)und [**glPolygonStipple**](glpolygonstipple.md)von bedeutung. Dies sind:



| Storage Parameter                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ UNPACK \_ SWAP \_ BYTES                                         | True gibt an, dass die Bytereihenfolge für Multibyte-Farbkomponenten, Tiefenkomponenten, Farbindizes oder Schablonenindizes umgekehrt wird. Das heißt, wenn eine 4-Byte-Komponente aus den Bytes *b* 0, *b* 1, *b* 2 , *b* 3 besteht, wird sie im Arbeitsspeicher als *b* 3 , *b* 2 , *b* 1 , *b* 0 gespeichert, wenn GL \_ UNPACK \_ SWAP BYTES true \_ ist. GL \_ UNPACK \_ SWAP BYTES hat keine Auswirkungen auf die \_ Speicherreihenfolge von Komponenten innerhalb eines Pixels, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten oder Indizes. Beispielsweise werden die drei Komponenten eines GL \_ RGB-Formatpixels unabhängig vom Wert von GL UNPACK SWAP BYTES immer mit roter erster, grüner und blauer Sekunde \_ \_ \_ gespeichert.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ UNPACK \_ LSB \_ FIRST                                          | True gibt an, dass Bits innerhalb eines Byte von der geringsten bis zur höchsten Bedeutung sortiert werden. Andernfalls ist das erste Bit in jedem Byte das wichtigste. Dies ist nur für Bitmapdaten von Bedeutung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GL \_ UNPACK \_ ROW \_ LENGTH                                         | Wenn größer als 0 (null) ist, definiert GL \_ UNPACK \_ ROW LENGTH die Anzahl der Pixel in einer \_ Zeile. Wenn das erste Pixel einer Zeile an Position p im Arbeitsspeicher platziert wird, wird die Position des ersten Pixels der nächsten Zeile abgerufen, indem die Gleichung übersprungen wird, ![ die die Position des ersten Pixels der nächsten Zeile in GL_UNPACK_ROW_LENGTH anzeigt. ](images/pix01.png) \[ \]Zeilenneuzeilenkomponenten oder -indizes, wobei *n* die Anzahl der Komponenten oder Indizes in einem Pixel ist, *l* die Anzahl der Pixel in einer Zeile (gl \- pack row \- \- length, wenn sie größer als 0 ist, das Width-Argument für die Pixelroutine andernfalls ), *ein* der Wert der Gl \- \- pack-Ausrichtung und *s* die Größe einer einzelnen Komponente in Bytes ist (wenn *ein*  <  *s* ist, dann ist es wie *ein*  =  *s*). Bei 1-Bit-Werten wird die Position der nächsten Zeile abgerufen, indem die Gleichung übersprungen wird, ![ die die Position der nächsten Zeile in GL_UNPACK_ROW_LENGTH anzeigt.](images/pix02.png)<br/> -Komponenten oder -Indizes. Die *Wortkomponente* in dieser Beschreibung bezieht sich auf die Nichtindexwerte Rot, Grün, Blau, Alpha und Tiefe. Storage Format GL \_ RGB enthält z. B. drei Komponenten pro Pixel: zuerst rot, dann grün und schließlich blau.<br/> |
| GL \_ UNPACK \_ SKIP PIXELS \_ und <br/> GL \_ UNPACK \_ SKIP \_ ROWS | Diese Werte werden dem Programmierer zur Vereinfachung bereitgestellt. sie bieten keine Funktionalität, die nicht dupliziert werden kann, indem der an [**glDrawPixels**](gldrawpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)oder [**glPolygonStipple übergebene**](glpolygonstipple.md)Zeiger erhöht wird. Das Festlegen von GL \_ UNPACK \_ SKIP PIXELS auf \_ *i* entspricht dem Erhöhen des Zeigers um *i n* Komponenten oder Indizes, wobei *n* die Anzahl der Komponenten oder Indizes in jedem Pixel ist. Das Festlegen von GL \_ UNPACK \_ SKIP ROWS auf \_ *j* entspricht dem Erhöhen des Zeigers um *j k* Komponenten oder Indizes, wobei *k* die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im Abschnitt GL \_ UNPACK ROW LENGTH \_ \_ berechnet.                                                                                                                                                                                                                                    |
| GL \_ UNPACK \_ ALIGNMENT                                           | Gibt die Ausrichtungsanforderungen für den Anfang jeder Pixelzeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byteausrichtung), 2 (Zeilen, die an gerade nummerierten Bytes ausgerichtet sind), 4 (Wortausrichtung) und 8 (Zeilen beginnen bei Doppelwortgrenzen).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *pname* festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glPixelStore-Funktion** legt Pixelspeichermodi fest, die sich auf den Betrieb nachfolgender [**glDrawPixels**](gldrawpixels.md) und [**glReadPixels**](glreadpixels.md) sowie auf das Entpacken von Polygonstipplemustern (siehe [**glPolygonStipple),**](glpolygonstipple.md)Bitmaps (siehe [**glBitmap**](glbitmap.md)) und Texturmuster (siehe [**glTexImage1D**](glteximage1d.md), [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D)**](gltexsubimage2d.md)auswirken.

Die folgende Tabelle enthält den Typ, den Anfangswert und den Bereich gültiger Werte für jeden Speicherparameter, der mit **glPixelStore** festgelegt werden kann.



| Pname                    | type    | Anfangswert | Gültiger Bereich   |
|--------------------------|---------|---------------|---------------|
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true oder false |
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true oder false |
| GL \_ PACK \_ ROW \_ LENGTH    | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ ROWS     | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ PIXELS   | integer | 0             | \[0,?)        |
| GL \_ \_ PACK-AUSRICHTUNG      | integer | 4             | 1, 2, 4 oder 8 |
| GL \_ UNPACK \_ SWAP \_ BYTES  | Boolean | false         | true oder false |
| GL \_ UNPACK \_ LSB \_ FIRST   | Boolean | false         | true oder false |
| GL \_ UNPACK \_ ROW \_ LENGTH  | integer | 0             | \[0,?)        |
| GL \_ UNPACK \_ SKIP \_ ROWS   | integer | 0             | \[0,?)        |
| GL \_ ENTPACKEN SKIP \_ \_ PIXELS | integer | 0             | \[0,?)        |
| GL \_ ENTPACKEN DER \_ AUSRICHTUNG    | integer | 4             | 1, 2, 4 oder 8 |



 

Die **glPixelStoref-Funktion** kann zum Festlegen eines beliebigen Pixelspeicherparameters verwendet werden. Wenn der Parametertyp boolesch ist und *param* 0,0 ist, ist der Parameter false. Andernfalls wird sie auf TRUE festgelegt. Wenn *pname ein* ganzzahliger Typparameter ist, wird *der Parameter* auf die nächste ganze Zahl gerundet.

Ebenso kann die **glPixelStorei-Funktion** auch verwendet werden, um einen der Pixelspeicherparameter festlegen. Boolesche Parameter werden auf FALSE festgelegt, *wenn param* 0 und andernfalls TRUE ist. Der *Parameter param* wird in einen Gleitkomma konvertiert, bevor er echten Parametern zugewiesen wird.

Die Pixelspeichermodi sind wirksam, wenn [**glDrawPixels,**](gldrawpixels.md) [**glReadPixels,**](glreadpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)oder [**glPolygonStipple**](glpolygonstipple.md) in einer Anzeigeliste platziert werden, um die Interpretation von Speicherdaten zu steuern. Die Pixelspeichermodi, die beim Ausführen einer Anzeigeliste wirksam sind, sind nicht von Bedeutung.

Die folgenden Funktionen rufen Informationen im Zusammenhang mit **glPixelStore ab:**

[**glGet mit**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) Argument GL \_ PACK SWAP \_ \_ BYTES

**glGet** mit dem Argument GL \_ PACK \_ LSB \_ FIRST

**glGet** mit argument GL \_ PACK \_ ROW \_ LENGTH

**glGet** mit Argument GL \_ PACK \_ SKIP \_ ROWS

**glGet mit** Argument GL \_ PACK SKIP \_ \_ PIXELS

**glGet** mit Argument GL \_ PACK \_ ALIGNMENT

**glGet mit** Argument GL \_ UNPACK \_ SWAP \_ BYTES

**glGet** mit dem Argument GL \_ UNPACK \_ LSB \_ FIRST

**glGet mit** dem Argument GL \_ UNPACK \_ ROW \_ LENGTH

**glGet mit** argument GL \_ UNPACK \_ SKIP \_ ROWS

**glGet mit** argument GL \_ UNPACK \_ SKIP \_ PIXELS

**glGet mit** argument GL \_ UNPACK \_ ALIGNMENT

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

[**glBitmap**](glbitmap.md)
</dt> <dt>

[**glDrawPixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glPixelMap**](glpixelmap.md)
</dt> <dt>

[**glPixelTransfer**](glpixeltransfer.md)
</dt> <dt>

[**glPixelZoom**](glpixelzoom.md)
</dt> <dt>

[**glPolygonStipple**](glpolygonstipple.md)
</dt> <dt>

[**glReadPixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





