---
description: Aaux Source Control (ASC) Pack
ms.assetid: 3df80895-81e1-42a4-a095-913e77b199e5
title: Aaux Source Control (ASC) Pack
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eab942ccff1cf38e6962d508c9c9bfc99ea9fed6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747184"
---
# <a name="aaux-source-control-asc-pack"></a>Aaux Source Control (ASC) Pack

In den folgenden Tabellen sind die Werte aufgeführt, die vom msdv-Treiber zum Ausfüllen von **dwdvaauxctl** verwendet werden.

**dwDVAAuxCtl1** Member der [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur. Weitere Informationen finden Sie unter [dvinfo Field Settings in the msdv Driver](dvinfo-field-settings-in-the-msdv-driver.md).

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

CGMS (2)

00

00

00

00

ISR (2)

11

11

11

11

CMP (2)

11

11

11

11

SS (2)

11

11

11

11

REC St (1)

1

1

1

1

REC-Ende (1)

1

1

1

1

Modus "Rec" (3)

001

001

001

001

CH einfügen (3)

111

111

111

111

DRF (1)

1

1

1

1

Geschwindigkeit (7)

010:0000

010:0000

010:0000

010:0000

Reserviert (1)

1

1

1

1

Genre (7)

111:1111

111:1111

111:1111

111:1111

ASC Pack (beide audioblöcke)\*

0xffa0cf3f

0xffa0cf3f

0xffa0cf3f

0xffa0cf3f



 

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

CGMS (2)

00

00

00

00

Reserviert (4)

1111

1111

1111

1111

EFC (2)

00

00

00

00

REC St (1)

1

1

1

1

REC-Ende (1)

1

1

1

1

Fade St (1)

1

1

1

1

Ende ausblenden (1)

1

1

1

1

Reserviert (4)

1111

1111

1111

1111

DRF (1)

1

1

1

1

Geschwindigkeit (7)

111:1000

110:0100

111:1000

110:0100

Reserviert (8)

1111:1111

1111:1111

1111:1111

1111:1111

ASC Pack (beide audioblöcke)\*

0xffa0cf3f

0xffa0cf3f

0xffa0cf3f

0xffa0cf3f



 

\* Die *dvinfo* -Struktur enthält zwei Aaux als Pakete für audioblöcke 1 und 2. DV50 hat vier audioblöcke. die Blöcke 3 und 4 werden nicht in der *dvinfo* -Struktur dargestellt.

Dvcr 100-Einstellungen (geplant)



DV-Standard

DVCPRO 100 – geplant

FOURCC

dvh1

System

1080-60i

720-60uhr

1080-50i

CGMS (2)

00

00

00

Reserviert (4)

1111

1111

1111

EFC (2)

00

00

00

REC St (1)

1

1

1

REC-Ende (1)

1

1

1

Fade St (1)

1

1

1

Ende ausblenden (1)

1

1

1

Reserviert (4)

1111

1111

1111

DRF (1)

1

1

1

Geschwindigkeit (7)

111:1000

111:1000

110:0100

Reserviert (8)

1111:1111

1111:1111

1111:1111

ASC Pack (beide audioblöcke)\*

0xfff8ff3c

0xfff8ff3c

0xffe4ff3c



 

\* DVCPRO 100 weist 8 audioblöcke auf. die Blöcke 3 bis 8 werden nicht in der *dvinfo* -Struktur dargestellt.

## <a name="remarks"></a>Bemerkungen

Die folgenden Feldcodes sind von Interesse:

-   **CGMS**: Verwaltungssystem für die Kopier Generierung 0 = Kopieren ohne Einschränkung zulässig.

    Die eigentlichen ASC Packs im DV-Stream können unterschiedliche Werte enthalten.

<!-- -->

-   **REC-Modus**: Aufzeichnungsmodus. 1 = Original
-   **Geschwindigkeit**: VTR-Wiedergabegeschwindigkeit.

    IEC 61834-Definition:

    -   010:0000 = normale Geschwindigkeit, 525-60 oder 625-50

    Definition von SMPTE 314m:

    -   111:1000 = normale Geschwindigkeit, 525-60
    -   110:0100 = normale Geschwindigkeit, 625-50

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dvinfo-Feld Einstellungen im msdv-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



