---
title: Fontdirentry-Struktur
description: Enthält Informationen über eine einzelne Schriftart in einer Schriftart Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- Fontdirentry-Struktur Menüs und weitere Ressourcen
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1cee72a490fd2b94b1c810797f656d81418c0f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475771"
---
# <a name="fontdirentry-structure"></a>Fontdirentry-Struktur

Enthält Informationen über eine einzelne Schriftart in einer Schriftart Ressourcengruppe. Die hier bereitgestellte Struktur Definition dient nur der Erläuterung. Es ist in keiner Standard Header Datei vorhanden.

## <a name="syntax"></a>Syntax


```C++
typedef struct {
  WORD  dfVersion;
  DWORD dfSize;
  CHAR  dfCopyright[60];
  WORD  dfType;
  WORD  dfPoints;
  WORD  dfVertRes;
  WORD  dfHorizRes;
  WORD  dfAscent;
  WORD  dfInternalLeading;
  WORD  dfExternalLeading;
  BYTE  dfItalic;
  BYTE  dfUnderline;
  BYTE  dfStrikeOut;
  WORD  dfWeight;
  BYTE  dfCharSet;
  WORD  dfPixWidth;
  WORD  dfPixHeight;
  BYTE  dfPitchAndFamily;
  WORD  dfAvgWidth;
  WORD  dfMaxWidth;
  BYTE  dfFirstChar;
  BYTE  dfLastChar;
  BYTE  dfDefaultChar;
  BYTE  dfBreakChar;
  WORD  dfWidthBytes;
  DWORD dfDevice;
  DWORD dfFace;
  DWORD dfReserved;
  CHAR  szDeviceName;
  CHAR  szFaceName;
} FONTDIRENTRY;
```



## <a name="members"></a>Member

<dl> <dt>

**dfversion**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Eine benutzerdefinierte Versionsnummer für die Ressourcen Daten, die Tools zum Lesen und Schreiben von Ressourcen Dateien verwenden können.

</dd> <dt>

**dfsize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Datei (in Bytes).

</dd> <dt>

**dfcopyright \[ 60\]**
</dt> <dd>

Typ: **char**

</dd> <dd>

Die Copyright Informationen des Schriftart Lieferanten.

</dd> <dt>

**dftype**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Typ der Schriftart Datei.

</dd> <dt>

**dfpoints**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Punktgröße, bei der dieser Zeichensatz am besten aussieht.

</dd> <dt>

**dfvertres**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die vertikale Auflösung in Punkten pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die horizontale Auflösung in Punkten pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.

</dd> <dt>

**dfascent**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Der Abstand zwischen dem oberen Rand einer Zeichen Definitions Zelle und der Baseline der typografischen Schriftart.

</dd> <dt>

**dfinternalleading**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Menge der führenden innerhalb der durch das **dfpixheight** -Member festgelegten Begrenzungen. In diesem Bereich können Akzente und andere diakritische Zeichen auftreten.

</dd> <dt>

**dfexternalleading**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Menge der zusätzlichen führenden, die von der Anwendung zwischen Zeilen hinzugefügt werden.

</dd> <dt>

**dsptalic**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Eine kursiv Schrift, wenn nicht gleich 0 (null).

</dd> <dt>

**dfunderline**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Eine unterstrichene Schriftart, wenn ungleich 0 (null).

</dd> <dt>

**dfstrikeout**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Eine ausstrich Schriftart, wenn nicht gleich 0 (null).

</dd> <dt>

**dfweight**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Gewichtung der Schriftart im Bereich von 0 bis 1000. 400 ist z. b. Roman, und 700 ist fett formatiert. Wenn dieser Wert 0 (null) ist, wird eine Standard Gewichtung verwendet. Weitere definierte Werte finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.

</dd> <dt>

**dfcharset**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Der Zeichensatz der Schriftart. Informationen zu vordefinierten Werten finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.

</dd> <dt>

**dfpixwidth**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Breite des Rasters, in dem eine Vektor Schriftart digitalisiert wurde. Wenn das Element bei Raster Schriftarten nicht gleich 0 (null) ist, stellt es die Breite für alle Zeichen in der Bitmap dar. Wenn der Member gleich 0 (null) ist, weist die Schriftart Zeichen variabler Breite auf.

</dd> <dt>

**dfpixheight**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Höhe der Zeichen Bitmap für Raster Schriftarten oder die Höhe des Rasters, in dem eine Vektor Schriftart digitalisiert wurde.

</dd> <dt>

**dfpitchandfamily**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Die Tonhöhe und die Familie der Schriftart. Weitere Informationen finden Sie in der Beschreibung der [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) -Struktur.

</dd> <dt>

**dfavgwidth**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die durchschnittliche Breite der Zeichen in der Schriftart (im Allgemeinen als Breite des Buchstaben x definiert). Dieser Wert enthält nicht den für Fett-oder kursiv Zeichen erforderlichen Überlauf.

</dd> <dt>

**dfmaxwidth**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Breite des breitesten Zeichens in der Schriftart.

</dd> <dt>

**dffirstchar**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Der erste Zeichencode, der in der Schriftart definiert ist.

</dd> <dt>

**dflastchar**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Der letzte Zeichencode, der in der Schriftart definiert ist.

</dd> <dt>

**dfdefaultchar**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Das Zeichen, das nicht in der Schriftart, sondern in Zeichen ersetzt werden soll.

</dd> <dt>

**dfbreakchar**
</dt> <dd>

Type: **Byte**

</dd> <dd>

Das Zeichen, das zum Definieren von Wort Umbrüchen für die Textausrichtung verwendet wird.

</dd> <dt>

**dfwidthbytes**
</dt> <dd>

Typ: **Word**

</dd> <dd>

Die Anzahl der Bytes in jeder Zeile der Bitmap. Dieser Wert ist immer, auch wenn die Zeilen an Wortgrenzen beginnen. Bei Vektor Schriftarten hat dieser Member keine Bedeutung.

</dd> <dt>

**dfdevice**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Offset in der Datei mit einer auf NULL endenden Zeichenfolge, die einen Gerätenamen angibt. Bei einer generischen Schriftart ist dieser Wert 0 (null).

</dd> <dt>

**dfface**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Offset in der Datei mit einer auf NULL endenden Zeichenfolge, die die Schriftart benennt.

</dd> <dt>

**dfreserved**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Dieser Member ist reserviert.

</dd> <dt>

**szdevicename**
</dt> <dd>

Typ: **char**

</dd> <dd>

Der Name des Geräts, wenn diese Schriftart Datei für ein bestimmtes Gerät bestimmt ist.

</dd> <dt>

**szfakename**
</dt> <dd>

Typ: **char**

</dd> <dd>

Der Schriftart Name der Schriftart.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es gibt eine **fontdirentry** -Struktur für jede Schriftart in der RES-Datei. Anwendungen, die RES-Dateien mit Schriftart Ressourcen generieren, müssen der Datei auch eine **fontdirentry** -Struktur für jede Schriftart hinzufügen.

Schriftart Deklarationen können mit anderen Ressourcen Deklarationen in gemischt werden. RC-Datei, da Schriftarten in der RES-Datei nicht zusammenhängend sein müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**Direntry**](direntry.md)
</dt> <dt>

[**Fontgrouphdr**](fontgrouphdr.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Ressourcen](resources.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**"LogFont"**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

