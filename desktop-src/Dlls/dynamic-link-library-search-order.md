---
description: Anwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem sie einen vollständigen Pfad angeben oder einen anderen Mechanismus wie ein Manifest verwenden. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der DLL, wie in diesem Thema beschrieben.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Dynamic Link Library-Suchreihenfolge
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: e2abe21e0283adab4fbc3c17db6503772e20c217cf3019ea775812b0f45e5145
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083440"
---
# <a name="dynamic-link-library-search-order"></a>Dynamic Link Library-Suchreihenfolge

Ein System kann mehrere Versionen derselben Dynamic Link Library (DLL) enthalten. Anwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem sie einen vollständigen Pfad angeben oder einen anderen Mechanismus wie ein Manifest verwenden. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der DLL, wie in diesem Thema beschrieben.

-   [Faktoren, die sich auf die Suche auswirken](#factors-that-affect-searching)
-   [Suchauftrag für UWP-Apps](#search-order-for-uwp-apps)
    -   [Standardsuchauftrag für UWP-Apps](#standard-search-order-for-uwp-apps)
    -   [Alternative Such reihenfolge für UWP-Apps](#alternate-search-order-for-uwp-apps)
-   [Suchauftrag für Desktopanwendungen](#search-order-for-desktop-applications)
    -   [Standardsuch reihenfolge für Desktopanwendungen](#standard-search-order-for-desktop-applications)
    -   [Alternative Such reihenfolge für Desktopanwendungen](#alternate-search-order-for-desktop-applications)
    -   [Suchauftrag **mitHILFE von LOAD \_ \_ LIBRARY-SUCHflags**](#search-order-using-load_library_search-flags)
-   [Zugehörige Themen](#related-topics)

## <a name="factors-that-affect-searching"></a>Faktoren, die sich auf die Suche auswirken

Die folgenden Faktoren beeinflussen, ob das System nach einer DLL sucht:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, prüft das System nur auf Umleitung und ein Manifest, bevor es in die geladene DLL auflöst, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und der abhängigen DLLs der bekannten DLL, falls welche), anstatt nach der DLL zu suchen. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.
-   Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als würden sie nur mit ihren Modulnamen geladen. Dies gilt auch dann, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

## <a name="search-order-for-uwp-apps"></a>Suchauftrag für UWP-Apps

Wenn eine UWP-App für Windows 10 (oder eine Store-App für Windows 8.x) ein gepacktes Modul lädt, indem die [**LoadPackagedLibrary-Funktion**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) aufruft, muss sich die DLL im Paketabhängigkeitsdiagramm des Prozesses befindet. Weitere Informationen finden Sie unter **LoadPackagedLibrary**. Wenn eine UWP-App ein Modul auf andere Weise lädt und keinen vollständigen Pfad anweist, sucht das System zur Ladezeit nach der DLL und ihren Abhängigkeiten, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und der abhängigen DLLs der bekannten DLL, falls verfügbar). Das System sucht nicht nach der DLL. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Wenn das System nach einem Modul oder seinen Abhängigkeiten suchen muss, verwendet es immer die Such reihenfolge für UWP-Apps, auch wenn es sich bei einer Abhängigkeit nicht um UWP-App-Code handelt.

### <a name="standard-search-order-for-uwp-apps"></a>Standardsuch reihenfolge für UWP-Apps

Wenn das Modul noch nicht geladen ist oder in der Liste der bekannten DLLs enthalten ist, durchsucht das System diese Speicherorte in der folgenden Reihenfolge:

1.  Das Paketabhängigkeitsdiagramm des Prozesses. Dies ist das Paket der Anwendung sowie alle Abhängigkeiten, die im Abschnitt des Paketmanifests `<PackageDependency>` `<Dependencies>` der Anwendung angegeben sind. Abhängigkeiten werden in der Reihenfolge durchsucht, in der sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem der aufrufende Prozess geladen wurde.
3.  Das Systemverzeichnis (%SystemRoot% \\ system32).

Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als würden sie nur mit ihren Modulnamen geladen. Dies gilt auch dann, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

### <a name="alternate-search-order-for-uwp-apps"></a>Alternative Such reihenfolge für UWP-Apps

Wenn ein Modul die Standardsuch reihenfolge durch Aufrufen der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **LOAD WITH ALTERED SEARCH \_ \_ \_ \_ PATH** ändert, durchsucht das System das Verzeichnis, aus dem das angegebene Modul geladen wurde, anstelle des Verzeichnisses des aufrufenden Prozesses. Das System durchsucht diese Speicherorte in der folgenden Reihenfolge:

1.  Das Paketabhängigkeitsdiagramm des Prozesses. Dies ist das Paket der Anwendung sowie alle Abhängigkeiten, die im Abschnitt des Paketmanifests `<PackageDependency>` `<Dependencies>` der Anwendung angegeben sind. Abhängigkeiten werden in der Reihenfolge durchsucht, in der sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem das angegebene Modul geladen wurde.
3.  Das Systemverzeichnis (%SystemRoot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Suchauftrag für Desktopanwendungen

Desktopanwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem sie einen vollständigen Pfad angeben, [die DLL-Umleitung](dynamic-link-library-redirection.md)verwenden oder ein Manifest [verwenden.](/windows/desktop/SbsCs/manifests) Wenn keine dieser Methoden verwendet wird, sucht das System zur Ladezeit nach der DLL, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis sie sich befindet. Das System sucht nicht nach der DLL.
-   Wenn sich die DLL in der Liste der bekannten DLLs für die Version von Windows befindet, auf der die Anwendung ausgeführt wird, verwendet das System seine Kopie der bekannten DLL (und der abhängigen DLLs der bekannten DLL, falls verfügbar). Das System sucht nicht nach der DLL. Eine Liste der bekannten DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ LOCAL MACHINE SYSTEM \_ \\ \\ CurrentControlSet \\ Control Session Manager \\ \\ KnownDLLs**.

Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als würden sie nur mit ihren Modulnamen geladen. Dies gilt auch dann, wenn die erste DLL durch Angabe eines vollständigen Pfads geladen wurde.

> [!IMPORTANT]
> Wenn ein Angreifer die Kontrolle über eines der verzeichnisse erhält, die durchsucht werden, kann er eine schädliche Kopie der DLL in diesem Verzeichnis platzieren. Möglichkeiten, solche Angriffe zu verhindern, finden Sie unter [Dynamic Link Library Security](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Standardsuch reihenfolge für Desktopanwendungen

Die vom System verwendete STANDARD-DLL-Such reihenfolge hängt davon ab, ob der sichere DLL-Suchmodus aktiviert oder deaktiviert ist. Tresor Im DLL-Suchmodus wird das aktuelle Verzeichnis des Benutzers später in der Such reihenfolge platziert.

Tresor Der DLL-Suchmodus ist standardmäßig aktiviert. Um dieses Feature zu deaktivieren, erstellen Sie den **Registrierungswert HKEY \_ LOCAL MACHINE System \_ \\ \\ CurrentControlSet \\ Control Session \\ Manager** \\ **SafeDllSearchMode** und legen ihn auf 0 fest. Durch aufrufen [**der SetDllDirectory-Funktion**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) wird **SafeDllSearchMode** effektiv deaktiviert, während sich das angegebene Verzeichnis im Suchpfad befindet, und ändert die Suchrichtung wie in diesem Thema beschrieben.

Wenn **SafeDllSearchMode** aktiviert ist, lautet die Such reihenfolge wie folgt:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das Systemverzeichnis Verwenden Sie [**die GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses zu erhalten.
3.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber es wird durchsucht.
4.  Das Windows-Verzeichnis. Verwenden Sie [**die GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses zu erhalten.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den **Registrierungsschlüssel App Paths** angegeben wird. Der **Schlüssel "App-Pfade"** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

Wenn **SafeDllSearchMode** deaktiviert ist, lautet die Such reihenfolge wie folgt:

1.  Das Verzeichnis, aus dem die Anwendung geladen wurde.
2.  Das aktuelle Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie [**die GetSystemDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) um den Pfad dieses Verzeichnisses zu erhalten.
4.  Das 16-Bit-Systemverzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, aber es wird durchsucht.
5.  Das Windows-Verzeichnis. Verwenden Sie [**die GetWindowsDirectory-Funktion,**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) um den Pfad dieses Verzeichnisses zu erhalten.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgeführt sind. Beachten Sie, dass dies nicht den anwendungsspezifischen Pfad enthält, der durch den **Registrierungsschlüssel App Paths** angegeben wird. Der **Schlüssel "App-Pfade"** wird beim Berechnen des DLL-Suchpfads nicht verwendet.

### <a name="alternate-search-order-for-desktop-applications"></a>Alternative Such reihenfolge für Desktopanwendungen

Die vom System verwendete Standardsuch reihenfolge kann durch Aufrufen der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **LOAD WITH ALTERED SEARCH PATH geändert \_ \_ \_ \_ werden.** Die Standardsuchrichtung kann auch durch Aufrufen der [**SetDllDirectory-Funktion geändert**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) werden.

> [!NOTE]
> Die Standardsuch reihenfolge des Prozesses wird auch durch Aufrufen der [**SetDllDirectory-Funktion**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) im übergeordneten Prozess vor dem Start des aktuellen Prozesses beeinflusst.

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

Eine Anwendung kann eine Suchreihenfolge mithilfe eines oder mehrerer **LOAD \_ LIBRARY \_ SEARCH-Flags** mit der [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) angeben. Eine Anwendung kann auch **LOAD \_ LIBRARY \_ SEARCH-Flags** mit der [**SetDefaultDllDirectories-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) verwenden, um eine DLL-Suchreihenfolge für einen Prozess einzurichten. Die Anwendung kann mithilfe der Funktionen [**AddDllDirectory oder SetDllDirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) zusätzliche Verzeichnisse für die Prozess-DLL-Suchreihenfolge angeben. [](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)

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

[Dynamic Link Library Redirection (Umleitung der Dynamic Link-Bibliothek)](dynamic-link-library-redirection.md)
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

 

 
