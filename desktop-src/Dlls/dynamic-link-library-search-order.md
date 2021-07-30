---
description: Anwendungen können den Speicherort steuern, von dem aus eine DLL geladen wird, indem sie einen vollständigen Pfad angeben oder einen anderen Mechanismus wie ein Manifest verwenden. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der DLL, wie in diesem Thema beschrieben.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Dynamic Link Library-Suchreihenfolge
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 73c90e176983aa542ec524c2bfa32623821c2f21
ms.sourcegitcommit: 3cea99a2ed9579a94236fa7924abd6149db51a58
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/30/2021
ms.locfileid: "114991837"
---
# <a name="dynamic-link-library-search-order"></a>Dynamic Link Library-Suchreihenfolge

Ein System kann mehrere Versionen derselben Dynamic Link Library (DLL) enthalten. Anwendungen können den Speicherort steuern, von dem aus eine DLL geladen wird, indem sie einen vollständigen Pfad angeben oder einen anderen Mechanismus wie ein Manifest verwenden. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der DLL, wie in diesem Thema beschrieben.

-   [Faktoren, die sich auf die Suche auswirken](#factors-that-affect-searching)
-   [Suchreihenfolge für UWP-Apps](#search-order-for-uwp-apps)
    -   [Standardsuchreihenfolge für UWP-Apps](#standard-search-order-for-uwp-apps)
    -   [Alternative Suchreihenfolge für UWP-Apps](#alternate-search-order-for-uwp-apps)
-   [Suchreihenfolge für Desktopanwendungen](#search-order-for-desktop-applications)
    -   [Standardsuchreihenfolge für Desktopanwendungen](#standard-search-order-for-desktop-applications)
    -   [Alternative Suchreihenfolge für Desktopanwendungen](#alternate-search-order-for-desktop-applications)
    -   [Suchreihenfolge mit **LOAD \_ LIBRARY \_ SEARCH-Flags**](#search-order-using-load_library_search-flags)
-   [Zugehörige Themen](#related-topics)

## <a name="factors-that-affect-searching"></a>Faktoren, die sich auf die Suche auswirken

Die folgenden Faktoren beeinflussen, ob das System nach einer DLL sucht:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, überprüft das System vor dem Auflösen in die geladene DLL nur die Umleitung und ein Manifest, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und ggf. der abhängigen DLLs der bekannten DLL), anstatt nach der DLL zu suchen. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie im folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.
-   Wenn eine DLL Über Abhängigkeiten verfügt, sucht das System nach den abhängigen DLLs, als wären sie nur mit ihren Modulnamen geladen worden. Dies gilt auch, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

## <a name="search-order-for-uwp-apps"></a>Suchreihenfolge für UWP-Apps

Wenn eine UWP-App für Windows 10 (oder eine Store-App für Windows 8.x) ein gepacktes Modul durch Aufrufen der [**LoadPackagedLibrary-Funktion**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) lädt, muss sich die DLL im Paketabhängigkeitsdiagramm des Prozesses befinden. Weitere Informationen finden Sie unter **LoadPackagedLibrary**. Wenn eine UWP-App ein Modul auf andere Weise lädt und keinen vollständigen Pfad angibt, sucht das System zur Ladezeit nach der DLL und ihren Abhängigkeiten, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und ggf. die abhängigen DLLs der bekannten DLL). Das System sucht nicht nach der DLL. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie im folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Wenn das System nach einem Modul oder seinen Abhängigkeiten suchen muss, verwendet es immer die Suchreihenfolge für UWP-Apps, auch wenn es sich bei einer Abhängigkeit nicht um UWP-App-Code handelt.

### <a name="standard-search-order-for-uwp-apps"></a>Standardsuchreihenfolge für UWP-Apps

Wenn das Modul nicht bereits geladen ist oder in der Liste der bekannten DLLs enthalten ist, durchsucht das System diese Speicherorte in der folgenden Reihenfolge:

1.  Das Paketabhängigkeitsdiagramm des Prozesses. Dies ist das Paket der Anwendung sowie alle Abhängigkeiten, `<PackageDependency>` die wie im Abschnitt des `<Dependencies>` Paketmanifests der Anwendung angegeben sind. Abhängigkeiten werden in der Reihenfolge durchsucht, in der sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem der aufrufende Prozess geladen wurde.
3.  Das Systemverzeichnis (%SystemRoot% \\ system32).

Wenn eine DLL Über Abhängigkeiten verfügt, sucht das System nach den abhängigen DLLs, als wären sie nur mit ihren Modulnamen geladen worden. Dies gilt auch, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

### <a name="alternate-search-order-for-uwp-apps"></a>Alternative Suchreihenfolge für UWP-Apps

Wenn ein Modul die Standardsuchreihenfolge durch Aufrufen der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** ändert, durchsucht das System das Verzeichnis, aus dem das angegebene Modul geladen wurde, anstelle des Verzeichnisses des aufrufenden Prozesses. Das System durchsucht diese Speicherorte in dieser Reihenfolge:

1.  Das Paketabhängigkeitsdiagramm des Prozesses. Dies ist das Paket der Anwendung sowie alle Abhängigkeiten, `<PackageDependency>` die wie im Abschnitt des `<Dependencies>` Paketmanifests der Anwendung angegeben sind. Abhängigkeiten werden in der Reihenfolge durchsucht, in der sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem das angegebene Modul geladen wurde.
3.  Das Systemverzeichnis (%SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Suchreihenfolge für Desktopanwendungen

Desktopanwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem sie einen vollständigen Pfad angeben, die [DLL-Umleitung](dynamic-link-library-redirection.md)verwenden oder ein [Manifest](/windows/desktop/SbsCs/manifests)verwenden. Wenn keine dieser Methoden verwendet wird, sucht das System zur Ladezeit nach der DLL, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und ggf. die abhängigen DLLs der bekannten DLL). Das System sucht nicht nach der DLL. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie im folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Wenn eine DLL Über Abhängigkeiten verfügt, sucht das System nach den abhängigen DLLs, als wären sie nur mit ihren Modulnamen geladen worden. Dies gilt auch, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

> [!IMPORTANT]
> Wenn ein Angreifer die Kontrolle über eines der durchsuchten Verzeichnisse erlangt, kann er eine schädliche Kopie der DLL in diesem Verzeichnis ablegen. Möglichkeiten, solche Angriffe zu verhindern, finden Sie unter [Dynamic Link Library Security](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Standardsuchreihenfolge für Desktopanwendungen

Die vom System verwendete Standard-DLL-Suchreihenfolge hängt davon ab, ob der Sichere DLL-Suchmodus aktiviert oder deaktiviert ist. Tresor Im DLL-Suchmodus wird das aktuelle Verzeichnis des Benutzers später in der Suchreihenfolge platziert.

Tresor Der DLL-Suchmodus ist standardmäßig aktiviert. Um dieses Feature zu deaktivieren, erstellen Sie den Registrierungswert **HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session \\ Manager** \\ **SafeDllSearchMode,** und legen Sie ihn auf 0 fest. Das Aufrufen der [**SetDllDirectory-Funktion**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) deaktiviert **SafeDllSearchMode** effektiv, während sich das angegebene Verzeichnis im Suchpfad befindet, und ändert die Suchreihenfolge, wie in diesem Thema beschrieben.

Wenn **SafeDllSearchMode** aktiviert ist, lautet die Suchreihenfolge wie folgt:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
3.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber sie wird durchsucht.
4.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der **App-Pfadschlüssel** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

Wenn **SafeDllSearchMode** deaktiviert ist, lautet die Suchreihenfolge wie folgt:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das aktuelle Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
4.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber sie wird durchsucht.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der **App-Pfadschlüssel** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

### <a name="alternate-search-order-for-desktop-applications"></a>Alternative Suchreihenfolge für Desktopanwendungen

Die vom System verwendete Standardsuchreihenfolge kann durch Aufrufen der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** geändert werden. Die Standardsuchreihenfolge kann auch durch Aufrufen der [**SetDllDirectory-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) geändert werden.

> [!NOTE]
> Die Standardsuchreihenfolge des Prozesses wird auch durch Aufrufen der [**SetDllDirectory-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) im übergeordneten Prozess vor dem Start des aktuellen Prozesses beeinflusst.

Wenn Sie eine alternative Suchstrategie angeben, wird ihr Verhalten fortgesetzt, bis alle zugeordneten ausführbaren Module gefunden wurden. Nachdem das System mit der Verarbeitung von DLL-Initialisierungsroutinen begonnen hat, wird das System zur Standardsuchestrategie zurückgesetzt.

Die [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) unterstützt eine alternative Suchreihenfolge, wenn der Aufruf **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** angibt und der *lpFileName-Parameter* einen absoluten Pfad angibt.

Beachten Sie, dass sich die Standardsuchstrategie und die alternative Suchstrategie, die von [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** angegeben wird, in nur einer Weise unterscheiden: Die Standardsuche beginnt im Verzeichnis der aufrufenden Anwendung, und die alternative Suche beginnt im Verzeichnis des ausführbaren Moduls, das **LoadLibraryEx** lädt.

Wenn **SafeDllSearchMode** aktiviert ist, lautet die alternative Suchreihenfolge wie folgt:

1.  Das durch *lpFileName* angegebene Verzeichnis.
2.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
3.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber sie wird durchsucht.
4.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der **App-Pfadschlüssel** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

Wenn **SafeDllSearchMode** deaktiviert ist, lautet die alternative Suchreihenfolge wie folgt:

1.  Das durch *lpFileName* angegebene Verzeichnis.
2.  Das aktuelle Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
4.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber sie wird durchsucht.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der **App-Pfadschlüssel** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

Die [**SetDllDirectory-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) unterstützt eine alternative Suchreihenfolge, wenn der *lpPathName-Parameter* einen Pfad angibt. Die alternative Suchreihenfolge lautet wie folgt:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das durch den *lpPathName-Parameter* von [**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)angegebene Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses abzurufen. Der Name dieses Verzeichnisses lautet System32.
4.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber sie wird durchsucht. Der Name dieses Verzeichnisses lautet System.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses abzurufen.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der **App-Pfadschlüssel** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

Wenn der *lpPathName-Parameter* eine leere Zeichenfolge ist, entfernt der Aufruf das aktuelle Verzeichnis aus der Suchreihenfolge.

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) deaktiviert effektiv den Suchmodus für sichere DLLs, während sich das angegebene Verzeichnis im Suchpfad befindet. Um den sicheren DLL-Suchmodus basierend auf dem **SafeDllSearchMode-Registrierungswert** wiederherzustellen und das aktuelle Verzeichnis in der Suchreihenfolge wiederherzustellen, rufen **Sie SetDllDirectory** mit *lpPathName* als NULL auf.

### <a name="search-order-using-load_library_search-flags"></a>Suchreihenfolge mit **LOAD \_ LIBRARY \_ SEARCH-Flags**

Eine Anwendung kann eine Suchreihenfolge angeben, indem sie mindestens ein **LOAD \_ LIBRARY \_ SEARCH-Flag** mit der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) verwendet. Eine Anwendung kann auch **LOAD \_ LIBRARY \_ SEARCH-Flags** mit der [**SetDefaultDllDirectories-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) verwenden, um eine DLL-Suchreihenfolge für einen Prozess einzurichten. Die Anwendung kann mithilfe der Funktionen [**AddDllDirectory oder SetDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) zusätzliche Verzeichnisse für die Prozess-DLL-Suchreihenfolge angeben. [](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

Welche Verzeichnisse durchsucht werden, hängt von den Flags ab, die mit [**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)angegeben sind. Wenn mehrere Flags verwendet werden, werden die entsprechenden Verzeichnisse in der folgenden Reihenfolge durchsucht:

1.  Das Verzeichnis, das die DLL enthält (**LOAD LIBRARY SEARCH DLL LOAD \_ \_ \_ \_ \_ DIR**). Dieses Verzeichnis wird nur nach Abhängigkeiten der zu ladenden DLL durchsucht.
2.  Das Anwendungsverzeichnis (**LOAD LIBRARY SEARCH APPLICATION \_ \_ \_ \_ DIR**).
3.  Pfade, die explizit mit der [**AddDllDirectory-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) (**LOAD LIBRARY SEARCH USER \_ \_ \_ \_ DIRS**) oder der [**SetDllDirectory-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) hinzugefügt werden. Wenn mehr als ein Pfad hinzugefügt wurde, ist die Reihenfolge, in der die Pfade durchsucht werden, nicht angegeben.
4.  Das Systemverzeichnis (**LOAD \_ LIBRARY SEARCH \_ \_ SYSTEM32**).

Wenn die Anwendung [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) nicht mit **LOAD \_ LIBRARY \_ SEARCH-Flags** aufruft oder eine DLL-Suchreihenfolge für den Prozess einrichtet, sucht das System entweder mithilfe der Standardsuchreihenfolge oder der alternativen Suchreihenfolge nach DLLs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**AddDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Anwendungsregistrierung](/windows/desktop/shell/app-registration)
</dt> <dt>

[Dynamic Link Library Redirection](dynamic-link-library-redirection.md)
</dt> <dt>

[Sicherheit der Dynamic Link Library](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**SetDefaultDllDirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**SetDllDirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Komponenten nebeneinander](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 
