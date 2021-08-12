---
description: COM+ Version 1.5 fügt neue Features hinzu, die entwickelt wurden, um die allgemeine Skalierbarkeit, Verfügbarkeit und Verwaltbarkeit von COM+-Anwendungen sowohl für Entwickler als auch für Systemadministratoren zu erhöhen.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Neues in COM+ 1.5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0fd6705775e84f49d3a60afd7d89b7a5412b4a87fd5d04f202fadc77fd850d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118304881"
---
# <a name="whats-new-in-com-15"></a>Neues in COM+ 1.5

COM+ Version 1.5 fügt neue Features hinzu, die entwickelt wurden, um die allgemeine Skalierbarkeit, Verfügbarkeit und Verwaltbarkeit von COM+-Anwendungen sowohl für Entwickler als auch für Systemadministratoren zu erhöhen.

COM+ 1.5 ist ab Windows XP und Windows Server 2003 verfügbar. Die neuen COM+1.5-Features sind in Version Windows 2000 nicht verfügbar.

## <a name="application-level-access-checks-enabled-by-default"></a>Application-Level Zugriffsüberprüfungen standardmäßig aktiviert

Im Rahmen der verbesserten Sicherheit des Systems werden Zugriffsüberprüfungen standardmäßig aktiviert, wenn eine COM+-Anwendung erstellt wird. In früheren Versionen wurden Zugriffsüberprüfungen standardmäßig auf Anwendungsebene deaktiviert und standardmäßig auf Komponentenebene aktiviert. Ab Windows Server 2003 werden Zugriffsüberprüfungen standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert. Weitere Informationen und Verfahren zum Ändern der Standardeinstellungen [](enabling-access-checks-at-the-component-level.md) finden Sie unter Erstellen einer neuen [COM+-Anwendung](creating-a-new-com--application.md) [,](enabling-access-checks-for-an-application.md)Aktivieren von Zugriffsüberprüfungen für eine Anwendung und Aktivieren von Zugriffsüberprüfungen auf Komponentenebene.

## <a name="application-pooling"></a>Anwendungspooling

Mit der neuen ConcurrentApps-Eigenschaft des [**COMAdminCatalogObject-Objekts**](comadmincatalogobject.md) in der [**Anwendungssammlung**](applications.md) fügt COM+-Anwendungspooling Skalierbarkeit für Singlethreadprozesse hinzu und ist in den neuen COM+-Anwendungswiederverwendungsdienst integriert. Ausführliche [Informationen finden Sie unter COM+-Anwendungspooling.](com--application-pooling.md)

## <a name="application-recycling"></a>Wiederverwendung von Anwendungen

Die Wiederverwendung von Anwendungen erhöht die Gesamtstabilität Ihrer Anwendungen erheblich. Da die Leistung der meisten Anwendungen im Laufe der Zeit aufgrund von Faktoren wie Arbeitsspeicherverlusten, der Abhängigkeit von Drittanbietercode und der nicht skalierbaren Ressourcennutzung beeinträchtigt werden kann, bietet die COM+-Anwendungswiederverwendung eine einfache Lösung zum ordnungsgemäßen Herunterfahren eines mit einer Anwendung verbundenen Prozesses und zum Neustarten. Ausführliche [Informationen finden Sie unter COM+-Anwendungswiederverwendung.](com--application-recycling.md) Eine Schritt-für-Schritt-Anleitung zum Konfigurieren der Prozesswiederverwendung finden Sie auch unter "Konfigurieren der Prozesswiederverwendung" in der Hilfe zur Verwaltung von Komponentendiensten.

## <a name="com-partitions"></a>COM+-Partitionen

In diesem Release bietet COM+ Unterstützung für COM+-Partitionen, ein Feature, mit dem mehrere Versionen von COM+-Anwendungen auf demselben Computer installiert und konfiguriert werden können. Mit diesem Feature können Sie die Kosten und den zeitaufwändigen Aufwand sparen, wenn Sie mehrere Server verwenden, um verschiedene Versionen einer Anwendung zu verwalten. Auf einem einzelnen Computer fungiert jede Partition tatsächlich als virtueller Server. Nach der Installation der Anwendung in jeder Partition erstellen Sie Partitionssätze, die Benutzer den logischen Servern zuordnen. Ausführliche [Informationen zum Einrichten](com--partitions.md) und Verwalten von COM+-Partitionen finden Sie unter COM+-Partitionen. Schritt-für-Schritt-Verfahren finden Sie auch unter "Verwalten von Anwendungspartitionen" in der Hilfe zur Verwaltung von Komponentendiensten.

## <a name="com-services-without-components"></a>COM+-Dienste ohne Komponenten

Mit COM+ 1.5 können Sie die von COM+ bereitgestellten Dienste verwenden, ohne eine Komponente erstellen zu müssen, die die Methoden enthält, die diese Dienste aufrufen. Dies hat große Vorteile für Entwickler, die normalerweise keine Komponenten verwenden, aber COM+-Dienste wie Transaktionen oder die COM+-Tracker verwenden möchten. Durch die Verwendung von COM+-Diensten ohne Komponenten können Entwickler den Aufwand vermeiden, eine Komponente zu erstellen, die nur für den Zugriff auf die benötigten COM+-Dienste verwendet wird. Ausführliche [Informationen finden Sie unter COM+-Dienste](com--services-without-components.md) ohne Komponenten.

## <a name="com-soap-service"></a>COM+-SOAP-Dienst

Mit COM+ 1.5 können Sie jetzt eine COM+-Anwendung als XML-Webdienst verfügbar machen. Sie können auch transparent einen XML-Webdienst als COM-Komponente verwenden, unabhängig davon, ob er mit COM+ bereitgestellt wird oder nicht. Dies bedeutet, dass Sie ganz einfach neue XML-Webdienste aus vorhandenen COM+-Anwendungen erstellen und XML-Webdienste problemlos in neue COM+-Anwendungen integrieren können. Ausführliche [Informationen finden Sie unter COM+-SOAP-Dienst.](com--soap-service.md)

## <a name="configurable-isolation-levels"></a>Konfigurierbare Isolationsstufen

COM+-Entwickler können die neue TxIsolationLevel-Eigenschaft oder das Component Services-Verwaltungstool verwenden, um die Isolationsstufe einer Anwendung nach Bedarf zu konfigurieren und so die Parallelität, Leistung und Skalierbarkeit zu erhöhen. Diese Flexibilität ermöglicht es Personen mit dem richtigen Fachwissen, jede letzte Unzen Durchsatz aus ihren Anwendungen zu erhalten. Ausführliche [Informationen finden Sie unter Konfigurieren von Transaktionsisolationsstufen.](configuring-transaction-isolation-levels.md)

## <a name="creating-private-components"></a>Erstellen privater Komponenten

In Szenarien mit mehreren Hilfskomponenten in einer Anwendung, die nur von anderen Komponenten innerhalb dieser Anwendung aufgerufen werden sollen, können Sie mit dieser Com+-Version die neue Eigenschaft IsPrivateComponent verwenden, um diese Komponenten als privat zu markieren. (In der vorherigen Version von COM+ mussten alle Komponenten öffentlich sein, um Zugriff auf COM+-Dienste zu haben, was bedeutet, dass diese Komponenten von anderen Anwendungen aktiviert werden konnten.) Eine private Komponente kann nur von anderen Komponenten in derselben Anwendung gesehen und aktiviert werden, was Ihnen mehr Kontrolle darüber gibt, welche Funktionalität verfügbar ist. Sie müssen nur die öffentlichen Komponenten dokumentieren und verwalten, während Sie private Komponenten verwenden, auf die von außerhalb der Anwendung nicht zugegriffen werden kann, die jedoch weiterhin alle COM+-Dienste nutzen können.

## <a name="dtc-security-settings"></a>DTC-Einstellungen

Es wurden mehrere neue Sicherheitseinstellungen für den Microsoft Distributed Transaction Coordinator (DTC) hinzugefügt, mit denen Sie Ihre Sicherheitsebenen für die Verwaltung verteilter Transaktionen anpassen können. Weitere Informationen zu diesen Einstellungen und deren Implementierung finden Sie unter DTC Security Considerations (Überlegungen zur DTC-Sicherheit).

Zur Vereinfachung der gegenseitigen Authentifizierung ist der DTC auf die Ausführung unter dem NetworkService-Konto beschränkt. Ausführliche Informationen finden Sie unter Verwalten von Konten und Berechtigungen.

Für die Wiederherstellung mit XA-Datenbanken wird empfohlen, dem NetworkService-Konto die Berechtigungen und Rollen zur Verfügung zu stellen, die für diese Wiederherstellung erforderlich sind. Die genaue Methode, dies zu tun, ist für jede Datenbank spezifisch. Weitere Informationen finden Sie unter Deaktivieren nativer verteilter Transaktionen und Deaktivieren von TIP- und XA-Transaktionen.

Um bei der Verwendung von XA-Transaktionen ein sichereres System zu bieten, enthalten Windows Server 2003-Plattformen einen neuen Registrierungseintrag zum Angeben von XA-DLL-Dateien. Beim Upgrade auf Windows Server 2003 können Sie wie zuvor mit XA-Transaktionen arbeiten, indem Sie einen Registrierungseintrag unter **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ MSDTC \\ XADLL** erstellen. Dabei ist der Wertname der Name der DLL (im Format *dllname*.dll), und der Wert ist der vollständige Pfad der DLL-Datei. Sie müssen einen Eintrag für jede XA-DLL-Datei erstellen, die verwendet wird. Wenn der Computer, auf dem DTC ausgeführt wird, Teil eines Clusters ist, muss der Registrierungseintrag für jeden Knoten im Cluster vorgenommen werden. Weitere Informationen finden Sie unter Verwalten von XA-Transaktionen.

## <a name="low-memory-activation-gates"></a>Low-Memory Activation Gates

In dieser Version überprüft COM+ automatisch den Arbeitsspeicher, bevor ein COM+-Server oder -Objekt erstellt wird. Wenn der Prozentsatz des für die Anwendung verfügbaren virtuellen Arbeitsspeichers unter einen festen Schwellenwert fällt, schlägt die Aktivierung fehl, bevor das Objekt erstellt wird. Durch das Fehlschlagen dieser Aktivierungen, die normalerweise ausgeführt werden, erhöht der [COM+-Low-Memory Activation Gates-Dienst](com--low-memory-activation-gates.md) die Systemzuverlässigkeit stark.

## <a name="moving-and-copying-com-components"></a>Verschieben und Kopieren von COM-Komponenten

Mit diesem Release können Sie mit COM+ Ihre Komponenten verschieben und kopieren. Dies bedeutet, dass Sie eine einzelne physische Implementierung einer Komponente mehrmals konfigurieren können. Sie erhalten die Wiederverwendung von Komponenten auf binärer Ebene und nicht auf Quellcodeebene. Dies führt zu weniger Code, geringeren Entwicklungskosten und einer schnelleren Markteinführungszeit. Ausführliche [Informationen finden Sie](moving-components.md) unter Verschieben von Komponenten und [Kopieren](copying-components.md) von Komponenten.

## <a name="network-access"></a>Netzwerkzugriff

Der COM+-Netzwerkzugriff ist auf Windows Server 2003 standardmäßig deaktiviert, was bedeutet, dass COM+ standardmäßig nur lokal verwendet werden kann. Verwenden Sie das folgende Verfahren, um den COM+-Netzwerkzugriff zu aktivieren.

**So aktivieren Sie den COM+-Netzwerkzugriff**

1.  Zeigen Sie **im Menü** Start auf **Systemsteuerung**, und wählen Sie dann Programme hinzufügen oder **entfernen aus.**

2.  Klicken **Sie auf Add/Remove Windows Components (Komponenten hinzufügen/entfernen).**

3.  Wählen Sie **Anwendungsserver** aus, und klicken Sie auf **Details**.

4.  Aktivieren Sie das Kontrollkästchen neben **Netzwerk-COM+-Zugriff aktivieren,** und klicken Sie dann auf **OK.**

5.  Klicken **Sie auf Weiter** , um den Assistenten Windows Komponenten abzuschließen.

6.  Klicken Sie auf **Fertig stellen**, und beenden Sie den Assistenten.

Der Zugriff auf DTC-Netzwerktransaktionen ist auf Windows Server 2003 standardmäßig deaktiviert. Auf diesen Plattformen kann der DTC standardmäßig nur lokale Transaktionen ausführen. Verwenden Sie das folgende Verfahren, um den DTC-Netzwerkzugriff zu aktivieren.

> [!NOTE]
> Sie können den DTC-Netzwerkzugriff auch über das Verwaltungstool Komponentendienste oder programmgesteuert über die COM+-Verwaltungsbibliothek aktivieren. Informationen zum Verfahren finden Sie unter "Konfigurieren der DTC-Sicherheit" in der Hilfe zur Verwaltung von Komponentendiensten.

**So aktivieren Sie den DTC-Netzwerkzugriff**

1.  Zeigen Sie **im Menü** Start auf **Systemsteuerung**, und wählen Sie dann Programme hinzufügen oder **entfernen aus.**

2.  Klicken **Sie auf Add/Remove Windows Components (Komponenten hinzufügen/entfernen).**

3.  Wählen Sie **Anwendungsserver** aus, und klicken Sie auf **Details**.

4.  Aktivieren Sie das Kontrollkästchen neben **Netzwerk-DTC-Zugriff aktivieren,** und klicken Sie dann auf **OK.**

5.  Klicken **Sie auf Weiter** , um den Assistenten Windows Komponenten abzuschließen.

6.  Klicken Sie auf **Fertig stellen**, und beenden Sie den Assistenten.

## <a name="pausing-and-disabling-applications"></a>Anhalten und Deaktivieren von Anwendungen

COM+-Anwendungen sind jetzt besser verwaltbar. Ein Administrator kann COM+-Serveranwendungen anhalten und fortsetzen oder COM+-Bibliotheks-, Serveranwendungen oder sogar einzelne konfigurierte Komponenten deaktivieren und aktivieren. Sowohl das Anhalten als auch das Deaktivieren von Features verhindern zukünftige Aktivierungen, ohne dass vorhandene Komponenteninstanzen betroffen sind. Weitere Informationen finden Sie unter "Verwalten von COM+-Anwendungen" in der Hilfe zur Verwaltung von Komponentendiensten.

## <a name="process-dumping"></a>Prozessdumkung

Die Problembehandlung für Anwendungen in einer Produktionsumgebung ist nicht einfach. Wie sammeln Sie Informationen zu einem Problem, ohne die ausgeführten Prozesse zu stören? COM+ bietet jetzt eine Lösung über das neue Prozessabbildfeature. Mit diesem Feature kann der Systemadministrator den gesamten Zustand eines Prozesses abbilden, ohne ihn zu beenden. Weitere Informationen finden Sie unter "Verwalten des Prozessabbildtools zum Debuggen von COM+-Anwendungen" in der Hilfe zur Verwaltung von Komponentendiensten.

## <a name="process-initialization"></a>Prozessin initialisierung

Viele Serveranwendungen müssen eine bestimmte Initialisierung und Bereinigung ausführen, wenn sie gestartet und heruntergefahren werden. Wenn Sie auf Windows Server 2003 ausführen, können Sie eine Klasse erstellen, die die [**IProcessInitializer-Schnittstelle**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) implementiert. Wenn der Prozess gestartet wird, ruft er [**IProcessInitializer::Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) auf und ruft beim Herunterfahren [**IProcessInitializer::Shutdown auf.**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown) Dies gibt Ihrer Komponente die Möglichkeit, die erforderlichen Aufgaben auszuführen, z. B. das Initialisieren von Verbindungen, Dateien und Caches.

## <a name="running-com-applications-as-nt-services"></a>Ausführen von COM+-Anwendungen als NT-Dienste

COM+-Entwickler können jetzt das Component Services-Verwaltungstool verwenden, um eine COM+-Serveranwendung als NT-Dienst zu konfigurieren und zu implementieren. Dies bedeutet, dass der Server automatisch gestartet oder neu gestartet werden kann, wenn Ihre Anwendung immer ausgeführt werden muss. dass Ihre COM+-Anwendung als lokales Systemkonto ausgeführt werden kann, wenn privilegierte Vorgänge ausgeführt werden müssen; und dass die abhängigen Dienste Ihrer Anwendung jetzt automatisch gestartet werden können. Ausführliche [Informationen finden Sie unter COM+-Anwendungen, die](com--applications-running-as-service-applications.md) als Dienstanwendungen ausgeführt werden.

## <a name="side-by-side-assemblies"></a>Seite-an-Seite-Assemblys

Mithilfe von SxS-Assemblys (Side-by-Side) können Anwendungen angeben, welche Version einer System-DLL oder klassischen COM-Komponente verwendet werden soll, z. B. MDAC, MFS, MSVCRT oder MSXML. Wenn eine ASP-Anwendung z. B. auf MSXML Version 2.0 basiert, können Sie sicherstellen, dass diese Anwendung auch dann weiterhin MSXML Version 2.0 verwendet, nachdem Service Packs auf den Server angewendet wurden. Das heißt, selbst wenn eine neue Version von MSXML auf dem Computer installiert ist, bleibt Version 2.0 erhalten und wird von Ihrer Anwendung verwendet.

Zum Konfigurieren von SxS-Assemblys müssen Sie den Pfad zur DLL kennen und wissen, dass die COM+-Manifestdatei in jedem virtuellen Verzeichnis vorhanden ist, das die DLL verwenden muss. Das COM+-Manifest ist eine XML-Datei, die Informationen darüber enthält, wo eine DLL installiert ist. Das Manifest wird verwendet, um einen Aktivierungskontext für die Anwendung zu erstellen. Aktivierungskontexte ermöglichen es einer Anwendung, eine bestimmte DLL-Version, EINE COM-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden. Sie können das Component Services-Verwaltungstool oder die ApplicationDirectory-Eigenschaft verwenden, um den vollständigen Pfad des Anwendungsstammverzeichnisses ein eingaben, das eine gültige SxS-Assemblymanifestdatei enthält. Weitere Informationen finden Sie unter [Isolierte Anwendungen und nebenseitige Assemblys.](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)

## <a name="windows-error-reporting"></a>Windows-Fehlerberichterstattung

COM+ 1.5 bietet Unterstützung für die Windows-Fehlerberichterstattung (WER)-Komponente, die ab Windows XP verfügbar ist. MIT können Benutzer Microsoft über Anwendungsfehler, Kernelfehler und nicht reagierende Anwendungen benachrichtigen. Diese Benachrichtigungen ermöglichen es den Microsoft-Kundensupportteams, technische Probleme effektiver zu lösen. Darüber hinaus ermöglicht die Windows-Fehlerberichterstattung-Komponente COM+-Entwicklern, Informationen zu erhalten, die zur Verbesserung ihrer Anwendungen verwendet werden können. Weitere Informationen finden Sie unter [Windows-Fehlerberichterstattung](/windows/desktop/wer/windows-error-reporting).

 

 
