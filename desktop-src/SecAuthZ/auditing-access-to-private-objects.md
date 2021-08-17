---
description: Ein geschützter Server kann die folgenden Funktionen verwenden, um Überwachungsberichte im Sicherheitsereignisprotokoll zu generieren.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Überwachen des Zugriffs auf private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eac3a38a9f0af292a77a539491e0cea5f1faf40b570f34a35371ad43a7abe757
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117784591"
---
# <a name="auditing-access-to-private-objects"></a>Überwachen des Zugriffs auf private Objekte

Ein geschützter Server kann die folgenden Funktionen verwenden, um Überwachungsberichte im Sicherheitsereignisprotokoll zu generieren.



| Funktion                                                                                                     | Beschreibung                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AccessCheckAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Identisch mit der [**AccessCheck-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) mit der Ausnahme, dass überwachungsmeldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generiert werden können.                                                                            |
| [**AccessCheckByTypeAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Identisch mit der [**AccessCheckByType-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) mit der Ausnahme, dass überwachungsmeldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generiert werden können.                                                                |
| [**AccessCheckByTypeResultListAndAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Identisch mit der [**AccessCheckByTypeResultList-Funktion,**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) mit der Ausnahme, dass überwachungsmeldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generiert werden können.                                            |
| [**AccessCheckByTypeResultListAndAuditAlarmByHandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Identisch mit der [**AccessCheckByTypeResultListAndAuditAlarm-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) mit der Ausnahme, dass der aufrufende Thread die Zugriffsüberprüfung durchführen kann, bevor die Identität des Clients angenommen wird. |
| [**ObjectCloseAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Generiert eine Überwachungsmeldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu schließen.                                                                                                                                   |
| [**ObjectDeleteAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Generiert eine Überwachungsmeldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu löschen.                                                                                                                                  |
| [**ObjectOpenAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Generiert eine Überwachungsmeldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu öffnen oder zu erstellen.                                                                                                                          |
| [**ObjectPrivilegeAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Generiert eine Überwachungsmeldung, um anzugeben, dass ein Client versucht hat, einen angegebenen Berechtigungssatz in Verbindung mit einem Versuch zu verwenden, auf ein privates Objekt zu zugreifen.                                                              |
| [**PrivilegedServiceAuditAlarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Generiert eine Überwachungsmeldung, um anzugeben, dass ein Client versucht hat, einen angegebenen Berechtigungssatz zu verwenden.                                                                                                                        |



 

 

 
