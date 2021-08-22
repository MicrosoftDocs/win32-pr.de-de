---
description: VAUX-Quellcodeverwaltungspaket (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: VAUX-Quellcodeverwaltungspaket (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcdc91d5c4b2cea460c85b696c59bfce7799d39aed0a6bfcbc03f3d3c522a6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072074"
---
# <a name="vaux-source-control-vsc-pack"></a>VAUX-Quellcodeverwaltungspaket (VSC)

In den folgenden Tabellen sind die Werte aufgeführt, die vom MSDV-Treiber verwendet werden, um den **dwDVVAuxCtl-Member** der [**DVINFO-Struktur**](/windows/desktop/api/strmif/ns-strmif-dvinfo) auszufüllen. Weitere Informationen finden Sie unter [DVINFO-Feld Einstellungen im MSDV-Treiber.](dvinfo-field-settings-in-the-msdv-driver.md)

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

REC ST (1)

1

1

1

1

Reserviert (1)

1

1

1

1

REC-MODUS (2)

00

00

00

00

Reserviert (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

ST (1)

1

1

1

1

SC (1)

1

1

1

1

BCSYS (2)

00

01

00

01

Reserviert (1)

1

1

1

1

GENRE (7)

111:1111

111:1111

111:1111

111:1111

VSC-Paket

0xFFFCC83F

0xFFFDC83F

0xFFFCC83F

0xFFFDC83F



 

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

CGMS (2)

00

00

00

00

Reserviert (6)

11:1111

11:1111

11:1111

11:1111

Reserviert (2)

11

11

11

11

Reserviert (2)

00

00

00

00

Reserviert (1)

1

1

1

1

DISP (3)

000

000

000

000

FF (1)

1

1

1

1

FS (1)

1

1

1

1

FC (1)

1

1

1

1

IL (1)

1

1

1

1

Reserviert (2)

11

11

11

11

Reserviert (2)

00

00

00

00

Reserviert (8)

1111:1111

1111:1111

1111:1111

1111:1111

VSC-Paket

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F

0xFFFCC83F



 

**DVCPRO 100 Einstellungen (geplant)**



DV Standard

DVCPRO 100 – geplant

FOURCC

dvh1

System

1080-60i

720p-60p

1080-50i

CGMS (2)

00

00

00

Reserviert (6)

11:1111

11:1111

11:1111

Reserviert (2)

11

11

11

Reserviert (2)

00

00

00

Reserviert (1)

1

1

1

DISP (3)

010

010

010

FF (1)

1

1

1

FS (1)

1

1

1

FC (1)

1

1

1

IL (1)

1

1

1

Reserviert (2)

11

11

11

Reserviert (2)

00

00

00

Reserviert (8)

1111:1111

1111:1111

1111:1111

VSC-Paket

0xFFFCCA3F

0xFFFCCA3F

0xFFFCCA3F



 

## <a name="remarks"></a>Hinweise

Die folgenden Feldcodes sind von Interesse:

-   **CGMS:** Generierungsverwaltungssystem für Kopiervorgang. 0 = Kopiervorgang ohne Einschränkung zulässig.

    Die tatsächlichen VSC-Pakete im DV-Stream können unterschiedliche Werte enthalten.

<!-- -->

-   **REC MODE:** Aufzeichnungsmodus. 1 = Original.
-   **DISP:** Anzeigeauswahlmodus. 000 = Seitenverhältnis 4:3, vollständiges Format; 010 = Seitenverhältnis 16:9.
-   **BCSYS:** Broadcastsystem. Dieses Feld definiert den Typ der Breitbildschirmsignalisierungsinformationen.
    -   0 = Typ 0 (siehe IEC 61880)
    -   1 = Typ 1 (siehe ETSI EN 300 294)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[DVINFO-Feld Einstellungen im MSDV-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



