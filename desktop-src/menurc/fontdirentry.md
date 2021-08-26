---
title: FONTDIRENTRY-Struktur
description: Enthält Informationen zu einer einzelnen Schriftart in einer Schriftartressourcengruppe. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.
ms.assetid: 0ada2afe-b299-4ef2-99b7-96da10ee218a
keywords:
- FONTDIRENTRY-StrukturMenüs und andere Ressourcen
topic_type:
- apiref
api_name:
- FONTDIRENTRY
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e236104730dbbfe79ec0ed3d18cbb465402ed8827c6037a2457bec18faf63024
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886740"
---
# <a name="fontdirentry-structure"></a>FONTDIRENTRY-Struktur

Enthält Informationen zu einer einzelnen Schriftart in einer Schriftartressourcengruppe. Die hier bereitgestellte Strukturdefinition dient nur zur Erklärung. sie ist in keiner Standardheaderdatei vorhanden.

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

**dfVersion**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Eine benutzerdefinierte Versionsnummer für die Ressourcendaten, die Tools zum Lesen und Schreiben von Ressourcendateien verwenden können.

</dd> <dt>

**dfSize**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Die Größe der Datei (in Bytes).

</dd> <dt>

**dfCopyright \[ 60\]**
</dt> <dd>

Typ: **CHAR**

</dd> <dd>

Die Copyrightinformationen des Schriftartanbieters.

</dd> <dt>

**dfType**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Typ der Schriftartdatei.

</dd> <dt>

**dfPoints**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Punktgröße, an der dieser Zeichensatz am besten aussieht.

</dd> <dt>

**dfVertRes**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die vertikale Auflösung in Punkt pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.

</dd> <dt>

**dfHorizRes**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die horizontale Auflösung in Punkt pro Zoll, bei der dieser Zeichensatz digitalisiert wurde.

</dd> <dt>

**dfAscent**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Der Abstand vom oberen Rand einer Zeichendefinitionszelle zur Baseline der typografischen Schriftart.

</dd> <dt>

**dfInternalLeading**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Menge der führenden Innerhalb der Begrenzungen, die vom **dfPixHeight-Member** festgelegt werden. Akzente und andere diakritische Zeichen können in diesem Bereich auftreten.

</dd> <dt>

**dfExternalLeading**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Menge der zusätzlichen führenden Werte, die die Anwendung zwischen Zeilen hinzufügt.

</dd> <dt>

**dfItalic**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Eine italische Schriftart, wenn nicht gleich 0 (null) ist.

</dd> <dt>

**dfUnderline**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Eine unterstrichene Schriftart, wenn nicht gleich 0 (null) ist.

</dd> <dt>

**dfStrikeOut**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Eine durchsstrichene Schriftart, wenn nicht gleich 0 (null) ist.

</dd> <dt>

**dfWeight**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Gewichtung der Schriftart im Bereich von 0 bis 1000. Beispielsweise ist 400 roman und 700 fett. Wenn dieser Wert 0 (null) ist, wird eine Standardgewichtung verwendet. Weitere definierte Werte finden Sie in der Beschreibung der [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfCharSet**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Der Zeichensatz der Schriftart. Vordefinierte Werte finden Sie in der Beschreibung der [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfPixWidth**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Breite des Rasters, auf dem eine Vektorschriftart digitalisiert wurde. Wenn der Member für Rasterschriftarten ungleich 0 (null) ist, stellt er die Breite für alle Zeichen in der Bitmap dar. Wenn der Member gleich 0 (null) ist, weist die Schriftart Zeichen variabler Breite auf.

</dd> <dt>

**dfPixHeight**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Höhe der Zeichenbitmap für Rasterschriftarten oder die Höhe des Rasters, auf dem eine Vektorschriftart digitalisiert wurde.

</dd> <dt>

**dfPitchAndFamily**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Die Tonhöhe und die Familie der Schriftart. Weitere Informationen finden Sie in der Beschreibung der [**LOGFONT-Struktur.**](/windows/win32/api/wingdi/ns-wingdi-logfonta)

</dd> <dt>

**dfAvgWidth**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die durchschnittliche Breite von Zeichen in der Schriftart (im Allgemeinen als Breite des Buchstabens x definiert). Dieser Wert enthält nicht den Überhänge, der für fette oder kursiv formatierte Zeichen erforderlich ist.

</dd> <dt>

**dfMaxWidth**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Breite des breitesten Zeichens in der Schriftart.

</dd> <dt>

**dfFirstChar**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Der erste in der Schriftart definierte Zeichencode.

</dd> <dt>

**dfLastChar**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Der letzte in der Schriftart definierte Zeichencode.

</dd> <dt>

**dfDefaultChar**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Das Zeichen, das zeichenweise ersetzt werden soll, die nicht in der Schriftart enthalten sind.

</dd> <dt>

**dfBreakChar**
</dt> <dd>

Typ: **BYTE**

</dd> <dd>

Das Zeichen, das zum Definieren von Wortumbrüchen für die Textgrundlegende verwendet wird.

</dd> <dt>

**dfWidthBytes**
</dt> <dd>

Typ: **WORD**

</dd> <dd>

Die Anzahl der Bytes in jeder Zeile der Bitmap. Dieser Wert ist immer gleich, sodass die Zeilen an Wortgrenzen beginnen. Für Vektorschriftarten hat dieser Member keine Bedeutung.

</dd> <dt>

**dfDevice**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Offset in der Datei zu einer auf NULL endenden Zeichenfolge, die einen Gerätenamen angibt. Bei einer generischen Schriftart ist dieser Wert 0 (null).

</dd> <dt>

**dfFace**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Der Offset in der Datei zu einer auf NULL beendeten Zeichenfolge, die die Schriftart benennt.

</dd> <dt>

**dfReserved**
</dt> <dd>

Typ: **DWORD**

</dd> <dd>

Dieses Mitglied ist reserviert.

</dd> <dt>

**szDeviceName**
</dt> <dd>

Typ: **CHAR**

</dd> <dd>

Der Name des Geräts, wenn diese Schriftartdatei für ein bestimmtes Gerät festgelegt ist.

</dd> <dt>

**szFaceName**
</dt> <dd>

Typ: **CHAR**

</dd> <dd>

Der Schriftartname der Schriftart.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es gibt eine **FONTDIRENTRY-Struktur** für jede Schriftart in der RES-Datei. Anwendungen, die RES-Dateien mit Schriftartressourcen generieren, müssen der Datei außerdem eine **FONTDIRENTRY-Struktur** für jede Schriftart hinzufügen.

Schriftartdeklarationen können mit anderen Ressourcendeklarationen im gemischt werden. RC-Datei, da Schriftarten in der RES-Datei nicht zusammenhängend sein müssen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>       |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**DIRENTRY**](direntry.md)
</dt> <dt>

[**FONTGROUPHDR**](fontgrouphdr.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Ressourcen](resources.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[**Logfont**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> </dl>

 

