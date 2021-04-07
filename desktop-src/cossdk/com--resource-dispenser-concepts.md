---
description: Anwendungskomponenten verwenden den com+-Ressourcen Verteiler, um auf freigegebene, nicht dauerhafte Zustandsinformationen zuzugreifen und diese zu verwalten, z. b. Verbindungen zwischen Komponenten und einem bestimmten Ressourcen-Manager.
ms.assetid: 252c7180-61b1-485d-883d-36bf77357a29
title: Konzepte des com+-Ressourcen Verteilers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f0fcf281d6d7b8ed0e087b6d77e4d686e28e1fa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103748065"
---
# <a name="com-resource-dispenser-concepts"></a>Konzepte des com+-Ressourcen Verteilers

Anwendungskomponenten verwenden den com+-Ressourcen Verteiler, um auf freigegebene, nicht dauerhafte Zustandsinformationen zuzugreifen und diese zu verwalten, z. b. Verbindungen zwischen Komponenten und einem bestimmten Ressourcen-Manager. Zur Laufzeit werden dynamische Ressourcenpools, wie z. b. Datenbankverbindungen, Netzwerkverbindungen, Verbindungen zu Warteschlangen, Threads, Objekte und Speicherblöcke, dem Ressourcen Verteiler zur Verfügung gestellt. Beim Anwendungsprozess wird eine hohe Leistung erzielt, indem eine Mindestanzahl häufig verwendeter Ressourcen verwendet wird. Der Ressourcen Verteiler kann auch Transaktionen und die Zusammenstellung automatisieren. (Weitere Informationen zu dieser Funktion finden Sie unter [Automatische Ressourcenrückgewinnung](automatic-resource-reclamation.md) .)

> [!Note]  
> Eine *Ressource* ist alles, was ein Ressourcen Spender erstellt. Eine Verbindung mit einem Ressourcen-Manager ist beispielsweise eine gemeinsame Ressource. Ressourcen befinden sich im Arbeitsspeicher des Ressourcen Verteilers und werden niemals in den Dispenser-Manager kopiert. Eine Ressource ist nur durch ein undurchsichtiges handle (**RESID**) bekannt und kann möglicherweise Transaktionen ausführen. Obwohl es sich bei den verwalteten Ressourcen oft um Verbindungen mit einer Komponente handelt, die einen permanenten Zustand verwaltet, sind die Verbindungen selbst nicht dauerhaft. Ein Ressourcen Spender verwendet häufig einen zugehörigen Ressourcen-Manager, um den permanenten Zustand beizubehalten.

 

Die Architektur des com+-Ressourcen Dispenser-Systems besteht aus Ressourcen Spendern und einem Dispenser-Manager. Ressourcen Spender sind vom Benutzer bereitgestellte Komponenten, die Anwendungen einfache Schnittstellen für freigegebene Ressourcen bereitstellen. Der Dispenser Manager ist eine von com+ bereitgestellte Komponente, die die Aktivitäten der verschiedenen Ressourcen Spender koordiniert.

Ein Ressourcen Verteiler ist eine DLL-Komponente (Dynamic-Link Library), die mindestens zwei Schnittstellen bereitstellt. Der erste [**idispenser-Treiber**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver)stellt dem Dispenser-Manager grundlegende Informationen zum Erstellen, zerstören und eintragen der von ihm verwalteten Ressourcen bereit. Die zweite ist für die Anwendungen verfügbar und kann eine COM-Schnittstelle oder ein Satz von Schnittstellen oder eine Anwendungsprogrammierschnittstelle (Application Programming Interface, API) sein, mit der eine Komponente über eine Import Bibliothek verknüpft ist. Eine Anwendung kann einen beliebigen Ressourcen Verteiler abrufen, der wiederum eine beliebige API für die Anwendung anbieten kann. Wenn der Ressourcen Verteiler eine Automatisierungskomponente ist, kann von Microsoft Visual Basic darauf zugegriffen werden. Ein Ressourcen Verteiler wird instanziiert, wenn eine Anwendungs Komponente darauf verweist.

Der von com+ bereitgestellte Dispenser-Manager verfolgt Ressourcen Spender und Koordinaten zwischen diesen. Es werden zwei Schnittstellen implementiert: [**idispenser Server Manager**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispensermanager) und [**ihälter**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder). Ressourcen Spender registrieren sich selbst mithilfe der **idispenser Server Manager** -Schnittstelle. Der Dispenser-Manager gibt Ihnen dann einen Zeiger auf eine **ihälter** , die Sie verwenden, um den Dispenser-Manager über ihre Aktivitäten zu benachrichtigen.

Ein transaktionaler Ressourcen Verteiler muss in eine Distributed Transaction Coordinator Transaktion (DTC) eingetragen werden. Dies impliziert die Verwendung eines internen oder externen Ressourcen-Managers (für den Ressourcen Verteiler), der OLE-Transaktionen-kompatibel ist.

> [!Note]  
> Das COM+-Programmiermodell umfasst *deklarative Transaktionen*, die den Schutz der von einem Anwendungs Objekt ausgeführten Arbeit während ihrer Lebensdauer erleichtern. Wenn ein Anwendungs Objekt einen com+-Ressourcen Verteiler verwendet, ist die ausgeführten Aufgaben automatisch transaktional. Das heißt, die Komponente muss Transaktionen nicht explizit deklarieren. Diese Transaktionen werden in der OLE Transactions-Spezifikation definiert, die vom DTC implementiert und im Auftrag des Anwendungs Objekts durch com+ initiiert wird. Weitere Informationen finden Sie im DTC-Entwicklungs Handbuch.

 

Ressourcen müssen nicht transaktional sein. Ein Ressourcen Verteiler, der nicht transaktionale Ressourcen eingibt, kann dennoch eine hohe Leistung erzielen, da Anwendungs Objekte auf einen freigegebenen Pool dieser Ressourcen zugreifen können. Diese Art von Ressourcen Verteiler gibt den Wert " \_ false" aus der [**idispenser Server Driver:: enlistresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) -Methode zurück. Dies bedeutet, dass der Ressourcen Verteiler die Ressource nicht eingetragen hat, da die Ressource nicht transaktional ist.

Der Ressourcen Verteiler kann auch unabhängig von com+ funktionieren und bietet nur Funktionen für das Ressourcen Pooling. Wenn ein Ressourcen Verteiler z. b. eine API (z. b. ODBC) verfügbar macht, kann der Ressourcen Verteiler eine DLL sein, auf die die Anwendung über eine Import Bibliothek (oder die [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und die [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion) zugreift. Ein Ressourcen Verteiler kann auch eine COM-Komponente sein, auf die eine Anwendung durch Aufrufen von [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)zugreift. Ohne com+ kann die [**enlistresource**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispenserdriver-enlistresource) -Methode eines Ressourcen Verteilers nie aufgerufen werden, da der Dispenser-Manager keine Kenntnis von der aktuellen Komponenten Transaktion hat.

Beim Start muss sich eine ressourcendispenser-dll beim Dispenser-Manager registrieren. Der Dispenser Manager ist die steuernde Führungskraft, die das Laden und Entladen von Ressourcen Spendern verwaltet, den COM+-Kontext bereitstellt und den Inventur Statistik-Manager steuert. (Weitere Informationen finden Sie unter [com+-Dispenser-Manager](com--dispenser-manager.md).) Der Ressourcen Spender ruft zuerst die [**getdispenser Server Manager**](/windows/desktop/api/MtxDM/nf-mtxdm-getdispensermanager) -Funktion auf und ruft dann die [**idispenser Server Manager:: registerdispenser**](/windows/desktop/api/ComSvcs/nf-comsvcs-idispensermanager-registerdispenser) -Methode auf und übergibt dabei den [**idispenser Server Driver**](/windows/desktop/api/ComSvcs/nn-comsvcs-idispenserdriver) -Zeiger, den der Ressourcen Spender implementiert. Dieser Rückruf gibt einen Verweis auf [**ihälter**](/windows/desktop/api/ComSvcs/nn-comsvcs-iholder)zurück.

Zum Herunterfahren Ruft ein Ressourcen Spender [**ihälter:: Close**](/windows/desktop/api/ComSvcs/nf-comsvcs-iholder-close)auf. Um sicherzustellen, dass das Herunterfahren des Pakets ordnungsgemäß ausgeführt wird, muss ein Ressourcen Verteiler in der Lage sein, die Situation zu behandeln, in der Anrufe weiterhin von Geschäftsobjekten eingehen, nachdem com+ den Dispenser zum Herunterfahren aufgefordert

Die folgenden Themen in diesem Abschnitt enthalten ausführlichere Informationen über den com+-Ressourcen Verteiler Dienst:

-   [Com+-Dispenser-Manager](com--dispenser-manager.md)
-   [Com+-ressourcendispenser-Thread Typen](com--resource-dispenser-thread-types.md)
-   [In einem Pool zusammengefasste Ressourcen Zustände für com+-Ressourcen Spender verfügbar](pooled-resource-states-available-to-com--resource-dispenser.md)
-   [Eintragen einer Ressource in eine Transaktion](enlisting-a-resource-in-a-transaction.md)
-   [Ressourcen Zuordnungs Prozess Ressourcen Verteiler](resource-dispenser-resource-allocation-process.md)
-   [Nachverfolgen nicht zugewiesener Ressourcen](tracking-non-allocated-resources.md)
-   [Automatische Ressourcenrückgewinnung](automatic-resource-reclamation.md)
-   [In com+-ressourcendispenser-Schnittstellen verwendete Typen](types-used-in-com--resource-dispenser-interfaces.md)
-   [Com+-Ressourcen Verteiler Schnittstellen](com--resource-dispenser-interfaces.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aufgaben des com+-Ressourcen Verteilers](com--resource-dispenser-tasks.md)
</dt> </dl>

 

 
