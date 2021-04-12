---
description: Mit der com+-Version 1,5 werden neue Funktionen hinzugefügt, die entwickelt wurden, um die allgemeine Skalierbarkeit, Verfügbarkeit und Verwaltbarkeit von com+-Anwendungen sowohl für Entwickler als auch für Systemadministratoren zu erhöhen.
ms.assetid: e7073ba5-6b19-4d94-8cc0-b4e16bb44afd
title: Neuerungen in com+ 1,5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 994237002ea5d19c2cb00364f1064df38ed7271f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393170"
---
# <a name="whats-new-in-com-15"></a>Neues in com+ 1,5

Mit der com+-Version 1,5 werden neue Funktionen hinzugefügt, die entwickelt wurden, um die allgemeine Skalierbarkeit, Verfügbarkeit und Verwaltbarkeit von com+-Anwendungen sowohl für Entwickler als auch für Systemadministratoren zu erhöhen.

Com+ 1,5 ist ab Windows XP und Windows Server 2003 verfügbar. Die neuen com+ 1,5-Features sind in Windows 2000 nicht verfügbar.

## <a name="application-level-access-checks-enabled-by-default"></a>Standardmäßig aktivierte Application-Level Zugriffs Überprüfungen

Im Rahmen der verbesserten Sicherheit des Systems sind Zugriffs Überprüfungen beim Erstellen einer COM+-Anwendung standardmäßig aktiviert. In früheren Versionen wurden Zugriffs Überprüfungen standardmäßig auf der Anwendungsebene deaktiviert und auf Komponentenebene standardmäßig aktiviert. Ab Windows Server 2003 sind Zugriffs Überprüfungen standardmäßig auf Anwendungsebene aktiviert und auf Komponentenebene standardmäßig deaktiviert. Weitere Informationen und Verfahren zum Ändern der Standardeinstellungen finden Sie unter [Erstellen einer neuen COM+-Anwendung](creating-a-new-com--application.md), [Aktivieren von Zugriffs Überprüfungen für eine Anwendung](enabling-access-checks-for-an-application.md)und [Aktivieren von Zugriffs Überprüfungen auf der Komponentenebene](enabling-access-checks-at-the-component-level.md) .

## <a name="application-pooling"></a>Anwendungs Pooling

Mit der neuen concurrentapps-Eigenschaft des [**COMAdminCatalogObject**](comadmincatalogobject.md) -Objekts in der [**Anwendungs**](applications.md) Auflistung bietet com+-Anwendungs Pooling eine Skalierbarkeit für Single Thread-Prozesse und ist in den neuen com+-Anwendungs Wiederverwendungs Dienst integriert. Ausführliche Informationen finden Sie unter [com+-Anwendungs Pooling](com--application-pooling.md) .

## <a name="application-recycling"></a>Anwendungs Wiederverwendung

Die Wiederverwendung von Anwendungen erhöht die Gesamtstabilität Ihrer Anwendungen erheblich. Da die Leistung der meisten Anwendungen im Lauf der Zeit aufgrund von Faktoren wie Speicher Verlusten, Abhängigkeit von Drittanbieter Code und nicht skalierbarer Ressourcenverwendung beeinträchtigt werden kann, bietet die com+-Anwendungs Wiederverwendung eine einfache Lösung, um einen Prozess, der einer Anwendung zugeordnet ist, ordnungsgemäß herunterzufahren und neu zu starten. Ausführliche Informationen finden Sie unter [com+-Anwendungs Wiederverwendung](com--application-recycling.md) . Eine Schritt-für-Schritt-Anleitung zum Konfigurieren der Prozess Wiederverwendung finden Sie auch unter "Konfigurieren der Prozess Wiederverwendung" in der Hilfe zur Verwaltung von Komponenten Diensten.

## <a name="com-partitions"></a>Com+-Partitionen

In dieser Version führt com+ Unterstützung für COM+-Partitionen ein, ein Feature, mit dem mehrere Versionen von com+-Anwendungen auf demselben Computer installiert und konfiguriert werden können. Mit dieser Funktion können Sie die Kosten und den zeitaufwändigen Aufwand für die Verwendung mehrerer Server für die Verwaltung unterschiedlicher Versionen einer Anwendung sparen. Auf einem einzelnen Computer fungiert jede Partition als virtueller Server. Nachdem Sie die Anwendung in jeder Partition installiert haben, erstellen Sie Partitions Sätze, die Benutzer den logischen Servern zuordnen. Ausführliche Informationen zum Einrichten und Verwalten von COM+-Partitionen finden Sie unter [com+-Partitionen](com--partitions.md) . Eine Schritt-für-Schritt-Anleitung finden Sie auch unter "Verwalten von Anwendungs Partitionen" in der Hilfe zur Verwaltung von Komponenten Diensten.

## <a name="com-services-without-components"></a>Com+-Dienste ohne Komponenten

Mit com+ 1,5 können Sie die von com+ bereitgestellten Dienste verwenden, ohne eine-Komponente zu erstellen, die die Methoden enthält, mit denen diese Dienste aufgerufen werden. Dadurch profitieren Sie von Entwicklern, die normalerweise keine Komponenten verwenden, aber com+-Dienste wie Transaktionen oder com+-Tracker verwenden möchten. Durch die Verwendung von COM+-Diensten ohne Komponenten können Entwickler den Aufwand vermeiden, mit dem eine Komponente erstellt wird, die nur für den Zugriff auf die benötigten com+-Dienste verwendet wird. Ausführliche Informationen finden Sie unter [com+-Dienste ohne Komponenten](com--services-without-components.md) .

## <a name="com-soap-service"></a>Com+-SOAP-Dienst

Mit com+ 1,5 können Sie jetzt eine COM+-Anwendung als XML-Webdienst verfügbar machen. Sie können einen XML-Webdienst, unabhängig davon, ob er mit com+ bereitgestellt wurde, auch transparent als COM-Komponente verwenden. Dies bedeutet, dass Sie auf einfache Weise neue XML-Webdienste aus vorhandenen COM+-Anwendungen erstellen und XML-Webdienste problemlos in neue COM+-Anwendungen integrieren können. Ausführliche Informationen finden Sie unter [com+-SOAP-Dienst](com--soap-service.md) .

## <a name="configurable-isolation-levels"></a>Konfigurierbare Isolations Stufen

Com+-Entwickler können die neue txisolationlevel-Eigenschaft oder das Verwaltungs Programmkomponenten Dienste verwenden, um die Isolationsstufe einer Anwendung nach Bedarf zu konfigurieren und gleichzeitig die Parallelität, Leistung und Skalierbarkeit zu erhöhen. Diese Flexibilität ermöglicht denjenigen, die über die richtige Menge an Fachkenntnissen verfügen, die jeweils letzte Unze Durchsatz aus Ihren Anwendungen zu erzielen. Ausführliche Informationen finden Sie unter [Konfigurieren von Transaktions Isolations Stufen](configuring-transaction-isolation-levels.md) .

## <a name="creating-private-components"></a>Erstellen privater Komponenten

In Szenarien, in denen mehrere Hilfskomponenten in einer Anwendung vorhanden sind, die nur von anderen Komponenten innerhalb dieser Anwendung aufgerufen werden sollen, können Sie mit dieser Version von com+ die neue Eigenschaft "isprivatecomponent" verwenden, um diese Komponenten als privat zu markieren. (In der vorherigen Version von com+ mussten alle Komponenten öffentlich sein, um Zugriff auf COM+-Dienste zu haben. Dies bedeutet, dass diese Komponenten von anderen Anwendungen aus aktiviert werden könnten.) Eine private Komponente kann nur von anderen Komponenten in der gleichen Anwendung angezeigt und aktiviert werden, sodass Sie mehr Kontrolle darüber haben, welche Funktionalität verfügbar gemacht werden soll. Sie müssen nur die öffentlichen Komponenten dokumentieren und verwalten, während Sie private Komponenten verwenden, auf die von außerhalb der Anwendung nicht zugegriffen werden kann, die jedoch weiterhin alle com+-Dienste nutzen können.

## <a name="dtc-security-settings"></a>DTC-Sicherheitseinstellungen

Für den Microsoft Distributed Transaction Coordinator (DTC) wurden mehrere neue Sicherheitseinstellungen hinzugefügt, mit denen Sie Ihre Sicherheitsstufen für die Verwaltung verteilter Transaktionen anpassen können. Weitere Informationen zu diesen Einstellungen und deren Implementierung finden Sie unter DTC-Sicherheitsüberlegungen.

Zum Vereinfachen der gegenseitigen Authentifizierung ist der DTC auf die Ausführung unter dem Network Service-Konto beschränkt. Ausführliche Informationen finden Sie unter Verwalten von Konten und Berechtigungen.

Für die Wiederherstellung mit XA-Datenbanken wird empfohlen, dass dem Network Service-Konto die Berechtigungen und Rollen zur Verfügung gestellt werden, die zum Ausführen dieser Wiederherstellung erforderlich sind. Die genaue Methode hierfür ist für jede Datenbank spezifisch. Weitere Informationen finden Sie unter Deaktivieren nativer verteilter Transaktionen und Deaktivieren von Tip-und XA-Transaktionen.

Um bei der Verwendung von XA-Transaktionen ein sichereren System bereitzustellen, enthalten Windows Server 2003-Plattformen einen neuen Registrierungs Eintrag zum Angeben von XA-DLL-Dateien. Wenn Sie ein Upgrade auf Windows Server 2003 durchführen, können Sie mit den XA-Transaktionen arbeiten, indem Sie einen Registrierungs Eintrag unter **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ MSDTC \\ xadll** erstellen, wobei der Wert Name der Name der dll (im Format *dllName*. dll) und der Wert der vollständige Pfad der DLL-Datei ist. Sie müssen einen Eintrag für jede verwendete XA-DLL-Datei erstellen. Wenn der Computer, auf dem DTC ausgeführt wird, Teil eines Clusters ist, muss der Registrierungs Eintrag für jeden Knoten im Cluster erstellt werden. Weitere Informationen finden Sie unter Verwalten von XA-Transaktionen.

## <a name="low-memory-activation-gates"></a>Low-Memory Aktivierungs Gates

Mit dieser Version prüft com+ automatisch den Arbeitsspeicher, bevor ein com+-Server oder-Objekt erstellt wird. Wenn der Prozentsatz des für die Anwendung verfügbaren virtuellen Speichers unter einen festgelegten Schwellenwert fällt, schlägt die Aktivierung fehl, bevor das Objekt erstellt wird. Durch das Fehlschlagen dieser Aktivierungen, die normalerweise ausgeführt werden, erhöht der [com+-Low-Memory Activation Gates](com--low-memory-activation-gates.md) -Dienst die Systemzuverlässigkeit erheblich.

## <a name="moving-and-copying-com-components"></a>Verschieben und Kopieren von COM-Komponenten

Mit dieser Version können Sie die Komponenten mit com+ verschieben und kopieren. Dies bedeutet, dass Sie eine einzelne physische Implementierung einer Komponente viele verschiedene Male konfigurieren können. Sie erhalten die Wiederverwendung von Komponenten auf Binär Ebene anstelle der Quell Code Ebene. Dies führt zu weniger Code, geringeren Entwicklungskosten und schnellerer Markteinführungszeit. Ausführliche Informationen finden Sie unter [Verschieben von Komponenten](moving-components.md) und [Kopieren von Komponenten](copying-components.md) .

## <a name="network-access"></a>Netzwerkzugriff

Der com+-Netzwerk Zugriff ist unter Windows Server 2003 standardmäßig deaktiviert. Dies bedeutet, dass com+ standardmäßig nur lokal verwendet werden kann. Verwenden Sie das folgende Verfahren, um den com+-Netzwerk Zugriff zu aktivieren.

**So aktivieren Sie den com+-Netzwerk Zugriff**

1.  Zeigen Sie im **Startmenü** auf **Systemsteuerung**, **und wählen Sie** dann Software aus.

2.  Klicken Sie auf **Windows-Komponenten hinzufügen/entfernen**.

3.  Wählen Sie **Anwendungsserver** aus, und klicken Sie auf **Details**.

4.  Aktivieren Sie das Kontrollkästchen neben **com+-Netzwerk Zugriff aktivieren**, und klicken Sie dann auf **OK**.

5.  Klicken Sie auf **weiter** , um den Assistenten für Windows-Komponenten abzuschließen.

6.  Klicken Sie auf **Fertig stellen**, und beenden Sie den Assistenten.

Der Zugriff auf DTC-Netzwerk Transaktionen ist unter Windows Server 2003 standardmäßig deaktiviert. Auf diesen Plattformen kann der DTC standardmäßig nur lokale Transaktionen ausführen. Verwenden Sie das folgende Verfahren, um den DTC-Netzwerk Zugriff zu aktivieren.

> [!NOTE]
> Sie können auch den DTC-Netzwerk Zugriff aktivieren, indem Sie das Verwaltungs Programmkomponenten Dienste oder Programm gesteuert über die com+-Verwaltungs Bibliothek verwenden. Informationen zur Vorgehensweise finden Sie unter "Konfigurieren der DTC-Sicherheit" in der Hilfe zur Verwaltung von Komponenten Diensten.

**So aktivieren Sie den DTC-Netzwerk Zugriff**

1.  Zeigen Sie im **Startmenü** auf **Systemsteuerung**, **und wählen Sie** dann Software aus.

2.  Klicken Sie auf **Windows-Komponenten hinzufügen/entfernen**.

3.  Wählen Sie **Anwendungsserver** aus, und klicken Sie auf **Details**.

4.  Aktivieren Sie das Kontrollkästchen neben **Netzwerk-DTC-Zugriff aktivieren**, und klicken Sie dann auf **OK**.

5.  Klicken Sie auf **weiter** , um den Assistenten für Windows-Komponenten abzuschließen.

6.  Klicken Sie auf **Fertig stellen**, und beenden Sie den Assistenten.

## <a name="pausing-and-disabling-applications"></a>Anhalten und Deaktivieren von Anwendungen

Com+-Anwendungen sind jetzt besser verwaltbar. Ein Administrator kann com+-Server Anwendungen anhalten und fortsetzen oder COM+-Bibliotheks-oder Server Anwendungen oder sogar einzelne konfigurierte Komponenten deaktivieren und aktivieren. Sowohl das anhalten als auch das Deaktivieren von Features verhindern zukünftige Aktivierungen, ohne dass vorhandene Komponenten Instanzen beeinträchtigt werden. Weitere Informationen finden Sie unter "Verwalten von com+-Anwendungen" in der Hilfe zur Verwaltung von Komponenten Diensten.

## <a name="process-dumping"></a>Prozess Sicherung

Die Problembehandlung von Anwendungen in einer Produktionsumgebung ist nicht einfach. Wie erfassen Sie Informationen zu einem Problem, ohne die laufenden Prozesse zu beeinträchtigen? Com+ bietet nun eine Lösung durch das neue Prozess Sicherungs Feature. Diese Funktion ermöglicht es dem Systemadministrator, den gesamten Status eines Prozesses zu sichern, ohne ihn zu beenden. Weitere Informationen finden Sie unter "Verwalten des prozessdumptools für das Debuggen von com+-Anwendungen" in der Hilfe zur Verwaltung von Komponenten Diensten.

## <a name="process-initialization"></a>Prozess Initialisierung

Viele Server Anwendungen müssen eine bestimmte Initialisierung und Bereinigung durchführen, wenn Sie gestartet und heruntergefahren werden. Wenn Sie unter Windows Server 2003 ausgeführt werden, können Sie eine Klasse erstellen, die die [**IProcessInitializer**](/windows/desktop/api/ComSvcs/nn-comsvcs-iprocessinitializer) -Schnittstelle implementiert. Beim Starten des Prozesses wird [**IProcessInitializer:: Startup**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-startup) aufgerufen. beim Herunterfahren wird [**IProcessInitializer:: Shutdown**](/windows/desktop/api/ComSvcs/nf-comsvcs-iprocessinitializer-shutdown)aufgerufen. Dadurch haben Sie die Möglichkeit, erforderliche Aufgaben auszuführen, z. b. Verbindungen, Dateien und Caches zu initialisieren.

## <a name="running-com-applications-as-nt-services"></a>Ausführen von com+-Anwendungen als NT-Dienste

Com+-Entwickler können nun das Verwaltungs Programmkomponenten Dienste verwenden, um eine COM+-Serveranwendung als NT-Dienst zu konfigurieren und zu implementieren. Dies bedeutet, dass der Server automatisch gestartet oder neu gestartet werden kann, wenn die Anwendung immer ausgeführt werden muss. Ihre COM+-Anwendung kann als lokales Systemkonto ausgeführt werden, wenn Sie privilegierte Vorgänge ausführen muss. und die abhängigen Dienste Ihrer Anwendung können nun automatisch gestartet werden. Ausführliche Informationen finden Sie unter [com+-Anwendungen, die als Dienst Anwendungen ausgeführt](com--applications-running-as-service-applications.md) werden.

## <a name="side-by-side-assemblies"></a>Parallele Assemblys

Parallele Assemblys (SxS) ermöglichen Anwendungen, anzugeben, welche Version einer System-DLL oder einer klassischen COM-Komponente verwendet werden soll, z. b. MDAC, MFS, MSVCRT oder MSXML. Wenn eine ASP-Anwendung z. b. die MSXML-Version 2,0 verwendet, können Sie sicherstellen, dass diese Anwendung weiterhin MSXML-Version 2,0 verwendet, auch nachdem Service Packs auf den Server angewendet wurden. Das heißt, auch wenn eine neue Version von MSXML auf dem Computer installiert ist, bleibt Version 2,0 und wird von Ihrer Anwendung verwendet.

Zum Konfigurieren von SxS-Assemblys müssen Sie den Pfad zur DLL kennen und angeben, dass die com+-Manifest-Datei in jedem virtuellen Verzeichnis vorhanden ist, in dem die dll verwendet werden muss. Das com+-Manifest ist eine XML-Datei, die Informationen darüber enthält, wo eine DLL installiert ist. Das Manifest wird verwendet, um einen Aktivierungs Kontext für die Anwendung zu erstellen. Aktivierungs Kontexte ermöglichen es einer Anwendung, eine bestimmte dll-Version, com-Objektinstanz oder eine benutzerdefinierte Fensterversion zu laden. Sie können das Verwaltungs Programmkomponenten Dienste oder die ApplicationDirectory-Eigenschaft verwenden, um den vollständigen Pfad des Stamm Verzeichnisses der Anwendung einzugeben, das eine gültige SxS-Assemblymanifest-Datei enthält. Weitere Informationen finden Sie unter [isolierte Anwendungen und](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)parallele Assemblys.

## <a name="windows-error-reporting"></a>Windows-Fehlerberichterstattung

Com+ 1,5 bietet Unterstützung für die Komponente Windows-Fehlerberichterstattung (wer), die ab Windows XP verfügbar ist. Wer ermöglicht es Benutzern, Microsoft über Anwendungsfehler, Kernel Fehler und nicht reagierende Anwendungen zu benachrichtigen. Diese Benachrichtigungen ermöglichen es den Microsoft-Kundensupport Teams, technische Probleme effektiver zu lösen. Außerdem ermöglicht es die Windows-Fehlerberichterstattung Komponente com+-Entwicklern, Informationen zu erhalten, die zur Verbesserung ihrer Anwendungen verwendet werden können. Weitere Informationen finden Sie unter [Windows-Fehlerberichterstattung](/windows/desktop/wer/windows-error-reporting).

 

 
