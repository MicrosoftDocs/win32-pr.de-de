---
title: NAP-Schnittstellen
description: NAP-Schnittstellen
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b704e8924886047b0a50aef7929f52be276a0417d118f2026e47706f95678a2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620819"
---
# <a name="nap-interfaces"></a>NAP-Schnittstellen

> [!Note]  
> Die Netzwerkzugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Das NAP-System besteht aus den folgenden Schnittstellen.



| Schnittstellenname                                                                   | BESCHREIBUNG                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapCertRelyingParty**](inapcertrelyingparty.md)                             | Stellt Methoden bereit, die von zertifikatvertrauenden Seiten für die Kommunikation mit NapAgent verwendet werden müssen.                                                        |
| [**INapClientManagement**](inapclientmanagement.md)                             | Wird für die NAP-Clientverwaltung von SoH-Cache und SoH-Austauschtriggern verwendet. Veraltet.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Wird für die NAP-Clientverwaltung von SoH-Cache und SoH-Austauschtriggern verwendet.                                                                            |
| [**INapComponentConfig**](inapcomponentconfig.md)                               | Wird für die benutzerdefinierte Konfiguration von SHV-Komponenten verwendet. Veraltet.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit, um eine Netzwerkrichtlinienserver-Benutzeroberfläche (NETWORK Policy Server, NPS) remote zu konfigurieren.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Stellt NAP-Systemkonfigurationsmethoden für System health validators (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern. |
| [**INapComponentInfo**](inapcomponentinfo.md)                                   | Muss von Plug-In-Komponenten wie SHAs und SHVs implementiert werden, damit sie vom NAP-System kommuniziert werden können.                          |
| [**INapEnforcementClientBinding**](inapenforcementclientbinding.md)             | Wird von Erzwingungsclients für die Kommunikation mit NapAgent verwendet.                                                                                       |
| [**INapEnforcementClientCallback**](inapenforcementclientcallback.md)           | Erzwingungsclients müssen diese Schnittstelle implementieren, damit NapAgent mit ihnen kommunizieren kann.                                                  |
| [**INapEnforcementClientConnection**](inapenforcementclientconnection.md)       | Ermöglicht die Clientverbindungsverwaltung. Veraltet.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Ermöglicht die Clientverbindungsverwaltung.                                                                                                            |
| [**INapServerCallback**](inapservercallback.md)                                 | SHVs verwenden die einzelne Methode auf dieser Schnittstelle, um die asynchrone Anforderungsvervollständigung zu signalisieren.                                                             |
| [**INapServerInfo**](inapserverinfo.md)                                         | Wird von Verwaltungsclients (z. B. WMI-Anbieter, Befehlszeilentools usw.) zum Abfragen des Status des NAP-Serversystems verwendet.                             |
| [**INapServerManagement**](inapservermanagement.md)                             | Wird für die grundlegende Verwaltung des NAP-Servers verwendet.                                                                                                        |
| [**INapSoHConstructor**](inapsohconstructor.md)                                 | Wird von SHAs zum Erstellen von SoH-Anforderungen und von SHVs zum Erstellen von SoH-Antworten verwendet.                                                                      |
| [**INapSoHProcessor**](inapsohprocessor.md)                                     | Wird von SHAs zum Verarbeiten des Inhalts von SoH-Antworten und von SHVs zum Verarbeiten des Inhalts von SoH-Anforderungen verwendet.                                          |
| [**INapSystemHealthAgentBinding**](inapsystemhealthagentbinding.md)             | SHAs müssen diese Schnittstelle für die Kommunikation mit napagent verwenden. Veraltet.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | SHAs müssen diese Schnittstelle für die Kommunikation mit napagent verwenden.                                                                                      |
| [**INapSystemHealthAgentCallback**](inapsystemhealthagentcallback.md)           | SHAs müssen diese Schnittstelle implementieren, um die Verarbeitung mit dem NAP-System zu koordinieren.                                                                    |
| [**INapSystemHealthAgentRequest**](inapsystemhealthagentrequest.md)             | SHAs verwenden diese Schnittstelle, um ihre Verarbeitung mit dem NAP-System zu kommunizieren und zu koordinieren.                                                         |
| [**INapSystemHealthValidator**](inapsystemhealthvalidator.md)                   | Stellt Methoden bereit, die ein SHV implementieren muss, damit das NAP-System mit ihm kommunizieren kann.                                                         |
| [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)   | SHVs verwenden diese Schnittstelle für die Datenkommunikation mit ihrer clientseitigen Entsprechung. Veraltet.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | SHVs verwenden diese Schnittstelle für die Datenkommunikation mit ihrer clientseitigen Entsprechung.                                                                  |



 

 

 




