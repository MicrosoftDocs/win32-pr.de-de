---
description: Wenn eine Anwendung dynamisch eine Dynamic Link Library lädt, ohne einen vollqualifizierten Pfadnamen anzugeben, versucht Windows, die DLL zu finden, indem ein klar definierter Satz von Verzeichnissen in einer bestimmten Reihenfolge durchsucht wird, wie in Dynamic-Link Library Search Order (Reihenfolge der Bibliothekssuche) beschrieben. Wenn ein Angreifer die Kontrolle über eines der Verzeichnisse im DLL-Suchpfad erhält, kann er eine schädliche Kopie der DLL in diesem Verzeichnis platzieren. Dies wird manchmal als DLL-Vorabladeangriff oder binärer Planting-Angriff bezeichnet.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Dynamic-Link Bibliothekssicherheit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 582122debce68ade593c007e431e62a91a7fa07f395f148b7eaa05cac13bc56a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119290400"
---
# <a name="dynamic-link-library-security"></a>Dynamic-Link Bibliothekssicherheit

Wenn eine Anwendung dynamisch eine Dynamic Link Library lädt, ohne einen vollqualifizierten Pfadnamen anzugeben, versucht Windows, die DLL zu finden, indem ein klar definierter Satz von Verzeichnissen in einer bestimmten Reihenfolge durchsucht wird, wie in Dynamic Link Library Search Order (Such reihenfolge der [Dynamic Link-Bibliothek) beschrieben.](dynamic-link-library-search-order.md) Wenn ein Angreifer die Kontrolle über eines der Verzeichnisse im DLL-Suchpfad erhält, kann er eine schädliche Kopie der DLL in diesem Verzeichnis platzieren. Dies wird manchmal als *DLL-Vorabladeangriff oder* *binärer Planting-Angriff bezeichnet.* Wenn das System keine legitime Kopie der DLL findet, bevor es das kompromittierte Verzeichnis durchsucht, lädt es die schädliche DLL. Wenn die Anwendung mit Administratorrechten ausgeführt wird, kann der Angreifer bei der Erhöhung lokaler Berechtigungen erfolgreich sein.

Angenommen, eine Anwendung ist so konzipiert, dass sie eine DLL aus dem aktuellen Verzeichnis des Benutzers geladen und ordnungsgemäß fehlschlägt, wenn die DLL nicht gefunden wird. Die Anwendung ruft [**LoadLibrary nur**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit dem Namen der DLL auf, wodurch das System nach der DLL sucht. Wenn der sichere DLL-Suchmodus aktiviert ist und die Anwendung keine alternative Such reihenfolge verwendet, durchsucht das System Verzeichnisse in der folgenden Reihenfolge:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das Systemverzeichnis
3.  Das 16-Bit-Systemverzeichnis.
4.  Das Windows-Verzeichnis.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind.

Im Weiteren erhält ein Angreifer mit Kenntnis der Anwendung die Kontrolle über das aktuelle Verzeichnis und platziert eine schädliche Kopie der DLL in diesem Verzeichnis. Wenn die Anwendung den **LoadLibrary-Aufruf** aus gibt, sucht das System nach der DLL, sucht die schädliche Kopie der DLL im aktuellen Verzeichnis und lädt sie. Die schädliche Kopie der DLL wird dann in der Anwendung ausgeführt und erhält die Berechtigungen des Benutzers.

Entwickler können ihre Anwendungen vor DLL-Vorabladen schützen, indem sie die folgenden Richtlinien befolgen:

-   Geben Sie nach Möglichkeit einen vollqualifizierten Pfad an, wenn Sie die [**Funktionen LoadLibrary,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) [**LoadLibraryEx,**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)oder [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) verwenden.
-   Verwenden Sie die LOAD LIBRARY SEARCH-Flags mit der LoadLibraryEx-Funktion, oder verwenden Sie diese Flags mit der \_ \_ Funktion [**SetDefaultDllDirectories,**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) um eine DLL-Such reihenfolge für einen Prozess zu erstellen, und verwenden Sie dann die [**Funktionen AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) oder [**SetDllDirectory,**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) um die Liste zu ändern. Weitere Informationen finden Sie unter [Dynamic Link Library Search Order](dynamic-link-library-search-order.md).

    **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Flags und Funktionen sind auf Systemen verfügbar, auf dem [KB2533623](https://support.microsoft.com/kb/2533623) installiert ist.

-   Verwenden Sie auf Systemen mit [installiertem KB2533623](https://support.microsoft.com/kb/2533623) die LOAD LIBRARY SEARCH-Flags mit der LoadLibraryEx-Funktion, oder verwenden Sie diese Flags mit der \_ \_ [](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) [**SetDefaultDllDirectories-Funktion,**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) um eine DLL-Such reihenfolge für einen Prozess zu erstellen, und verwenden Sie dann die [**Funktionen AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) oder [**SetDllDirectory,**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) um die Liste zu ändern. Weitere Informationen finden Sie unter [Dynamic Link Library Search Order](dynamic-link-library-search-order.md).
-   Erwägen Sie die [Verwendung der DLL-Umleitung](dynamic-link-library-redirection.md) oder [eines Manifests,](/windows/desktop/SbsCs/manifests) um sicherzustellen, dass Ihre Anwendung die richtige DLL verwendet.
-   Stellen Sie bei Verwendung der Standardsuch reihenfolge sicher, dass der sichere DLL-Suchmodus aktiviert ist. Dadurch wird das aktuelle Verzeichnis des Benutzers später in der Such reihenfolge platziert, was die Wahrscheinlichkeit erhöht, dass Windows eine legitime Kopie der DLL vor einer schädlichen Kopie findet. Tresor Der DLL-Suchmodus ist ab Windows XP mit Service Pack 2 (SP2) standardmäßig aktiviert und wird durch den Registrierungswert SafeDllSearchMode des **HKEY \_ LOCAL \_ \\ MACHINE-Systems \\ CurrentControlSet \\ Control Session \\ Manager** \\  gesteuert. Weitere Informationen finden Sie unter [Dynamic Link Library Search Order](dynamic-link-library-search-order.md).
-   Entfernen Sie das aktuelle Verzeichnis aus dem Standardsuchpfad, indem [**Sie SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) mit einer leeren Zeichenfolge ("") aufrufen. Dies sollte einmal früh in der Prozessin initialisierung erfolgen, nicht vor und nach Aufrufen von [**LoadLibrary.**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) Beachten Sie, **dass SetDllDirectory** den gesamten Prozess beeinflusst und dass mehrere Threads, die **SetDllDirectory** mit unterschiedlichen Werten aufrufen, zu nicht definiertem Verhalten führen können. Wenn Ihre Anwendung DLLs von Drittanbietern lädt, testen Sie sorgfältig, um Inkompatibilitäten zu identifizieren.
-   Verwenden Sie die [**SearchPath-Funktion**](/windows/desktop/api/processenv/nf-processenv-searchpathw) nicht, um einen Pfad zu einer DLL für einen nachfolgenden [**LoadLibrary-Aufruf**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) abzurufen, es sei denn, der Suchmodus für den sicheren Prozess ist aktiviert. Wenn der Suchmodus für den sicheren Prozess nicht aktiviert ist, verwendet die **SearchPath-Funktion** eine andere Such reihenfolge als **LoadLibrary** und durchsucht wahrscheinlich zuerst das aktuelle Verzeichnis des Benutzers nach der angegebenen DLL. Verwenden Sie die Funktion [**SetSearchPathMode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) mit BASE SEARCH PATH ENABLE SAFE SEARCHMODE, um den Suchmodus für den sicheren Prozess für die  \_ \_ \_ \_ \_ SearchPath-Funktion zu aktivieren. Dadurch wird das aktuelle Verzeichnis an das Ende der **Suchliste SearchPath** für die Lebensdauer des Prozesses verschiebt. Beachten Sie, dass das aktuelle Verzeichnis nicht aus dem Suchpfad entfernt wird. Wenn das System also keine legitime Kopie der DLL findet, bevor es das aktuelle Verzeichnis erreicht, ist die Anwendung weiterhin anfällig. Wie bei [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)sollte der Aufruf von **SetSearchPathMode** frühzeitig in der Prozessin initialisierung erfolgen und wirkt sich auf den gesamten Prozess aus. Wenn Ihre Anwendung DLLs von Drittanbietern lädt, testen Sie sorgfältig, um Inkompatibilitäten zu identifizieren.
-   Machen Sie keine Annahmen über die Betriebssystemversion basierend auf einem [**LoadLibrary-Aufruf,**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) der nach einer DLL sucht. Wenn die Anwendung in einer Umgebung ausgeführt wird, in der die DLL legitimerweise nicht vorhanden ist, sich aber eine schädliche Kopie der DLL im Suchpfad befindet, kann die schädliche Kopie der DLL geladen werden. Verwenden Sie stattdessen die empfohlenen Techniken, die unter [Abrufen der Systemversion beschrieben sind.](/windows/desktop/SysInfo/getting-the-system-version)

Das Tool Prozessmonitor kann verwendet werden, um DLL-Ladevorgänge zu identifizieren, die möglicherweise anfällig sind. Das Prozessmonitortool kann von heruntergeladen <https://technet.microsoft.com/sysinternals/bb896645.aspx> werden.

Im folgenden Verfahren wird beschrieben, wie Sie den Prozessmonitor verwenden, um DLL-Ladevorgänge in Ihrer Anwendung zu untersuchen.

**So verwenden Sie den Prozessmonitor zum Untersuchen von DLL-Ladevorgängen in Ihrer Anwendung**

1.  Starten Sie den Prozessmonitor.
2.  Fügen Sie im Prozessmonitor die folgenden Filter ein:
    -   Der Vorgang ist "CreateFile".
    -   Der Vorgang ist "LoadImage".
    -   Pfad enthält .cpl
    -   Pfad enthält .dll
    -   Path contains .drv (Pfad enthält .drv)
    -   Pfad enthält .exe
    -   Path contains .ocx (Pfad enthält .ocx)
    -   Pfad enthält .scr
    -   Pfad enthält .sys
3.  Schließen Sie die folgenden Filter aus:
    -   Prozessname ist procmon.exe
    -   Prozessname ist Procmon64.exe
    -   Prozessname ist "System"
    -   Vorgang beginnt mit IRP \_ MJ\_
    -   Vorgang beginnt mit FASTIO\_
    -   Ergebnis: SUCCESS
    -   Der Pfad endet mit pagefile.sys
4.  Versuchen Sie, Ihre Anwendung mit dem aktuellen Verzeichnis zu starten, das auf ein bestimmtes Verzeichnis festgelegt ist. Doppelklicken Sie beispielsweise auf eine Datei mit einer Erweiterung, deren Dateihandler Ihrer Anwendung zugewiesen ist.
5.  Überprüfen Sie die Ausgabe des Prozessmonitors auf Pfade, die verdächtig aussehen, z. B. einen Aufruf des aktuellen Verzeichnisses zum Laden einer DLL. Diese Art von Aufruf kann auf ein Sicherheitsrisiko in Ihrer Anwendung hinweisen.

 

 
