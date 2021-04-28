---
description: Application Verifier (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bac2a8bc900ea9d1f35ae228371226355657b930
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088688"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Cookbook zur Anwendungsqualität unter Windows 7 und Windows Server 2008 R2)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients:** Windows XP, Windows Vista, Windows 7  
**Server:** Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>BESCHREIBUNG

Fördern und erzwingen Application Verifier als Qualitätsgate für die entwicklung. Dies umfasst mehrere Verbesserungen:

-   Wir haben zusätzliche Überprüfungen durchgeführt, um Probleme zu beheben, die Windows-Fehlerberichterstattung Threadpoolverwendung festgestellt haben.
-   Wir haben 32- und 64-Bit-Versionen des Pakets kombiniert, um Änderungen in Windows 7 zu erfüllen, einschließlich der Anforderungen zum Testen von 32-Bit-Komponenten unter einer 64-Bit-Version von Windows sowie zur allgemeinen Vereinfachung.
-   Wir haben zusätzliche Überprüfungen für Multithreadanwendungen, das Ausführen von 32-Bit-Anwendungen unter 64-Bit-Windows sowie viele Fehlerbehebungen durchgeführt.

Diese Änderungen sollten keine negativen Auswirkungen auf Benutzer haben, die die Threadüberprüfungen nicht aktivieren. Diejenigen, die dies tun, sollten zusätzliche Unterstützung bei der Ermittlung und Diagnose vorhandener Probleme bei der Threadpoolverwendung erhalten. Unabhängig davon, ob Sie Threadüberprüfungen aktivieren, profitieren Sie von den anderen Verbesserungen und Fehlerbehebungen in diesem Dienst.

Bei der Verwendung dieses Diensts gibt es zwar geringfügige Leistungssentwerte, die Leistungsstufen sollten jedoch akzeptabel bleiben, da sie in der Regel nicht in Einzelhandelsumgebungen ausgeführt werden.

## <a name="usage"></a>Verbrauch

**Allgemeine Informationen**

So stellen Sie zuverlässige Windows-Anwendungen zur Verfügung:

1.  Testen Sie Anwendungen, die in nicht verwaltetem (nativem) Code mit Application Verifier debugger und mit einem Ganzseiten-Heap geschrieben wurden, bevor Sie sie für Kunden freigeben.
2.  Führen Sie die schritte aus, die Application Verifier, um fehleranstrante Bedingungen zu beheben.
3.  Nachdem Ihre Anwendung freigegeben wurde, überwachen Sie regelmäßig die von der Anwendung erfassten Anwendungsfehlerberichte Windows-Fehlerberichterstattung.

Threadpoolüberprüfungen sind standardmäßig unter der Überprüfungsüberschrift "Grundlagen" aktiviert. Da dies in der Standardeinstellung enthalten ist, müssen Benutzer nur Application Verifier für ihren Code mit den Standardeinstellungen ausführen, um die neuen Überprüfungen zu nutzen.

**Details**

Sie sollten mindestens Application Verifier ausführen, wobei die Einstellung Grundlagen ausgewählt ist. Dies ist für WinLogo und WinQual erforderlich. Die Einstellung Grundlagen überprüft Folgendes:

-   **Details zum Beenden von Ausnahmen:** Stellt sicher, dass Anwendungen Zugriffsverletzungen nicht mithilfe der strukturierten Ausnahmebehandlung ausblenden.
-   **Behandelt Beendigungsdetails–** Testet, um sicherzustellen, dass die Anwendung nicht versucht, ungültige Handles zu verwenden.
-   **Heaps Stop Details** – Checks for memory corruptions issues in the heap (Details zum Beenden von Heaps– Überprüfungen auf Speicherbeschädigungen im Heap)
-   Details zum Beenden der **Eingabe/Ausgabe:** Überwacht die Ausführung asynchroner E/A-Vorgänge und führt verschiedene Überprüfungen durch.
-   **Details zum Beenden** von Datenverlusten: Erkennt Lecks, indem die von einer DLL erzeugten Ressourcen nachzuverfolgen sind, die zum Zeitpunkt des Entladens der DLL nicht freigegeben wurden.
-   **Details zum Beenden** von Sperren: Überprüft die richtige Verwendung für kritische Abschnitte
-   **Details zum Beenden** des Arbeitsspeichers: Stellt sicher, dass APIs für die Bearbeitung des virtuellen Speicherplatzes ordnungsgemäß verwendet werden (z. B. VirtualAlloc, MapViewOfFile).
-   **TLS-Beendigungsdetails:** Stellt sicher, dass lokale Threadspeicher-APIs ordnungsgemäß verwendet werden.
-   **Threadpool-Beendigungsdetails:** Stellt die korrekte Verwendung von Threadpool-APIs sicher und erzwingt Konsistenzprüfungen für Workerthreadzustände nach einem Rückruf.

Wenn Ihre Anwendung von einer "Pre-Vista"-Anwendung migriert wird, sollten Sie "LuaPriv" (auch als UAC-Überprüfungen bezeichnet) nutzen. Der Berechtigungsvorhersager für eingeschränkte Benutzerkonten (LuaPriv) hat zwei Hauptziele:

-   **Vorhersage:** Bei der Ausführung einer Anwendung mit Administratorrechten können Sie vorhersagen, ob diese Anwendung auch funktioniert, wenn sie mit weniger Berechtigungen ausgeführt wird (im Allgemeinen als normaler Benutzer). Wenn die Anwendung z. B. in Dateien schreibt, die nur Administratorzugriff zulassen, kann diese Anwendung nicht in dieselbe Datei schreiben, wenn sie als Nichtadministrator ausgeführt wird.
-   **Diagnose:** Identifizieren Sie bei der Ausführung mit Nichtadministratorberechtigungen potenzielle Probleme, die bei der aktuellen Ausführung möglicherweise bereits vorhanden sind. Wenn die Anwendung im vorherigen Beispiel versucht, in eine Datei zu schreiben, die nur Mitgliedern der Administratorgruppe Zugriff gewährt, erhält die Anwendung den Fehler ACCESS \_ DENIED. Wenn die Anwendung nicht ordnungsgemäß funktioniert, kann dieser Vorgang der Grund dafür sein.

LuaPriv identifiziert die folgenden Arten von Problemen:



| **Potenzielles Problem**       | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eingeschränkte Namespaces     | Das Erstellen eines benannten Synchronisierungsobjekts (Event, Semaphore, Mutex usw.) ohne Namespace kann die Ausführung ohne Berechtigungen auf einigen Betriebssystemen erschweren, da das Betriebssystem das Objekt möglicherweise in einem eingeschränkten Namespace platzieren möchte. Das Erstellen eines solchen Objekts in einem eingeschränkten Namespace (z. B. dem globalen Namespace) erfordert SeCreateGlobalPrivilege, das nur Administratoren gewährt wird.<br/> LuaPriv kennzeichnet beide Probleme, wenn sie erkannt werden.<br/> |
| Harte Administratorüberprüfungen | Einige Anwendungen abfragen das Sicherheitstoken des Benutzers, um herauszufinden, über wie viele Berechtigungen er verfügt. In diesen Fällen kann die Anwendung ihr Verhalten ändern, je nachdem, über welche Leistungsfähigkeit der Benutzer verfügt. <br/> LuaPriv kennzeichnet API-Aufrufe, die diese Informationen zurückgeben.<br/>                                                                                                                                                                                                |
| Anfordern von Berechtigungen     | Eine Anwendung versucht möglicherweise, eine sicherheitsrelevante Berechtigung (z. B. SeTcbPrivilege oder SeSecurityPrivilege) zu aktivieren, bevor sie einen Vorgang ausführt, der sie erfordert. <br/> LuaPriv-Flags versuchen, sicherheitsrelevante Berechtigungen zu aktivieren. <br/>                                                                                                                                                                                                                               |
| Fehlende Berechtigungen        | Wenn eine Anwendung versucht, eine Berechtigung zu aktivieren, über die der Benutzer nicht verfügt, signalisiert sie wahrscheinlich, dass die Anwendung die Berechtigung erwartet, was zu Verhaltensunterschieden führen kann. <br/> LuaPriv kennzeichnet fehlgeschlagene Berechtigungsanforderungen. <br/>                                                                                                                                                                                                                                       |
| INI-File-Vorgänge       | Versuche, in zugeordnete INI-Dateien (WritePrivateProfileSection und ähnliche APIs) zu schreiben, können als Benutzer ohne Administratorrechte fehlschlagen. <br/> LuaPriv kennzeichnet solche Vorgänge.<br/>                                                                                                                                                                                                                                                                                                            |
| Zugriff verweigert             | Wenn die Anwendung versucht, auf ein Objekt (Datei, Registrierungsschlüssel usw.) zu zugreifen, der Versuch jedoch aufgrund unzureichenden Zugriffs fehlschlägt, erwartet die Anwendung wahrscheinlich, dass sie mit mehr Berechtigungen ausgeführt wird, als sie besitzt. <br/> LuaPriv kennzeichnet objektoffene Versuche, die mit ACCESS DENIED und \_ ähnlichen Fehlern fehlschlagen.<br/>                                                                                                                                                               |
| Verweigern von ACEs                 | Wenn ein Objekt aces verweigern in seiner DACL enthält, verweigert es explizit den Zugriff auf bestimmte Entitäten. <br/> Dies ist ungewöhnlich und erschwert die Vorhersage, daher kennzeichnet LuaPriv ACEs verweigern, wenn sie gefunden werden.<br/>                                                                                                                                                                                                                                                                     |
| Zugriff eingeschränkt         | Wenn eine Anwendung versucht, ein Objekt für Rechte zu öffnen, die normalen Benutzern nicht gewährt werden (z. B. wenn versucht wird, in eine Datei zu schreiben, die nur von Administratoren geschrieben werden kann), funktioniert die Anwendung wahrscheinlich nicht gleich, wenn sie als normaler Benutzer ausgeführt wird. <br/> LuaPriv kennzeichnet solche Vorgänge.<br/>                                                                                                                                                                      |
| MAXIMAL \_ ZULÄSSIG          | Wenn eine Anwendung ein Objekt für MAXIMUM ALLOWED öffnet, erfolgt die tatsächliche Zugriffsüberprüfung für das \_ Objekt an anderer Stelle. Der meiste Code, der dies tut, funktioniert nicht ordnungsgemäß und funktioniert bei der Ausführung ohne Berechtigungen mit sicherheit unterschiedlich. <br/> LuaPriv kennzeichnet daher alle Incidents von MAXIMUM \_ ALLOWED. <br/>                                                                                                                                                            |



 

Häufig übersehene Probleme werden in den nebulous Misc Checks erfasst:

-   Details zum Beenden von gefährlichen APIs
-   Details zum Beenden von dirty stacks
-   Zeitrollover

Wir haben eine neue Druckverifizierer hinzugefügt. Diese Ebene hilft beim Suchen und Beheben von Problemen, die beim Aufrufen des Drucksubsystems durch eine Anwendung entstehen können. Die Drucküberprüfung ist auf die beiden Ebenen des Drucksubsystems ausgerichtet, die PrintAPI-Ebene und die PrintDriver-Ebene.

*Drucken einer API-Ebene*

Die Drucküberprüfung testet die Schnittstelle zwischen einem Programm und Winspool.drv und prntvpt.dll und testet die Schnittstellen dieser DLLs. Sie können die Regeln zum Aufrufen von Funktionen in dieser Schnittstelle im MSDN-Hilfeabschnitt für APIs überprüfen, die von winspool.drv und prntvpt.dll exportiert werden.

*Drucktreiberebene*

Die Drucküberprüfung testet auch die Schnittstelle zwischen einem Hauptdrucktreiber wie UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL oder MXDWDRV.DLL und den Druckertreiber-Plug-Ins. Informationen zu dieser Schnittstelle finden Sie im MSDN und im WDK.

Beachten Sie, dass einige dieser Überprüfungen nur für Windows 7 gelten, während andere unter Windows 7 einfach besser funktionieren.

In der Regel wird die Application Verifier nur von Debugversionen ausgeführt, sodass die Leistung im Allgemeinen kein Problem ist. Wenn durch die Verwendung dieser oder einer anderen Application Verifier Überprüfung Leistungsprobleme auftreten, führen Sie eine Überprüfung nach der anderen aus, bis Sie alle erforderlichen Überprüfungen durchgeführt haben.

Fast 10 % der Anwendungsabstürze auf Windows-Systemen sind auf Heapbeschädigungen zurückzuführen. Diese Abstürze können nach dem Fakt nahezu unmöglich gedebuggt werden. Die beste Möglichkeit, diese Probleme zu vermeiden, besteht darin, mit den Funktionen des Seitenheaps in Application Verifier zu testen. Es gibt zwei Varianten von Seitenheap: "Full" und "Light". Full ist die Standardeinstellung. erzwingen, dass ein Debugger sofort beendet wird, wenn eine Beschädigung erkannt wird. Dieses Feature MUSS unter dem Debugger ausgeführt werden. Dies ist jedoch auch die ressourcenstärkste Ressource. Wenn ein Benutzer Zeitsteuerungsprobleme hat und bereits ein Szenario unter "Vollständiger" Seitenheap ausgeführt hat, werden diese Probleme wahrscheinlich behoben, wenn er auf "Light" festgelegt ist. Darüber hinaus stürzt der Light Page Heap erst ab, wenn der Prozess beendet wird. Sie stellt zwar eine Stapelüberwachung für die Zuordnung bereit, kann jedoch erheblich länger für die Diagnose als die Nutzung der vollständigen Entsprechung dauern.

Überwachen Sie den Zuverlässigkeitsstatus der Anwendungen über das Winqual-Webportal. In diesem Portal werden die über die Windows-Fehlerberichterstattung erfassten Fehlerberichte angezeigt, sodass die häufigsten Fehler leicht identifiziert werden können. Weitere Informationen finden Sie unter Windows-Fehlerberichterstattung: Erste Schritte. Microsoft berechnet für diesen Dienst keine Gebühren.

Um WinQual nutzen zu können, müssen Sie:

1.  Registrieren Sie Ihr Unternehmen für WinQual, für das eine VeriSign-ID erforderlich ist. Windows 7-Informationen zu WinQual finden Sie im Entwicklerportal unter Windows Vista SP1 \\ Windows Server 2008. Es wird bald einen Windows 7-Speicherort haben.
2.  Ordnen Sie die ISV-Anwendungen einem Produktnamen und dem ISV-Namen zu, der die Fehlerberichte mit dem Unternehmen verknüpft. Andere ISVs können Ihre Fehlerberichte nicht anzeigen.
3.  Verwenden Sie das Portal, um die wichtigsten Probleme zu identifizieren. ISVs können auch Antworten erstellen, die Kunden darüber informieren, welche Schritte nach einem Fehler erforderlich sind. Das Antwortsystem unterstützt mehr als 10 Sprachen weltweit.

Ein weiterer Hinweis: Application Verifier ist nur so gut wie die Codepfade, für die Sie es ausführen. Der Wert der Kombination dieses Tools mit einem Code Coverage-Tool kann nicht überbewertet werden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

**Debugtools für Windows:**

-   [Übersicht und Downloadwebsite](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [MSDN-Onlinedokumentation](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Übersicht](/previous-versions/ms220948(v=vs.80))
-   [Download](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier für Microsoft Visual Studio 2008/.NET Framework 3.5](/previous-versions/ms220948(v=vs.80))

    **Hinweis:** Die Application Verifier Version, die in Visual Studio enthalten ist, ist recht veraltet. Verwenden Sie nach Möglichkeit stattdessen das eigenständige Paket. Aus diesem Grund verfügen zukünftige Versionen von Visual Studio nicht mehr über eingebettete Application Verifier.

**WinQual:**

-   [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Windows-Fehlerberichterstattung: Erste Schritte](../wer/using-wer.md)

 

 
