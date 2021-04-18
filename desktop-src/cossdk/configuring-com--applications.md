---
description: Eine COM+-Anwendung ist im Wesentlichen ein deklaratives Konstrukt, mit dem Sie beliebig viele Komponenten konfigurieren können. Beispielsweise können Sie die Komponenten in einer Anwendung mit einer allgemeinen Sicherheitsrichtlinie konfigurieren.
ms.assetid: 50039b30-1c91-4e93-9f23-873accb651cf
title: Com+-Anwendungen werden konfiguriert.
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16319baf7e34348751e9cafd0efcbd99906d0985
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344201"
---
# <a name="configuring-com-applications"></a>Com+-Anwendungen werden konfiguriert.

Eine COM+-Anwendung ist im Wesentlichen ein deklaratives Konstrukt, mit dem Sie beliebig viele Komponenten konfigurieren können. Beispielsweise können Sie die Komponenten in einer Anwendung mit einer allgemeinen Sicherheitsrichtlinie konfigurieren.

Die Konfiguration ist ein wesentlicher Bestandteil des Entwicklungsprozesses für COM+-Anwendungen. Wie Sie eine Anwendung konfigurieren, hängt davon ab, wie COM+ Dienste für Sie bereitstellt und wie Sie sich bei der Ausführung verhält.

Sie können com+-Anwendungen entweder mithilfe des Verwaltungs Tools Komponenten Dienste oder mithilfe der Skript fähigen Verwaltungs Objekte und-Schnittstellen konfigurieren, die die zugrunde liegenden Funktionen des Verwaltungs Tools bereitstellen. Ausführliche Informationen zum Durchführen der Skript gesteuerten Verwaltung finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).

Sie können Elemente auf den folgenden Ebenen in com+-Anwendungen konfigurieren:

-   [Einstellungen auf Anwendungsebene](#application-level-settings)
-   [Einstellungen auf Komponentenebene (Klassenebene)](#component-level-class-level-settings)
-   [Einstellung auf Schnittstellen Ebene](#interface-level-setting)
-   [Einstellung auf Methoden Ebene](#method-level-setting)
-   [Zugehörige Themen](#related-topics)

Wie Sie Komponenten in einer Anwendung installieren, kann sich darauf auswirken, wie Sie diese konfigurieren können. Sie sollten Komponenten immer in com+-Anwendungen installieren (anstatt Sie zu importieren). Durch die Installation von-Komponenten werden diese zusammen mit Schnittstellen und Typbibliotheken vollständig in der com+-Klassen Registrierungsdatenbank (RegDB) registriert, sodass Sie Sie konfigurieren können.

## <a name="application-level-settings"></a>Application-Level Einstellungen



| Attribut                                                                                        | BESCHREIBUNG                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Aktivierung](context-activation.md)<br/>                                                  | Gibt den Anwendungstyp an: entweder Serveranwendung oder Bibliotheks Anwendung.<br/>                                                                                                            |
| [Aktivieren von Zugriffs Überprüfungen](enabling-access-checks-for-an-application.md)<br/>               | Schaltet die Sicherheitsüberprüfung ein und aus.<br/>                                                                                                                                                      |
| [Sicherheitsstufe](setting-a-security-level-for-access-checks.md)<br/>                      | Gibt an, dass Zugriffs Überprüfungen auf Prozessebene (Zugriffs Überprüfungs Stufen, die von Rollen generiert werden) oder sowohl auf dem Prozess als auch auf Komponentenebene (vollständige rollenbasierte Sicherheit) ausgeführt werden.<br/> |
| [Authentifizierungsebene](setting-an-authentication-level-for-a-server-application.md)<br/>  | Legt die Authentifizierungs Ebene fest, die für Aufrufe der Anwendung verwendet wird.<br/>                                                                                                                        |
| [Identitätswechsel Ebene](setting-an-impersonation-level.md)<br/>                             | Legt die Identitätswechsel Ebene fest, die bei Aufrufen von anderen Anwendungen verwendet wird.<br/>                                                                                                                        |
| [Queuing](creating-queuable-components.md)<br/>                                           | Gibt an, dass Anwendungskomponenten Warteschlangen Dienste verwenden.<br/>                                                                                                                         |
| [Aktivieren von CRM](configuring-com--crm-components.md)<br/>                                     | Ermöglicht die Verwendung ausgleichender Ressourcen-Manager.<br/>                                                                                                                                           |
| [Ausführen einer Anwendung als Dienst](com--applications-running-as-service-applications.md)<br/> | Konfiguriert und implementiert eine COM+-Serveranwendung als NT-Dienst.<br/>                                                                                                                    |
| [Com+-SOAP-Dienst](com--soap-service.md)<br/>                                            | Macht eine COM+-Anwendung als XML-Webdienst verfügbar.<br/>                                                                                                                                        |
| [Anwendungs Pooling](com--application-pooling.md)<br/>                                   | Fügt die Skalierbarkeit für Single Thread-Prozesse hinzu und ist in den com+-Anwendungs Wiederverwendungs Dienst integriert.<br/>                                                                               |
| [Anwendungs Wiederverwendung](com--application-recycling.md)<br/>                               | Erhöht die Anwendungs Stabilität, indem ein Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß heruntergefahren und neu gestartet wird.<br/>                                                                  |
| [Prozess Sicherung](what-s-new-in-com--1-5.md)<br/>                                         | Sichert den gesamten Status eines Prozesses, ohne ihn zu Debugzwecken zu beenden.<br/>                                                                                                      |
| Server Prozess wird heruntergefahren<br/>                                                               | Beendet einen Prozess nach einem angegebenen Leerlauf Zeitraum.<br/>                                                                                                                                      |
| Berechtigungen<br/>                                                                           | Deaktiviert Änderungen an den Konfigurationseinstellungen, einschließlich der Löschung.<br/>                                                                                                                          |
| Sicherheitsidentität<br/>                                                                     | Gibt die Identität an, unter der die Anwendung ausgeführt wird.<br/>                                                                                                                                 |
| Im Debugger starten<br/>                                                                    | Gibt an, dass die Anwendung in einem Debugger mit benutzerdefinierten Befehlszeilen Einstellungen gestartet wird.<br/>                                                                                |
| Unterstützung für 3 GB aktivieren<br/>                                                                    | Ermöglicht die Verwendung des erweiterten Adressraums des Prozess Speichers.<br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a>Component-Level Einstellungen (auf Klassenebene)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="configuring-transactions.md">Transaktionen</a><br/></td>
<td>Legt die automatischen Transaktions Anforderungen deaktiviert, nicht unterstützt, unterstützt, erforderlich oder erfordert neu.<br/></td>
</tr>
<tr class="even">
<td><a href="setting-the-synchronization-attribute.md">Synchronisierung</a><br/></td>
<td>Legt die Synchronisierungs Anforderungen deaktiviert, nicht unterstützt, unterstützt, erforderlich oder erfordert neu.<br/></td>
</tr>
<tr class="odd">
<td><a href="enabling-jit-activation-for-a-component.md">JIT-Aktivierung</a><br/></td>
<td>Aktiviert die Just-in-Time-Aktivierung.<br/></td>
</tr>
<tr class="even">
<td><a href="configuring-a-component-to-be-pooled.md">Objektpooling</a><br/></td>
<td>Aktiviert das Objekt Pooling. Minimale und maximale Poolgröße und Objekt Timeout Werte sind konfigurierbar.<br/></td>
</tr>
<tr class="odd">
<td><a href="specifying-an-object-constructor-string-for-a-component.md">Objekt Erstellung</a><br/></td>
<td>Aktiviert die parametrisierte Objekt Erstellung mit einer administrativ angegebenen Konstruktorzeichenfolge. <br/>
<blockquote>
[!Note]<br />
Die Konstruktorzeichenfolge sollte nicht verwendet werden, um sicherheitsrelevante Informationen zu speichern.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="enabling-access-checks-at-the-component-level.md">Zugriffs Überprüfungen auf Komponentenebene</a><br/></td>
<td>Schaltet die rollenbasierte Sicherheitsüberprüfung auf Komponentenebene ein bzw. aus.<br/></td>
</tr>
<tr class="odd">
<td><a href="assigning-roles-to-components--interfaces--or-methods.md">Deklarative Rollenzuweisung</a><br/></td>
<td>Ermöglicht die explizite Zuweisung von Rollen zur Komponente.<br/></td>
</tr>
<tr class="even">
<td><a href="persistent-client-side-failures.md">Queue Exception-Klasse</a><br/></td>
<td>Gibt eine Ausnahme Klasse für die Behandlung von Client seitigen Fehlern an.<br/></td>
</tr>
<tr class="odd">
<td><a href="com--instrumentation-concepts.md">Instrumentierungs Ereignisse und Statistiken</a><br/></td>
<td>Ermöglicht eine ausführliche Berichterstellung für Systemereignisse und Objekt Statistiken.<br/></td>
</tr>
<tr class="even">
<td><a href="context-activation.md">Aktivierungs Kontext</a><br/></td>
<td>Aktiviert die erzwungene Aktivierung eines Objekts im Kontext-oder Standardkontext des Aufrufers.<br/></td>
</tr>
<tr class="odd">
<td><a href="what-s-new-in-com--1-5.md">Erstellen privater Komponenten</a><br/></td>
<td>Markiert die Komponente als privat für die Anwendung. Eine private Komponente kann nur von anderen Komponenten in der gleichen Anwendung angezeigt und aktiviert werden.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a>Interface-Level Einstellung



| Attribut                                                                                           | BESCHREIBUNG                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [In Warteschlange](creating-queuable-components.md)<br/>                                               | Gibt eine in IDL definierte Warteschlangen Schnittstelle an.<br/>                                                                       |
| [Deklarative Rollenzuweisung](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Ermöglicht die explizite Zuweisung von Rollen zur Schnittstelle und implizit geerbte Rollen aus der Komponentenebene.<br/> |



 

## <a name="method-level-setting"></a>Method-Level Einstellung



| Attribut                                                                                           | BESCHREIBUNG                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [Automatisch abgeschlossen](enabling-auto-done-for-a-method.md)<br/>                                         | Deaktiviert das Objekt in der Rückgabe der Methode und Stimmen in der Transaktion automatisch.<br/>                                                       |
| [Deklarative Rollenzuweisung](assigning-roles-to-components--interfaces--or-methods.md)<br/> | Ermöglicht die explizite Zuweisung von Rollen zur-Methode sowie implizit geerbte Rollen aus der-Schnittstelle und der-Komponentenebene.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Automatisieren der com+-Verwaltung](automating-com--administration.md)
</dt> <dt>

[Com+-Anwendungen werden erstellt.](creating-com--applications.md)
</dt> <dt>

[Bereitstellen von com+-Anwendungen](deploying-com--applications.md)
</dt> </dl>

 

 




