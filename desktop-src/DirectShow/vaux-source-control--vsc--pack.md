---
description: Vaux-Quell Code Verwaltungspaket (VSC)
ms.assetid: 9d5dd89e-9084-409d-86c0-30b57645d33d
title: Vaux-Quell Code Verwaltungspaket (VSC)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ed51363a15c0024dcaf3edca5d21217cb29396d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866444"
---
# <a name="vaux-source-control-vsc-pack"></a>Vaux-Quell Code Verwaltungspaket (VSC)

In den folgenden Tabellen sind die Werte aufgeführt, die vom msdv-Treiber verwendet werden, um den **dwdvvauxctl** -Member der [**dvinfo**](/windows/desktop/api/strmif/ns-strmif-dvinfo) -Struktur auszufüllen. Weitere Informationen finden Sie unter [dvinfo Field Settings in the msdv Driver](dvinfo-field-settings-in-the-msdv-driver.md).

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

Reserviert (1)

1

1

1

1

Modus "Rec" (2)

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

Il (1)

1

1

1

1

St (1)

1

1

1

1

SC (1)

1

1

1

1

Bcsys (2)

00

01

00

01

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

VSC-Paket

0xfffcc83f

0xfffdc83f

0xfffcc83f

0xfffdc83f



 

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

Il (1)

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

0xfffcc83f

0xfffcc83f

0xfffcc83f

0xfffcc83f



 

**DVCPRO 100-Einstellungen (geplant)**



DV-Standard

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

Il (1)

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

0xfffcca3f

0xfffcca3f

0xfffcca3f



 

## <a name="remarks"></a>Bemerkungen

Die folgenden Feldcodes sind von Interesse:

-   **CGMS**: Verwaltungssystem für die Kopier Generierung 0 = Kopieren ohne Einschränkung zulässig.

    Die tatsächlichen VSC-Pakete im DV-Stream können unterschiedliche Werte enthalten.

<!-- -->

-   **REC-Modus**: Aufzeichnungsmodus. 1 = Original.
-   **DISP**: zeigt den SELECT-Modus an. 000 = 4:3 Seitenverhältnis, vollständiges Format; 010 = 16:9-Seitenverhältnis.
-   **Bcsys**: Broadcast System. Dieses Feld definiert den Typ der Anzeigeinformationen für Breite Bildschirme.
    -   0 = Typ 0 (siehe IEC 61880)
    -   1 = Typ 1 (siehe ETSI EN 300 294)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> <dt>

[Dvinfo-Feld Einstellungen im msdv-Treiber](dvinfo-field-settings-in-the-msdv-driver.md)
</dt> </dl>

 

 



