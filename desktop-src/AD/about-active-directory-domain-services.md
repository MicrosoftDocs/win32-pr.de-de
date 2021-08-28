---
title: Informationen Active Directory Domain Services
description: Dieser Leitfaden enthält wichtige Informationen zur Integration von Microsoft Active Directory in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory unterstützen.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory , Informationen zu
- Active Directory Domain Services Active Directory , Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5db36807362ba5542fdc6a946905c7ba9f9189
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466607"
---
# <a name="about-active-directory-domain-services"></a>Informationen Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Schreiben leistungsstarker Anwendungen, die Active Directory Domain Services

Dieser Leitfaden enthält wichtige Informationen zur Integration von Active Directory Domain Services in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory Domain Services unterstützen, einschließlich:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Diese Themen sind für Softwareentwickler. Supportprobleme finden Sie unter [Microsoft-Support](https://windows.microsoft.com/windows/support#1tc). Informationen zum Verwalten von Active Directory finden Sie [unter](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) Active Directory Domain Services techNet.

 

## <a name="fundamental-directory-features"></a>Grundlegende Verzeichnisfunktionen

Ein Verzeichnisdienst ist ein grundlegender Dienst für verteilte Anwendungen. Ein Verzeichnisdienst muss die in der folgenden Tabelle aufgeführten Funktionen bereitstellen.



| Funktion               | BESCHREIBUNG                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Standorttransparenz | In der Lage, Benutzer-, Gruppen-, Netzwerkdienst- oder Ressourcendaten ohne die Objektadresse zu finden           |
| Objektdaten           | Möglichkeit zum Speichern von Benutzer-, Gruppen-, Organisations- und Dienstdaten in einer hierarchischen Struktur                    |
| Umfangreiche Abfrage            | Suchen eines Objekts durch Abfragen von Objekteigenschaften                                          |
| Hochverfügbarkeit     | In der Lage, ein Replikat des Verzeichnisses an einem Speicherort zu finden, der für Lese-/Schreibvorgänge effizient ist |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Erweiterte Funktionen Active Directory Domain Services

Active Directory Domain Services enthält die in der folgenden Tabelle aufgeführten Funktionen.




| Funktion | BESCHREIBUNG | 
|---------|-------------|
| Unterstützung für Internetstandards | Active Directory Domain Services implementiert seine Features in Übereinstimmung mit veröffentlichten Internetstandards wie LDAP und DNS. | 
| Eng integrierte und flexible Sicherheit | Einige Vorteile:<br /><ul><li>Auswahl der Authentifizierungspakete. Kerberos, Secure Sockets Layer (SSL) oder eine Kombination; Richten Sie beispielsweise einen SSL-Kanal für die Verschlüsselung ein, und verwenden Sie dann Kerberos für die Authentifizierung.</li><li>Zentrale Verwaltung des Dienst- und Ressourcenzugriffs mithilfe der Benutzer und Gruppen in Active Directory Domain Services.</li><li>Delegierung der Verwaltung, damit zentrale Administratoren Administrative Aufgaben wie kennwortverändernde oder bestimmte Objekterstellung und -löschung delegieren können.</li><li>Der Active Directory-Server verwendet dieselben Zugriffssteuerungsmechanismen, die auch für Dateisysteme in den Windows verwendet werden. Daher funktionieren dieselben Tools, die die Zugriffssteuerung in einem Dateisystem verwalten, für Active Directory Domain Services.</li><li>Umfassende Public Key-Infrastruktur. Die Unterstützung für Den Microsoft-Zertifikatserver und Smartcards ist in Active Directory Domain Services integriert, um Smartcardanmeldung und Zertifikatverwaltung zu ermöglichen.</li></ul> | 
| Einfach programmierbar | Auf den Active Directory-Server kann programmgesteuert über die Active Directory-Dienstschnittstellen-API, die Lightweight <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Directory</a> <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Access Protocol-API</a> oder den <a href="/dotnet/api/system.directoryservices">System.DirectoryServices-Namespace</a> zugegriffen und verwaltet werden. | 
| Verzeichnisfähige Systemdienste | Ihre Clientanwendung kann problemlos auf verteilten Desktops bereitgestellt werden, indem sie ein Windows Installer-Paket erstellt und die im Windows verfügbaren Anwendungsbereitstellungsfunktion verwendet. | 
| Wichtige Anwendungsintegration | Wichtige verteilte Anwendungen, z. B. Exchange, sind in Active Directory Domain Services. Daher können Unternehmen die Anzahl der zu verwaltenden Verzeichnisdienste reduzieren. | 
| Umfassendes und erweiterbares Schema | Das Schema definiert, welche Objekte und Eigenschaften geschrieben und aus einem Verzeichnisdienst gelesen werden können. Das Active Directory-Schema ist sehr aktiv. Die meisten Objekte und Eigenschaften, die für einen Dienst erforderlich sind, sind verfügbar. Falls nicht, kann eine verteilte Anwendung das Schema erweitern, um die Anwendungsanforderungen zu unterstützen. | 




 

Weitere Informationen zu Active Directory Domain Services finden Sie unter:

-   [Grundlegende Konzepte der Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Active Directory-Architektur](active-directory-domain-services-architecture.md)
-   [Active Directory-Schema](active-directory-schema.md)

