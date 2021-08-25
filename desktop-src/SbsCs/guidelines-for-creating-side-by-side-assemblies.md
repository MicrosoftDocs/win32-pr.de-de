---
description: In den folgenden Richtlinien wird erläutert, wie Sie eigene COM- oder Win32-Assemblys erstellen.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Richtlinien zum Erstellen von nebenseitigen Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19054f0c48f74a373f0ce502cb6b52374db5ded00fcde3c284fad2609ba21e5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885250"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Richtlinien zum Erstellen von nebenseitigen Assemblys

In den folgenden Richtlinien wird erläutert, wie Sie eigene COM- oder Win32-Assemblys erstellen. Möglicherweise müssen Sie keine eigenen nebenseitigen Assemblys erstellen, wenn die erforderliche Funktionalität von einer der [unterstützten Microsoft-Nebenassemblys](supported-microsoft-side-by-side-assemblies.md)bereitgestellt wird. Verwenden Sie in diesem Fall die von Microsoft bereitgestellten Assemblys, und befolgen Sie die Verfahren für die Verwendung paralleler Assemblys in [Using Isolated Applications und Side-by-Side Assemblies](using-isolated-applications-and-side-by-side-assemblies.md).

Überlegen Sie zunächst, ob Ihre Komponente einen geeigneten Kandidaten für eine nebenseitige Assembly bildet. Weitere Informationen finden Sie unter [Sollten Sie eine freigegebene Komponente als nebenseitige Assembly bereitstellen?](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md)

Befolgen Sie die folgenden Richtlinien, um eine side-by-side-Assembly zu erstellen:

-   Entscheiden Sie, welche Ressourcen in die Assembly aufgenommen werden sollen. Beachten Sie, dass eine Assembly aus einer oder mehreren Dateien besteht, die Anwendungen und Kunden immer zusammen bereitgestellt werden. Die Assembly dient als grundlegende Einheit für Benennung, Bindung, Versionsinformationen, Bereitstellung und [Standardkonfiguration.](default-configuration.md) Wenn Sie sich nicht sicher sind, ob zwei Ressourcen zur gleichen Assembly gehören, wird als allgemeine Regel empfohlen, dass sie in separate Assemblys aufgenommen werden. In der Regel besteht eine side-by-side-Assembly aus einer einzelnen DLL.
-   Erstellen Sie ein [Assemblymanifest](manifests.md) für die Assembly. Das Manifest sollte das COM-Objekt oder die Typbibliotheken in der Assembly beschreiben. Weitere Informationen dazu, was in einem Assemblymanifest erstellt werden soll, finden Sie unter [Assemblymanifeste.](assembly-manifests.md)
-   Werten Sie die Verwendung von -Objekten aus, wenn mehr als eine Version der Assembly auf dem System ausgeführt wird. Bestimmen Sie, ob verschiedene Versionen der Assembly separate Datenstrukturen erfordern, z. B. speicherzuordnungsbasierte Dateien, Named Pipes, registrierte Windows Nachrichten und Klassen, freigegebener Arbeitsspeicher, Semaphore, Mutexe und Hardwaretreiber. Alle Datenstrukturen, die über Assemblyversionen hinweg verwendet werden, müssen abwärtskompatible Versionen sein. Entscheiden Sie, welche Datenstrukturen versionsübergreifend verwendet werden können und welche Datenstrukturen für eine Version privat sein müssen. Bestimmen Sie, ob freigegebene Datenstrukturen separate Synchronisierungsobjekte wie Semaphore und Mutexe erfordern.
-   Erstellen Sie Ihre DLL so, dass sie gut als parallele Assembly funktioniert, indem Sie die Richtlinien unter [Erstellen einer DLL für eine parallele Assembly](authoring-a-dll-for-a-side-by-side-assembly.md)einhalten.
-   Erstellen Sie eine Reihe von Headerdateien und Hilfsfunktionen, um eine einfache Möglichkeit zur Versionsversion von Registrierungsschlüsseln zu bieten, die den Assemblyzustand enthalten. Assemblys speichern ihre Zustandseinstellungen häufig in Registrierungsschlüsseln. Registrierungseinstellungen müssen einzeln geschrieben werden, um mehrere Assemblyversionen zu isolieren, die gleichzeitig ausgeführt werden können. Entwerfen Sie die side-by-side-Assembly und -DLL so, dass sie den Zustand der Assembly in Szenarios für die side-by-side-Freigabe ordnungsgemäß speichert und behandelt. Befolgen Sie die Richtlinien unter [Erstellungsstatus Storage für parallele Assemblys.](authoring-state-storage-for-side-by-side-assemblies.md)
-   Entwickler von Anwendungen, die [private Assemblys](/windows/desktop/Msi/private-assemblies) verwenden, sollten das Anwendungsverzeichnis schützen. Wenn die Anwendung mithilfe des [Windows Installers](../msi/windows-installer-portal.md)installiert wird, kann das Anwendungsverzeichnis mithilfe der LockPermissions-Tabelle geschützt werden. In der Regel erhält das System Lese-, Schreib- und Ausführungszugriff auf private Assemblys. alle anderen Prozesse erhalten nur Ausführungs- und Lesezugriff.
-   Testen Sie die Assembly mithilfe von Szenarien mit nebeneinander verwendeter Freigabe, um sicherzustellen, dass es sich um eine gültige side-by-side-Assembly handelt. Eine erfolgreiche Installation der Assembly reicht nicht aus, um sicherzustellen, dass sie erwartungsgemäß funktioniert.
-   Übernehmen Sie eine Methode zum Nummerieren von Updates für Ihre Assembly. Jede Assembly ist einer vierteiligen Versionsnummer zugeordnet. Die Haupt-, Neben-, Build- und Revisionsteile sind von links nach rechts durch Zeiträume getrennt. Ändern sie die Haupt- oder Nebennummer einer Assembly für eine Version, die mit früheren Versionen nicht kompatibel ist. Ändern Sie nur die Build- und Revisionsteile für abwärtskompatible Änderungen an der Assembly. Beispielsweise kann ein Entwickler eine Nummerierungsmethode verwenden, bei der alle 1.0.0 verwendet werden. \* Versionsnummern beziehen sich auf Updateversionen der Assemblyversion 1.0.0.0.

 

 
