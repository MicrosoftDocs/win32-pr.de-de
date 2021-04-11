---
description: Wenn Sie Ihre eigenen parallelen Assemblys erstellen, befolgen Sie die Richtlinien zum Erstellen paralleler Assemblys.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Erstellen von DLLs für parallele Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa15f3876c60ce55be00d60d8f417eb0c2cbf6ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216547"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Erstellen von DLLs für parallele Assemblys

Wenn Sie eigene parallele Assemblys erstellen, befolgen Sie die [Richtlinien zum Erstellen](guidelines-for-creating-side-by-side-assemblies.md) paralleler Assemblys und zum Erstellen beliebiger DLLs, die in der Assembly gemäß den folgenden Richtlinien verwendet werden:

-   Ihre DLLs sollten so entworfen werden, dass mehrere Versionen gleichzeitig und im selben Prozess ausgeführt werden können, ohne dass sich diese gegenseitig beeinträchtigen. Viele Anwendungen hosten z. b. mehrere Plug-ins, die jeweils eine andere Version einer Komponente benötigen. Der Entwickler muss die parallele Assembly entwerfen und testen, um sicherzustellen, dass mehrere Versionen der Komponenten ordnungsgemäß funktionieren, wenn Sie gleichzeitig im selben Prozess ausgeführt werden.

-   Wenn Sie beabsichtigen, die Komponente als freigegebene Komponente auf Systemen vor Windows XP bereitzustellen, müssen Sie die Komponente auf diesen Systemen weiterhin als eine einzelne Instanz freigegebene Komponente installieren. In diesem Fall müssen Sie sicherstellen, dass die Komponente abwärts kompatibel ist.

-   Evaluieren Sie die Verwendung von-Objekten, wenn mehr als eine Version der Assembly auf dem System ausgeführt wird. Stellen Sie fest, ob für verschiedene Versionen der Assembly separate Datenstrukturen erforderlich sind, wie z. b. Speicher Abbild Dateien, Named Pipes, registrierte Windows-Meldungen und-Klassen, gemeinsam genutzter Speicher, Semaphore, Mutexe und Hardwaretreiber. Alle Datenstrukturen, die in Assemblyversionen verwendet werden, müssen abwärts kompatibel sein. Entscheiden Sie, welche Datenstrukturen in verschiedenen Versionen verwendet werden können und welche Datenstrukturen für eine Version privat sein müssen. Stellen Sie fest, ob freigegebene Datenstrukturen separate Synchronisierungs Objekte erfordern, z. b. Semaphore und Mutexe.

-   Einige Objekte, z. b. Fenster Klassen und Atome, werden für jeden Prozess eindeutig benannt. Objekte, wie z. b. Fenster Klassen, sollten für jede Assembly mit dem Manifest versioniert werden. Verwenden Sie für Objekte, wie z. b. Atome, versionsspezifische Bezeichner, es sei denn, Sie planen eine Versions übergreifende Freigabe. Wenn Sie versionsspezifische Bezeichner verwenden, verwenden Sie die vierteilige Versionsnummer.

-   Fügen Sie keinen selbst Registrierungscode in eine DLL ein. Eine DLL in einer parallelen Assembly kann nicht selbst registriert werden.

-   Definieren Sie alle Versions spezifischen Namen in der DLL mit \# define-Anweisungen. Dadurch können alle Registrierungsschlüssel von einem Speicherort aus geändert werden. Wenn Sie eine neue Version der Assembly freigeben, müssen Sie diese define-Anweisung nur ändern \# . Beispiel:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Speichern Sie alle nicht persistenten Daten im temporären Verzeichnis.

-   Legen Sie keine Benutzerdaten an globalen Speicherorten ab. Halten Sie die Anwendungsdaten von den Benutzerdaten getrennt.

-   Weisen Sie alle freigegebenen Dateien einer Dateiversion zu, die vom Namen der Anwendung abhängt.

-   Weisen Sie alle Nachrichten und Datenstrukturen zu, die für die Verarbeitung einer Version verwendet werden, um eine unbeabsichtigte prozessübergreifende Freigabe zu verhindern.

-   Die dll sollte nicht von der Freigabe über Versionen abhängen, die möglicherweise nicht vorhanden sind, wie z. b. freigegebene Speicher Abschnitte, die nicht für verschiedene Versionen der Assembly freigegeben sind.

-   Wenn Sie neue Funktionen hinzufügen, die nicht dem Binär Schnittstellen-Kompatibilitäts Vertrag der ursprünglichen dll folgen, müssen Sie eine neue CLSID, ProgID und einen Dateinamen zuweisen. In zukünftigen Versionen ihrer parallelen Assembly müssen diese CLSID, ProgID und der Dateiname verwendet werden. Dies verhindert einen Konflikt, wenn eine Version der dll, die nicht nebeneinander ist, über eine Seite-an-Seite-Version registriert wird.

-   Wenn Sie dieselbe CLSID oder ProgID wieder verwenden, testen Sie, um sicherzustellen, dass die Assembly abwärts kompatibel ist.

-   Initialisieren Sie die Standardeinstellungen für die Assembly im Assemblycode, und legen Sie Sie fest. Speichern Sie die Standardeinstellungen nicht in der Registrierung.

-   Weisen Sie allen Datenstrukturen Versionen zu.

-   In Ihrer dll sollte der Status der parallelen Assembly gespeichert werden, wie unter [Authoring State Storage for Side-by-Side](authoring-state-storage-for-side-by-side-assemblies.md)Assemblys beschrieben.

 

 



