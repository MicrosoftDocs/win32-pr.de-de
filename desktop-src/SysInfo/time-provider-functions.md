---
description: Die folgenden Funktionen werden von Zeitanbietern verwendet.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Zeitanbieterfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884815"
---
# <a name="time-provider-functions"></a>Zeitanbieterfunktionen

Die folgenden Funktionen werden von Zeitanbietern verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Benachrichtigt das System, dass neue Beispiele verfügbar sind.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Ruft die Systemzeitstatusinformationen ab.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Protokolliert ein Zeitanbieterereignis im Ereignisprotokoll.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Legt die Statusinformationen des Zeitanbieters fest.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Gibt eine [**SetProviderStatusInfo-Struktur**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) frei.                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Eine Rückruffunktion, die vom Zeitanbieter-Manager aufgerufen wird, um den Zeitanbieter herunterfahren.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Eine Rückruffunktion, die vom Zeitanbieter-Manager aufgerufen wird, um Befehle an den Zeitanbieter zu senden. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Eine Rückruffunktion, die vom Zeitanbieter-Manager aufgerufen wird, wenn die Zeitanbieter-DLL geladen wird.  |



 

 

 



