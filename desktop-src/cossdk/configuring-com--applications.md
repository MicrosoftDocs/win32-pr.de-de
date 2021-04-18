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
# <a name="configuring-com-applications"></a><span data-ttu-id="e0c71-104">Com+-Anwendungen werden konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="e0c71-104">Configuring COM+ Applications</span></span>

<span data-ttu-id="e0c71-105">Eine COM+-Anwendung ist im Wesentlichen ein deklaratives Konstrukt, mit dem Sie beliebig viele Komponenten konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="e0c71-105">A COM+ application is essentially a declarative construct that enables you to configure any number of components in common.</span></span> <span data-ttu-id="e0c71-106">Beispielsweise können Sie die Komponenten in einer Anwendung mit einer allgemeinen Sicherheitsrichtlinie konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e0c71-106">For example, you can configure the components in an application with a common security policy.</span></span>

<span data-ttu-id="e0c71-107">Die Konfiguration ist ein wesentlicher Bestandteil des Entwicklungsprozesses für COM+-Anwendungen.</span><span class="sxs-lookup"><span data-stu-id="e0c71-107">Configuration is an essential part of the development process for COM+ applications.</span></span> <span data-ttu-id="e0c71-108">Wie Sie eine Anwendung konfigurieren, hängt davon ab, wie COM+ Dienste für Sie bereitstellt und wie Sie sich bei der Ausführung verhält.</span><span class="sxs-lookup"><span data-stu-id="e0c71-108">How you configure an application will determine how COM+ will provide services for it and how it behaves when running.</span></span>

<span data-ttu-id="e0c71-109">Sie können com+-Anwendungen entweder mithilfe des Verwaltungs Tools Komponenten Dienste oder mithilfe der Skript fähigen Verwaltungs Objekte und-Schnittstellen konfigurieren, die die zugrunde liegenden Funktionen des Verwaltungs Tools bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e0c71-109">You can configure COM+ applications using either the Component Services administration tool or the scriptable administration objects and interfaces that provide the underlying functionality of the administration tool.</span></span> <span data-ttu-id="e0c71-110">Ausführliche Informationen zum Durchführen der Skript gesteuerten Verwaltung finden Sie unter [Automatisieren der com+-Verwaltung](automating-com--administration.md).</span><span class="sxs-lookup"><span data-stu-id="e0c71-110">For details on performing scripted administration, see [Automating COM+ Administration](automating-com--administration.md).</span></span>

<span data-ttu-id="e0c71-111">Sie können Elemente auf den folgenden Ebenen in com+-Anwendungen konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="e0c71-111">You can configure elements at the following levels within COM+ applications:</span></span>

-   [<span data-ttu-id="e0c71-112">Einstellungen auf Anwendungsebene</span><span class="sxs-lookup"><span data-stu-id="e0c71-112">Application-Level Settings</span></span>](#application-level-settings)
-   [<span data-ttu-id="e0c71-113">Einstellungen auf Komponentenebene (Klassenebene)</span><span class="sxs-lookup"><span data-stu-id="e0c71-113">Component-Level (Class-Level) Settings</span></span>](#component-level-class-level-settings)
-   [<span data-ttu-id="e0c71-114">Einstellung auf Schnittstellen Ebene</span><span class="sxs-lookup"><span data-stu-id="e0c71-114">Interface-Level Setting</span></span>](#interface-level-setting)
-   [<span data-ttu-id="e0c71-115">Einstellung auf Methoden Ebene</span><span class="sxs-lookup"><span data-stu-id="e0c71-115">Method-Level Setting</span></span>](#method-level-setting)
-   [<span data-ttu-id="e0c71-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0c71-116">Related topics</span></span>](#related-topics)

<span data-ttu-id="e0c71-117">Wie Sie Komponenten in einer Anwendung installieren, kann sich darauf auswirken, wie Sie diese konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="e0c71-117">How you install components into an application can affect how you can configure them.</span></span> <span data-ttu-id="e0c71-118">Sie sollten Komponenten immer in com+-Anwendungen installieren (anstatt Sie zu importieren).</span><span class="sxs-lookup"><span data-stu-id="e0c71-118">You should always install components into COM+ applications (as opposed to importing them).</span></span> <span data-ttu-id="e0c71-119">Durch die Installation von-Komponenten werden diese zusammen mit Schnittstellen und Typbibliotheken vollständig in der com+-Klassen Registrierungsdatenbank (RegDB) registriert, sodass Sie Sie konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="e0c71-119">Installing components will fully register them, along with interfaces and type libraries, in the COM+ class registration database (RegDB) so that you can configure them.</span></span>

## <a name="application-level-settings"></a><span data-ttu-id="e0c71-120">Application-Level Einstellungen</span><span class="sxs-lookup"><span data-stu-id="e0c71-120">Application-Level Settings</span></span>



| <span data-ttu-id="e0c71-121">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0c71-121">Attribute</span></span>                                                                                        | <span data-ttu-id="e0c71-122">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0c71-122">Description</span></span>                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0c71-123">Aktivierung</span><span class="sxs-lookup"><span data-stu-id="e0c71-123">Activation</span></span>](context-activation.md)<br/>                                                  | <span data-ttu-id="e0c71-124">Gibt den Anwendungstyp an: entweder Serveranwendung oder Bibliotheks Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e0c71-124">Specifies application type: either server application or library application.</span></span><br/>                                                                                                            |
| [<span data-ttu-id="e0c71-125">Aktivieren von Zugriffs Überprüfungen</span><span class="sxs-lookup"><span data-stu-id="e0c71-125">Enabling access checks</span></span>](enabling-access-checks-for-an-application.md)<br/>               | <span data-ttu-id="e0c71-126">Schaltet die Sicherheitsüberprüfung ein und aus.</span><span class="sxs-lookup"><span data-stu-id="e0c71-126">Turns security checking on and off.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="e0c71-127">Sicherheitsstufe</span><span class="sxs-lookup"><span data-stu-id="e0c71-127">Security level</span></span>](setting-a-security-level-for-access-checks.md)<br/>                      | <span data-ttu-id="e0c71-128">Gibt an, dass Zugriffs Überprüfungen auf Prozessebene (Zugriffs Überprüfungs Stufen, die von Rollen generiert werden) oder sowohl auf dem Prozess als auch auf Komponentenebene (vollständige rollenbasierte Sicherheit) ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e0c71-128">Specifies that access checks will be performed at the process level (access-checking levels generated from roles) or both at process and at component levels (full role-based security).</span></span><br/> |
| [<span data-ttu-id="e0c71-129">Authentifizierungsebene</span><span class="sxs-lookup"><span data-stu-id="e0c71-129">Authentication level</span></span>](setting-an-authentication-level-for-a-server-application.md)<br/>  | <span data-ttu-id="e0c71-130">Legt die Authentifizierungs Ebene fest, die für Aufrufe der Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0c71-130">Sets the authentication level used on calls into the application.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e0c71-131">Identitätswechsel Ebene</span><span class="sxs-lookup"><span data-stu-id="e0c71-131">Impersonation level</span></span>](setting-an-impersonation-level.md)<br/>                             | <span data-ttu-id="e0c71-132">Legt die Identitätswechsel Ebene fest, die bei Aufrufen von anderen Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e0c71-132">Sets the impersonation level used on calls to other applications.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="e0c71-133">Queuing</span><span class="sxs-lookup"><span data-stu-id="e0c71-133">Queuing</span></span>](creating-queuable-components.md)<br/>                                           | <span data-ttu-id="e0c71-134">Gibt an, dass Anwendungskomponenten Warteschlangen Dienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="e0c71-134">Specifies that application components will use queuing services.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="e0c71-135">Aktivieren von CRM</span><span class="sxs-lookup"><span data-stu-id="e0c71-135">Enable CRM</span></span>](configuring-com--crm-components.md)<br/>                                     | <span data-ttu-id="e0c71-136">Ermöglicht die Verwendung ausgleichender Ressourcen-Manager.</span><span class="sxs-lookup"><span data-stu-id="e0c71-136">Enables use of Compensating Resource Managers.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="e0c71-137">Ausführen einer Anwendung als Dienst</span><span class="sxs-lookup"><span data-stu-id="e0c71-137">Run application as a service</span></span>](com--applications-running-as-service-applications.md)<br/> | <span data-ttu-id="e0c71-138">Konfiguriert und implementiert eine COM+-Serveranwendung als NT-Dienst.</span><span class="sxs-lookup"><span data-stu-id="e0c71-138">Configures and implements a COM+ server application as an NT service.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e0c71-139">Com+-SOAP-Dienst</span><span class="sxs-lookup"><span data-stu-id="e0c71-139">COM+ SOAP service</span></span>](com--soap-service.md)<br/>                                            | <span data-ttu-id="e0c71-140">Macht eine COM+-Anwendung als XML-Webdienst verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e0c71-140">Exposes a COM+ application as an XML web service.</span></span><br/>                                                                                                                                        |
| [<span data-ttu-id="e0c71-141">Anwendungs Pooling</span><span class="sxs-lookup"><span data-stu-id="e0c71-141">Application pooling</span></span>](com--application-pooling.md)<br/>                                   | <span data-ttu-id="e0c71-142">Fügt die Skalierbarkeit für Single Thread-Prozesse hinzu und ist in den com+-Anwendungs Wiederverwendungs Dienst integriert.</span><span class="sxs-lookup"><span data-stu-id="e0c71-142">Adds scalability for single-threaded processes and integrates with the COM+ Application Recycling service.</span></span><br/>                                                                               |
| [<span data-ttu-id="e0c71-143">Anwendungs Wiederverwendung</span><span class="sxs-lookup"><span data-stu-id="e0c71-143">Application recycling</span></span>](com--application-recycling.md)<br/>                               | <span data-ttu-id="e0c71-144">Erhöht die Anwendungs Stabilität, indem ein Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß heruntergefahren und neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e0c71-144">Increases application stability by gracefully shutting down a process associated with an application and restarting it.</span></span><br/>                                                                  |
| [<span data-ttu-id="e0c71-145">Prozess Sicherung</span><span class="sxs-lookup"><span data-stu-id="e0c71-145">Process dumping</span></span>](what-s-new-in-com--1-5.md)<br/>                                         | <span data-ttu-id="e0c71-146">Sichert den gesamten Status eines Prozesses, ohne ihn zu Debugzwecken zu beenden.</span><span class="sxs-lookup"><span data-stu-id="e0c71-146">Dumps the entire state of a process without terminating it, for debugging purposes.</span></span><br/>                                                                                                      |
| <span data-ttu-id="e0c71-147">Server Prozess wird heruntergefahren</span><span class="sxs-lookup"><span data-stu-id="e0c71-147">Server process shutdown</span></span><br/>                                                               | <span data-ttu-id="e0c71-148">Beendet einen Prozess nach einem angegebenen Leerlauf Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="e0c71-148">Shuts down a process after a specified idle period.</span></span><br/>                                                                                                                                      |
| <span data-ttu-id="e0c71-149">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="e0c71-149">Permissions</span></span><br/>                                                                           | <span data-ttu-id="e0c71-150">Deaktiviert Änderungen an den Konfigurationseinstellungen, einschließlich der Löschung.</span><span class="sxs-lookup"><span data-stu-id="e0c71-150">Disables changes to configuration settings, including deletion.</span></span><br/>                                                                                                                          |
| <span data-ttu-id="e0c71-151">Sicherheitsidentität</span><span class="sxs-lookup"><span data-stu-id="e0c71-151">Security identity</span></span><br/>                                                                     | <span data-ttu-id="e0c71-152">Gibt die Identität an, unter der die Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0c71-152">Specifies the identity under which the application runs.</span></span><br/>                                                                                                                                 |
| <span data-ttu-id="e0c71-153">Im Debugger starten</span><span class="sxs-lookup"><span data-stu-id="e0c71-153">Launch in debugger</span></span><br/>                                                                    | <span data-ttu-id="e0c71-154">Gibt an, dass die Anwendung in einem Debugger mit benutzerdefinierten Befehlszeilen Einstellungen gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="e0c71-154">Specifies that the application will be launched in a debugger, with user-specified command-line settings.</span></span><br/>                                                                                |
| <span data-ttu-id="e0c71-155">Unterstützung für 3 GB aktivieren</span><span class="sxs-lookup"><span data-stu-id="e0c71-155">Enable 3GB support</span></span><br/>                                                                    | <span data-ttu-id="e0c71-156">Ermöglicht die Verwendung des erweiterten Adressraums des Prozess Speichers.</span><span class="sxs-lookup"><span data-stu-id="e0c71-156">Enables use of extended process memory address space.</span></span><br/>                                                                                                                                    |



 

## <a name="component-level-class-level-settings"></a><span data-ttu-id="e0c71-157">Component-Level Einstellungen (auf Klassenebene)</span><span class="sxs-lookup"><span data-stu-id="e0c71-157">Component-Level (Class-Level) Settings</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e0c71-158">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0c71-158">Attribute</span></span></th>
<th><span data-ttu-id="e0c71-159">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0c71-159">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e0c71-160"><a href="configuring-transactions.md">Transaktionen</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-160"><a href="configuring-transactions.md">Transactions</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-161">Legt die automatischen Transaktions Anforderungen deaktiviert, nicht unterstützt, unterstützt, erforderlich oder erfordert neu.</span><span class="sxs-lookup"><span data-stu-id="e0c71-161">Sets automatic transaction requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c71-162"><a href="setting-the-synchronization-attribute.md">Synchronisierung</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-162"><a href="setting-the-synchronization-attribute.md">Synchronization</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-163">Legt die Synchronisierungs Anforderungen deaktiviert, nicht unterstützt, unterstützt, erforderlich oder erfordert neu.</span><span class="sxs-lookup"><span data-stu-id="e0c71-163">Sets synchronization requirements Disabled, Not Supported, Supported, Required, or Requires New.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c71-164"><a href="enabling-jit-activation-for-a-component.md">JIT-Aktivierung</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-164"><a href="enabling-jit-activation-for-a-component.md">JIT Activation</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-165">Aktiviert die Just-in-Time-Aktivierung.</span><span class="sxs-lookup"><span data-stu-id="e0c71-165">Enables just-in-time activation.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c71-166"><a href="configuring-a-component-to-be-pooled.md">Objektpooling</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-166"><a href="configuring-a-component-to-be-pooled.md">Object pooling</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-167">Aktiviert das Objekt Pooling.</span><span class="sxs-lookup"><span data-stu-id="e0c71-167">Enables object pooling.</span></span> <span data-ttu-id="e0c71-168">Minimale und maximale Poolgröße und Objekt Timeout Werte sind konfigurierbar.</span><span class="sxs-lookup"><span data-stu-id="e0c71-168">Minimum and maximum pool size and object time-out values are configurable.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c71-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Objekt Erstellung</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-169"><a href="specifying-an-object-constructor-string-for-a-component.md">Object construction</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-170">Aktiviert die parametrisierte Objekt Erstellung mit einer administrativ angegebenen Konstruktorzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e0c71-170">Enables parameterized object construction with an administratively specified constructor string.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="e0c71-171">Die Konstruktorzeichenfolge sollte nicht verwendet werden, um sicherheitsrelevante Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="e0c71-171">The constructor string should not be used to store security-sensitive information.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c71-172"><a href="enabling-access-checks-at-the-component-level.md">Zugriffs Überprüfungen auf Komponentenebene</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-172"><a href="enabling-access-checks-at-the-component-level.md">Component-level access checks</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-173">Schaltet die rollenbasierte Sicherheitsüberprüfung auf Komponentenebene ein bzw. aus.</span><span class="sxs-lookup"><span data-stu-id="e0c71-173">Turns on or off component-level role-based security checking.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c71-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Deklarative Rollenzuweisung</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-174"><a href="assigning-roles-to-components--interfaces--or-methods.md">Declarative role assignment</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-175">Ermöglicht die explizite Zuweisung von Rollen zur Komponente.</span><span class="sxs-lookup"><span data-stu-id="e0c71-175">Enables explicit assignment of roles to the component.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c71-176"><a href="persistent-client-side-failures.md">Queue Exception-Klasse</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-176"><a href="persistent-client-side-failures.md">Queuing exception class</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-177">Gibt eine Ausnahme Klasse für die Behandlung von Client seitigen Fehlern an.</span><span class="sxs-lookup"><span data-stu-id="e0c71-177">Indicates an exception class for handling client-side failures.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c71-178"><a href="com--instrumentation-concepts.md">Instrumentierungs Ereignisse und Statistiken</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-178"><a href="com--instrumentation-concepts.md">Instrumentation events and statistics</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-179">Ermöglicht eine ausführliche Berichterstellung für Systemereignisse und Objekt Statistiken.</span><span class="sxs-lookup"><span data-stu-id="e0c71-179">Enables detailed system event and object statistics reporting.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e0c71-180"><a href="context-activation.md">Aktivierungs Kontext</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-180"><a href="context-activation.md">Activation context</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-181">Aktiviert die erzwungene Aktivierung eines Objekts im Kontext-oder Standardkontext des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="e0c71-181">Enables forced activation of an object in the caller's context or default context.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e0c71-182"><a href="what-s-new-in-com--1-5.md">Erstellen privater Komponenten</a></span><span class="sxs-lookup"><span data-stu-id="e0c71-182"><a href="what-s-new-in-com--1-5.md">Creating private components</a></span></span><br/></td>
<td><span data-ttu-id="e0c71-183">Markiert die Komponente als privat für die Anwendung.</span><span class="sxs-lookup"><span data-stu-id="e0c71-183">Marks component as private to the application.</span></span> <span data-ttu-id="e0c71-184">Eine private Komponente kann nur von anderen Komponenten in der gleichen Anwendung angezeigt und aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="e0c71-184">A private component can be seen and activated only by other components in the same application.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="interface-level-setting"></a><span data-ttu-id="e0c71-185">Interface-Level Einstellung</span><span class="sxs-lookup"><span data-stu-id="e0c71-185">Interface-Level Setting</span></span>



| <span data-ttu-id="e0c71-186">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0c71-186">Attribute</span></span>                                                                                           | <span data-ttu-id="e0c71-187">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0c71-187">Description</span></span>                                                                                                                      |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0c71-188">In Warteschlange</span><span class="sxs-lookup"><span data-stu-id="e0c71-188">Queued</span></span>](creating-queuable-components.md)<br/>                                               | <span data-ttu-id="e0c71-189">Gibt eine in IDL definierte Warteschlangen Schnittstelle an.</span><span class="sxs-lookup"><span data-stu-id="e0c71-189">Indicates a queuable interface, defined in IDL.</span></span><br/>                                                                       |
| [<span data-ttu-id="e0c71-190">Deklarative Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="e0c71-190">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="e0c71-191">Ermöglicht die explizite Zuweisung von Rollen zur Schnittstelle und implizit geerbte Rollen aus der Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="e0c71-191">Enables explicit assignment of roles to the interface as well as implicitly inherited roles from the component level.</span></span><br/> |



 

## <a name="method-level-setting"></a><span data-ttu-id="e0c71-192">Method-Level Einstellung</span><span class="sxs-lookup"><span data-stu-id="e0c71-192">Method-Level Setting</span></span>



| <span data-ttu-id="e0c71-193">Attribut</span><span class="sxs-lookup"><span data-stu-id="e0c71-193">Attribute</span></span>                                                                                           | <span data-ttu-id="e0c71-194">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0c71-194">Description</span></span>                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0c71-195">Automatisch abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="e0c71-195">Auto-done</span></span>](enabling-auto-done-for-a-method.md)<br/>                                         | <span data-ttu-id="e0c71-196">Deaktiviert das Objekt in der Rückgabe der Methode und Stimmen in der Transaktion automatisch.</span><span class="sxs-lookup"><span data-stu-id="e0c71-196">Automatically deactivates object on method return and votes in transaction.</span></span><br/>                                                       |
| [<span data-ttu-id="e0c71-197">Deklarative Rollenzuweisung</span><span class="sxs-lookup"><span data-stu-id="e0c71-197">Declarative role assignment</span></span>](assigning-roles-to-components--interfaces--or-methods.md)<br/> | <span data-ttu-id="e0c71-198">Ermöglicht die explizite Zuweisung von Rollen zur-Methode sowie implizit geerbte Rollen aus der-Schnittstelle und der-Komponentenebene.</span><span class="sxs-lookup"><span data-stu-id="e0c71-198">Enables explicit assignment of roles to the method as well as implicitly inherited roles from the interface and component levels.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="e0c71-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e0c71-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0c71-200">Automatisieren der com+-Verwaltung</span><span class="sxs-lookup"><span data-stu-id="e0c71-200">Automating COM+ Administration</span></span>](automating-com--administration.md)
</dt> <dt>

[<span data-ttu-id="e0c71-201">Com+-Anwendungen werden erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0c71-201">Creating COM+ Applications</span></span>](creating-com--applications.md)
</dt> <dt>

[<span data-ttu-id="e0c71-202">Bereitstellen von com+-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="e0c71-202">Deploying COM+ Applications</span></span>](deploying-com--applications.md)
</dt> </dl>

 

 




