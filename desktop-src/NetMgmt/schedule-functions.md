---
title: Zeit Plan Funktionen
description: Die Dienstfunktionen für den Netzwerk Verwaltungs Zeitplan übermitteln und verwalten Aufträge, die auf einem bestimmten Computer zu einem bestimmten Zeitpunkt (oder Uhrzeiten) ausgeführt werden.
ms.assetid: 1ddc9b95-fdbc-4e39-9b55-2a5bc570b95d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3421ae46de8e8152356f64d3855b4fe95c228878
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106342150"
---
# <a name="schedule-functions"></a>Zeit Plan Funktionen

Die Dienstfunktionen für den Netzwerk Verwaltungs Zeitplan übermitteln und verwalten Aufträge, die auf einem bestimmten Computer zu einem bestimmten Zeitpunkt (oder Uhrzeiten) ausgeführt werden. Aufträge können Befehle und Programme enthalten. Die-Funktionen verwalten Aufträge auf Remote Computern und lokalen Computern, sofern der Zeit Plan Dienst auf dem Computer ausgeführt wird.

Die Zeit Plan Dienstfunktionen sind nachfolgend aufgeführt.



| Funktion                                                                     | BESCHREIBUNG                                                      |
|------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd)                               | Sendet einen Auftrag, der zu einem bestimmten Zeitpunkt (Datum und Uhrzeit) ausgeführt wird.        |
| [**NetScheduleJobDel**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobdel)                               | Bricht einen Bereich von Aufträgen in der Warteschlange ab, die auf einem Computer ausgeführt werden.             |
| [**Netschedulejobenum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum)                             | Listet die Aufträge auf einem angegebenen Computer auf.                   |
| [**Netschedulejobgetinfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo)                       | Gibt Informationen zu einem bestimmten Auftrag auf einem Computer in der Warteschlange zurück. |
| [**Getnetscheduleaccountinformation**](/windows/desktop/api/AtAcct/nf-atacct-getnetscheduleaccountinformation) | Ruft den unter Dienst Kontonamen ab.                           |
| [**Setnetscheduleaccountinformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation) | Legt den unter Dienst Kontonamen und das Kennwort fest.                   |



 

Damit die Funktionen für den Netzwerk Verwaltungs Zeitplan erfolgreich sind, muss ein Aufrufer auf dem Computer, auf dem der Zeit Plan Dienst ausgeführt wird, über Administratorrechte verfügen. Die Zeit Plan Dienstfunktionen werden auch als "Job"-und "at Command"-Funktionen bezeichnet. Weitere Informationen zum Aufrufen von Funktionen, für die Administratorrechte erforderlich sind, finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).

Die [**at \_ Info**](/windows/desktop/api/Lmat/ns-lmat-at_info) -Struktur wird von der [**NetScheduleJobAdd**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobadd) -Funktion verwendet, um beim Senden eines Auftrags Informationen anzugeben, und von der [**netschedulejobgetinfo**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobgetinfo) -Funktion zum Abrufen von Informationen zu einem Auftrag, der übermittelt wurde. Die [**at \_**](/windows/desktop/api/Lmat/ns-lmat-at_enum) -enumerationsstruktur wird von [**netschedulejobenum**](/windows/desktop/api/Lmat/nf-lmat-netschedulejobenum) zum Auflisten und Zurückgeben von Informationen zu einer gesamten Warteschlange von übermittelten Aufträgen verwendet.

 

 