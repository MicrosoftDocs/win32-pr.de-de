---
description: Referenz zu AVI-Riff Dateien
ms.assetid: 2d8cf5be-1252-4b58-89b1-f5c53ea17d0e
title: Referenz zu AVI-Riff Dateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83f28a7254ac9eb927381e313603ffd2bd0d050c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482547"
---
# <a name="avi-riff-file-reference"></a>Referenz zu AVI-Riff Dateien

Das Microsoft AVI-Dateiformat ist eine bitdateispezifikation, die für Anwendungen verwendet wird, die audiovideosequenzen erfassen, bearbeiten und wiedergeben. Im Allgemeinen enthalten AVI-Dateien mehrere Streams mit unterschiedlichen Datentypen. Die meisten AVI-Sequenzen verwenden sowohl Audiodaten als auch Videodaten Ströme. Eine einfache Variation für eine AVI-Sequenz verwendet Videodaten und erfordert keinen Audiodatenstrom.

In diesem Abschnitt werden die Dateiformat Erweiterungen von OpenDML AVI nicht beschrieben. Weitere Informationen zu diesen Erweiterungen finden Sie unter *OpenDML AVI-Dateiformat Erweiterungen*, die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden.

## <a name="fourccs"></a>Fourccs

Ein FourCC (aus vier Zeichen bestehende Code) ist 32 eine Ganzzahl ohne Vorzeichen, die durch die Verkettung von vier ASCII-Zeichen erstellt wurde. Das FourCC "abcd" wird beispielsweise auf einem Little-Endian System als 0x64636261 dargestellt. Fourccs kann Leerzeichen enthalten, sodass "ABC" ein gültiger FourCC ist. Das Dateiformat AVI verwendet FOURCC-Codes, um Streamtypen, Datenblöcke, Indexeinträge und andere Informationen zu identifizieren.

## <a name="riff-file-format"></a>Riff-Datei Format

Das Format der AVI-Datei basiert auf dem Dokumentformat "Riff" (Ressourcenaustausch Dateiformat). Eine Riff Datei besteht aus einem Riff-Header, gefolgt von NULL oder mehr *Listen* und *Blöcken*.

-   Der Riff-Header weist die folgende Form auf:

    `'RIFF' fileSize fileType (data)`

    Wenn ' Riff ' der Literale FourCC-Code ' Riff ' ist, `fileSize` ist ein 4-Byte-Wert, der die Größe der Daten in der Datei angibt, und `fileType` ein FourCC, der den spezifischen Dateityp identifiziert. Der Wert von `fileSize` schließt die Größe des `fileType` FourCC plus die Größe der nachfolgenden Daten ein, aber nicht die Größe von ' Riff ' FourCC oder die Größe von `fileSize` . Die Datei Daten bestehen aus Blöcken und Listen in beliebiger Reihenfolge.

-   Ein Block weist die folgende Form auf:

    `ckID ckSize ckData`

    dabei `ckID` ist ein FourCC, der die im Block enthaltenen Daten identifiziert, `ckSize` ein 4-Byte-Wert, der die Größe der Daten in angibt `ckData` , und `ckData` 0 (null) oder mehr Daten bytes. Die Daten werden immer bis zum nächsten **Wort** Rand aufgefüllt. `ckSize` Gibt die Größe der gültigen Daten im Block an. die Auffüll Zeichen, die Größe von `ckID` oder die Größe von sind nicht enthalten `ckSize` .

-   Eine Liste weist die folgende Form auf:

    `'LIST' listSize listType listData`

    wobei ' List ' der Literale FourCC-Code ' List ' ist, `listSize` ein 4-Byte-Wert, der die Größe der Liste angibt, `listType` ein FourCC-Code ist und `listData` aus Blöcken oder Listen in beliebiger Reihenfolge besteht. Der Wert von `listSize` schließt die Größe von `listType` plus der Größe von ein `listData` ; er enthält nicht den "List"-FourCC oder die Größe von `listSize` .

Im restlichen Teil dieses Abschnitts werden die folgenden Notation zum Beschreiben von Riff Segmenten verwendet:

`ckID ( ckData )`

Gibt an, wo die Segmentgröße implizit ist. Mit dieser Notation kann eine Liste wie folgt dargestellt werden:

`'LIST' ( listType ( listData ) )`

Optionale Elemente werden in eckige Klammern gestellt: `[ optional element ]`

## <a name="avi-riff-form"></a>AVI-Riff-Formular

AVI-Dateien werden durch den FourCC "AVI" im Riff-Header identifiziert. Alle AVI-Dateien enthalten zwei verbindliche Listen Blöcke, die das Format der Streams bzw. der Streamdaten definieren. Eine AVI-Datei kann auch einen Indexblock enthalten, der den Speicherort der Datenblöcke in der Datei liefert. Eine AVI-Datei mit diesen Komponenten weist die folgende Form auf:


```C++
RIFF ('AVI '
      LIST ('hdrl' ... )
      LIST ('movi' ... )
      ['idx1' (<AVI Index>) ]
     )
```



Die Liste "HDRL" definiert das Format der Daten und ist das erste erforderliche Listen Segment. Die "MOVI"-Liste enthält die Daten für die AVI-Sequenz und ist das zweite erforderliche Listen Segment. Die "idx1"-Liste enthält den Index. Bei AVI-Dateien müssen diese drei Komponenten in der richtigen Reihenfolge aufbewahrt werden.

> [!Note]  
> Die OpenDML-Erweiterungen definieren einen anderen Indextyp, der durch den FourCC "INDX" identifiziert wird.

 

Die Listen "HDRL" und "MOVI" verwenden unter Segmente für Ihre Daten. Das folgende Beispiel zeigt das AVI-Riff-Formular, das mit den Blöcken erweitert wird, die zum Durchführen dieser Listen benötigt werden:


```C++
RIFF ('AVI '
      LIST ('hdrl'
            'avih'(<Main AVI Header>)
            LIST ('strl'
                  'strh'(<Stream header>)
                  'strf'(<Stream format>)
                  [ 'strd'(<Additional header data>) ]
                  [ 'strn'(<Stream name>) ]
                  ...
                 )
             ...
           )
      LIST ('movi'
            {SubChunk | LIST ('rec '
                              SubChunk1
                              SubChunk2
                              ...
                             )
               ...
            }
            ...
           )
      ['idx1' (<AVI Index>) ]
     )
```



## <a name="avi-main-header"></a>AVI-Haupt Header

Die "HDRL"-Liste beginnt mit dem Haupt-AVI-Header, der in einem "avih"-Block enthalten ist. Der Haupt Header enthält globale Informationen für die gesamte AVI-Datei, z. b. die Anzahl der Streams in der Datei und die Breite und Höhe der AVI-Sequenz. Der Haupt Header Block besteht aus einer [**avimainheader**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) -Struktur.

## <a name="avi-stream-headers"></a>AVI-Streamheader

Eine oder mehrere "String"-Listen folgen dem Haupt Header. Für jeden Datenstrom ist eine "strinl"-Liste erforderlich. Jede "" "" "" "" "" "" "" Liste enthält Informationen zu einem Datenstrom in der Datei und muss einen Datenstrom-Header Block ("" "" "" "" "" "" "" ") und einen" " Darüber hinaus kann eine "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "" "".

Der Datenstrom [**-Header Block**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) ("" "" "" "" "

Ein Datenstrom Format Block ("" "" "" "" "" "" "" "" "" "" " Das Datenstrom Format Segment beschreibt das Format der Daten im Stream. Die in diesem Segment enthaltenen Daten sind vom Streamtyp abhängig. Bei Videostreams handelt es sich bei den Informationen um eine [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur, die ggf. Paletteninformationen einschließt. Für Audiostreams ist die Information eine [**WaveFormatEx**](/previous-versions/dd757713(v=vs.85)) -Struktur.

Wenn das Datenstrom Header-Daten Segment ("Strind") vorhanden ist, folgt es dem Datenstrom Format Block. Das Format und der Inhalt dieses Blocks werden vom Codec-Treiber definiert. Diese Informationen werden in der Regel von Treibern für die Konfiguration verwendet. Anwendungen, die AVI-Dateien lesen und schreiben, müssen diese Informationen nicht interpretieren. Sie werden einfach als Speicherblock an den und vom Treiber übertragen.

Der optionale Abschnitt "stringenter" enthält eine auf NULL endenden Text Zeichenfolge, die den Datenstrom beschreibt.

Die Streamheader in der HDRL-Liste sind den Datenstrom Daten in der Liste "MOVI" entsprechend der Reihenfolge der "stringenten" Blöcke zugeordnet. Der erste "" Bereich "" "" "" "" "" "" "" "" "" ".

## <a name="stream-data-movi-list"></a>Streamdaten ("MOVI"-Liste)

Das Befolgen der Header Informationen ist eine "MOVI"-Liste, die die eigentlichen Daten in den Streams enthält – d. h. die Video Frames und Audiobeispiele. Die Datenblöcke können sich direkt in der Liste "MOVI" befinden, oder Sie können in "Rec"-Listen gruppiert werden. Die ' REC '-Gruppierung impliziert, dass die gruppierten Blöcke alle gleichzeitig vom Datenträger gelesen werden sollen, und ist für Dateien vorgesehen, die für die Wiedergabe von CD-ROM verschachtelt sind.

Der FourCC, der die einzelnen Daten Segmente identifiziert, besteht aus einer zweistelligen streamnummer, gefolgt von einem aus zwei Zeichen bestehenden Code, der den Typ der Informationen im Block definiert.



| Code mit zwei Zeichen | BESCHREIBUNG              |
|--------------------|--------------------------|
| db                 | Nicht komprimierter Videorahmen |
| dc                 | Komprimierter Videorahmen   |
| pc                 | Palettenänderung           |
| WB                 | Audiodaten               |



 

Wenn Stream 0 z. b. Audiodaten enthält, haben die Datenblöcke für diesen Stream den FourCC "00wb". Wenn Stream 1 Video enthält, haben die Datenblöcke für diesen Stream den FourCC "01dB" oder "01dc". Mit Video Datenblöcken können auch neue Paletteneinträge definiert werden, um die Palette während einer AVI-Sequenz zu aktualisieren. Jeder palettenänderungs Block (' xxpc ') enthält eine [**avipalchange**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avipalchange) -Struktur. Wenn ein Stream Palettenänderungen enthält, legen Sie das **avisf \_ Video \_ palchanges** -Flag im **dwFlags** -Member der [**avistreamheader**](/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader) -Struktur für diesen Stream fest.

Textstreams können beliebige zwei Zeichen Codes verwenden.

## <a name="avi-index-entries"></a>AVI-Index Einträge

<dl> <dt>

<span id="AVI_1.0_index"></span><span id="avi_1.0_index"></span><span id="AVI_1.0_INDEX"></span>AVI 1,0-Index
</dt> <dd>

Ein optionaler Index (' idx1 ') kann der Liste ' MOVI ' folgen. Der Index enthält eine Liste der Datenblöcke und deren Speicherort in der Datei. Sie besteht aus einer [**avioldindex**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avioldindex) -Struktur mit Einträgen für jeden Datenblock, einschließlich ' REC '-Blöcken. Wenn die Datei einen Index enthält, legen Sie das **avif \_ HasIndex** -Flag im **dwFlags** -Member der [**avimainheader**](/previous-versions/windows/desktop/api/Aviriff/ns-aviriff-avimainheader) -Struktur fest.

</dd> <dt>

<span id="AVI_2.0_index"></span><span id="avi_2.0_index"></span><span id="AVI_2.0_INDEX"></span>AVI 2,0-Index
</dt> <dd>

Ein AVI 2,0-Index kann als einzelner Block angezeigt werden. Alternativ können Index Segmente innerhalb des Abschnitts "MOVI" verschachtelt werden. Wenn die Index Segmente in den Block "MOVI" eingefügt werden, enthält ein Superindex einen Index der Index Segmente. Die [**avimetaindex**](/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimetaindex) -Struktur ist die Basis Struktur sowohl für die Index Segmente als auch für den Super Index. Weitere Informationen finden Sie in den *OpenDML AVI-Dateiformat Erweiterungen*, die vom OpenDML AVI M-JPEG-Dateiformat-Unterausschuss veröffentlicht werden. (Diese Ressource ist möglicherweise nicht in einigen Sprachen und Ländern verfügbar.)

</dd> </dl>

## <a name="other-data-chunks"></a>Andere Datenblöcke

Daten können in einer AVI-Datei durch Einfügen von "Junk"-Blöcken nach Bedarf ausgerichtet werden. Anwendungen sollten den Inhalt eines "Junk"-Blocks ignorieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[AVI-Datei Format](avi-file-format.md)
</dt> </dl>

 

 
