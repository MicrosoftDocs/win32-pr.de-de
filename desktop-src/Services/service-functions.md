---
description: Die folgenden Funktionen werden von Diensten verwendet oder implementiert.
ms.assetid: 63666848-cbac-4853-8b91-89303f9854c0
title: Dienstfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55553e29b2ae9fb8e60db2f421fd8aa68cee1c6b79542c7d3d61ef5bcef490f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118888962"
---
# <a name="service-functions"></a>Dienstfunktionen

Die folgenden Funktionen werden von Diensten verwendet oder implementiert.



| Funktion                                                             | BESCHREIBUNG                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [**Handler**](/windows/desktop/api/Winsvc/nc-winsvc-lphandler_function)                                           | Eine anwendungsdefinierte Rückruffunktion, die mit der [**RegisterServiceCtrlHandler-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera) verwendet wird.     |
| [**HandlerEx**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)                                       | Eine anwendungsdefinierte Rückruffunktion, die mit der [**RegisterServiceCtrlHandlerEx-Funktion**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) verwendet wird. |
| [**RegisterServiceCtrlHandler**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlera)     | Registriert eine Funktion zur Verarbeitung von Dienststeuerungsanforderungen.                                                                              |
| [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) | Registriert eine Funktion zur Verarbeitung erweiterter Dienststeuerungsanforderungen.                                                                     |
| [**ServiceMain**](/windows/win32/api/winsvc/nc-winsvc-lpservice_main_functiona)                                   | Eine anwendungsdefinierte Funktion, die als Ausgangspunkt für einen Dienst dient.                                                      |
| [**SetServiceBits**](/windows/desktop/api/Lmserver/nf-lmserver-setservicebits)                             | Registriert einen Diensttyp beim Dienststeuerungs-Manager und dem Serverdienst.                                                     |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)                         | Aktualisiert die Statusinformationen des Dienststeuerungs-Managers für den aufrufenden Dienst.                                                     |
| [**StartServiceCtrlDispatcher**](/windows/desktop/api/Winsvc/nf-winsvc-startservicectrldispatchera)     | Verbindet den Hauptthread eines Dienstprozesses mit dem Dienststeuerungs-Manager.                                                         |



 

Die folgenden Funktionen werden von Programmen verwendet, die Dienste steuern, konfigurieren oder mit ihnen interagieren.



| Funktion                                                                 | BESCHREIBUNG                                                                                                                                 |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)                       | Ändert die Konfigurationsparameter eines Diensts.                                                                                          |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)                     | Ändert die optionalen Konfigurationsparameter eines Diensts.                                                                                 |
| [**CloseServiceHandle**](/windows/desktop/api/Winsvc/nf-winsvc-closeservicehandle)                         | Schließt das angegebene Handle für ein Dienststeuerungs-Manager-Objekt oder ein Dienstobjekt.                                                        |
| [**ControlService**](/windows/desktop/api/Winsvc/nf-winsvc-controlservice)                                 | Sendet einen Steuerelementcode an einen Dienst.                                                                                                          |
| [**ControlServiceEx**](/windows/desktop/api/Winsvc/nf-winsvc-controlserviceexa)                             | Sendet einen Steuerelementcode an einen Dienst.                                                                                                          |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)                                   | Erstellt ein Dienstobjekt und fügt es der angegebenen Dienststeuerungs-Manager-Datenbank hinzu.                                                     |
| [**DeleteService**](/windows/desktop/api/Winsvc/nf-winsvc-deleteservice)                                   | Markiert den angegebenen Dienst zum Löschen aus der Dienststeuerungs-Manager-Datenbank.                                                         |
| [**EnumDependentServices**](/windows/desktop/api/Winsvc/nf-winsvc-enumdependentservicesa)                   | Ruft den Namen und den Status jedes Diensts ab, der vom angegebenen Dienst abhängt.                                                        |
| [**EnumServicesStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusexa)                     | Listet Dienste in der angegebenen Dienststeuerungs-Manager-Datenbank basierend auf der angegebenen Informationsebene auf.                             |
| [**GetServiceDisplayName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicedisplaynamea)                   | Ruft den Anzeigenamen des angegebenen Diensts ab.                                                                                        |
| [**GetServiceKeyName**](/windows/desktop/api/Winsvc/nf-winsvc-getservicekeynamea)                           | Ruft den Dienstnamen des angegebenen Diensts ab.                                                                                        |
| [**NotifyBootConfigStatus**](/windows/desktop/api/Winsvc/nf-winsvc-notifybootconfigstatus)                 | Meldet den Startstatus an den Dienststeuerungs-Manager.                                                                                     |
| [**NotifyServiceStatusChange**](/windows/desktop/api/Winsvc/nf-winsvc-notifyservicestatuschangea)           | Ermöglicht es einer Anwendung, Benachrichtigungen zu erhalten, wenn der angegebene Dienst erstellt oder gelöscht wird oder wenn sich der Status ändert.                 |
| [**OpenSCManager**](/windows/desktop/api/Winsvc/nf-winsvc-openscmanagera)                                   | Stellt eine Verbindung mit dem Dienststeuerungs-Manager auf dem angegebenen Computer her und öffnet die angegebene Dienststeuerungs-Manager-Datenbank. |
| [**Openservice**](/windows/desktop/api/Winsvc/nf-winsvc-openservicea)                                       | Öffnet einen vorhandenen Dienst.                                                                                                                  |
| [**QueryServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfiga)                         | Ruft die Konfigurationsparameter des angegebenen Diensts ab.                                                                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)                       | Ruft die optionalen Konfigurationsparameter des angegebenen Diensts ab.                                                                   |
| [**QueryServiceDynamicInformation**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicedynamicinformation) | Ruft dynamische Informationen im Zusammenhang mit dem aktuellen Dienststart ab.                                                                         |
| [**QueryServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-queryserviceobjectsecurity)    | Ruft eine Kopie der Sicherheitsbeschreibung ab, die einem Dienstobjekt zugeordnet ist.                                                               |
| [**QueryServiceStatusEx**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatusex)                     | Ruft den aktuellen Status des angegebenen Diensts basierend auf der angegebenen Informationsebene ab.                                             |
| [**SetServiceObjectSecurity**](/windows/desktop/api/winsvc/nf-winsvc-setserviceobjectsecurity)        | Legt die Sicherheitsbeschreibung eines Dienstobjekts fest.                                                                                           |
| [**Startservice**](/windows/desktop/api/Winsvc/nf-winsvc-startservicea)                                     | Startet einen Dienst.                                                                                                                           |



 

## <a name="obsolete-functions"></a>Veraltete Funktionen

Die folgenden Funktionen sind veraltet.<dl>

[**EnumServicesStatus**](/windows/desktop/api/Winsvc/nf-winsvc-enumservicesstatusa)  
[**LockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-lockservicedatabase)  
[**QueryServiceLockStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicelockstatusa)  
[**QueryServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-queryservicestatus)  
[**UnlockServiceDatabase**](/windows/desktop/api/Winsvc/nf-winsvc-unlockservicedatabase)  
</dl>

 

 
