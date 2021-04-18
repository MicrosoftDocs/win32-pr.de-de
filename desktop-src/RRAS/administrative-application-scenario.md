---
title: Verwaltungs Anwendungsszenario
description: Administrative Anwendungen greifen auf eine Teilmenge von MGM-Funktionen zu, die sich auf das Auflisten von Multicast Weiterleitungs Einträgen (MFEs) und MFE-Statistiken beziehen.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c7d69b88503f7a4af18f0ab4650923a2845f5c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341456"
---
# <a name="administrative-application-scenario"></a>Verwaltungs Anwendungsszenario

Administrative Anwendungen greifen auf eine Teilmenge von MGM-Funktionen zu, die sich auf das Auflisten von Multicast Weiterleitungs Einträgen (MFEs) und MFE-Statistiken beziehen. Eine Anwendung muss nicht beim Multicast-Gruppen-Manager registriert werden, um diese Funktionen zu verwenden (d. h., die Anwendung benötigt kein Handle).

## <a name="enumerating-mfes"></a>Auflisten von MFEs

In der folgenden Tabelle werden eine Reihe von Schritten bei Interaktionen zwischen einer administrativen Anwendung und dem Multicast-Gruppen-Manager zusammengefasst. In der ersten Spalte werden die Aktionen beschrieben, die die administrative Anwendung ausführt, und die Antworten der administrativen Anwendung auf den Multicast-Gruppen-Manager. In der zweiten Spalte werden die Antworten des Multicast-Gruppen-Managers auf die administrative Anwendung beschrieben. Die dritte Spalte enthält alle zusätzlichen Informationen.

Jede Zeile der Tabelle stellt einen Schritt dar.



| Aktion für administrative Anwendung                                                                                                                                                                                      | Multicast-Gruppen-Manager-Aktion                                                                                                                                                                                                                                                              | Notizen                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrufen eines oder mehrerer MFEs mithilfe der [**mgmgetfirstmfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) -Funktion.                                                                                                                                   | Gibt so viele MFEs zurück, wie Sie in den vom Client bereitgestellten Puffer passen. Wenn keine MFEs im bereitgestellten Puffer zurückgegeben werden können, geben \_ Sie nicht ausreichenden \_ Puffer und die Größe des Puffers zurück, der zum Zurückgeben eines MFE benötigt wird.<br/>                                                              | Clients können auch MFE-Statistiken mithilfe der entsprechenden Statistikfunktionen, [**mgmgetfirstmfestats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) und [**mgmgetnextmfestats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats), abrufen. |
| Wenn \_ \_ der Puffer nicht ausreichend ist, können Sie die [**mgmgetfirstmfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) -Funktion erneut aufrufen, indem Sie einen Puffer der angegeben Größe verwenden.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Fahren Sie mit dem Aufruf der [**mgmgetnextmfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) -Funktion fort, und stellen Sie als einen der Parameter das letzte MFE bereit, das durch den vorherigen Aufruf der [**mgmgetfirstmfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) -Funktion zurückgegeben wurde. | Gibt so viele MFEs zurück, wie Sie in den vom Client bereitgestellten Puffer passen. Wenn keine MFEs im bereitgestellten Puffer zurückgegeben werden können, geben Sie nicht \_ ausreichenden \_ Puffer und die Größe des Puffers zurück, der für ein MFE benötigt wird.<br/> Gibt den Fehler \_ keine \_ weiteren Elemente zurück, \_ Wenn keine weiteren MFEs mehr vorhanden sind.<br/> |                                                                                                                                                                                                 |
| Setzen Sie die Enumeration fort, bis der Fehler \_ keine \_ weiteren \_ Elemente mehr empfangen.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Verwenden Sie die [**mgmgetmfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) -und [**mgmgetmfestats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) -Funktionen, um eine bestimmte MFE oder einen bestimmten Satz von MFE-Statistiken abzurufen.

 

 

 





