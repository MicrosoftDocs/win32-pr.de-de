---
description: Ein geschützter Server kann die folgenden Funktionen verwenden, um Überwachungsberichte im Sicherheits Ereignisprotokoll zu generieren.
ms.assetid: 4edee246-4fa7-4947-9737-34198f36e3ab
title: Überwachen des Zugriffs auf private Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3669841714fe9c24f6346404bc8634222bc4557e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960914"
---
# <a name="auditing-access-to-private-objects"></a>Überwachen des Zugriffs auf private Objekte

Ein geschützter Server kann die folgenden Funktionen verwenden, um Überwachungsberichte im Sicherheits Ereignisprotokoll zu generieren.



| Funktion                                                                                                     | BESCHREIBUNG                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Accesscheckandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckandauditalarma)                                                 | Identisch mit der [**AccessCheck**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheck) -Funktion, mit der Ausnahme, dass Sie Überwachungs Meldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generieren kann.                                                                            |
| [**Accesscheckbytypeandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytypeandauditalarma)                                     | Identisch mit der [**accesscheckbytype**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytype) -Funktion, mit der Ausnahme, dass Sie Überwachungs Meldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generieren kann.                                                                |
| [**Accesscheckbytyperesultlistandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma)                 | Identisch mit der [**accesscheckbytyperesultlist**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-accesscheckbytyperesultlist) -Funktion, mit der Ausnahme, dass Sie Überwachungs Meldungen für fehlgeschlagene oder erfolgreiche Zugriffsversuche generieren kann.                                            |
| [**Accesscheckbytyperesultlistandauditalarmyhandle**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarmbyhandlea) | Identisch mit der [**accesscheckbytyperesultlistandauditalarm**](/windows/desktop/api/Winbase/nf-winbase-accesscheckbytyperesultlistandauditalarma) -Funktion, mit der Ausnahme, dass der aufrufende Thread die Zugriffs Überprüfung vor der Identität des Clients durchführen kann. |
| [**Objectcloseauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectcloseauditalarma)                                                       | Generiert eine Überwachungs Meldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu schließen.                                                                                                                                   |
| [**Objectdeleteauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                       | Generiert eine Überwachungs Meldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu löschen.                                                                                                                                  |
| [**Objectopenauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectopenauditalarma)                                                         | Generiert eine Überwachungs Meldung, um anzugeben, dass ein Client versucht hat, ein privates Objekt zu öffnen oder zu erstellen.                                                                                                                          |
| [**Objectprivilegeauditalarm**](/windows/desktop/api/Winbase/nf-winbase-objectprivilegeauditalarma)                                               | Generiert eine Überwachungs Meldung, um anzugeben, dass ein Client versucht hat, einen angegebenen Berechtigungs Satz in Verbindung mit einem Zugriffs Versuch auf ein privates Objekt zu verwenden.                                                              |
| [**Privilegedserviceauditalarm**](/windows/desktop/api/Winbase/nf-winbase-privilegedserviceauditalarma)                                           | Generiert eine Überwachungs Meldung, um anzugeben, dass ein Client versucht hat, einen angegebenen Satz von Berechtigungen zu verwenden.                                                                                                                        |



 

 

 
