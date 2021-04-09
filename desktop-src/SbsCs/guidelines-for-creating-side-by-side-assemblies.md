---
description: In den folgenden Richtlinien wird erläutert, wie Sie Ihre eigenen com-oder Win32-Assemblys nebeneinander erstellen.
ms.assetid: e10fe92c-bce8-420e-a84c-2748e929eb1b
title: Richtlinien zum Erstellen paralleler Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af8e8fd2bd31a65477b44d3afcf2156d5160a72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128829"
---
# <a name="guidelines-for-creating-side-by-side-assemblies"></a>Richtlinien zum Erstellen paralleler Assemblys

In den folgenden Richtlinien wird erläutert, wie Sie Ihre eigenen com-oder Win32-Assemblys nebeneinander erstellen. Sie müssen möglicherweise keine eigenen parallelen Assemblys erstellen, wenn die erforderliche Funktionalität von einer der [unterstützten Microsoft-](supported-microsoft-side-by-side-assemblies.md)parallelen Assemblys bereitgestellt wird. Verwenden Sie in diesem Fall die von Microsoft bereitgestellten Assemblys, und befolgen Sie die Verfahren zum Verwenden paralleler Assemblys in [Verwenden von isolierten Anwendungen und](using-isolated-applications-and-side-by-side-assemblies.md)parallelen Assemblys.

Überprüfen Sie zunächst, ob die Komponente für eine parallele Assembly geeignet ist. Weitere Informationen finden Sie unter [soll eine freigegebene Komponente als parallele Assembly bereit](should-you-provide-a-shared-component-as-a-side-by-side-assembly.md) gestellt werden?

Befolgen Sie die folgenden Richtlinien, um eine parallele Assembly zu erstellen:

-   Entscheiden Sie, welche Ressourcen in der Assembly enthalten sein sollen. Beachten Sie, dass eine Assembly aus einer oder mehreren Dateien besteht, die für Anwendungen und Kunden stets gleichzeitig bereitgestellt werden. Die Assembly dient als grundlegende Einheit für Benennung, Bindung, Versionsverwaltung, Bereitstellung und [Standardkonfiguration](default-configuration.md). Als allgemeine Regel gilt: Wenn Sie unsicher sind, ob zwei Ressourcen in derselben Assembly angehören, empfiehlt es sich, dass Sie in separaten Assemblys verfasst werden. In der Regel besteht eine parallele Assembly aus einer einzelnen dll.
-   Erstellen Sie ein [Assemblymanifest](manifests.md) für die Assembly. Das Manifest sollte das COM-Objekt oder die Typbibliotheken in der Assembly beschreiben. Weitere Informationen zu den zu erstellenden Assemblymanifesten finden [](assembly-manifests.md)Sie unter Assemblymanifeste.
-   Wertet die Verwendung von Objekten aus, wenn mehr als eine Version der Assembly auf dem System ausgeführt wird. Stellen Sie fest, ob für verschiedene Versionen der Assembly separate Datenstrukturen erforderlich sind, wie z. b. Speicher Abbild Dateien, Named Pipes, registrierte Windows-Meldungen und-Klassen, gemeinsam genutzter Speicher, Semaphore, Mutexe und Hardwaretreiber. Alle Datenstrukturen, die in Assemblyversionen verwendet werden, müssen abwärts kompatible Versionen sein. Entscheiden Sie, welche Datenstrukturen in verschiedenen Versionen verwendet werden können und welche Datenstrukturen für eine Version privat sein müssen. Stellen Sie fest, ob für freigegebene Datenstrukturen separate Synchronisierungs Objekte wie Semaphore und Mutexe erforderlich sind.
-   Erstellen Sie die dll als parallele Assembly, indem Sie die Richtlinien zum [Erstellen einer DLL für eine parallele Assembly](authoring-a-dll-for-a-side-by-side-assembly.md)einhalten.
-   Erstellen Sie einen Satz von Header Dateien und Hilfsfunktionen, um eine einfache Möglichkeit zur Versions Angabe von Registrierungs Schlüsseln mit dem assemblystatus zu bieten. Assemblys speichern Ihre Zustands Einstellungen häufig in Registrierungs Schlüsseln. Registrierungs Einstellungen müssen auf einzelner Versions Basis geschrieben werden, um mehrere Assemblyversionen zu isolieren, die gleichzeitig ausgeführt werden können. Entwerfen Sie Ihre parallele Assembly und dll, um den Status der Assembly bei parallelen Freigabe Szenarien ordnungsgemäß zu speichern und zu verarbeiten. Befolgen Sie die Richtlinien [zum Erstellen des Zustands Speichers für](authoring-state-storage-for-side-by-side-assemblies.md)parallele Assemblys.
-   Entwickler von Anwendungen, die [private](/windows/desktop/Msi/private-assemblies) Assemblys verwenden, sollten das Anwendungsverzeichnis sichern. Wenn die Anwendung mit dem [Windows Installer](../msi/windows-installer-portal.md)installiert wird, kann das Anwendungsverzeichnis mithilfe der lockberechtigungs-Tabelle gesichert werden. In der Regel erhält das System Lese-, Schreib-und Ausführungs Zugriff auf private Assemblys. alle anderen Prozesse erhalten nur den Ausführungs-und Lesezugriff.
-   Testen Sie die Assembly mithilfe von Szenarien mit paralleler Freigabe, um sicherzustellen, dass es sich um eine gültige parallele Assembly handelt. Die erfolgreiche Installation der Assembly ist nicht ausreichend, um sicherzustellen, dass Sie erwartungsgemäß funktioniert.
-   Übernehmen Sie eine Methode zum Nummerieren von Updates für die Assembly. Jede Assembly ist einer vierteiligen Versionsnummer zugeordnet. Von links nach rechts, die Teile Hauptversion, neben Version, Build und Revision sind durch Punkte getrennt. Ändern Sie die Haupt-oder Nebenzahl einer Assembly für eine Version, die mit früheren Versionen nicht kompatibel ist. Ändern Sie nur die Build-und Revisions Teile für abwärts kompatible Änderungen an der Assembly. Ein Entwickler kann z. b. eine nummerierungmethode übernehmen, in der alle 1.0.0. \* Versionsnummern beziehen sich auf die Assemblyversion 1.0.0.0.

 

 
