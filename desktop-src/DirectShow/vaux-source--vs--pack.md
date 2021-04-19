---
description: Vaux-Quelle (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: Vaux-Quelle (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28f7ad2a91f1be1291b564013041e6dfa23bb014
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356261"
---
# <a name="vaux-source-vs-pack"></a>Vaux-Quelle (VS)

In den folgenden Tabellen sind die Werte aufgeführt, die vom msdv-Treiber verwendet werden, um den **dwdvvauxsrc** -Member der [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur auszufüllen. Weitere Informationen finden Sie unter [dvinfo Field Settings in the msdv Driver](dvinfo-field-settings-in-the-msdv-driver.md).

**Dvcr-Einstellungen**



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

TV-Kanal (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

TV-Kanal (4)

1111

1111

1111

1111

Quellcode (2)

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

0:0001

0:0001

0:0000

0:0000

Kategorie "Tuner" (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS-Paket

0xffc1ffff

0xffe1ffff

0xffc0ffff

0xffe0ffff



 

**DVCPRO-Einstellungen 25 und DVCPRO 50 (geplant)**



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

Reserviert (8)

1111:1111

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

1

EN (1)

1

1

1

1

CLF (2)

11

11

11

11

Reserviert (4)

1111

1111

1111

1111

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

0:0100

0:0100

Visc (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS-Paket

0x7fc0ffff

0x7fe0ffff

0x7fc4ffff

0x7fe4ffff



 

**Dvcr 100-Einstellungen (geplant)**



DV-Standard

DVCPRO 100 – geplant

FOURCC

dvh1

System

1080-60i

720-60uhr

1080-50i

Reserviert (8)

1111:1111

1111:1111

1111:1111

B/W (1)

1

1

1

EN (1)

1

1

1

CLF (2)

11

11

11

Reserviert (4)

1111

1111

1111

Reserviert (2)

11

11

11

50/60 (1)

0

0

1

STYPE (5)

1:0100

1:1000

1:0100

Visc (8)

1111:1111

1111:1111

1111:1111

VS-Paket

0x7fd4ffff

0x7fd8ffff

0x7ff4ffff



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Feldcodes sind von Interesse:

-   **B/W**: Schwarzes und Weißes Flag. 1 = Farbe.
-   **50/60**: Anzahl der Felder.
    -   0 = 60 Felder
    -   1 = 50 Felder
-   **SType**: Signaltyp.

    IEC 61834-Definition:

    -   0:0000 = 525-60 oder 625-50, DVSD
    -   0:0001 = 525-60 oder 625-50, dvsl (wie in IEC 61883-5 definiert)

    Definition von SMPTE 314m:

    -   0:0000 = 4:1:1-Komprimierung
    -   0:0100 = 4:2:2-Komprimierung

    SMPTE 370-Definition:

    -   1:0100 = 1080/60i (60 Hz) oder 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dvinfo-Feld Einstellungen im msdv-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



