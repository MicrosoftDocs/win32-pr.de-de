---
title: Informationen zu Active Directory Domain Services
description: Dieses Handbuch enthält wichtige Informationen zur Integration von Microsoft Active Directory in verteilte Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory unterstützen.
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory, Informationen zu
- Active Directory Domain Services Active Directory, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d8dafb89533d796f0651ad08b913eacda1d0fe9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039034"
---
# <a name="about-active-directory-domain-services"></a>Informationen zu Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>Schreiben leistungsfähiger Anwendungen, die Active Directory Domain Services verwenden

Dieses Handbuch enthält wichtige Informationen zur Integration von Active Directory Domain Services in verteilten Anwendungen, die für Betriebssysteme entwickelt wurden, die Active Directory Domain Services unterstützen, einschließlich:

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> Diese Themen gelten für Softwareentwickler. Informationen zu Problemen bei der Unterstützung finden Sie unter [Microsoft-Support](https://windows.microsoft.com/windows/support#1tc). Weitere Informationen zum Verwalten von Active Directory finden Sie unter [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) auf TechNet.

 

## <a name="fundamental-directory-features"></a>Grundlegende Verzeichnis Features

Ein Verzeichnisdienst ist ein grundlegender Dienst für verteilte Anwendungen. Ein Verzeichnisdienst muss die in der folgenden Tabelle aufgeführten Funktionen bereitstellen.



| Funktion               | BESCHREIBUNG                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| Standort Transparenz | Suchen von Benutzern, Gruppen, vernetzten Diensten oder Ressourcen, Daten ohne die Objekt Adresse           |
| Objektdaten           | Speichern von Benutzer-, Gruppen-, Organisations-und Dienst Daten in einer hierarchischen Struktur                    |
| Umfassende Abfrage            | Ein Objekt kann durch Abfragen von Objekteigenschaften gefunden werden.                                          |
| Hochverfügbarkeit     | Auffinden eines Replikats des Verzeichnisses an einem Speicherort, der für Lese-/Schreibvorgänge effizient ist |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Erweiterte Features von Active Directory Domain Services

Active Directory Domain Services stellt die Funktionen bereit, die in der folgenden Tabelle aufgeführt sind.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Funktion</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Unterstützung für Internet Standards</td>
<td>Active Directory Domain Services implementiert seine Features gemäß den veröffentlichten Internet Standards wie z. b. LDAP und DNS.</td>
</tr>
<tr class="even">
<td>Eng integrierte und flexible Sicherheit</td>
<td>Einige Vorteile:<br/>
<ul>
<li>Auswahl der Authentifizierungs Pakete. Kerberos, Secure Sockets Layer (SSL) oder eine Kombination richten Sie z. b. einen SSL-Kanal für die Verschlüsselung ein, und verwenden Sie Kerberos für die Authentifizierung.</li>
<li>Zentrale Verwaltung des Dienst-und Ressourcen Zugriffs mithilfe der Benutzer und Gruppen in Active Directory Domain Services.</li>
<li>Delegierung der Verwaltung, damit zentrale Administratoren administrative Aufgaben wie das Ändern von Kenn Wörtern oder das Erstellen und Löschen bestimmter Objekte delegieren können.</li>
<li>Der Active Directory Server verwendet die gleichen Zugriffs Steuerungsmechanismen, die für Dateisysteme in den Windows-Betriebssystemen verwendet werden. Folglich funktionieren die gleichen Tools, mit denen die Zugriffs Steuerung in einem Dateisystem verwaltet wird, für Active Directory Domain Services.</li>
<li>Umfassende Public Key-Infrastruktur Der Microsoft-Zertifikat Server und die Smartcard-Unterstützung sind in Active Directory Domain Services integriert, um die Smartcard-Anmeldung und Zertifikat Verwaltung bereitzustellen.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Leicht programmierbar</td>
<td>Auf den Active Directory Server kann Programm gesteuert zugegriffen werden, und er kann über die <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory Dienst Schnittstellen</a> -API, die <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol</a> -API oder den <a href="/dotnet/api/system.directoryservices">System. DirectoryServices</a> -Namespace verwaltet werden.</td>
</tr>
<tr class="even">
<td>Verzeichnis aktivierte Systemdienste</td>
<td>Die Client Anwendung kann auf einfache Weise auf verteilten Desktops bereitgestellt werden, indem ein Windows Installer Paket erstellt und das in den Windows-Betriebssystemen verfügbare Anwendungs Bereitstellungs Feature verwendet wird.</td>
</tr>
<tr class="odd">
<td>Schlüssel Anwendungsintegration</td>
<td>Wichtige verteilte Anwendungen, wie z. b. Exchange, sind in Active Directory Domain Services integriert. Daher können Unternehmen die Anzahl der zu verwaltenden Verzeichnisdienste reduzieren.</td>
</tr>
<tr class="even">
<td>Umfassendes und erweiterbares Schema</td>
<td>Das Schema definiert, welche Objekte und Eigenschaften von einem Verzeichnisdienst geschrieben und gelesen werden können. Das Active Directory Schema ist umfangreich. Die meisten Objekte und Eigenschaften, die ein Dienst benötigt, sind verfügbar. Andernfalls kann eine verteilte Anwendung das Schema so erweitern, dass die Anwendungsanforderungen unterstützt werden.</td>
</tr>
</tbody>
</table>



 

Weitere Informationen zu Active Directory Domain Services finden Sie unter:

-   [Grundlegende Konzepte von Active Directory Domain Services](core-concepts-of-active-directory-domain-services.md)
-   [Active Directory-Architektur](active-directory-domain-services-architecture.md)
-   [Active Directory-Schema](active-directory-schema.md)

