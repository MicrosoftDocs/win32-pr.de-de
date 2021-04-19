---
description: Die folgenden Funktionen werden von Zeit Anbietern verwendet.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Zeit Anbieter Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20a24f15bd67751dc09a689078a8a518224267c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352621"
---
# <a name="time-provider-functions"></a>Zeit Anbieter Funktionen

Die folgenden Funktionen werden von Zeit Anbietern verwendet.



| Funktion                                                               | BESCHREIBUNG                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**Alertsamplesavailfunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Benachrichtigt das System, dass neue Beispiele vorhanden sind.                                              |
| [**Gettimesysinfofunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Ruft die Systemzeit Zustandsinformationen ab.                                                           |
| [**Logtimeproveventfunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Protokolliert ein Zeit Anbieter Ereignis im Ereignisprotokoll.                                                           |
| [**Setproviderstatus-Func**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Legt die Statusinformationen des Zeit Anbieters fest.                                                           |
| [**Setproviderstatusinfofreifunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Gibt eine [**setproviderstatusinfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) -Struktur frei.                          |
| [**Timeprovclose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Eine Rückruffunktion, die vom Zeit Anbieter-Manager zum Herunterfahren des Zeit Anbieters aufgerufen wird.        |
| [**Timeprovcommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Eine Rückruffunktion, die vom Zeit Anbieter-Manager zum Senden von Befehlen an den Zeit Anbieter aufgerufen wird. |
| [**Timeprovopen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Eine Rückruffunktion, die vom Zeit Anbieter-Manager aufgerufen wird, wenn die Zeit Anbieter-DLL geladen wird.  |



 

 

 



