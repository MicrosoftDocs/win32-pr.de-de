---
description: Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen und aktualisierten Programmier Elemente für-Dienste.
ms.assetid: 4be7e244-ad4c-440d-b04e-23afb4c7ddf2
title: Neuerungen in den Diensten für Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51bd2e8bfa5426447e24485ed026f27e90fdcaa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369837"
---
# <a name="whats-new-in-services-for-windows-7"></a>Neues in den Diensten für Windows 7

Windows 7 und Windows Server 2008 R2 enthalten die folgenden neuen und aktualisierten Programmier Elemente für-Dienste.

## <a name="new-capabilities"></a>Neue Funktionen

Ein Dienst kann sich registrieren, um gestartet oder angehalten zu werden, wenn ein Auslöserereignis auftritt. Dadurch entfällt die Notwendigkeit, Dienste zu starten, wenn das System gestartet wird, oder Dienste, die auf ein Ereignis warten oder es aktiv warten. ein Dienst kann bei Bedarf gestartet werden, anstatt automatisch zu starten, ob eine Arbeit durchzuführen ist. Weitere Informationen finden Sie unter [Service Triggerereignisse](service-trigger-events.md).

## <a name="updated-functions"></a>Aktualisierte Funktionen



| Funktion                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangeServiceConfig**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfiga)<br/>   | Ändert die Konfigurationsparameter eines Dienstanbieter. Diese Funktion unterstützt verwaltete Dienst Konten und virtuelle Konten. Weitere Informationen finden Sie unter [schrittweise Anleitung für Dienst Konten](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/>                                      |
| [**ChangeServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-changeserviceconfig2a)<br/> | Ändert die optionalen Konfigurationsparameter eines Dienstanbieter. Diese Funktion unterstützt neue Konfigurations Informationsebenen für Prozessor Gruppen und Dienst Triggerereignisse.<br/>                                                                                                        |
| [**CreateService**](/windows/desktop/api/Winsvc/nf-winsvc-createservicea)<br/>               | Erstellt ein Dienst Objekt und fügt es der angegebenen Dienststeuerungs-Manager-Datenbank hinzu. Diese Funktion unterstützt verwaltete Dienst Konten und virtuelle Konten. Weitere Informationen finden Sie unter [schrittweise Anleitung für Dienst Konten](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/dd548356(v=ws.10)).<br/> |
| [**Handlerex**](/windows/desktop/api/WinSvc/nc-winsvc-lphandler_function_ex)<br/>                       | Eine Anwendungs definierte Rückruffunktion, die mit der [**RegisterServiceCtrlHandlerEx**](/windows/desktop/api/Winsvc/nf-winsvc-registerservicectrlhandlerexa) -Funktion verwendet wird. Diese Rückruffunktion unterstützt neue erweiterte Kontrollcodes für Systemzeit Änderungen und Dienst Triggerereignisse.<br/>                            |
| [**QueryServiceConfig2**](/windows/desktop/api/Winsvc/nf-winsvc-queryserviceconfig2a)<br/>   | Ruft die optionalen Konfigurationsparameter eines Dienstanbieter ab. Diese Funktion unterstützt neue Konfigurations Informationsebenen für Prozessor Gruppen und Dienst Triggerereignisse.<br/>                                                                                                      |
| [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)<br/>         | Aktualisiert die Statusinformationen des Dienststeuerungs-Managers für den aufrufenden Dienst. Diese Funktion unterstützt neue erweiterte Kontrollcodes für Systemzeit Änderungen und Dienst Triggerereignisse.<br/>                                                                                         |



 

## <a name="new-structures"></a>Neue Strukturen



| Struktur                                                                                       | BESCHREIBUNG                                                            |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| [**Dienst \_ Zeit Änderungs \_ Informationen**](/windows/desktop/api/winsvc/ns-winsvc-service_timechange_info)<br/>                         | Enthält Einstellungen für die Änderung der Systemzeit. <br/>                      |
| [**Dienst-Auslösung \_**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger)<br/>                                          | Stellt ein Dienst Auslöserereignis dar.<br/>                         |
| [**Dienst \_ \_ auslöserinformationen**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_info)<br/>                               | Enthält Informationen zu Ereignis auslöserereignissen für einen Dienst.<br/>           |
| [**Dienst \_ auslösende \_ spezifisches \_ Daten \_ Element**](/windows/desktop/api/winsvc/ns-winsvc-service_trigger_specific_data_item)<br/> | Enthält auslösende spezifische Daten für ein Dienst Auslöserereignis.<br/> |



 

 

