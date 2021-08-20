---
description: Anwendungen können von einer bestimmten Version einer freigegebenen DLL abhängen und fehlschlagen, wenn eine andere Anwendung mit einer neueren oder älteren Version derselben DLL installiert ist.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Dynamic-Link-Bibliotheksumleitung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58b41c47d35597e5639e3836fb2e9b449beaf24c49ea10076209b4c1bbdf4a8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815828"
---
# <a name="dynamic-link-library-redirection"></a>Dynamic-Link-Bibliotheksumleitung

Anwendungen können von einer bestimmten Version einer freigegebenen DLL abhängen und fehlschlagen, wenn eine andere Anwendung mit einer neueren oder älteren Version derselben DLL installiert ist. Es gibt zwei Möglichkeiten, sicherzustellen, dass Ihre Anwendung die richtige DLL verwendet: DLL-Umleitung und nebeneinander ausgeführte Komponenten. Entwickler und Administratoren sollten die DLL-Umleitung für vorhandene Anwendungen verwenden, da keine Änderungen an der Anwendung erforderlich sind. Wenn Sie eine neue Anwendung erstellen oder eine Anwendung aktualisieren und Ihre Anwendung von potenziellen Problemen isolieren möchten, erstellen Sie eine [nebenseitige Komponente](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Um die DLL-Umleitung computerweit zu aktivieren, müssen Sie einen neuen Registrierungsschlüssel erstellen. Erstellen Sie unter **HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options** einen neuen DWORD-Schlüssel namens **DevOverrideEnable,** und legen Sie ihn auf 1 fest. Danach müssen Sie den Computer neu starten, um die Auswirkungen anzuzeigen.

Um die DLL-Umleitung zu verwenden, erstellen Sie eine *Umleitungsdatei* für Ihre Anwendung. Die Umleitungsdatei muss wie folgt benannt werden: *\_ App-Name*.local. Wenn der Anwendungsname beispielsweise Editor.exe ist, sollte die Umleitungsdatei Editor.exe.local benannt werden. Sie müssen die LOCAL-Datei im Anwendungsverzeichnis installieren. Sie müssen auch die DLLs im Anwendungsverzeichnis installieren.

Der Inhalt einer Umleitungsdatei wird ignoriert, aber ihr Vorhandensein bewirkt, dass Windows das Anwendungsverzeichnis beim Laden einer DLL zuerst überprüft, unabhängig vom Pfad, der für [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)angegeben ist. Wenn die DLL nicht im Anwendungsverzeichnis gefunden wird, verwenden diese Funktionen ihre übliche Suchreihenfolge. Wenn beispielsweise die Anwendung c: \\ myapp \\myapp.exe **LoadLibrary** mit dem folgenden Pfad aufruft:

c: \\ Allgemeine \\ \\ Dateisystemdateienmydll.dll \\

Und wenn sowohl c: \\ myapp \\myapp.exe.local als auch c: \\ myapp \\mydll.dll vorhanden sind, [**lädt LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) c: \\ myapp \\mydll.dll. Andernfalls **lädt LoadLibrary** c: \\ programme common files system \\ \\ \\mydll.dll.

Wenn ein Verzeichnis namens c: \\ myapp \\myapp.exe.local vorhanden ist und mydll.dll enthält, lädt [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) alternativ c: \\ myapp \\myapp.exe.local \\mydll.dll.

Wenn die Anwendung über ein Manifest verfügt, werden alle lokalen Dateien ignoriert.

Wenn Sie die DLL-Umleitung verwenden und die Anwendung nicht auf alle Laufwerke und Verzeichnisse in der Suchreihenfolge zugreifen kann, beendet [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) die Suche, sobald der Zugriff verweigert wird. (Wenn Sie keine DLL-Umleitung verwenden, überspringt **LoadLibrary** Verzeichnisse, auf die sie nicht zugreifen kann, und setzt dann die Suche fort.)

Es empfiehlt sich, Anwendungs-DLLs im gleichen Verzeichnis zu installieren, das die Anwendung enthält, auch wenn Sie keine DLL-Umleitung verwenden. Dadurch wird sichergestellt, dass bei der Installation der Anwendung keine anderen Kopien der DLL überschrieben werden und andere Anwendungen fehlschlagen. Wenn Sie diese bewährte Methode befolgen, überschreiben andere Anwendungen ihre Kopie der DLL nicht und verursachen einen Fehler bei der Anwendung.

 

 
