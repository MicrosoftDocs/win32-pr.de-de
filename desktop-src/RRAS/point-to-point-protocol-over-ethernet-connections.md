---
title: Point-to-Point-Protokoll über Ethernet-Verbindungen
description: Windows Server 2003, Windows XP und höher bieten Unterstützung für Point-to-Point-Protokoll Over Ethernet (PPPoE). Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der RASENTRY-Struktur fest.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92703bac13d129ed29cee1c22328825de67325239c1906c1728b96d53398647b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789810"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Point-to-Point-Protokoll über Ethernet-Verbindungen

Windows Server 2003, Windows XP und höher bieten Unterstützung für Point-to-Point-Protokoll Over Ethernet (PPPoE). Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der [**RASENTRY-Struktur**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) fest.



| Member                      | Wert             |
|-----------------------------|-------------------|
| RASENTRY.dwType             | \_RASET-Breitband  |
| RAENTRY.szDeviceType        | RASDT \_ PPPoE      |
| RASENTRY.szLocalPhoneNumber | Der Name des Diensts. |



 

Verwenden Sie [**die RasSetEntryProperties-Funktion,**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) um diese Werte festlegen.

Sie können auch [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) und das RASEDFLAG \_ NewBroadbandEntry-Flag für [**RASENTRYDLG**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) verwenden, um einen Assistenten zum Erstellen eines PPPoE-Telefonbucheintrags anzuzeigen.

 

 