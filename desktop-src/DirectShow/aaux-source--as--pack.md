---
description: Aaux-Quelle (as)-Paket
ms.assetid: 0e173fe5-0b9d-48e8-bcbd-403614d51558
title: Aaux-Quelle (as)-Paket
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe479a0740da08f42ca5d80e1f0b6f5174f6917b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213983"
---
# <a name="aaux-source-as-pack"></a>Aaux-Quelle (as)-Paket

In den folgenden Tabellen sind die Werte aufgeführt, die vom msdv-Treiber zum Ausfüllen der **dwdvaauxsrc** -und **dwDVAAuxSrc1** -Member der [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur verwendet werden. Weitere Informationen finden Sie unter [dvinfo Field Settings in the msdv Driver](dvinfo-field-settings-in-the-msdv-driver.md).

Dvcr-Einstellungen



DV-Standard

Dvcr (IEC 61834)

FOURCC

dvsl

DVSD

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

AF-Größe (6)

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

Audiomodus (4)

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

Qu (3)

001

001

001

001

Als Paket

    Audio Block 1\*

0xD1 c130cf

0xd1e130d0

0xd1c030cf

0xd1e030d0

    Audio Block 2\*

0x00000000

0x00000000

0xD1 c03f

0xd1e03\d0



 

Dvcr 25-und DVCPRO 50-Einstellungen (geplant)



DV-Standard

DVCPRO (SMPTE 314m) – geplant

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

AF-Größe (6)

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

Audiomodus (4)

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

Qu (3)

000

000

000

000

Als Paket

    Audio Block 1\*

0xc0c01056

0xc0e01058

0xc0c21056

0xc0e21058

    Audio Block 2\*

0xc0c01156

0xc0e01158

0xc0c21156

0xc0e21158



 

> [!Note]  
> \* Die [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur enthält zwei Aaux als Pakete für audioblöcke 1 und 2. DV50 hat vier audioblöcke. die Blöcke 3 und 4 werden nicht in der **dvinfo** -Struktur dargestellt.

 

Dvcr 100-Einstellungen (geplant)



DV-Standard

DVCPRO 100 – geplant

FOURCC

dvh1

System

1080-60i

720-60uhr

1080-50i

LF (1)

0

0

0

Reserviert (1)

1

1

1

AF-Größe (6)

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

Audiomodus (4)

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

Qu (3)

000

000

000

Als Paket

    Audio Block 1\*

0xc0c31056

0xc0c31056

0xc0d31058

    Audio Block 2\*

0xc0c31156

0xc0c31156

0xc0d31158



 

> [!Note]  
> \* DVCPRO 100 weist 8 audioblöcke auf. die Blöcke 3 bis 8 werden nicht in der [dvinfo](dvinfo-field-settings-in-the-msdv-driver.md) -Struktur dargestellt.

 

## <a name="remarks"></a>Bemerkungen

Die folgenden Feldcodes sind von Interesse:

-   LF: Flag für gesperrten Modus. Gibt an, ob das Audiogerät gesperrt ist.
    -   0 = gesperrt
    -   1 = entsperrt
-   AF size: die Größe des Audioframes. Gibt die Anzahl von Audiobeispielen pro Frame an.

    IEC 61834-Definition:

    -   00:1111 = 1068 Stichproben pro Frame
    -   01:0000 = 1280 Stichproben pro Frame

    Definition von SMPTE 314m:

    -   01:0110 = 1602 Stichproben pro Frame
    -   01:1000 = 1920 Stichproben pro Frame

    Abhängig von der Framerate kann die genaue Anzahl von Stichproben in einem Frame variieren. Beispielsweise ist NTSC 30000/1001 Frames pro Sekunde (29,97 fps). Mit 32-kHz-Audiodaten sind ungefähr 1067,73 Audiobeispiele pro Frame vorhanden. Folglich ist der Nominalkurs 1068, die tatsächliche Zahl variiert jedoch je nach Frame. Außerdem kann die Anzahl von Audiobeispielen pro Frame mit entsperrtem Audiowert innerhalb eines bestimmten Zeitraums innerhalb eines bestimmten Zeitraums variieren.

<!-- -->

-   SM: Stereo Modus.
    -   0 = Stereo
    -   1 = Mono
-   CHN: Anzahl der Audiokanäle pro Audioblock.
    -   0 = ein Kanal pro Audioblock
    -   1 = zwei Kanäle pro Audioblock
-   Audiomodus: gibt den Inhalt des Audiosignals in jedem Kanal an. Die Interpretation dieses Felds hängt davon ab, welche Werte in den SM-und CHN-Feldern abgelegt werden. Die unten angegebenen Definitionen gelten für die Werte, die von msdv verwendet werden. Weitere Informationen finden Sie unter Spezifikationen.

    IEC 61834-Definition:

    -   0000 = ch a/c/e/g ist Linker Channel, ch b/d/f/h ist rechter Kanal
    -   1111 = keine Audiodaten

    Definition von SMPTE 314m:

    -   0000 = CH1 (CH3)
    -   0001 = CH2 (CH4)

-   50/60: Anzahl der Felder.
    -   0 = 60 Felder
    -   1 = 50 Felder
-   SType: Systemtyp.

    IEC 61834-Definition:

    -   00000 = 525-60 oder 625-50, DVSD
    -   00001 = 525-60 oder 625-50, dvsl (siehe IEC 61883-5)

    Definition von SMPTE 314m/SPMTE 370:

    -   00000 = 2 audioblöcke pro Videorahmen
    -   00010 = 4 audioblöcke pro Videorahmen
    -   00011 = 8 audioblöcke pro Videorahmen

-   SMP: Stichproben Häufigkeit.
    -   000 = 48 kHz
    -   010 = 32 kHz
-   Qu: Quantisierung.
    -   0 = 16 Bits linear
    -   1 = 12 Bits nicht linear

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dvinfo-Feld Einstellungen im msdv-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



