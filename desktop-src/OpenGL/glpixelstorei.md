---
title: glPixelStorei-Funktion (Gl.h)
description: Legt Pixelspeichermodi fest. | glPixelStorei-Funktion (Gl.h)
ms.assetid: 1e1e94e9-aabe-4923-a0a9-f1c041a925ba
keywords:
- glPixelStorei-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelStorei
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d8658db575bbc58cd7aa1170612895f7f895ccc22f11afdfdb99be90db44fa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118938183"
---
# <a name="glpixelstorei-function"></a>glPixelStorei-Funktion

Legt Pixelspeichermodi fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelStorei(
   GLenum pname,
   GLint  param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pname* 
</dt> <dd>

Der symbolische Name des parameters, der festgelegt werden soll. Sechs der Speicherparameter beeinflussen, wie Pixeldaten an den Clientspeicher zurückgegeben werden, und sind daher nur für [**glReadPixels-Befehle**](glreadpixels.md) von Bedeutung. Sie lauten wie folgt.



| Storage Parameter                                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ PACK \_ SWAP \_ BYTES                                       | True gibt an, dass die Byte reihenfolge für Multibyte-Farbkomponenten, Tiefenkomponenten, Farbindizes oder Schablonenindizes umgekehrt wird. Das heißt, wenn eine Vier-Byte-Komponente aus den Bytes *b* 0, *b* 1, *b* 2, *b* 3 besteht, wird sie im Arbeitsspeicher als *b* 3, *b* 2, *b* 1 , *b* 0 gespeichert, wenn GL PACK SWAP BYTES true \_ \_ \_ ist. GL PACK SWAP BYTES hat keine Auswirkungen auf die Speicher reihenfolge der Komponenten innerhalb eines Pixels, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten \_ \_ oder \_ Indizes. Beispielsweise werden die drei Komponenten eines GL-RGB-Formatpixels immer mit Rot zuerst, grüne Sekunde und blauem Dritten gespeichert, unabhängig vom Wert von \_ GL \_ PACK SWAP \_ \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                               |
| GL \_ PACK \_ LSB \_ FIRST                                        | True gibt an, dass Bits innerhalb eines Byte von der geringsten bedeutungsreich bis zur signifikantesten geordnet werden. Andernfalls ist das erste Bit in jedem Byte das wichtigste Bit. Dieser Parameter ist nur für Bitmapdaten von Bedeutung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| ZEILENLÄNGE \_ DES GL \_ \_ PACK-PAKETS                                       | Wenn der Wert größer als 0 (null) ist, definiert GL \_ PACK ROW LENGTH die Anzahl der Pixel in einer \_ \_ Zeile. Wenn das erste Pixel einer Zeile an der Position p im Arbeitsspeicher platziert wird, wird die Position des ersten Pixels der nächsten Zeile ermittelt, indem die Gleichung übersprungen wird, die die Position des ersten Pixels der nächsten Zeile ![ in GL_PACK_ROW_LENGTH. ](images/pix01.png) \[ Zeilenzeilenkomponenten oder -indizes, wobei n die Anzahl der Komponenten oder Indizes in einem Pixel ist, l die Anzahl von Pixeln in einer Zeile (Zeilenlänge von gl pack, wenn sie größer als 0 (null) ist, andernfalls das Breitenargument für die Pixelroutine), ist ein der Wert der Gl Pack-Ausrichtung, und s ist die Größe einer einzelnen Komponente in Bytes \]   \- \- \-  \- \-  (wenn   <     =  ein s ist, dann ist es so, als wäre ein s ). bei 1-Bit-Werten wird die Position der nächsten Zeile durch Überspringen der Gleichung ermittelt, die die Position der nächsten Zeile ![ in der GL_PACK_ROW_LENGTH.](images/pix02.png)<br/> Komponenten oder Indizes. Die *Wortkomponente* in dieser Beschreibung bezieht sich auf die Nichtindexwerte Rot, Grün, Blau, Alpha und Tiefe. Storage GL RGB hat beispielsweise drei Komponenten pro Pixel: zuerst rot, dann grün \_ und schließlich blau.<br/> |
| GL \_ PACK SKIP PIXELS \_ \_ und <br/> GL \_ PACK \_ SKIP \_ ROWS | Diese Werte werden dem Programmierer zur Vereinfachung zur Verfügung gestellt. sie bieten keine Funktionalität, die nicht dupliziert werden kann, indem der an glReadPixel übergebene Zeiger [**inkrementiert wird.**](glreadpixels.md) Das Festlegen von GL PACK SKIP PIXELS auf i entspricht dem Erhöhen des Zeigers um i n Komponenten oder Indizes, wobei n die Anzahl der Komponenten oder Indizes in jedem \_ \_ Pixel \_ ist.    Das Festlegen von GL PACK SKIP ROWS auf j entspricht dem Erhöhen des Zeigers um j k Komponenten oder Indizes, wobei k die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im \_ Abschnitt GL PACK ROW LENGTH \_ \_    \_ \_ \_ berechnet.                                                                                                                                                                                                                                                                                                                                                                                                   |
| GL \_ PACK \_ ALIGNMENT                                         | Gibt die Ausrichtungsanforderungen für den Anfang jeder Pixelzeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byteausrichtung), 2 (Zeilen, die an gleichmäßig nummerierten Bytes ausgerichtet sind), 4 (Wortausrichtung) und 8 (Zeilen beginnen an Doppeltwortgrenzen).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |



 

Die anderen sechs Speicherparameter beeinflussen, wie Pixeldaten aus dem Clientspeicher gelesen werden. Diese Werte sind für [**glDrawPixels,**](gldrawpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)und [**glPolygonStipple von bedeutung.**](glpolygonstipple.md) Dies sind:



| Storage Parameter                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GL \_ UNPACK \_ SWAP \_ BYTES                                         | True gibt an, dass die Byte reihenfolge für Multibyte-Farbkomponenten, Tiefenkomponenten, Farbindizes oder Schablonenindizes umgekehrt wird. Das heißt, wenn eine Vier-Byte-Komponente aus Bytes *b* 0, *b* 1, *b* 2, *b* 3 besteht, wird sie im Arbeitsspeicher als *b* 3, *b* 2, *b* 1, *b* 0 gespeichert, wenn GL \_ UNPACK SWAP \_ BYTES true \_ ist. GL UNPACK SWAP BYTES hat keine Auswirkungen auf die Speicher reihenfolge der Komponenten innerhalb eines Pixels, sondern nur auf die Reihenfolge der Bytes innerhalb von Komponenten \_ \_ oder \_ Indizes. Beispielsweise werden die drei Komponenten eines GL RGB-Formatpixels immer mit Rot zuerst, grüne Sekunde und blauem dritten Platz gespeichert, unabhängig vom Wert von \_ GL \_ UNPACK \_ SWAP \_ BYTES.                                                                                                                                                                                                                                                                                                                                                                                           |
| GL \_ UNPACK \_ LSB \_ FIRST                                          | True gibt an, dass Bits innerhalb eines Byte von der geringsten bedeutungsreich bis zur signifikantesten geordnet werden. Andernfalls ist das erste Bit in jedem Byte das wichtigste Bit. Dies ist nur für Bitmapdaten von Bedeutung.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| GL \_ UNPACK \_ ROW \_ LENGTH                                         | Wenn der Wert größer als 0 (null) ist, definiert GL \_ UNPACK \_ ROW LENGTH die Anzahl der Pixel in einer \_ Zeile. Wenn das erste Pixel einer Zeile an der Position p im Arbeitsspeicher platziert wird, wird die Position des ersten Pixels der nächsten Zeile durch Überspringen der Gleichung ermittelt, die die Position des ersten Pixels der nächsten Zeile ![ in GL_UNPACK_ROW_LENGTH. ](images/pix01.png) \[ Zeilenzeilenkomponenten oder -indizes, wobei n die Anzahl der Komponenten oder Indizes in einem Pixel ist, l die Anzahl von Pixeln in einer Zeile (Zeilenlänge von gl pack, wenn sie größer als 0 (null) ist, andernfalls das Breitenargument für die Pixelroutine), ist ein der Wert der Gl Pack-Ausrichtung, und s ist die Größe einer einzelnen Komponente in Bytes \]   \- \- \-  \- \-  (wenn   <     =  ein s ist, dann ist es so, als wäre ein s ). bei 1-Bit-Werten wird die Position der nächsten Zeile durch Überspringen der Gleichung ermittelt, die die Position der nächsten Zeile ![ in GL_UNPACK_ROW_LENGTH.](images/pix02.png)<br/> Komponenten oder Indizes. Die *Wortkomponente* in dieser Beschreibung bezieht sich auf die Nichtindexwerte Rot, Grün, Blau, Alpha und Tiefe. Storage GL RGB hat beispielsweise drei Komponenten pro Pixel: zuerst rot, dann grün \_ und schließlich blau.<br/> |
| GL \_ UNPACK \_ SKIP PIXELS \_ and <br/> GL \_ UNPACK \_ SKIP \_ ROWS | Diese Werte werden dem Programmierer zur Vereinfachung zur Verfügung gestellt. sie bieten keine Funktionalität, die nicht dupliziert werden kann, indem der an [**glDrawPixels,**](gldrawpixels.md) [**glTexImage1D,**](glteximage1d.md) [**glTexImage2D,**](glteximage2d.md) [**glBitmap**](glbitmap.md)oder [**glPolygonStipple**](glpolygonstipple.md)übergebene Zeiger inkrementiert wird. Das Festlegen von GL UNPACK SKIP PIXELS auf i entspricht dem Erhöhen des Zeigers um i n Komponenten oder Indizes, wobei n die Anzahl der Komponenten oder Indizes in jedem \_ \_ Pixel \_ ist.    Das Festlegen von GL UNPACK SKIP ROWS auf j entspricht dem Erhöhen des Zeigers um j k Komponenten oder Indizes, wobei k die Anzahl der Komponenten oder Indizes pro Zeile ist, wie oben im \_ \_ Abschnitt GL \_ UNPACK ROW LENGTH    \_ \_ \_ berechnet.                                                                                                                                                                                                                                    |
| GL \_ ENTPACKEN DER \_ AUSRICHTUNG                                           | Gibt die Ausrichtungsanforderungen für den Anfang jeder Pixelzeile im Arbeitsspeicher an. Die zulässigen Werte sind 1 (Byteausrichtung), 2 (Zeilen, die an gleichmäßig nummerierten Bytes ausgerichtet sind), 4 (Wortausrichtung) und 8 (Zeilen beginnen an Doppeltwortgrenzen).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf *den pname* festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Die **glPixelStore-Funktion** legt Pixelspeichermodi fest, die sich auf den Betrieb nachfolgender [**glDrawPixels**](gldrawpixels.md) und [**glReadPixels**](glreadpixels.md) sowie das Entpacken von Polygon-Ausschnittmustern (siehe [**glPolygonStipple),**](glpolygonstipple.md)Bitmaps (siehe [**glBitmap)**](glbitmap.md)und Texturmuster auswirken (siehe [**glTexImage1D**](glteximage1d.md), [**glTexImage2D,**](glteximage2d.md) [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md)).

Die folgende Tabelle enthält den Typ, den Anfangswert und den Bereich gültiger Werte für jeden der Speicherparameter, die mit **glPixelStore festgelegt werden können.**



| Pname                    | type    | Anfangswert | Gültiger Bereich   |
|--------------------------|---------|---------------|---------------|
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true oder false |
| GL \_ PACK \_ SWAP \_ BYTES    | Boolean | false         | true oder false |
| ZEILENLÄNGE \_ DES GL \_ \_ PACK-PAKETS    | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ ROWS     | integer | 0             | \[0,?)        |
| GL \_ PACK \_ SKIP \_ PIXELS   | integer | 0             | \[0,?)        |
| GL \_ PACK \_ ALIGNMENT      | integer | 4             | 1, 2, 4 oder 8 |
| GL \_ UNPACK \_ SWAP \_ BYTES  | Boolean | false         | true oder false |
| GL \_ UNPACK \_ LSB \_ FIRST   | Boolean | false         | true oder false |
| GL \_ UNPACK \_ ROW \_ LENGTH  | integer | 0             | \[0,?)        |
| GL \_ UNPACK \_ SKIP \_ ROWS   | integer | 0             | \[0,?)        |
| GL \_ ENTPACKEN SKIP \_ \_ PIXELS | integer | 0             | \[0,?)        |
| GL \_ ENTPACKEN DER \_ AUSRICHTUNG    | integer | 4             | 1, 2, 4 oder 8 |



 

Die [**glPixelStoref-Funktion**](glpixelstoref.md) kann zum Festlegen eines beliebigen Pixelspeicherparameters verwendet werden. Wenn der Parametertyp boolesch ist und *param* 0,0 ist, ist der Parameter false. Andernfalls wird sie auf TRUE festgelegt. Wenn *pname ein* ganzzahliger Typparameter ist, wird *der Parameter* auf die nächste ganze Zahl gerundet.

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

 

 





