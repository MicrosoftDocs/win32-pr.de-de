---
title: NAP-Schnittstellen
description: NAP-Schnittstellen
ms.assetid: fff854b9-9c83-4db2-bceb-22509b261a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ff67fe21922c5b1baf9c2825dc7ea2852f14331
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037472"
---
# <a name="nap-interfaces"></a>NAP-Schnittstellen

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Das NAP-System besteht aus den folgenden Schnittstellen.



| Schnittstellenname                                                                   | BESCHREIBUNG                                                                                                                                         |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Inapcertrelyingparty**](inapcertrelyingparty.md)                             | Stellt Methoden bereit, die von Zertifikat vertrauenden Seiten für die Kommunikation mit dem NAPAgent verwendet werden müssen.                                                        |
| [**Inapclientmanagement**](inapclientmanagement.md)                             | Wird für die NAP-Client Verwaltung von SoH-Cache und SoH-Austausch Triggern verwendet. Veraltet.                                                                |
| [**INapClientManagement2**](inapclientmanagement2.md)                           | Wird für die NAP-Client Verwaltung von SoH-Cache und SoH-Austausch Triggern verwendet.                                                                            |
| [**Inapcomponentconfig**](inapcomponentconfig.md)                               | Wird für die angepasste Konfiguration von SHV-Komponenten verwendet. Veraltet.                                                                                    |
| [**INapComponentConfig2**](inapcomponentconfig2.md)                             | Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um eine Netzwerk Richtlinien Server-Benutzeroberfläche (NPS) Remote zu konfigurieren.   |
| [**INapComponentConfig3**](inapcomponentconfig3.md)                             | Stellt NAP-System Konfigurations Methoden für System Integritätsprüfungen (SHVs) bereit, um Konfigurationsdaten für eine bestimmte Konfigurations-ID festzulegen und zu ändern. |
| [**Inapcomponentinfo**](inapcomponentinfo.md)                                   | Muss von Plug-in-Komponenten wie SHAs und SHVs implementiert werden, damit Sie vom NAP-System kommuniziert werden können.                          |
| [**Inapenforcementclientbinding**](inapenforcementclientbinding.md)             | Wird von Erzwingungs Clients für die Kommunikation mit dem NAPAgent verwendet.                                                                                       |
| [**Inapenforcementclientcallback**](inapenforcementclientcallback.md)           | Erzwingungs Clients müssen diese Schnittstelle implementieren, damit der NAPAgent mit Ihnen kommunizieren kann.                                                  |
| [**Inapenforcementclientconnection**](inapenforcementclientconnection.md)       | Ermöglicht die clientverbindungsverwaltung. Veraltet.                                                                                                |
| [**INapEnforcementClientConnection2**](inapenforcementclientconnection2.md)     | Ermöglicht die clientverbindungsverwaltung.                                                                                                            |
| [**Inapservercallback**](inapservercallback.md)                                 | SHVs verwenden die einzige Methode für diese Schnittstelle, um den Abschluss einer asynchronen Anforderung zu signalisieren.                                                             |
| [**Inapserverinfo**](inapserverinfo.md)                                         | Wird von Verwaltungs Clients (z. b. WMI-Anbietern, Befehlszeilen Tools usw.) verwendet, um den Status des NAP-Server Systems abzufragen.                             |
| [**Inapservermanagement**](inapservermanagement.md)                             | Wird für die grundlegende Verwaltung des NAP-Servers verwendet.                                                                                                        |
| [**Inapsohconstructor**](inapsohconstructor.md)                                 | Wird von SHAs zum Erstellen von SoH-Anforderungen und von SHVs zum Erstellen von SoH-Antworten verwendet.                                                                      |
| [**Inapsohprocessor**](inapsohprocessor.md)                                     | Wird von SHAs verwendet, um den Inhalt von SoH-Antworten zu verarbeiten, und von SHVs, um den Inhalt von SoH-Anforderungen zu verarbeiten.                                          |
| [**Inapsystemhealthagentbinding**](inapsystemhealthagentbinding.md)             | SHAs müssen diese Schnittstelle für die Kommunikation mit dem NAPAgent verwenden. Veraltet.                                                                          |
| [**INapSystemHealthAgentBinding2**](inapsystemhealthagentbinding2.md)           | SHAs müssen diese Schnittstelle für die Kommunikation mit dem NAPAgent verwenden.                                                                                      |
| [**Inapsystemhealthagentcallback**](inapsystemhealthagentcallback.md)           | SHAs müssen diese Schnittstelle implementieren, um die Verarbeitung mit dem NAP-System zu koordinieren.                                                                    |
| [**Inapsystemhealthagentrequest**](inapsystemhealthagentrequest.md)             | SHAs verwenden diese Schnittstelle, um ihre Verarbeitung mit dem NAP-System zu kommunizieren und zu koordinieren.                                                         |
| [**Inapsystemhealthvalidator**](inapsystemhealthvalidator.md)                   | Stellt Methoden bereit, die ein SHV implementieren muss, damit das NAP-System damit kommunizieren kann.                                                         |
| [**Inapsystemhealthvalidationrequest**](inapsystemhealthvalidationrequest.md)   | SHVs verwenden diese Schnittstelle für die Datenkommunikation mit Ihrer Client seitigen Gegenüberstellung. Veraltet.                                                      |
| [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) | SHVs verwenden diese Schnittstelle für die Datenkommunikation mit Ihrer Client seitigen Gegenüberstellung.                                                                  |



 

 

 




