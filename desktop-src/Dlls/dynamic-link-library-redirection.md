---
description: Anwendungen können von einer bestimmten Version einer freigegebenen DLL abhängen und beginnen mit einem Fehler, wenn eine andere Anwendung mit einer neueren oder einer älteren Version derselben DLL installiert wird.
ms.assetid: 3b426b6c-1ad5-43b9-81ea-5e6d3c6588c8
title: Umleitung der Dynamic-Link Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b575d566231058cca13c10a067a3c2e20078073
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350523"
---
# <a name="dynamic-link-library-redirection"></a>Umleitung der Dynamic-Link Bibliothek

Anwendungen können von einer bestimmten Version einer freigegebenen DLL abhängen und beginnen mit einem Fehler, wenn eine andere Anwendung mit einer neueren oder einer älteren Version derselben DLL installiert wird. Es gibt zwei Möglichkeiten, um sicherzustellen, dass Ihre Anwendung die richtige dll verwendet: DLL-Umleitung und parallele Komponenten. Entwickler und Administratoren sollten die DLL-Umleitung für vorhandene Anwendungen verwenden, da keine Änderungen an der Anwendung erforderlich sind. Wenn Sie eine neue Anwendung erstellen oder eine Anwendung aktualisieren und Ihre Anwendung vor möglichen Problemen isolieren möchten, erstellen Sie eine parallele [Komponente](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal).

Um die DLL-Umleitung Computer weit zu aktivieren, müssen Sie einen neuen Registrierungsschlüssel erstellen. Erstellen Sie einen neuen DWORD-Schlüssel namens " **devoverrideenable** " unter **HKLM\Software\Microsoft\Windows NT\CurrentVersion\Image File Execution Options** , und legen Sie ihn auf 1 fest. Danach müssen Sie den Computer neu starten, um die Auswirkungen anzuzeigen.

Um die DLL-Umleitung zu verwenden, erstellen Sie eine *Umleitungs Datei* für die Anwendung. Die Umleitungs Datei muss wie folgt benannt werden: *App- \_ Name*. local. Wenn der Anwendungsname beispielsweise Editor.exe ist, sollte die Umleitungs Datei Editor.exe. local benannt werden. Sie müssen die lokale Datei im Anwendungsverzeichnis installieren. Außerdem müssen Sie die DLLs im Anwendungsverzeichnis installieren.

Der Inhalt einer Umleitungs Datei wird ignoriert, aber das vorhanden sein bewirkt, dass Windows das Anwendungsverzeichnis beim Laden einer DLL zuerst überprüft, unabhängig von dem Pfad, der für [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)angegeben wurde. Wenn die dll nicht im Anwendungsverzeichnis gefunden wird, verwenden diese Funktionen ihre übliche Such Reihenfolge. Beispiel: Wenn die Anwendung c: \\ myapp \\myapp.exe **LoadLibrary** mit folgendem Pfad aufruft:

c: \\ Programmdateien: \\ \\ System \\mydll.dll

Wenn sowohl c: \\ myapp \\myapp.exe. local als auch c: \\ myapp \\mydll.dll vorhanden ist, lädt [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) c: \\ myapp \\mydll.dll. Andernfalls lädt " **LoadLibrary** " das \\ \\ Systemmydll.dll "Systemdateien Common Files" \\ \\ .

Wenn ein Verzeichnis mit dem Namen c: \\ myapp \\myapp.exe. local vorhanden ist und mydll.dll enthält, lädt [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Alternativ c: \\ myapp \\myapp.exe. local \\mydll.dll.

Wenn die Anwendung über ein Manifest verfügt, werden alle lokalen Dateien ignoriert.

Wenn Sie die DLL-Umleitung verwenden und die Anwendung keinen Zugriff auf alle Laufwerke und Verzeichnisse in der Such Reihenfolge hat, beendet [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) die Suche, sobald der Zugriff verweigert wird. (Wenn Sie keine DLL-Umleitung verwenden, überspringt **LoadLibrary** Verzeichnisse, auf die nicht zugegriffen werden kann, und setzt dann die Suche fort.)

Es empfiehlt sich, die Anwendungs-DLLs im gleichen Verzeichnis zu installieren, in dem auch die Anwendung enthalten ist, auch wenn Sie keine DLL-Umleitung verwenden. Dadurch wird sichergestellt, dass das Installieren der Anwendung keine anderen Kopien der dll überschreibt und dazu führt, dass andere Anwendungen fehlschlagen. Wenn Sie diese bewährte Vorgehensweise befolgen, überschreiben andere Anwendungen die Kopie der dll nicht und bewirken, dass Ihre Anwendung fehlschlägt.

 

 
