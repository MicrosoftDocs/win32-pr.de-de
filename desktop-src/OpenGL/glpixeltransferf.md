---
title: glpixeltransferf-Funktion (GL. h)
description: Die Funktionen "glpixeltransferf" und "glpixeltransferi" legen die Pixel Übertragungsmodi fest. | glpixeltransferf-Funktion (GL. h)
ms.assetid: c18ecbb9-af2a-4662-8e3f-0ac850b04fc1
keywords:
- glpixeltransferf-Funktion OpenGL
topic_type:
- apiref
api_name:
- glPixelTransferf
api_location:
- Opengl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d6404c9b219b8a27dd3d422bfb85cd45ac8cac
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "106363076"
---
# <a name="glpixeltransferf-function"></a>glpixeltransferf-Funktion

Die Funktionen " **glpixeltransferf** " und " [**glpixeltransferi**](glpixeltransferi.md) " legen die Pixel Übertragungsmodi fest.

## <a name="syntax"></a>Syntax


```C++
void WINAPI glPixelTransferf(
   GLenum  pname,
   GLfloat param
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pName* 
</dt> <dd>

Der symbolische Name des festzulegenden Pixel Übertragungs Parameters. In der folgenden Tabelle sind der Typ, der Anfangswert und der Bereich gültiger Werte für jeden der Pixel Übertragungsparameter angegeben, die mit **glpixeltransfer** festgelegt werden.



| PName             | type    | Anfangswert  | Gültiger Bereich  |
|-------------------|---------|----------------|--------------|
| GL- \_ Karten \_ Farbe    | Boolean | false          | TRUE/FALSE   |
| GL- \_ Karten \_ Schablone  | Boolean | false          | TRUE/FALSE   |
| GL- \_ Index \_ Verschiebung  | integer | 0              | (8, 8)        |
| GL- \_ Index \_ Offset | integer | 0              | (8, 8)        |
| GL. \_ Rote \_ Skala    | integer | 1.0            | (8, 8)        |
| GL- \_ grüne \_ Skala  | float   | 1.0            | (8, 8)        |
| GL \_ blaue \_ Skala   | float   | 1.0            | (8, 8)        |
| GL- \_ alpha \_ Skala  | float   | 1.0            | (8, 8)        |
| GL- \_ tiefen \_ Skala  | float   | 1.0            | (8, 8)        |
| GL- \_ roter \_ Bias     | float   | 0,0            | (8, 8)        |
| GL- \_ grüner \_ Bias   | float   | 0,0            | (8, 8)        |
| GL \_ Blue \_ Bias    | float   | 0,0            | (8, 8)        |
| GL- \_ alpha- \_ Bias   | float   | 0,0            | (8, 8)        |
| GL- \_ tiefen Abweichung \_   | float   | 0,0            | (8, 8)        |



 

</dd> <dt>

*param* 
</dt> <dd>

Der Wert, auf den *PName* festgelegt ist.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Mit der **glpixeltransfer** -Funktion werden Pixel Übertragungsmodi festgelegt, die sich auf den Vorgang der nachfolgenden Befehle [**glcopypixel**](glcopypixels.md), [**glCopyTexImage1D**](glcopyteximage1d.md), [**glCopyTexImage2D**](glcopyteximage2d.md), [**glCopyTexSubImage1D**](glcopytexsubimage1d.md), [**glCopyTexSubImage2D**](glcopytexsubimage2d.md), [**gldrawpixels**](gldrawpixels.md), [**gllesepixels**](glreadpixels.md), [**glTexImage1D**](glteximage1d.md), [**glTexImage2D**](glteximage2d.md), [**glTexSubImage1D**](gltexsubimage1d.md)und [**glTexSubImage2D**](gltexsubimage2d.md) auswirken. Die Algorithmen, die durch die Pixel Übertragungsmodi angegeben werden, werden nach dem Lesen aus dem Frame Puffer (**gllesepixels** und **glcopypixels**) oder dem Entpacken aus dem Client Speicher (**gldrawpixels**, **glTexImage1D** und **glTexImage2D**) in Pixel verarbeitet. Pixel Übertragungs Vorgänge erfolgen in derselben Reihenfolge und auf die gleiche Weise, unabhängig vom Befehl, der zum Pixel Vorgang geführt hat. Die Pixel Speicher Modi ([**glpixelstore**](glpixelstore-functions.md)) steuern das Entpacken von Pixeln, die aus dem Client Speicher gelesen werden, und das Packen von Pixeln, die in den Client Speicher zurückgeschrieben werden.

Bei Pixel Übertragungs Vorgängen werden vier grundlegende Pixel Typen verarbeitet: *Farbe*, *Farbindex*, *Tiefe* und *Schablone*. Farbpixel bestehen aus vier Gleit Komma Werten mit nicht spezifizierten Mantisse-und exponentengrößen, die so skaliert werden, dass 0,0 keine Intensität und 1,0 volle Intensität darstellt. Farbindizes umfassen einen einzelnen fest Komma Wert mit nicht spezifizierter Genauigkeit auf der rechten Seite des binären Punkts. Tiefe Pixel umfassen einen einzelnen Gleit Komma Wert mit nicht spezifizierten Mantisse-und exponentengrößen, so skaliert, dass 0,0 den minimalen tiefen Puffer Wert darstellt und 1,0 den maximalen tiefen Puffer Wert darstellt. Schließlich enthalten Schablonen Pixel einen einzelnen fest Komma Wert mit nicht spezifizierter Genauigkeit auf der rechten Seite des binären Punkts.

Die Pixel Übertragungs Vorgänge, die für die vier grundlegenden Pixel Typen ausgeführt werden, lauten wie folgt:



| Pixeltyp  | Pixel Übertragungsvorgang                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Color       | Jede der vier Farbkomponenten wird mit einem Skalierungsfaktor multipliziert und dann zu einem Bias-Faktor hinzugefügt. Das heißt, die rote Komponente wird mit einer roten Größe von GL multipliziert \_ \_ und dann zu GL \_ Red \_ Bias hinzugefügt. die grüne Komponente wird mit der grünen Skala von GL multipliziert \_ \_ und dann zu GL \_ Green Bias hinzugefügt \_ . die blaue Komponente wird mit der GL-blauen \_ Skala multipliziert \_ \_ \_ \_ \_ \_ \_ und dann zu GL Blue Bias hinzugefügt, und die Alpha Komponente wird mit der GL-Alpha Skala multipliziert. Nachdem alle vier Farbkomponenten skaliert und verzerrt wurden, werden beide an den Bereich \[ 0, 1 gebunden \] . Alle Farbskala-und biaswerte werden mit **glpixeltransfer** angegeben. <br/> Wenn \_ die GL \_ -Kartenfarbe true ist, wird jede Farbkomponente um die Größe der entsprechenden Farb-zu-Farben-Karte skaliert und dann durch den Inhalt dieser Karte ersetzt, der durch die skalierte Komponente indiziert wird. Das heißt, die rote Komponente wird von der GL \_ \_ -Pixel Map \_ r auf die \_ \_ r-Größe skaliert \_ und dann durch den Inhalt von GL- \_ Pixel \_ map r zu r ersetzt, der \_ \_ \_ von sich selbst indiziert wird. Die grüne Komponente wird um die Größe der GL \_ Pixel \_ map \_ g \_ auf g skaliert \_ \_ und dann durch den Inhalt von GL- \_ Pixel Zuordnung \_ \_ g \_ zu g durch \_ sich selbst indiziert. Die blaue Komponente wird von GL \_ Pixel \_ map b auf die Größe b skaliert \_ \_ \_ \_ und dann durch den Inhalt von GL- \_ Pixel \_ map \_ b zu b, der \_ \_ durch sich selbst indiziert wurde, ersetzt. Die Alpha Komponente wird von der GL \_ \_ -Pixel \_ -Zuordnung a \_ zu \_ einer Größe skaliert \_ und dann durch den Inhalt von GL-Pixel durch die Zuordnung \_ \_ \_ eines \_ zu \_ einem indizierten ersetzt. Alle Komponenten, die aus den Zuordnungen entnommen werden, werden dann an den Bereich \[ 0, 1 gebunden \] . Die GL- \_ Karten \_ Farbe wird mit **glpixeltransfer** angegeben. Der Inhalt der verschiedenen Zuordnungen wird mit **glpixelmap** angegeben.<br/>                                                                                                                        |
| Farbindex | Jeder Farbindex wird nach links von GL- \_ Index \_ Verschiebungs Bits verschoben und füllt alle Bits, die über die Anzahl der vom Festkomma Index getragene Bruchteile hinausgehen, mit Nullen auf. Wenn die GL- \_ Index \_ Verschiebung negativ ist, wird die UMSCHALTTASTE nach rechts und erneut auf NULL gefüllt. Der GL- \_ Index \_ Offset wird dann dem Index hinzugefügt. \_Die GL \_ -Index Verschiebung und der GL- \_ Index \_ Offset werden bei **glpixeltransfer** angegeben.<br/> An diesem Punkt unterscheidet sich der Vorgang abhängig vom erforderlichen Format der resultierenden Pixel. Wenn die resultierenden Pixel in einen Farb Index Puffer geschrieben werden sollen, oder wenn Sie im GL-Farb Indexformat in den Client Speicher eingelesen werden, \_ \_ werden die Pixel weiterhin als Indizes behandelt. Wenn die GL- \_ Karten \_ Farbe true ist, wird jeder Index durch 2 ^ *n* 1 maskiert, wobei *n* der \_ Größe von GL Pixel zugeordnet ist \_ \_ \_ \_ \_ , und dann durch den Inhalt von GL Pixel Map i ersetzt wird, der \_ \_ \_ \_ \_ durch den maskierten Wert indiziert wurde. Die GL- \_ Karten \_ Farbe wird mit **glpixeltransfer** angegeben. Der Inhalt der Index Zuordnung wird mit **glpixelmap** angegeben.<br/> Wenn die resultierenden Pixel in einen RGBA-Farb Puffer geschrieben werden sollen, oder wenn Sie in einem anderen Format als dem GL-Farbindex in den Client Speicher eingelesen werden \_ \_ , werden die Pixel von Indizes in Farben konvertiert, indem Sie auf die vier Zuordnungen GL Pixel Map i to \_ \_ \_ \_ \_ R, GL Pixel Map i to \_ G, \_ \_ \_ \_ GL Pixel Map \_ i to \_ \_ \_ \_ B und GL \_ Pixel \_ map \_ i \_ zu \_ a verweisen Vor der Dereferenzierung wird der Index durch 2 n 1 maskiert, wobei n für die Höhe von GL Pixel für die \_ \_ R- \_ \_ \_ \_ Größe der roten Karte steht, für GL \_ Pixel \_ map \_ i \_ to \_ G \_ size für die grüne Karte, GL \_ Pixel Map \_ \_ i \_ to \_ B \_ size für die blaue Karte und GL \_ Pixel \_ \_ \_ \_ eine \_ Größe für die Alpha Karte. Alle Komponenten, die aus den Zuordnungen entnommen werden, werden dann an den Bereich \[ 0, 1 gebunden \] . Der Inhalt der vier Zuordnungen wird mit **glpixelmap** angegeben.<br/> |
| Tiefe       | Jeder tiefen Wert wird mit einer tiefen Skala von GL multipliziert \_ \_ , dem \_ GL \_ -tiefen Bias hinzugefügt und dann an den Bereich \[ 0, 1 gebunden \] .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Schablone     | Jeder Index wird \_ \_ auf die Verschiebung von GL-Indizes verschoben, ebenso wie ein Farbindex, und wird dann dem GL- \_ Index Offset hinzugefügt \_ . Wenn die GL- \_ Karten Schablone den Wert \_ true hat, wird jeder Index durch 2n 1 maskiert, wobei *n* der Größe von GL \_ Pixel \_ \_ \_ entspricht \_ \_ und dann durch den Inhalt von GL-Pixel Zuordnungen durch \_ \_ \_ \_ \_ den maskierten Wert ersetzt wird.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |



 

Die [**glpixeltransferf**](glpixeltransfer.md) -Funktion kann verwendet werden, um beliebige Pixel Übertragungsparameter festzulegen. Wenn der Parametertyp Boolean ist, bedeutet 0,0 false, und jeder andere Wert impliziert true. Wenn " *PName* " ein ganzzahliger Parameter ist, wird *param* auf die nächste ganze Zahl gerundet.

Ebenso kann **glpixeltransferi** auch verwendet werden, um beliebige Pixel Übertragungsparameter festzulegen. Boolesche Parameter werden auf false festgelegt, wenn *param* den Wert 0 hat, andernfalls true. Der Parameter *param* wird in den Gleit Komma Wert konvertiert, bevor er den Real-Wert-Parametern zugewiesen wird.

Wenn ein Befehl " [**gldrawpixels**](gldrawpixels.md)", " [**gllesepixels**](glreadpixels.md)", " [**glcopypixels**](glcopypixels.md)", " [**glTexImage1D**](glteximage1d.md)" oder " [**glTexImage2D**](glteximage2d.md) " in eine Anzeigeliste eingefügt wird (siehe " [**glnewlist**](glnewlist.md) " und " [**glCallList**](glcalllist.md)"), werden die Einstellungen für den pixelübertragungsmodus wirksam, wenn die Anzeigeliste *ausgeführt* wird. Sie können sich von den Einstellungen unterscheiden, wenn der Befehl in die Anzeigeliste kompiliert wurde.

Mit den folgenden Funktionen werden Informationen im Zusammenhang mit **glpixeltransfer** abgerufen:

[**glget**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) mit dem Argument GL- \_ Karten \_ Farbe

**glget** mit Argument GL- \_ Karten \_ Schablone

**glget** mit dem Argument GL \_ Index \_ Shift

**glget** mit Argument GL- \_ Index \_ Offset

**glget** mit dem Argument GL \_ Red \_ Scale

**glget** mit dem Argument GL \_ Red \_ Bias

**glget** mit dem Argument GL \_ Green \_ Scale

**glget** mit dem Argument GL \_ Green \_ Bias

**glget** mit dem Argument GL \_ Blue \_ Scale

**glget** mit dem Argument GL \_ Blue \_ Bias

**glget** mit dem Argument GL \_ alpha \_ Scale

**glget** mit dem Argument GL \_ alpha- \_ Bias

**glget** mit dem Argument GL- \_ tiefen \_ Skala

**glget** mit Argument GL- \_ tiefen Abweichung \_

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

[**glCallList**](glcalllist.md)
</dt> <dt>

[**glcopypixels**](glcopypixels.md)
</dt> <dt>

[**gldrawpixels**](gldrawpixels.md)
</dt> <dt>

[**glEnd**](glend.md)
</dt> <dt>

[**glnewlist**](glnewlist.md)
</dt> <dt>

[**glpixelmap**](glpixelmap.md)
</dt> <dt>

[**glpixelstore**](glpixelstore-functions.md)
</dt> <dt>

[**glpixelzoom**](glpixelzoom.md)
</dt> <dt>

[**glread Pixels**](glreadpixels.md)
</dt> <dt>

[**glTexImage1D**](glteximage1d.md)
</dt> <dt>

[**glTexImage2D**](glteximage2d.md)
</dt> </dl>

 

 





