---
description: Die Referenz zur Skripterstellungs-API für WMI beschreibt jedes Skriptobjekt mit einer bestimmten Syntax. Eine Erläuterung dieser Syntax finden Sie unter Dokumentkonventionen für die Skript-API.
ms.assetid: 91bc0fad-1a4b-4b48-b5a0-1a6502d2ab26
ms.tgt_platform: multiple
title: Skripterstellung für API-Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd639e1b1ca482a2b1aa95a4e0a6a26672480660440af290c043814ce5f8e965
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050308"
---
# <a name="scripting-api-objects"></a>Skripterstellung für API-Objekte

Die Referenz zur Skripterstellungs-API für WMI beschreibt jedes Skriptobjekt mit einer bestimmten Syntax. Eine Erläuterung dieser Syntax finden Sie unter [Dokumentkonventionen für die Skripterstellungs-API.](document-conventions-for-the-scripting-api.md)

In der folgenden Tabelle sind WMI-Skriptobjekte und deren Verwendung aufgeführt.



| Object                                               | BESCHREIBUNG                                                                                                                                                                                                                                            |
|------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SWbemDateTime**](swbemdatetime.md)               | Erstellt und analysiert [CIM-datetime-Werte.](date-and-time-format.md)                                                                                                                                                                                 |
| [**SWbemEventSource**](swbemeventsource.md)         | Ruft Ereignisse in Verbindung mit [**SWbemServices.ExecNotificationQuery**](swbemservices-execnotificationquery.md)ab.                                                                                                                               |
| [**SWbemLastError**](swbemlasterror.md)             | Stellt erweiterte Fehlerinformationen bereit, wenn ein Fehler auftritt.                                                                                                                                                                                              |
| [**SWbemLocator**](swbemlocator.md)                 | Ruft ein [**SWbemServices-Objekt**](swbemservices.md) ab, das Zugriff auf WMI auf einem bestimmten Hostcomputer erhalten kann.                                                                                                                                     |
| [**SWbemMethod**](swbemmethod.md)                   | Enthält eine einzelne WMI-Methodendefinition.                                                                                                                                                                                                               |
| [**SWbemMethodSet**](swbemmethodset.md)             | Ruft eine Auflistung von [**SWbemMethod-Objekten**](swbemmethod.md) ab.                                                                                                                                                                                       |
| [**SWbemNamedValue**](swbemnamedvalue.md)           | Enthält einen einzelnen benannten Wert.                                                                                                                                                                                                                         |
| [**SWbemNamedValueSet**](swbemnamedvalueset.md)     | Ruft den Zugriff auf eine Auflistung von [**SWbemNamedValue-Objekten**](swbemnamedvalue.md) ab.                                                                                                                                                                     |
| [**Swbemobject**](swbemobject.md)                   | Enthält eine einzelne WMI-Objektklasse oder -Instanz und bearbeitet sie.                                                                                                                                                                                        |
| [**SWbemObjectEx**](swbemobjectex.md)               | Erweitert die Funktionalität von [**SWbemObject**](swbemobject.md). Dieses Objekt fügt die [**Refresh-Methode**](swbemrefresher-refresh.md) für [**SWbemRefresher-Objekte**](swbemrefresher.md) hinzu.                                                           |
| [**SWbemObjectPath**](swbemobjectpath.md)           | Generiert und überprüft einen Objektpfad.                                                                                                                                                                                                                |
| [**SWbemObjectSet**](swbemobjectset.md)             | Ruft den Zugriff auf eine Auflistung von [**SWbemObject-Objekten**](swbemobject.md) ab.                                                                                                                                                                             |
| [**SWbemPrivilege**](swbemprivilege.md)             | Legt eine Berechtigung fest oder löscht sie.                                                                                                                                                                                                                            |
| [**SWbemPrivilegeSet**](swbemprivilegeset.md)       | Ruft den Zugriff auf eine Auflistung von [**SWbemPrivilege-Objekten**](swbemprivilege.md) ab.                                                                                                                                                                       |
| [**SWbemProperty**](swbemproperty.md)               | Enthält eine einzelne WMI-Eigenschaft.                                                                                                                                                                                                                        |
| [**SWbemPropertySet**](swbempropertyset.md)         | Ruft den Zugriff auf eine Auflistung von [**SWbemProperty-Objekten**](swbemproperty.md) ab.                                                                                                                                                                         |
| [**SWbemQualifier**](swbemqualifier.md)             | Enthält einen einzelnen Eigenschaftsqualifizierer.                                                                                                                                                                                                                  |
| [**SWbemQualifierSet**](swbemqualifierset.md)       | Ruft den Zugriff auf eine Auflistung von [**SWbemQualifier-Objekten**](swbemqualifier.md) ab.                                                                                                                                                                       |
| [**SWbemRefresher**](swbemrefresher.md)             | Erfasst und aktualisiert Objekteigenschaftswerte in einem Vorgang.                                                                                                                                                                                          |
| [**SWbemRefreshableItem**](swbemrefreshableitem.md) | Stellt ein einzelnes aktualisierbares Element in einem [**SWbemRefresher-Objekt**](swbemrefresher.md) dar, z. B. eine -Eigenschaft.                                                                                                                                     |
| [**SWbemSecurity**](swbemsecurity.md)               | Verwaltet Sicherheitseinstellungen wie Component Object Model [**-Berechtigungen**](swbemsecurity-privileges.md)(COM), [**AuthenticationLevel**](swbemsecurity-authenticationlevel.md)und [**ImpersonationLevel.**](swbemsecurity-impersonationlevel.md)   |
| [**Swbemservices**](swbemservices.md)               | Erstellt, aktualisiert und ruft Instanzen oder Klassen ab.                                                                                                                                                                                                  |
| [**SWbemServicesEx**](swbemservicesex.md)           | Erweitert die Funktionalität von [**SWbemServices.**](swbemservices.md) Dieses Objekt fügt die [**Put-**](swbemservicesex-put.md) und [**PutAsync-Methoden**](swbemservicesex-putasync.md) hinzu, damit eine Klasse oder Instanz in mehreren Namespaces gespeichert werden kann. |
| [**SWbemSink**](swbemsink.md)                       | Empfängt die Ergebnisse von asynchronen Vorgängen und Ereignisbenachrichtigungen, die von Clientanwendungen verwendet werden.                                                                                                                                        |



 

 

 



