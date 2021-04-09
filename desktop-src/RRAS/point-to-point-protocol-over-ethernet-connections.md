---
title: Point-to-Point-Protokoll über Ethernet-Verbindungen
description: Windows Server 2003, Windows XP und spätere Betriebssysteme bieten Unterstützung für Point-to-Point-Protokoll over Ethernet (PPPoE). Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der rasentry-Struktur fest.
ms.assetid: abdbf22c-abeb-4363-bfa6-e0002d1637f4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed66d3a694896bdec9e0f53215a782d5896cd38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949041"
---
# <a name="point-to-point-protocol-over-ethernet-connections"></a>Point-to-Point-Protokoll über Ethernet-Verbindungen

Windows Server 2003, Windows XP und spätere Betriebssysteme bieten Unterstützung für Point-to-Point-Protokoll over Ethernet (PPPoE). Legen Sie für eine PPPoE-Verbindung die folgenden Werte in der [**rasentry**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) -Struktur fest.



| Member                      | Wert             |
|-----------------------------|-------------------|
| Rasentry. dwType             | Breitband- \_ Breitband  |
| Raentry. szde vicetype        | Rasdt \_ PPPoE      |
| Rasentry. szlocalphonenumber | Der Name des Diensts. |



 

Verwenden Sie die [**rassetentryproperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) -Funktion, um diese Werte festzulegen.

Sie können auch die Datei " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " und das Flag "rasedflag \_ newbroadbandentry" für " [**RasEntryDlg**](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga) " verwenden, um einen Assistenten zum Erstellen eines PPPoE Phonebook-Eintrags anzuzeigen.

 

 