---
description: Wenn Sie ihre eigenen nebeneinander angezeigten Assemblys erstellen, befolgen Sie die Richtlinien zum Erstellen von nebenseitigen Assemblys.
ms.assetid: e5fc3bae-0646-4418-a8f7-369856f03cd5
title: Erstellen von DLLs für side-by-side-Assemblys
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb83ba1d788d82e8d4fa7ab5f657170875b5deee6921aec3013406328dc2fcf8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142453"
---
# <a name="authoring-dlls-for-side-by-side-assemblies"></a>Erstellen von DLLs für side-by-side-Assemblys

Wenn Sie ihre eigenen parallelen Assemblys erstellen, befolgen Sie die Richtlinien zum Erstellen paralleler [Assemblys,](guidelines-for-creating-side-by-side-assemblies.md) und erstellen Sie alle DLLs, die in der Assembly verwendet werden, gemäß den folgenden Richtlinien:

-   Ihre DLLs sollten so entworfen werden, dass mehrere Versionen gleichzeitig und im gleichen Prozess ausgeführt werden können, ohne sich gegenseitig zu beeinträchtigen. Viele Anwendungen hosten beispielsweise mehrere Plug-Ins, für die jeweils eine andere Version einer Komponente erforderlich ist. Der Entwickler der parallelen Assembly muss entwerfen und testen, um sicherzustellen, dass mehrere Versionen der Komponente ordnungsgemäß funktionieren, wenn sie gleichzeitig im selben Prozess ausgeführt werden.

-   Wenn Sie ihre Komponente als freigegebene Komponente auf Systemen vor Windows XP bereitstellen möchten, müssen Sie die Komponente auf diesen Systemen weiterhin als freigegebene Einzelinstanzkomponente installieren. In diesem Fall müssen Sie sicherstellen, dass Ihre Komponente abwärtskompatibel ist.

-   Werten Sie die Verwendung von -Objekten aus, wenn mehr als eine Version der Assembly auf dem System ausgeführt wird. Bestimmen Sie, ob verschiedene Versionen der Assembly separate Datenstrukturen erfordern, z. B. speicherzuordnungsbasierte Dateien, Named Pipes, registrierte Windows Nachrichten und Klassen, freigegebener Arbeitsspeicher, Semaphore, Mutexe und Hardwaretreiber. Alle Datenstrukturen, die über Assemblyversionen hinweg verwendet werden, müssen abwärtskompatibel sein. Entscheiden Sie, welche Datenstrukturen versionsübergreifend verwendet werden können und welche Datenstrukturen für eine Version privat sein müssen. Bestimmen Sie, ob freigegebene Datenstrukturen separate Synchronisierungsobjekte wie Semaphore und Mutexe erfordern.

-   Einige Objekte, z. B. Fensterklassen und Atoms, werden für jeden Prozess eindeutig benannt. Objekte wie Fensterklassen sollten für jede Assembly mithilfe des Manifests versioniert werden. Verwenden Sie für Objekte wie Atoms versionsspezifische Bezeichner, es sei denn, Sie planen die Versionsfreigabe. Wenn Sie versionsspezifische Bezeichner verwenden, verwenden Sie die vierteilige Versionsnummer.

-   Fügen Sie keinen selbst registrierenden Code in eine DLL ein. Eine DLL in einer parallelen Assembly kann nicht selbst registriert werden.

-   Definieren Sie alle versionsspezifischen Namen in Ihrer DLL mit \# define-Anweisungen. Dadurch können alle Registrierungsschlüssel von einem Speicherort geändert werden. Wenn Sie eine neue Version der Assembly freigeben, müssen Sie nur diese \# define-Anweisung ändern. Beispiel:

    `#define MyRegistryKey "MyAssembly1.0.0.0"`

-   Store alle nicht beständigen Daten im Verzeichnis Temp.

-   Legen Sie Benutzerdaten nicht an globalen Standorten ab. Trennen Sie Anwendungsdaten von Benutzerdaten.

-   Weisen Sie allen freigegebenen Dateien eine Dateiversion zu, die vom Namen der Anwendung abhängt.

-   Weisen Sie alle Nachrichten und Datenstrukturen, die prozessübergreifend verwendet werden, einer Version zu, um unbeabsichtigte prozessübergreifende Freigaben zu verhindern.

-   Ihre DLL sollte nicht von der Freigabe zwischen Versionen abhängen, die möglicherweise nicht vorhanden sind, z. B. Freigegebene Speicherabschnitte, die nicht für verschiedene Versionen der Assembly freigegeben sind.

-   Wenn Sie neue Funktionen hinzufügen, die nicht dem Binärschnittstellen-Kompatibilitätsvertrag der ursprünglichen DLL entsprechen, müssen Sie eine neue CLSID, ProgId und einen Dateinamen zuweisen. Zukünftige Versionen Ihrer side-by-side-Assembly sind dann erforderlich, um diese CLSID, ProgId und den Dateinamen zu verwenden. Dadurch wird ein Konflikt verhindert, wenn eine version der DLL, die nicht nebeneinander ist, über eine nebenseitige Version registriert wird.

-   Wenn Sie dieselbe CLSID oder ProgId wiederverwenden, testen Sie, um sicherzustellen, dass die Assembly abwärtskompatibel ist.

-   Initialisieren sie die Standardeinstellungen für die Assembly im Assemblycode, und legen Sie sie fest. Speichern Sie die Standardeinstellungen nicht in der Registrierung.

-   Weisen Sie allen Datenstrukturen Versionen zu.

-   Die DLL sollte den Zustand der parallelen Assembly speichern, wie unter [Erstellungsstatus Storage für parallele Assemblys](authoring-state-storage-for-side-by-side-assemblies.md)beschrieben.

 

 



