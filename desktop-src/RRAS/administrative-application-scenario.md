---
title: Szenario für administrative Anwendungen
description: Administrative Anwendungen rufen eine Teilmenge von MGM-Funktionen auf, die sich auf das Aufzählen von Multicastweiterleitungseinträgen (MFEs) und MFE-Statistiken bezieht.
ms.assetid: ed172425-6d1e-45d8-8076-7705e833bfd5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527c8574a0e6ab85fe4e826a224377fa0de5de3851b7e31264b4c68c3c2fce56
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117791915"
---
# <a name="administrative-application-scenario"></a>Szenario für administrative Anwendungen

Administrative Anwendungen rufen eine Teilmenge von MGM-Funktionen auf, die sich auf das Aufzählen von Multicastweiterleitungseinträgen (MFEs) und MFE-Statistiken bezieht. Eine Anwendung muss sich nicht beim Multicastgruppen-Manager registrieren, um diese Funktionen verwenden zu können (d. h., die Anwendung benötigt kein Handle).

## <a name="enumerating-mfes"></a>Aufzählen von MFEs

In der folgenden Tabelle sind eine Reihe von Schritten in interaktionen zwischen einer administrativen Anwendung und dem Multicastgruppen-Manager zusammengefasst. Die erste Spalte beschreibt die Aktionen, die von der Administrativen Anwendung durchgeführt werden, und die Antworten der administrativen Anwendung an den Multicastgruppen-Manager. In der zweiten Spalte werden die Antworten des Multicastgruppen-Managers auf die administrative Anwendung beschrieben. In der dritten Spalte werden zusätzliche Informationen angezeigt.

Jede Zeile der Tabelle stellt einen Schritt dar.



| Administrative Anwendungsaktion                                                                                                                                                                                      | Multicastgruppen-Manager-Aktion                                                                                                                                                                                                                                                              | Hinweise                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Abrufen einer oder mehrere MFEs mithilfe der [**MgmGetFirstMfe-Funktion.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)                                                                                                                                   | Gibt so viele MFEs zurück, wie in den vom Client bereitgestellten Puffer passen. Wenn im angegebenen Puffer keine MFEs zurückgegeben werden können, geben Sie ERROR INSUFFICIENT BUFFER und die Größe des Puffers zurück, der zum Zurückgeben eines \_ \_ MFE erforderlich ist.<br/>                                                              | Clients können MFE-Statistiken auch mithilfe der entsprechenden Statistikfunktionen [**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats) und [**MgmGetNextMfeStats abrufen.**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats) |
| Wenn ERROR INSUFFICIENT BUFFER empfangen wird, rufen Sie \_ die \_ [**MgmGetFirstMfe-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) erneut mit einem Puffer der angegebenen Größe auf.                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |
| Rufen Sie weiterhin [**die MgmGetNextMfe-Funktion**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe) auf, und geben Sie als einen der Parameter den letzten MFE an, der durch den vorherigen Aufruf der [**MgmGetFirstMfe-Funktion zurückgegeben**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe) wurde. | Gibt so viele MFEs zurück, wie in den vom Client bereitgestellten Puffer passen. Wenn im angegebenen Puffer keine MFEs zurückgegeben werden können, geben Sie ERROR INSUFFICIENT BUFFER und die Größe des Puffers zurück, der für einen \_ \_ MFE benötigt wird.<br/> Gibt ERROR \_ NO \_ MORE ITEMS \_ zurück, wenn keine MFEs mehr verbleiben.<br/> |                                                                                                                                                                                                 |
| Setzen Sie die Enumeration fort, bis ERROR \_ NO MORE ITEMS empfangen \_ \_ wird.                                                                                                                                                     |                                                                                                                                                                                                                                                                                             |                                                                                                                                                                                                 |



 

> [!Note]  
> Verwenden Sie [**die Funktionen MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe) und [**MgmGetMfeStats,**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats) um einen bestimmten MFE- oder bestimmten Satz von MFE-Statistiken abzurufen.

 

 

 





