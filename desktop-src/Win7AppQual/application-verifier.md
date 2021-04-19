---
description: .
ms.assetid: edf719b7-9bd9-4e23-9bba-d0d7c3c5dbf5
title: Application Verifier (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 946d27ecfef46766fe82cc4df2061c7fa5196a45
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314993"
---
# <a name="application-verifier-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a>Application Verifier (Windows 7 und Windows Server 2008 R2 Anwendungsqualität Cookbook)

## <a name="affected-platforms"></a>Betroffene Plattformen

**Clients** -Windows XP, Windows Vista, Windows 7  
**Server** -Windows Server 2003, Windows Server 2008, Windows Server 2008 R2  


## <a name="description"></a>Beschreibung

Bewerben und erzwingen Sie Application Verifier als Quality Gate für die gesamte Entwicklung. Es umfasst mehrere Verbesserungen:

-   Wir haben zusätzliche Überprüfungen zur Behandlung von Problemen bereitgestellt, die das Windows-Fehlerberichterstattung Team während der Verwendung des Thread Pools erkannt hat.
-   Wir haben 32-und 64-Bit-Versionen des Pakets kombiniert, um Änderungen in Windows 7 zu beheben, einschließlich der Anforderungen zum Testen von 32-Bit-Komponenten unter einer 64-Bit-Version von Windows sowie zur allgemeinen Vereinfachung.
-   Wir haben zusätzliche Überprüfungen für Multithreadanwendungen, das Ausführen von 32-Bit-Anwendungen auf 64-Bit-Windows und viele Fehlerbehebungen umfasst.

Diese Änderungen sollten keine negativen Auswirkungen auf Benutzer haben, die die Thread Überprüfungen nicht aktivieren. Personen, die zusätzliche Unterstützung bei der Ermittlung und Diagnose vorhandener Probleme bei der Thread Pool Verwendung erhalten. Unabhängig davon, ob Sie Thread Überprüfungen aktivieren, profitieren Sie von den anderen Verbesserungen und Fehlerbehebungen in diesem Dienst.

Obwohl bei der Verwendung dieses diendienstanwender Dienst geringfügig beeinträchtigt wird, sollten die Leistungsstufen akzeptabel bleiben, da Sie in der Regel nicht in Einzelhandelsumgebungen ausgeführt werden.

## <a name="usage"></a>Verwendung

**Allgemeine Informationen**

So bieten Sie zuverlässige Windows-Anwendungen an:

1.  Testen Sie Anwendungen, die in nicht verwaltetem (nativem) Code geschrieben wurden, mit Application Verifier unter dem Debugger und mit dem vollständigen Heap, bevor Sie Sie für Kunden freigeben.
2.  Führen Sie die von Application Verifier bereitgestellten Schritte aus, um fehlgeleiteten-Bedingungen aufzulösen.
3.  Nachdem die Anwendung veröffentlicht wurde, überwachen Sie regelmäßig die von Windows-Fehlerberichterstattung gesammelten Anwendungsfehler Berichte.

Thread Pool Überprüfungen werden standardmäßig unter der Überschrift "Grundlagen" aktiviert. Da dies in der Standardeinstellung enthalten ist, müssen Benutzer nur Application Verifier in Ihrem Code mit den Standardeinstellungen ausführen, um die neuen Überprüfungen zu nutzen.

**Details**

Sie sollten Application Verifier mindestens mit der ausgewählten Einstellung Grundlagen ausführen. Dies ist für WinLogo und winqual erforderlich. Die Einstellung Grundlagen prüft folgendes:

-   **Ausnahmen: Details zum Ende** : stellt sicher, dass Anwendungen Zugriffs Verletzungen nicht mithilfe der strukturierten Ausnahmebehandlung ausblenden.
-   **Behandelt stoppdetails** -Tests, um sicherzustellen, dass die Anwendung nicht versucht, ungültige Handles zu verwenden.
-   **Details zum Ende von Heaps** : überprüft auf Probleme mit der Arbeitsspeicher Beschädigung im Heap.
-   **Details zu Eingabe-/ausgabestopps** : überwacht die Ausführung asynchroner e/a und führt verschiedene Überprüfungen durch.
-   **Details** zu "Details zum Ende"-erkennt Verluste durch Nachverfolgen der von einer DLL erstellten Ressourcen, die nicht durch den Zeitpunkt der dll-Entladung freigegeben wurden.
-   Sperr **Details für Sperren** : überprüft die korrekte Verwendung für kritische Abschnitte.
-   **Details** zum Arbeitsspeicher-Ende: stellt sicher, dass die APIs für Manipulationen virtueller Bereiche ordnungsgemäß verwendet werden (z. b. virtualbelegc, MapViewOfFile).
-   **TLS-Enddetails** : stellt sicher, dass die lokalen Thread Speicher-APIs ordnungsgemäß verwendet werden
-   **Thread Pool-Enddetails** : sicherstellen der korrekten Verwendung von Thread Pool-APIs und Erzwingen von Konsistenzprüfungen für Worker-Thread-Zustände nach einem Rückruf

Wenn Ihre Anwendung von einer "Pre-Vista"-Anwendung migriert wird, sollten Sie die "luapriv" (auch als UAC-Prüfungen bezeichnet) nutzen. Der Berechtigungs Prätor "eingeschränkte Benutzerkonten" (luapriv) hat zwei primäre Ziele:

-   Vorher **sage**: Wenn Sie eine Anwendung mit Administratorrechten ausführen, prognostizieren Sie vorher, ob diese Anwendung ebenfalls funktioniert, wenn Sie mit weniger Berechtigungen ausgeführt wird (in der Regel als normaler Benutzer). Wenn die Anwendung z. b. in Dateien schreibt, die nur Administratoren Zugriff gewähren, kann diese Anwendung nicht in dieselbe Datei schreiben, wenn Sie als nicht Administrator ausgeführt wird.
-   **Diagnose**: identifizieren Sie bei Ausführung mit nicht-Administrator Berechtigungen potenzielle Probleme, die möglicherweise bereits mit der aktuellen Ausführung vorhanden sind. Wenn das vorherige Beispiel fortgesetzt wird und die Anwendung versucht, in eine Datei zu schreiben, die nur Administratoren von Administrator Gruppen Zugriff gewährt, erhält die Anwendung den Fehler "Zugriff \_ verweigert". Wenn die Anwendung nicht ordnungsgemäß funktioniert, ist dieser Vorgang möglicherweise der Übeltäter.

Luapriv identifiziert die folgenden Arten von Problemen:



| **Mögliches Problem**       | **Beschreibung**                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Eingeschränkte Namespaces     | Wenn Sie ein benanntes Synchronisierungs Objekt (Ereignis, Semaphore, Mutex usw.) ohne Namespace erstellen, kann die Ausführung ohne Berechtigungen für einige Betriebssysteme erschwert werden, weil das Betriebssystem das Objekt in einem eingeschränkten Namespace platzieren kann. Das Erstellen eines solchen Objekts in einem eingeschränkten Namespace (z. b. dem globalen Namespace) erfordert SeCreateGlobalPrivilege, das nur Administratoren gewährt wird.<br/> Luapriv Flags beide diese Probleme, wenn Sie erkannt werden.<br/> |
| Prüfungen durch einen festen Administrator | Einige Anwendungen befragen das Sicherheits Token des Benutzers, um herauszufinden, wie viel Berechtigungen er hat. In diesen Fällen kann die Anwendung das Verhalten ändern, je nachdem, wie viel Leistung der Benutzer hat. <br/> Luapriv Flags-API-Aufrufe, die diese Informationen zurückgeben.<br/>                                                                                                                                                                                                |
| Anfordern von Berechtigungen     | Eine Anwendung versucht möglicherweise, ein sicherheitsrelevantes Privileg (z. b. SeTcbPrivilege oder SeSecurityPrivilege) zu aktivieren, bevor Sie einen Vorgang ausführt, für den Sie erforderlich ist. <br/> Luapriv-Flags versuchen, sicherheitsrelevante Berechtigungen zu aktivieren. <br/>                                                                                                                                                                                                                               |
| Fehlende Berechtigungen        | Wenn eine Anwendung versucht, eine Berechtigung zu aktivieren, die der Benutzer nicht besitzt, weist dies wahrscheinlich darauf hin, dass die Anwendung die Berechtigung erwartet, was zu Verhaltens unterschieden führen kann. <br/> Fehler bei luapriv-Flags bei Berechtigungsanforderungen. <br/>                                                                                                                                                                                                                                       |
| INI-File Vorgänge       | Versuche zum Schreiben in zugeordnete ini-Dateien ("Beschreib teprivateprofilesection" und ähnliche APIs) können als nicht Administrator Benutzer fehlschlagen. <br/> Luapriv Flags solche Vorgänge.<br/>                                                                                                                                                                                                                                                                                                            |
| Zugriff verweigert             | Wenn die Anwendung versucht, auf ein Objekt zuzugreifen (Datei, Registrierungsschlüssel usw.), der Versuch jedoch aufgrund unzureichenden Zugriffs fehlschlägt, erwartet die Anwendung wahrscheinlich, dass Sie mit mehr Berechtigungen ausgeführt wird. <br/> Luapriv Flags Object-Open-Versuche, bei denen der Zugriff \_ verweigert wird, und ähnliche Fehler.<br/>                                                                                                                                                               |
| Verweigern von ACEs                 | Wenn ein Objekt deny-ACEs in der DACL aufweist, wird der Zugriff auf bestimmte Entitäten explizit verweigert. <br/> Dies ist nicht üblich, und die Vorhersage ist schwierig, sodass die luapriv-Flags ACEs ablehnen, wenn Sie gefunden werden.<br/>                                                                                                                                                                                                                                                                     |
| Zugriff eingeschränkt         | Wenn eine Anwendung versucht, ein Objekt für Rechte zu öffnen, die nicht normalen Benutzern gewährt werden (z. b. Wenn Sie versuchen, in eine Datei zu schreiben, die nur von Administratoren bearbeitet werden kann), funktioniert die Anwendung wahrscheinlich nicht, wenn Sie als normaler Benutzer ausgeführt wird. <br/> Luapriv Flags solche Vorgänge.<br/>                                                                                                                                                                      |
| maximal \_ zulässig          | Wenn eine Anwendung ein Objekt für maximal zulässige Berechtigungen öffnet \_ , erfolgt die tatsächliche Zugriffs Überprüfung für das Objekt an anderer Stelle. Die meisten Codes, die dies tun, funktionieren nicht ordnungsgemäß und funktionieren fast sicherlich anders, wenn Sie ohne Berechtigungen ausgeführt werden. <br/> Luapriv markiert daher alle Vorfälle von maximal zulässigen Vorfällen \_ . <br/>                                                                                                                                                            |



 

Häufig übersehene Probleme werden bei den folgenden Überprüfungen aufgezeichnet:

-   Gefährliche APIs-Enddetails
-   Details zu geänderten Stapel Stopps
-   Zeitrollover

Wir haben einen neuen Druck-Verifier hinzugefügt. Diese Ebene hilft dabei, Probleme zu finden und zu beheben, die möglicherweise auftreten, wenn eine Anwendung das Druck Subsystem aufruft. Print Verifier zielt auf die beiden Ebenen des Druck Subsystems, der printapi-Schicht und der PrintDriver-Ebene ab.

*API-Ebene drucken*

Print Verifier testet die Schnittstelle zwischen einem Programm und winspool. drv und prntvpt.dll und testet die Schnittstellen dieser DLLs. Die Regeln zum Aufrufen von Funktionen in dieser Schnittstelle finden Sie im MSDN-Hilfe Abschnitt für APIs, die von winspool. drv und prntvpt.dll exportiert werden.

*Drucktreiber Ebene*

Außerdem testet die Druck Überprüfung die Schnittstelle zwischen einem Kern Druckertreiber, z. b. UNIDRV.DLL, UNIDRUI.DLL, PSCRIPT5.DLL, PS5UI.DLL oder MXDWDRV.DLL und den Druckertreiber-Plug-ins. Informationen zu dieser Schnittstelle finden Sie im MSDN und im WDK.

Beachten Sie, dass einige dieser Überprüfungen nur für Windows 7 gelten, andere unter Windows 7.

In der Regel führen nur Debugversionen den Application Verifier aus, sodass die Leistung im Allgemeinen kein Problem ist. Wenn Leistungsprobleme bei der Verwendung dieser oder einer anderen Application Verifier Prüfung auftreten, führen Sie eine Überprüfung gleichzeitig aus, bis Sie alle erforderlichen Überprüfungen durchgeführt haben.

Fast 10% der Anwendungs Abstürze auf Windows-Systemen sind auf eine Heap Beschädigung zurückzuführen. Diese Abstürze können nach dem Fakt fast nicht debuggt werden. Die beste Möglichkeit, diese Probleme zu vermeiden, besteht darin, die in Application Verifier gefundenen seitenheapfeatures zu testen. Es gibt zwei Arten von Seiten Heaps: "Full" und "Light". Der Standardwert ist "Full". Dadurch wird erzwungen, dass ein Debugger beim Erkennen von Beschädigungen sofort beendet wird. Diese Funktion muss im Debugger ausgeführt werden. Es ist jedoch auch die größte Ressourcen anspruchsvolle. Wenn ein Benutzer über zeitliche Probleme verfügt und bereits ein Szenario unter "Full" Page Heap ausgeführt hat, werden diese Probleme wahrscheinlich durch die Festlegung auf "Light" behoben. Außerdem stürzt der helle Seiten Heap erst ab, wenn der Prozess beendet wird. Es stellt eine Stapel Überwachung für die Zuordnung bereit, kann aber erheblich länger dauern, als die vollständige Entsprechung zu nutzen.

Überwachen Sie den Zuverlässigkeits Status der Anwendungen über das winqual-Webportal. In diesem Portal werden die Fehlerberichte angezeigt, die über Windows-Fehlerberichterstattung gesammelt wurden. Daher ist es einfach, die häufigsten Fehler zu identifizieren. Weitere Informationen hierzu finden Sie unter Windows-Fehlerberichterstattung: Getting Started. Microsoft berechnet diesen Dienst nicht.

Um winqual zu nutzen, müssen Sie folgende Schritte ausführen:

1.  Registrieren Sie Ihr Unternehmen für winqual, das eine VeriSign-ID erfordert. Windows 7-Informationen zu winqual finden Sie im Entwickler Portal unter Windows Vista SP1 \\ Windows Server 2008. In Kürze wird ein Windows 7-Speicherort angezeigt.
2.  Ordnen Sie die ISV-Anwendungen einem Produktnamen und dem ISV-Namen zu, mit dem die Fehlerberichte mit dem Unternehmen verknüpft werden. Andere ISVs können Ihre Fehlerberichte nicht anzeigen.
3.  Verwenden Sie das Portal, um die wichtigsten Probleme zu identifizieren. ISVs können auch Antworten erstellen, die Kunden informieren, welche Schritte nach einem Fehler ausgeführt werden müssen. Das Antwortsystem unterstützt weltweit mehr als 10 Sprachen.

Ein weiterer Hinweis: Application Verifier ist nur so gut wie die Codepfade, für die Sie ihn ausführen. Der Wert, mit dem dieses Tool mit einem Code Coverage Tool kombiniert werden kann, kann nicht überschrieben werden.

## <a name="links-to-other-resources"></a>Links zu anderen Ressourcen

**Debuggingtools für Windows:**

-   [Übersicht und Download Site](https://msdn.microsoft.com/windows/hardware/bg127145)
-   [MSDN-Online Dokumentation](/windows-hardware/drivers/debugger/)

**Application Verifier:**

-   [Übersicht](/previous-versions/ms220948(v=vs.80))
-   [Download](https://www.microsoft.com/downloads/details.aspx?FamilyID=c4a25ab9-649d-4a1b-b4a7-c9d8b095df18&amp;DisplayLang=en)
-   [Application Verifier für Microsoft Visual Studio 2008/.NET Framework 3,5](/previous-versions/ms220948(v=vs.80))

    **Hinweis:** die Application Verifier Version, die in Visual Studio ausgeliefert wird, ist veraltet. Verwenden Sie nach Möglichkeit stattdessen das eigenständige Paket. Aus diesem Grund werden in zukünftigen Versionen von Visual Studio keine eingebetteten Application Verifier mehr angezeigt.

**WinQual**

-   [Windows Quality Online Services (Winqual)](/windows-hardware/drivers/dashboard/winqual-submission-tool--winqualexe-)
-   [Windows-Fehlerberichterstattung: "Getting Started"](../wer/using-wer.md)

 

 
