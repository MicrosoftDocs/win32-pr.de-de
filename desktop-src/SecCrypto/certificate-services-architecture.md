---
description: Eine Entwicklungsplattform zum Aufbauen von Zertifizierungsstellen für Unternehmen oder zum Sichern von Internet Anwendungen.
ms.assetid: 6f217682-94bc-4d18-88ea-2f8a06eb83de
title: Architektur der Zertifikat Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b7e0545b2f0fe0dd8c30d1863ffdf52c64a9e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214857"
---
# <a name="certificate-services-architecture"></a>Architektur der Zertifikat Dienste

Bei den Zertifikat Diensten handelt es sich um eine Entwicklungsplattform zum Aufbauen von Zertifizierungsstellen für Unternehmen oder für sichere Internet Anwendungen Eine konfigurierte und betriebsbereite Zertifizierungsstelle ermöglicht es einem Standort, Zertifikate mit minimalem Verwaltungsaufwand und maximaler Sicherheit auszugeben, zu verfolgen, zu verwalten und zu widerrufen.

Die Zertifikat Dienste bestehen aus der Server-Engine, der Server Datenbank und einem Satz von Modulen und Tools, die zusammenarbeiten, um als Zertifizierungsstelle zu fungieren. Externe Anwendungen, Module und Verwaltungs Tools verwenden Component Object Model (com)-Schnittstellen für die Interaktion mit der Server-Engine. Das folgende Diagramm zeigt die Schnittstellen, die von der Server-Engine verwendet werden:

![Architektur der Zertifikat Dienste](images/certapi.png)

Ein betriebsfähiges Zertifizierungssystem weist in der Regel vier Haupt Subsysteme auf.



| Subsystem             | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client                | Der-Client ist die Software, die vom Endbenutzer verwendet wird, um eine [*Zertifikat Anforderung*](../secgloss/c-gly.md)zu generieren, die Anforderung zu senden und das fertige Zertifikat zu empfangen. Ein Beispiel für einen Client ist Microsoft Internet Explorer Version 5. Der Client interagiert in der Regel mit einer benutzerdefinierten Schnittstelle, die von der Vermittler Anwendung verwaltet wird.                                                                                                                                                                                                                                                                                              |
| Mittl          | Der Vermittler ist ein Subsystem, das aus der Vermittler Anwendung und der Client Schnittstelle für Zertifikat Dienste (*zertifikatdienstewebclient* im Setup Programm) besteht. Die Vermittler Anwendung interagiert direkt mit dem Client, empfängt Zertifikat Anforderungen und gibt fertige Zertifikate zurück. Er kommuniziert mit der Server-Engine über die Client Schnittstelle der Zertifikat Dienste, die die COM-Schnittstellen [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) und [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) enthält. Ein Beispiel für eine Vermittler Anwendung ist Microsoft Internetinformationsdienste. Die Vermittler Anwendung kann vollständig über Active Server Seiten implementiert werden. |
| Server                | Der Server ist das System, von dem das Zertifikat erstellt wird. Zusätzlich zur Server-Engine sind zwei konfigurierbare Komponenten enthalten. das Richtlinien Modul und das Beendigungs Modul. Das Richtlinien Modul interagiert mit der Server-Engine über die Schnittstellen [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) und [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) . Beendigungs Module (es können mehr als eine vorhanden sein) interagieren mit der Server-Engine über die Schnittstellen [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) und [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) .                                                                                                                                                                                       |
| Verwaltungs Client | Der administrative Client ist das System zum Überwachen und Verwalten von Zertifikaten und Anforderungen. Der administrative Client verwendet die [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) -Schnittstelle für die Kommunikation mit der Server-Engine.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Weitere Informationen zur Architektur von Zertifikat Diensten finden Sie unter [kryptografieschnittstellen](cryptography-interfaces.md), [Aufbau eines Zertifikats](building-a-certificate.md)und in den folgenden Themen.



| `Section`                                      | Inhalt                                                                                                                                                                                                                                                                    |
|----------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Richtlinien Module](policy-modules.md)         | Anpassbare Programme, die während der Auswertung von [*Zertifikat Anforderungen*](../secgloss/c-gly.md)verwendet werden können. Diese Programme erzwingen die Regeln, nach denen die Zertifikat Dienste die Anforderung ausstellen oder verweigern. |
| [Beenden von Modulen](exit-modules.md)             | Anpassbare Programme, die beim Auftreten von Vorgängen Benachrichtigungen von der Server-Engine empfangen, z. b. Wenn ein Zertifikat ausgegeben wird.                                                                                                                                       |
| [Erweiterungs Handler](extension-handlers.md) | COM-Objekte, die Routinen zum Codieren komplexer Erweiterungen und Datentypen bereitstellen.                                                                                                                                                                                 |
| [Vermittler](intermediaries.md)         | Programme, die mit Client Anwendungen kommunizieren, um das Übermitteln von Zertifikat Anforderungen zuzulassen.                                                                                                                                                                        |



 

 

 
