---
description: Die folgenden Funktionen werden von Diensten verwendet oder implementiert.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Dienstfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431a672e93c94e06a71812471aa3c74d0ac2f96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348155"
---
# <a name="service-functions"></a>Dienstfunktionen

Die folgenden Funktionen werden von Diensten verwendet oder implementiert.



| Funktion                                                             | BESCHREIBUNG                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Eine Anwendungs definierte Rückruffunktion, die mit der [**registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) -Funktion verwendet wird.     |
| [**Handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Eine Anwendungs definierte Rückruffunktion, die mit der [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion verwendet wird. |
| [**Registerservicectrlhandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Registriert eine Funktion zum Verarbeiten von Dienst Steuerungsanforderungen.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Registriert eine Funktion zum Verarbeiten erweiterter Dienst Steuerungsanforderungen.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Eine Anwendungs definierte Funktion, die als Ausgangspunkt für einen Dienst fungiert.                                                      |
| [**Setservicebits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Registriert einen Diensttyp mit dem Dienststeuerungs-Manager und dem Server Dienst.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Aktualisiert die Statusinformationen des Dienststeuerungs-Managers für den aufrufenden Dienst.                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Verbindet den Haupt Thread eines Dienst Prozesses mit dem Dienststeuerungs-Manager.                                                         |



 

Die folgenden Funktionen werden von Programmen verwendet, die-Dienste steuern, konfigurieren oder mit ihnen interagieren.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Ändert die Konfigurationsparameter eines Dienstanbieter.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Ändert die optionalen Konfigurationsparameter eines Dienstanbieter.                                                                                 |
| [**Closeservicehandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Schließt das angegebene Handle für ein Dienststeuerungs-Manager-Objekt oder ein Dienst Objekt.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Sendet einen Steuerungs Code an einen Dienst.                                                                                                          |
| [**Controlserviceex**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Sendet einen Steuerungs Code an einen Dienst.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Erstellt ein Dienst Objekt und fügt es der angegebenen Dienststeuerungs-Manager-Datenbank hinzu.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Markiert den angegebenen Dienst zum Löschen aus der Dienststeuerungs-Manager-Datenbank.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Ruft den Namen und den Status der einzelnen Dienste ab, die vom angegebenen Dienst abhängen.                                                        |
| [**EnumServicesStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Listet Dienste in der angegebenen Dienststeuerungs-Manager-Datenbank auf der Grundlage der angegebenen Informationsebene auf.                             |
| [**Getservicedisplayname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Ruft den anzeigen amen des angegebenen dienstanens ab.                                                                                        |
| [**Getservicekeyname**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Ruft den Dienstnamen des angegebenen dienstanens ab.                                                                                        |
| [**Notifybootconfigstatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Meldet den Startstatus für den Dienststeuerungs-Manager.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Ermöglicht es einer Anwendung, Benachrichtigungen zu empfangen, wenn der angegebene Dienst erstellt oder gelöscht wird oder wenn sich der Status ändert.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Stellt eine Verbindung mit dem Dienststeuerungs-Manager auf dem angegebenen Computer her und öffnet die angegebene Dienststeuerungs-Manager-Datenbank. |
| [**OpenService**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Öffnet einen vorhandenen Dienst.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Ruft die Konfigurationsparameter des angegebenen Dienstanbieter ab.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Ruft die optionalen Konfigurationsparameter des angegebenen Dienstanbieter ab.                                                                   |
| [**Queryservicedynamicinformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Ruft dynamische Informationen ab, die mit dem aktuellen Dienst Start verknüpft sind.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Ruft eine Kopie der einem Dienst Objekt zugeordneten Sicherheits Beschreibung ab.                                                               |
| [**QueryServiceStatus usex**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Ruft den aktuellen Status des angegebenen Dienstanbieter auf der Grundlage der angegebenen Informationsebene ab.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Legt die Sicherheits Beschreibung eines Dienst Objekts fest.                                                                                           |
| [**Start Service**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Startet einen Dienst.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen sind veraltet.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**Lock Service Database**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**Queryservicelockstatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**Unlockservicedatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
