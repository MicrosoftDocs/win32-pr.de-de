---
description: AAUX-Quellpaket (AS)
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: AAUX-Quellpaket (AS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89a2d8aa11c9560b2aa59165afd9bdaae775be7755a7a7d2a5e87a80df412d1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160261"
---
# <a name="aaux-source-as-pack"></a>AAUX-Quellpaket (AS)

In den folgenden Tabellen sind die Werte aufgeführt, die vom MSDV-Treiber verwendet werden, um die Member **dwDVAAuxSrc** und **dwDVAAuxSrc1** der [**DVINFO-Struktur**](/windows/desktop/api/strmif/ns-strmif-dvinfo) auszufüllen. Weitere Informationen finden Sie unter [DVINFO-Feld Einstellungen im MSDV-Treiber.](dvinfo-field-settings-in-the-msdv-driver.md)

DVCR Einstellungen



DV Standard

DVCR (IEC 61834)

FOURCC

dvsl

dvsd

System

525-60

625-50

525-60

625-50

LF (1)

1

1

1

1

Reserviert (1)

1

1

1

1

AF SIZE (6)

00:1111

01:0000

00:1111

01:0000

SM (1)

0

0

0

0

CHN (2)

01

01

01

01

PA (1)

1

1

1

1

AUDIOMODUS (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0000

0000

1111

1111

Reserviert (1)

1

1

1

1

ML (1)

1

1

1

1

50/60 (1)

0

1

0

1

STYPE (5)

0:0001

0:0001

0:0000

0:0000

EF (1)

1

1

1

1

TC (1)

1

1

1

1

SMP (3)

010

010

010

010

QU (3)

001

001

001

001

AS Pack

    Audio Block 1\*

0xD1C130CF

0xD1E130D0

0xD1C030CF

0xD1E030D0

    Audio Block 2\*

0x00000000

0x00000000

0xD1C03FCF

0xD1E03FD0



 

DVCR 25 und DVCPRO 50 Einstellungen (geplant)



DV Standard

DVCPRO (SMPTE 314M) – Geplant

FOURCC

dv25

dv50

System

525-60

625-50

525-60

625-50

LF (1)

0

0

0

0

Reserviert (1)

1

1

1

1

AF-GRÖßE (6)

01:0110

01:1000

01:0110

01:1000

Reserviert (1)

0

0

0

0

CHN (2)

00

00

00

00

Reserviert (1)

1

1

1

1

AUDIOMODUS (4)

    Audio Block 1\*

0000

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

0001

Reserviert (2)

11

11

11

11

50/60 (1)

0

1

0

1

STYPE (5)

0:0000

0:0000

0:0010

0:0010

Reserviert (2)

11

11

11

11

SMP (3)

000

000

000

000

QU (3)

000

000

000

000

AS Pack

    Audio Block 1\*

0xC0C01056

0xC0E01058

0xC0C21056

0xC0E21058

    Audio Block 2\*

0xC0C01156

0xC0E01158

0xC0C21156

0xC0E21158



 

> [!Note]  
> \* Die [**DVINFO-Struktur**](/windows/desktop/api/strmif/ns-strmif-dvinfo) enthält zwei AAUX AS-Pakete für die Audioblöcke 1 und 2. DV50 verfügt über vier Audioblöcke. Die Blöcke 3 und 4 werden in der **DVINFO-Struktur nicht** dargestellt.

 

DVCR 100 Einstellungen (geplant)



DV Standard

DVCPRO 100 – Geplant

FOURCC

dvh1

System

1080-60i

720-60p

1080-50i

LF (1)

0

0

0

Reserviert (1)

1

1

1

AF SIZE (6)

01:0110

01:0110

01:1000

Reserviert (1)

0

0

0

CHN (2)

00

00

00

Reserviert (1)

1

1

1

AUDIOMODUS (4)

    Audio Block 1\*

0000

0000

0000

    Audio Block 2\*

0001

0001

0001

Reserviert (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

0:0011

0:0011

0:0011

Reserviert (2)

11

11

11

SMP (3)

000

000

000

QU (3)

000

000

000

AS Pack

    Audio Block 1\*

0xC0C31056

0xC0C31056

0xC0D31058

    Audio Block 2\*

0xC0C31156

0xC0C31156

0xC0D31158



 

> [!Note]  
> \* DVCPRO 100 verfügt über 8 Audioblöcke. Die Blöcke 3 bis 8 werden in der [DVINFO-Struktur](dvinfo-field-settings-in-the-msdv-driver.md) nicht dargestellt.

 

## <a name="remarks"></a>Hinweise

Die folgenden Feldcodes sind von Interesse:

-   LF: Flag für den gesperrten Modus. Gibt an, ob die Audiodatei gesperrt ist.
    -   0 = Gesperrt
    -   1 = Entsperrt
-   AF-GRÖßE: Audioframegröße. Gibt die Anzahl der Audiobeispiele pro Frame an.

    IEC 61834-Definition:

    -   00:1111 = 1068 Stichproben pro Frame
    -   01:0000 = 1280 Stichproben pro Frame

    SMPTE 314M-Definition:

    -   01:0110 = 1602 Stichproben pro Frame
    -   01:1000 = 1920 Stichproben pro Frame

    Abhängig von der Bildfrequenz kann die genaue Anzahl von Stichproben in einem Frame variieren. Ntsc beträgt beispielsweise 30000/1001 Frames pro Sekunde (29,97 fps). Bei Audio mit 32 kHz gibt es etwa 1067,73 Audiobeispiele pro Frame. Daher beträgt die nominale Rate 1068, aber die tatsächliche Zahl variiert je nach Frame. Bei entsperrten Audiodaten kann die Anzahl der Audiobeispiele pro Frame im Laufe der Zeit innerhalb eines bestimmten Bereichs variieren.

<!-- -->

-   SM: Stereomodus.
    -   0 = Stereo
    -   1 = Mono
-   CHN: Anzahl der Audiokanäle pro Audioblock.
    -   0 = Ein Kanal pro Audioblock
    -   1 = Zwei Kanäle pro Audioblock
-   AUDIOMODUS: Gibt den Inhalt des Audiosignals auf jedem Kanal an. Die Interpretation dieses Felds hängt davon ab, welche Werte in den Feldern SM und CHN platziert werden. Die unten angegebenen Definitionen gelten für die von MSDV verwendeten Werte. Weitere Informationen finden Sie in den Spezifikationen.

    IEC 61834-Definition:

    -   0000 = Ch a/c/e/g ist linker Kanal, Ch b/d/f/h ist der rechte Kanal
    -   1111 = keine Audiodaten

    SMPTE 314M-Definition:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: Anzahl der Felder.
    -   0 = 60 Felder
    -   1 = 50 Felder
-   STYPE: Systemtyp.

    IEC 61834-Definition:

    -   00000 = 525-60 oder 625-50, dvsd
    -   00001 = 525-60 oder 625-50, dvsl (siehe IEC 61883-5)

    SMPTE 314M/SPMTE 370-Definition:

    -   00000 = 2 Audioblöcke pro Videoframe
    -   00010 = 4 Audioblöcke pro Videoframe
    -   00011 = 8 Audioblöcke pro Videoframe

-   SMP: Samplinghäufigkeit.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   QU: Quantisierung.
    -   0 = 16 Bit linear
    -   1 = 12 Bits nicht linear

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DVINFO-Einstellungen im MSDV-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



