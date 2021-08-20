---
description: VAUX-Quellpaket (VS)
ms.assetid: 5ffd2883-0e56-459f-b229-cc014b894237
title: VAUX-Quellpaket (VS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 477e7a3257c11d6d8b42e16d2f066251452bc42a489abe9e666e374a565fa77c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072097"
---
# <a name="vaux-source-vs-pack"></a>VAUX-Quellpaket (VS)

In den folgenden Tabellen sind die Werte aufgeführt, die vom MSDV-Treiber verwendet werden, um den **dwDVVAuxSrc-Member** der [**DVINFO-Struktur**](/windows/desktop/api/strmif/ns-strmif-dvinfo) auszufüllen. Weitere Informationen finden Sie unter [DVINFO-Feld Einstellungen im MSDV-Treiber.](dvinfo-field-settings-in-the-msdv-driver.md)

**DVCR Einstellungen**



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

TV-KANAL (8)

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

TV-KANAL (4)

1111

1111

1111

1111

QUELLCODE (2)

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

TUNER CATEGORY (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0xFFC1FFFF

0xFFE1FFFF

0xFFC0FFFF

0xFFE0FFFF



 

**DVCPRO 25 und DVCPRO 50 Einstellungen (geplant)**



DV Standard

DVCPRO (SMPTE 314M) – geplant

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

VISC (8)

1111:1111

1111:1111

1111:1111

1111:1111

VS Pack

0x7FC0FFFF

0x7FE0FFFF

0x7FC4FFFF

0x7FE4FFFF



 

**DVCR 100 Einstellungen (geplant)**



DV Standard

DVCPRO 100 – Geplant

FOURCC

dvh1

System

1080-60i

720-60p

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

VISC (8)

1111:1111

1111:1111

1111:1111

VS Pack

0x7FD4FFFF

0x7FD8FFFF

0x7FF4FFFF



 

## <a name="remarks"></a>Hinweise

Die folgenden Feldcodes sind von Interesse:

-   **B/W:** Schwarz-Weiß-Flag. 1 = Farbe.
-   **50/60**: Anzahl der Felder.
    -   0 = 60 Felder
    -   1 = 50 Felder
-   **STYPE:** Signaltyp.

    IEC 61834-Definition:

    -   0:0000 = 525-60 oder 625-50, dvsd
    -   0:0001 = 525-60 oder 625-50, dvsl (wie in IEC 61883-5 definiert)

    SMPTE 314M-Definition:

    -   0:0000 = 4:1:1 Komprimierung
    -   0:0100 = 4:2:2 Komprimierung

    SMPTE 370-Definition:

    -   1:0100 = 1080/60i (60 Hz) oder 1080/50i (50 Hz)
    -   1:1000 = 720/60p

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DVINFO-Einstellungen im MSDV-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



