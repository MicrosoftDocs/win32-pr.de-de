---
description: Eine COM+-Anwendung ist im Wesentlichen ein deklaratives Konstrukt, mit dem Sie eine beliebige Anzahl gemeinsamer Komponenten konfigurieren können. Beispielsweise können Sie die Komponenten in einer Anwendung mit einer gemeinsamen Sicherheitsrichtlinie konfigurieren.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Konfigurieren von COM+-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 372d15e00898d88b3aed13ca2edaa03bc8a666ceb62dc1389af3e8f6959c971f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117916930"
---
# <a name="configuring-com-applications"></a>Konfigurieren von COM+-Anwendungen

Eine COM+-Anwendung ist im Wesentlichen ein deklaratives Konstrukt, mit dem Sie eine beliebige Anzahl gemeinsamer Komponenten konfigurieren können. Beispielsweise können Sie die Komponenten in einer Anwendung mit einer gemeinsamen Sicherheitsrichtlinie konfigurieren.

Die Konfiguration ist ein wesentlicher Bestandteil des Entwicklungsprozesses für COM+-Anwendungen. Wie Sie eine Anwendung konfigurieren, bestimmt, wie COM+ Dienste für sie bereitstellen wird und wie sie sich bei der Ausführung verhält.

Sie können COM+-Anwendungen entweder mit dem Verwaltungstool komponentendienste oder mithilfe der skriptierbaren Verwaltungsobjekte und -schnittstellen konfigurieren, die die zugrunde liegende Funktionalität des Verwaltungtools bereitstellen. Weitere Informationen zum Ausführen der Skriptverwaltung finden Sie unter [Automatisieren der COM+-Verwaltung.](automating-com--administration.md)

Sie können Elemente auf den folgenden Ebenen in COM+-Anwendungen konfigurieren:

-   [Anwendungsebene Einstellungen](#application-level-settings)
-   [Komponentenebene (Klassenebene) Einstellungen](#component-level-class-level-settings)
-   [Einstellung auf Schnittstellenebene](#interface-level-setting)
-   [Einstellung auf Methodenebene](#method-level-setting)
-   [Zugehörige Themen](#related-topics)

Die Art und Weise, wie Sie Komponenten in einer Anwendung installieren, kann sich darauf auswirken, wie Sie sie konfigurieren können. Sie sollten Komponenten immer in COM+-Anwendungen installieren (anstatt sie zu importieren). Durch die Installation von Komponenten werden sie zusammen mit Schnittstellen und Typbibliotheken vollständig in der COM+-Klassenregistrierungsdatenbank (RegDB) registriert, damit Sie sie konfigurieren können.

## <a name="application-level-settings"></a>Application-Level Einstellungen



| attribute                                                                                        | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aktivierung](context-activation.md)<br/>                                                  | Gibt den Anwendungstyp an: Serveranwendung oder Bibliotheksanwendung.<br/>                                                                                                            |
| [Aktivieren von Zugriffsüberprüfungen](enabling-access-checks-for-an-application.md)<br/>               | Aktiviert und deaktiviert die Sicherheitsüberprüfung.<br/>                                                                                                                                                      |
| [Sicherheitsstufe](setting-a-security-level-for-access-checks.md)<br/>                      | Gibt an, dass Zugriffsüberprüfungen auf Prozessebene (aus Rollen generierte Zugriffsprüfungsebenen) oder sowohl auf Prozess- als auch auf Komponentenebene (vollständige rollenbasierte Sicherheit) ausgeführt werden.<br/> |
| [Authentifizierungsebene](setting-an-authentication-level-for-a-server-application.md)<br/>  | Legt die Authentifizierungsebene fest, die für Aufrufe in der Anwendung verwendet wird.<br/>                                                                                                                        |
| [Identitätswechselebene](setting-an-impersonation-level.md)<br/>                             | Legt die Identitätswechselebene fest, die für Aufrufe anderer Anwendungen verwendet wird.<br/>                                                                                                                        |
| [Queuing](creating-queuable-components.md)<br/>                                           | Gibt an, dass Anwendungskomponenten Warteschlangendienste verwenden.<br/>                                                                                                                         |
| [Aktivieren von CRM](configuring-com--crm-components.md)<br/>                                     | Ermöglicht die Verwendung von kompensierenden Ressourcen-Managern.<br/>                                                                                                                                           |
| [Ausführen von Application-as-a-Service](com--applications-running-as-service-applications.md)<br/> | Konfiguriert und implementiert eine COM+-Serveranwendung als NT-Dienst.<br/>                                                                                                                    |
| [COM+-SOAP-Dienst](com--soap-service.md)<br/>                                            | Macht eine COM+-Anwendung als XML-Webdienst verfügbar.<br/>                                                                                                                                        |
| [Anwendungspooling](com--application-pooling.md)<br/>                                   | Fügt Skalierbarkeit für Singlethreadprozesse hinzu und ist in den COM+-Anwendungswiederverwendungsdienst integriert.<br/>                                                                               |
| [Wiederverwendung von Anwendungen](com--application-recycling.md)<br/>                               | Erhöht die Anwendungsstabilität, indem ein Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß heruntergefahren und neu gestartet wird.<br/>                                                                  |
| [Prozessdumping](what-s-new-in-com--1-5.md)<br/>                                         | Gibt den gesamten Zustand eines Prozesses zu Debugzwecken ab, ohne ihn zu beenden.<br/>                                                                                                      |
| Herunterfahren des Serverprozesses<br/>                                                               | Beendet einen Prozess nach einem angegebenen Leerlaufzeitraum.<br/>                                                                                                                                      |
| Berechtigungen<br/>                                                                           | Deaktiviert Änderungen an Konfigurationseinstellungen, einschließlich des Löschens.<br/>                                                                                                                          |
| Sicherheitsidentität<br/>                                                                     | Gibt die Identität an, unter der die Anwendung ausgeführt wird.<br/>                                                                                                                                 |
| Starten im Debugger<br/>                                                                    | Gibt an, dass die Anwendung in einem Debugger mit benutzerspezifischen Befehlszeileneinstellungen gestartet wird.<br/>                                                                                |
| Aktivieren der 3-GB-Unterstützung<br/>                                                                    | Ermöglicht die Verwendung des erweiterten Prozessspeicher-Adressraums.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level (Klassenebene) Einstellungen



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>attribute</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transaktionen</a><br/></td>
<td>Legt die Anforderungen für automatische Transaktionen deaktiviert, Nicht unterstützt, unterstützt, erforderlich oder Neu erforderlich fest.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Synchronisierung</a><br/></td>
<td>Legt die Synchronisierungsanforderungen Deaktiviert, Nicht unterstützt, Unterstützt, Erforderlich oder Neu erforderlich fest.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">JIT-Aktivierung</a><br/></td>
<td>Aktiviert die Just-In-Time-Aktivierung.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Objektpooling</a><br/></td>
<td>Aktiviert Objektpooling. Mindest- und Höchstwerte für Poolgröße und Objekt-Time out sind konfigurierbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Objektkonstruktion</a><br/></td>
<td>Ermöglicht die Parametrisierung der Objektkonstruktion mit einer vom Administrator angegebenen Konstruktorzeichenfolge. <br/>
<blockquote>
[!Note]<br />
Die Konstruktorzeichenfolge sollte nicht zum Speichern sicherheitssensibler Informationen verwendet werden.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Zugriffsüberprüfungen auf Komponentenebene</a><br/></td>
<td>Aktiviert oder deaktiviert die rollenbasierte Sicherheitsüberprüfung auf Komponentenebene.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Deklarative Rollenzuweisung</a><br/></td>
<td>Ermöglicht die explizite Zuweisung von Rollen zur Komponente.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Warteschlangenausnahmeklasse</a><br/></td>
<td>Gibt eine Ausnahmeklasse für die Behandlung clientseitiger Fehler an.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Instrumentierungsereignisse und Statistiken</a><br/></td>
<td>Aktiviert detaillierte Systemereignis- und Objektstatistikberichte.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Aktivierungskontext</a><br/></td>
<td>Aktiviert die erzwungene Aktivierung eines Objekts im Kontext oder Standardkontext des Aufrufers.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Erstellen privater Komponenten</a><br/></td>
<td>Markiert die Komponente als privat für die Anwendung. Eine private Komponente kann nur von anderen Komponenten in derselben Anwendung gesehen und aktiviert werden.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Interface-Level Einstellung



| attribute                                                                                           | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [In Warteschlange](creating-queuable-components.md)<br/>                                               | Gibt eine in IDL definierte Warteschlangenschnittstelle an.<br/>                                                                       |
| [Deklarative Rollenzuweisung](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Ermöglicht die explizite Zuweisung von Rollen zur Schnittstelle sowie implizit geerbte Rollen von der Komponentenebene.<br/> |



 

## <a name="method-level-setting"></a>Method-Level Einstellung



| attribute                                                                                           | BESCHREIBUNG                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Automatisch fertig](enabling-auto-done-for-a-method.md)<br/>                                         | Deaktiviert das Objekt bei der Methoden-Rückgabe und stimmen in der Transaktion automatisch ab.<br/>                                                       |
| [Deklarative Rollenzuweisung](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Ermöglicht die explizite Zuweisung von Rollen zur -Methode sowie implizit geerbte Rollen von der Schnittstellen- und Komponentenebene.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatisieren der COM+-Verwaltung](automating-com--administration.md)
</dt> <dt>

[Erstellen von COM+-Anwendungen](creating-com--applications.md)
</dt> <dt>

[Bereitstellen von COM+-Anwendungen](deploying-com--applications.md)
</dt> </dl>

 

 




