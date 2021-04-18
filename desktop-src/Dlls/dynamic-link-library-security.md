---
description: Wenn eine Anwendung dynamisch eine Dynamic Link Library lädt, ohne einen voll qualifizierten Pfadnamen anzugeben, versucht Windows, die dll zu suchen, indem Sie einen klar definierten Satz von Verzeichnissen in einer bestimmten Reihenfolge durchsucht, wie in Dynamic-Link Bibliotheks Such Reihenfolge beschrieben. Wenn ein Angreifer die Kontrolle über eines der Verzeichnisse im dll-Suchpfad erlangt, kann er eine bösartige Kopie der dll in diesem Verzeichnis platzieren. Dies wird manchmal als ein dll-vorab Lade Angriff oder ein Binary Planting Angriff bezeichnet.
ms.assetid: 9493F299-789D-4CBC-9822-96EEAE39B494
title: Sicherheit der Dynamic-Link-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4016139762461784702ac0190c1ee65d8bc6e72d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366169"
---
# <a name="dynamic-link-library-security"></a>Sicherheit der Dynamic-Link-Bibliothek

Wenn eine Anwendung dynamisch eine Dynamic Link Library lädt, ohne einen voll qualifizierten Pfadnamen anzugeben, versucht Windows, die dll zu suchen, indem Sie einen klar definierten Satz von Verzeichnissen in einer bestimmten Reihenfolge durchsucht, wie in der [Such Reihenfolge der Dynamic-Link-Bibliothek](dynamic-link-library-search-order.md)beschrieben. Wenn ein Angreifer die Kontrolle über eines der Verzeichnisse im dll-Suchpfad erlangt, kann er eine bösartige Kopie der dll in diesem Verzeichnis platzieren. Dies wird manchmal als ein *dll-vorab Lade Angriff* oder ein *Binary Planting Angriff* bezeichnet. Wenn das System keine legitime Kopie der dll findet, bevor es das kompromittierte Verzeichnis durchsucht, lädt es die schädliche dll. Wenn die Anwendung mit Administratorrechten ausgeführt wird, kann der Angreifer eine lokale Berechtigungs Erweiterung haben.

Angenommen, eine Anwendung ist so konzipiert, dass Sie eine DLL aus dem aktuellen Verzeichnis des Benutzers lädt und ordnungsgemäß fehlschlägt, wenn die dll nicht gefunden wurde. Die Anwendung ruft [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) mit nur dem Namen der dll auf, was bewirkt, dass das System nach der dll sucht. Wenn der sichere DLL-Suchmodus aktiviert ist und die Anwendung keine Alternative Such Reihenfolge verwendet, durchsucht das Systemverzeichnisse in der folgenden Reihenfolge:

1.  Das Verzeichnis, in dem die Anwendung geladen wurde.
2.  Das Systemverzeichnis
3.  Das 16-Bit-System Verzeichnis.
4.  Das Windows-Verzeichnis.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind.

Wenn Sie das Beispiel fortsetzen, erhält ein Angreifer mit Kenntnis der Anwendung die Kontrolle über das aktuelle Verzeichnis und platziert eine bösartige Kopie der dll in diesem Verzeichnis. Wenn die Anwendung den **LoadLibrary** -Befehl ausgibt, sucht das System nach der dll, sucht nach der bösartigen Kopie der dll im aktuellen Verzeichnis und lädt Sie. Die bösartige Kopie der dll wird dann innerhalb der Anwendung ausgeführt und erhält die Berechtigungen des Benutzers.

Entwickler können Ihre Anwendungen vor dem Ausführen von dll-Vorlade Vorgängen schützen, indem Sie diese Richtlinien befolgen:

-   Geben Sie, sofern möglich, einen voll qualifizierten Pfad an, wenn Sie die Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya), [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa), [**feateprocess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)oder [**ShellExecute**](/windows/desktop/api/shellapi/nf-shellapi-shellexecutea) verwenden.
-   Verwenden Sie die \_ Suchflags der Lade Bibliothek \_ mit der [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion, oder verwenden Sie diese Flags mit der [**setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) -Funktion, um eine DLL-Such Reihenfolge für einen Prozess einzurichten, und verwenden Sie dann die [**adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) -oder [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) -Funktionen, um die Liste zu ändern. Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).

    **Windows 7, Windows Server 2008 R2, Windows Vista und Windows Server 2008:** Diese Flags und Funktionen sind auf Systemen verfügbar, auf denen [KB2533623](https://support.microsoft.com/kb/2533623) installiert ist.

-   Verwenden Sie auf Systemen, auf denen [KB2533623](https://support.microsoft.com/kb/2533623) installiert ist, die Suchflags für die Auslastungs \_ Bibliothek \_ mit der [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion, oder verwenden Sie diese Flags mit der [**setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) -Funktion, um eine DLL-Such Reihenfolge für einen Prozess einzurichten, und verwenden Sie dann die [**adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) -oder [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) -Funktionen Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).
-   Verwenden Sie ggf. die [dll-Umleitung](dynamic-link-library-redirection.md) oder ein [Manifest](/windows/desktop/SbsCs/manifests) , um sicherzustellen, dass die Anwendung die richtige dll verwendet
-   Wenn Sie die Standard Such Reihenfolge verwenden, stellen Sie sicher, dass der sichere DLL-Suchmodus aktiviert ist. Dadurch wird das aktuelle Verzeichnis des Benutzers später in der Such Reihenfolge platziert, wodurch die Wahrscheinlichkeit erhöht wird, dass Windows vor einer bösartigen Kopie eine legitime Kopie der dll findet. Der sichere DLL-Suchmodus ist ab Windows XP mit Service Pack 2 (SP2) standardmäßig aktiviert und wird durch den Registrierungs Wert des **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** gesteuert. Weitere Informationen finden Sie unter [Dynamic-Link Library Search Order](dynamic-link-library-search-order.md).
-   Entfernen Sie das aktuelle Verzeichnis aus dem Suchpfad Standard, indem Sie [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) mit einer leeren Zeichenfolge ("") aufrufen. Dies sollte einmal in der Prozess Initialisierung erfolgen, nicht vor und nach Aufrufen von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya). Beachten Sie, dass **setdlldirectory** den gesamten Prozess beeinflusst und dass mehrere Threads, die **setdlldirectory** mit unterschiedlichen Werten aufrufen, ein nicht definiertes Verhalten verursachen können. Wenn Ihre Anwendung Drittanbieter-DLLs lädt, testen Sie sorgfältig, um Inkompatibilitäten zu identifizieren.
-   Verwenden Sie nicht die [**SearchPath**](/windows/desktop/api/processenv/nf-processenv-searchpathw) -Funktion, um einen Pfad zu einer DLL für einen nachfolgenden [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Rückruf abzurufen, es sei denn, der sichere Prozess Suchmodus ist aktiviert. Wenn der Suchmodus für sichere Prozesse nicht aktiviert ist, verwendet die **SearchPath** -Funktion eine andere Such Reihenfolge als **LoadLibrary** und wird wahrscheinlich zuerst das aktuelle Verzeichnis des Benutzers nach der angegebenen DLL durchsuchen. Um den sicheren Prozess Suchmodus für die **SearchPath** -Funktion zu aktivieren, verwenden Sie die [**setsearchpathmode**](/windows/desktop/api/winbase/nf-winbase-setsearchpathmode) -Funktion mit dem Basis \_ \_ Suchpfad \_ enable \_ Safe \_ SearchMode. Dadurch wird das aktuelle Verzeichnis für die Lebensdauer des Prozesses an das Ende der Such Liste **Suchpfad** verschoben. Beachten Sie, dass das aktuelle Verzeichnis nicht aus dem Suchpfad entfernt wird, sodass die Anwendung immer noch anfällig ist, wenn das System keine legitime Kopie der dll findet, bevor Sie das aktuelle Verzeichnis erreicht. Wie bei [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)sollte das Aufrufen von **setsearchpathmode** früh in der Prozess Initialisierung erfolgen und wirkt sich auf den gesamten Prozess aus. Wenn Ihre Anwendung Drittanbieter-DLLs lädt, testen Sie sorgfältig, um Inkompatibilitäten zu identifizieren.
-   Nehmen Sie keine Annahmen über die Betriebssystemversion auf Grundlage eines [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Aufrufes, der nach einer DLL sucht. Wenn die Anwendung in einer Umgebung ausgeführt wird, in der die dll nicht vorhanden ist, aber eine bösartige Kopie der dll im Suchpfad vorhanden ist, kann die bösartige Kopie der DLL geladen werden. Verwenden Sie stattdessen die empfohlenen Verfahren, die unter " [System Version](/windows/desktop/SysInfo/getting-the-system-version)" beschrieben werden.

Das Tool Prozess Monitor kann verwendet werden, um dll-Ladevorgänge zu identifizieren, die anfällig sein könnten. Das Tool Prozess Monitor kann von heruntergeladen werden <https://technet.microsoft.com/sysinternals/bb896645.aspx> .

Im folgenden Verfahren wird beschrieben, wie Sie die Prozessüberwachung verwenden, um dll-Ladevorgänge in Ihrer Anwendung zu überprüfen.

**So verwenden Sie den Prozess Monitor zum Überprüfen von dll-Ladevorgängen in der Anwendung**

1.  Starten Sie den Prozess Monitor.
2.  Fügen Sie in Process Monitor die folgenden Filter ein:
    -   Vorgang ist "kreatefile".
    -   Vorgang ist "LoadImage"
    -   Pfad enthält. cpl
    -   Pfad enthält dll.
    -   Pfad enthält. drv
    -   Pfad enthält. exe
    -   Pfad enthält. ocx
    -   Pfad enthält. SCR
    -   Pfad enthält. sys
3.  Schließen Sie die folgenden Filter aus:
    -   Der Prozess Name ist procmon.exe
    -   Der Prozess Name ist Procmon64.exe
    -   Prozess Name ist System
    -   Der Vorgang beginnt mit "unp MJ". \_\_
    -   Der Vorgang beginnt mit FastIO.\_
    -   Ergebnis ist Erfolg
    -   Der Pfad endet mit pagefile.sys
4.  Versuchen Sie, die Anwendung mit dem aktuellen Verzeichnis zu starten, das auf ein bestimmtes Verzeichnis festgelegt ist. Doppelklicken Sie beispielsweise auf eine Datei mit einer Erweiterung, deren Datei Handler der Anwendung zugewiesen ist.
5.  Überprüfen Sie die Prozess Monitor Ausgabe für Pfade, die verdächtig aussehen, wie z. b. einen aufrufenden Befehl des aktuellen Verzeichnisses zum Laden einer DLL. Diese Art von Rückruf weist möglicherweise auf ein Sicherheitsrisiko in Ihrer Anwendung hin.

 

 
