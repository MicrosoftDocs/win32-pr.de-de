---
title: Informationen Active Directory Domain Services
description: Dieser Leitfaden enthält wichtige Informationen zur Integration von Microsoft Active Directory in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory unterstützen.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory , Informationen
- Active Directory Domain Services Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e4ef886409b435e1687d8ca6cf530b940852f3569818bb3afab69f57ab6b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841074"
---
# <a name="about-active-directory-domain-services"></a>Informationen Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Schreiben leistungsstarker Anwendungen, die Active Directory Domain Services verwenden

Dieser Leitfaden enthält wichtige Informationen zur Integration von Active Directory Domain Services in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory Domain Services unterstützen, einschließlich:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Diese Themen sind für Softwareentwickler vorgesehen. Supportprobleme finden Sie unter [Microsoft-Support](https://windows.microsoft.com/windows/support#1tc). Informationen zum Verwalten von Active Directory finden Sie unter [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) unter TechNet.

 

## <a name="fundamental-directory-features"></a>Grundlegende Verzeichnisfunktionen

Ein Verzeichnisdienst ist ein grundlegender Dienst für verteilte Anwendungen. Ein Verzeichnisdienst muss die in der folgenden Tabelle aufgeführten Funktionen bereitstellen.



| Funktion               | Beschreibung                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Standorttransparenz | In der Lage, Benutzer-, Gruppen-, Netzwerkdienst- oder Ressourcendaten ohne die Objektadresse zu finden           |
| Objektdaten           | Speichern von Benutzer-, Gruppen-, Organisations- und Dienstdaten in einer hierarchischen Struktur                    |
| Umfangreiche Abfrage            | Suchen eines Objekts durch Abfragen von Objekteigenschaften                                          |
| Hochverfügbarkeit     | In der Lage, ein Replikat des Verzeichnisses an einem Speicherort zu finden, der für Lese-/Schreibvorgänge effizient ist |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Erweiterte Features von Active Directory Domain Services

Active Directory Domain Services stellt die in der folgenden Tabelle aufgeführten Features bereit.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unterstützung für Internetstandards</td>
<td>Active Directory Domain Services implementiert seine Features in Übereinstimmung mit veröffentlichten Internetstandards wie LDAP und DNS.</td>
</tr>
<tr class="even">
<td>Eng integrierte und flexible Sicherheit</td>
<td>Einige Vorteile:<br/>
<ul>
<li>Auswahl von Authentifizierungspaketen. Kerberos, Secure Sockets Layer (SSL) oder eine Kombination; Richten Sie beispielsweise einen SSL-Kanal für die Verschlüsselung ein, und verwenden Sie dann Kerberos für die Authentifizierung.</li>
<li>Zentrale Verwaltung des Dienst- und Ressourcenzugriffs mithilfe der Benutzer und Gruppen in Active Directory Domain Services.</li>
<li>Delegierung der Verwaltung, sodass zentrale Administratoren administrative Aufgaben delegieren können, z. B. Kennwortänderungen oder die Erstellung und Löschung bestimmter Objekte.</li>
<li>Der Active Directory-Server verwendet die gleichen Zugriffssteuerungsmechanismen, die auf Dateisystemen in den Windows Betriebssystemen verwendet werden. Daher funktionieren die gleichen Tools, die die Zugriffssteuerung in einem Dateisystem verwalten, für Active Directory Domain Services.</li>
<li>Umfassende Public Key-Infrastruktur. Die Unterstützung von Microsoft Certificate Server und Smartcards ist in Active Directory Domain Services integriert, um die Smartcardanmeldung und Zertifikatverwaltung bereitzustellen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Leicht programmierbar</td>
<td>Auf den Active Directory-Server kann programmgesteuert über die <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory-Dienstschnittstellen-API,</a> die Lightweight <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Directory-Zugriffsprotokoll-API</a> oder den <a href="/dotnet/api/system.directoryservices">System.DirectoryServices-Namespace</a> zugegriffen und verwaltet werden.</td>
</tr>
<tr class="even">
<td>Verzeichnisfähige Systemdienste</td>
<td>Ihre Clientanwendung kann problemlos auf verteilten Desktops bereitgestellt werden, indem sie ein Windows Installer-Paket erstellt und das Anwendungsbereitstellungsfeature verwendet, das in den Windows Betriebssystemen verfügbar ist.</td>
</tr>
<tr class="odd">
<td>Wichtige Anwendungsintegration</td>
<td>Wichtige verteilte Anwendungen wie Exchange sind in Active Directory Domain Services integriert. Daher können Unternehmen die Anzahl der zu verwaltenden Verzeichnisdienste reduzieren.</td>
</tr>
<tr class="even">
<td>Umfangreiches und erweiterbares Schema</td>
<td>Das Schema definiert, welche Objekte und Eigenschaften aus einem Verzeichnisdienst geschrieben und gelesen werden können. Das Active Directory-Schema ist sehr umfangreiche. Die meisten Objekte und Eigenschaften, die ein Dienst benötigt, sind verfügbar. Andernfalls kann eine verteilte Anwendung das Schema erweitern, um die Anwendungsanforderungen zu unterstützen.</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu Active Directory Domain Services finden Sie unter:

-   [Grundlegende Konzepte der Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Active Directory-Architektur](active-directory-domain-services-architecture.md)
-   [Active Directory-Schema](active-directory-schema.md)

