---
description: Anwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem Sie einen vollständigen Pfad oder einen anderen Mechanismus, z. b. ein Manifest, angeben. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der dll, wie in diesem Thema beschrieben.
ms.assetid: 44228cf2-6306-466c-8f16-f513cd3ba8b5
title: Dynamic Link Library-Suchreihenfolge
ms.topic: article
ms.date: 09/11/2020
ms.custom: contperf-fy21q1
ms.openlocfilehash: 928cf9030e24c91145ae95e1eed680017bf68533
ms.sourcegitcommit: f374b50b37160b683da16b59ac9340282a8f50a5
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "104520331"
---
# <a name="dynamic-link-library-search-order"></a>Dynamic Link Library-Suchreihenfolge

Ein System kann mehrere Versionen derselben DLL (Dynamic Link Library) enthalten. Anwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem Sie einen vollständigen Pfad oder einen anderen Mechanismus, z. b. ein Manifest, angeben. Wenn diese Methoden nicht verwendet werden, sucht das System zur Ladezeit nach der dll, wie in diesem Thema beschrieben.

-   [Faktoren, die die Suche beeinflussen](#factors-that-affect-searching)
-   [Such Reihenfolge für UWP-apps](#search-order-for-uwp-apps)
    -   [Standard Such Reihenfolge für UWP-apps](#standard-search-order-for-uwp-apps)
    -   [Alternative Such Reihenfolge für UWP-apps](#alternate-search-order-for-uwp-apps)
-   [Such Reihenfolge für Desktop Anwendungen](#search-order-for-desktop-applications)
    -   [Standard Such Reihenfolge für Desktop Anwendungen](#standard-search-order-for-desktop-applications)
    -   [Alternative Such Reihenfolge für Desktop Anwendungen](#alternate-search-order-for-desktop-applications)
    -   [Such Reihenfolge mithilfe von **\_ \_ Suchflags der Lade Bibliothek**](/windows)
-   [Zugehörige Themen](#related-topics)

## <a name="factors-that-affect-searching"></a>Faktoren, die die Suche beeinflussen

Die folgenden Faktoren beeinflussen, ob das System nach einer DLL sucht:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, prüft das System nur die Umleitung und ein Manifest vor der Auflösung in die geladene DLL, unabhängig davon, in welchem Verzeichnis es sich befindet. Das System sucht nicht nach der dll.
-   Wenn die dll in der Liste der bekannten DLLs für die Windows-Version enthalten ist, in der die Anwendung ausgeführt wird, verwendet das System die Kopie der bekannten dll (sofern vorhanden), anstatt nach der dll zu suchen. Eine Liste bekannter DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.
-   Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als wären Sie nur mit den Modulnamen geladen worden. Dies gilt auch, wenn die erste dll durch Angabe eines vollständigen Pfads geladen wurde.

## <a name="search-order-for-uwp-apps"></a>Such Reihenfolge für UWP-apps

Wenn eine UWP-App für Windows 10 (oder eine Store-App für Windows 8. x) ein Paket Modul durch Aufrufen der [**loadpackagedlibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary) -Funktion lädt, muss sich die dll im Paket Abhängigkeits Diagramm des Prozesses befinden. Weitere Informationen finden Sie unter **loadpackagedlibrary**. Wenn eine UWP-App ein Modul auf andere Weise lädt und keinen vollständigen Pfad angibt, sucht das System zur Ladezeit nach der dll und den zugehörigen Abhängigkeiten, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis Sie sich befindet. Das System sucht nicht nach der dll.
-   Wenn die dll in der Liste der bekannten DLLs für die Version von Windows enthalten ist, in der die Anwendung ausgeführt wird, verwendet das System die Kopie der bekannten dll (und ggf. die abhängigen DLLs der bekannten dll). Das System sucht nicht nach der dll. Eine Liste bekannter DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Wenn das System nach einem Modul oder seinen Abhängigkeiten suchen muss, verwendet es immer die Such Reihenfolge für UWP-apps, auch wenn eine Abhängigkeit nicht UWP-app-Code ist.

### <a name="standard-search-order-for-uwp-apps"></a>Standard Such Reihenfolge für UWP-apps

Wenn das Modul nicht bereits geladen ist oder in der Liste bekannter DLLs vorhanden ist, durchsucht das System diese Speicherorte in dieser Reihenfolge:

1.  Das Paket Abhängigkeits Diagramm des Prozesses. Dabei handelt es sich um das Paket der Anwendung und alle Abhängigkeiten, die `<PackageDependency>` im `<Dependencies>` -Abschnitt des Paket Manifests der Anwendung angegeben werden. Abhängigkeiten werden in der Reihenfolge durchsucht, in der Sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem der aufrufende Prozess geladen wurde.
3.  Das System Verzeichnis (% systemroot% \\ system32).

Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als wären Sie nur mit den Modulnamen geladen worden. Dies gilt auch, wenn die erste dll durch Angabe eines vollständigen Pfads geladen wurde.

### <a name="alternate-search-order-for-uwp-apps"></a>Alternative Such Reihenfolge für UWP-apps

Wenn ein Modul die Standard Such Reihenfolge durch Aufrufen der [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion mit der **Last \_ mit dem \_ geänderten \_ \_ Suchpfad** ändert, durchsucht das System das Verzeichnis, aus dem das angegebene Modul geladen wurde, anstelle des Verzeichnisses des aufrufenden Prozesses. Das System durchsucht diese Speicherorte in dieser Reihenfolge:

1.  Das Paket Abhängigkeits Diagramm des Prozesses. Dabei handelt es sich um das Paket der Anwendung und alle Abhängigkeiten, die `<PackageDependency>` im `<Dependencies>` -Abschnitt des Paket Manifests der Anwendung angegeben werden. Abhängigkeiten werden in der Reihenfolge durchsucht, in der Sie im Manifest angezeigt werden.
2.  Das Verzeichnis, aus dem das angegebene Modul geladen wurde.
3.  Das System Verzeichnis (% systemroot% \\ system32).

## <a name="search-order-for-desktop-applications"></a>Such Reihenfolge für Desktop Anwendungen

Desktop Anwendungen können den Speicherort steuern, von dem eine DLL geladen wird, indem Sie einen vollständigen Pfad, mithilfe der [dll-Umleitung](dynamic-link-library-redirection.md)oder mithilfe eines [Manifests](/windows/desktop/SbsCs/manifests)angeben. Wenn keine dieser Methoden verwendet wird, sucht das System zur Ladezeit nach der dll, wie in diesem Abschnitt beschrieben.

Bevor das System nach einer DLL sucht, wird Folgendes überprüft:

-   Wenn eine DLL mit dem gleichen Modulnamen bereits in den Arbeitsspeicher geladen wurde, verwendet das System die geladene DLL, unabhängig davon, in welchem Verzeichnis Sie sich befindet. Das System sucht nicht nach der dll.
-   Wenn die dll in der Liste der bekannten DLLs für die Version von Windows enthalten ist, in der die Anwendung ausgeführt wird, verwendet das System die Kopie der bekannten dll (und ggf. die abhängigen DLLs der bekannten dll). Das System sucht nicht nach der dll. Eine Liste bekannter DLLs auf dem aktuellen System finden Sie unter dem folgenden Registrierungsschlüssel: **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager \\ KnownDLLs**.

Wenn eine DLL Abhängigkeiten aufweist, sucht das System nach den abhängigen DLLs, als wären Sie nur mit den Modulnamen geladen worden. Dies gilt auch, wenn die erste dll durch Angabe eines vollständigen Pfads geladen wurde.

> [!IMPORTANT]
> Wenn ein Angreifer die Kontrolle über eines der Verzeichnisse erhält, die durchsucht werden, kann er eine bösartige Kopie der dll in diesem Verzeichnis platzieren. Weitere Möglichkeiten, solche Angriffe zu verhindern, finden Sie unter [Dynamic-Link Library Security](dynamic-link-library-security.md).

### <a name="standard-search-order-for-desktop-applications"></a>Standard Such Reihenfolge für Desktop Anwendungen

Die vom System verwendete DLL-Standard Such Reihenfolge hängt davon ab, ob der sichere DLL-Suchmodus aktiviert oder deaktiviert ist. Der sichere DLL-Suchmodus platziert das aktuelle Verzeichnis des Benutzers später in der Such Reihenfolge.

Der sichere DLL-Suchmodus ist standardmäßig aktiviert. Um dieses Feature zu deaktivieren, erstellen Sie den Registrierungs Wert **HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ Session Manager** \\ **SafeDllSearchMode** , und legen Sie ihn auf 0 fest. Durch Aufrufen der [**setdlldirectory**](/windows/desktop/api/winbase/nf-winbase-setdlldirectorya) -Funktion wird **SafeDllSearchMode** deaktiviert, während sich das angegebene Verzeichnis im Suchpfad befindet, und die Such Reihenfolge ändert, wie in diesem Thema beschrieben.

Wenn **SafeDllSearchMode** aktiviert ist, lautet die Such Reihenfolge wie folgt:

1.  Das Verzeichnis, in dem die Anwendung geladen wurde.
2.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
3.  Das 16-Bit-System Verzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, sondern durchsucht wird.
4.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind. Beachten Sie, dass dies nicht den pro Anwendung-Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der Schlüssel für die **App-Pfade** wird beim Berechnen des dll-Suchpfades nicht verwendet.

Wenn **SafeDllSearchMode** deaktiviert ist, lautet die Such Reihenfolge wie folgt:

1.  Das Verzeichnis, in dem die Anwendung geladen wurde.
2.  Das aktuelle Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
4.  Das 16-Bit-System Verzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, sondern durchsucht wird.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind. Beachten Sie, dass dies nicht den pro Anwendung-Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der Schlüssel für die **App-Pfade** wird beim Berechnen des dll-Suchpfades nicht verwendet.

### <a name="alternate-search-order-for-desktop-applications"></a>Alternative Such Reihenfolge für Desktop Anwendungen

Die vom System verwendete Standard Such Reihenfolge kann durch Aufrufen der [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion mit der **Last \_ mit dem \_ geänderten \_ \_ Suchpfad** geändert werden. Die Standard Such Reihenfolge kann auch durch Aufrufen der Funktion [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) geändert werden.

> [!NOTE]
> Die Standard Such Reihenfolge des Prozesses wird auch durch Aufrufen der [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) -Funktion im übergeordneten Prozess vor dem Start des aktuellen Prozesses beeinträchtigt.

Wenn Sie eine Alternative Suchstrategie angeben, wird das Verhalten so lange fortgesetzt, bis alle zugehörigen ausführbaren Module gefunden wurden. Nachdem das System mit der Verarbeitung der dll-Initialisierungs Routinen begonnen hat, stellt das System die Standard Suchstrategie wieder her.

Die [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion unterstützt eine Alternative Such Reihenfolge, wenn der-Befehl **Load \_ mit einem \_ geänderten \_ \_ Suchpfad** angibt und der *lpFileName* -Parameter einen absoluten Pfad angibt.

Beachten Sie, dass die Standard Suchstrategie und die Alternative Suchstrategie, die von [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) mit **Load \_ mit dem \_ geänderten \_ \_ Suchpfad** festgelegt wird, sich in nur eine Weise unterscheiden: die Standardsuche beginnt im Verzeichnis der aufrufenden Anwendung, und die Alternative Suche beginnt im Verzeichnis des ausführbaren Moduls, das **LoadLibraryEx** lädt.

Wenn **SafeDllSearchMode** aktiviert ist, lautet die Alternative Such Reihenfolge wie folgt:

1.  Das von *lpFileName* angegebene Verzeichnis.
2.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
3.  Das 16-Bit-System Verzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, sondern durchsucht wird.
4.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
5.  Das aktuelle Verzeichnis.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind. Beachten Sie, dass dies nicht den pro Anwendung-Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der Schlüssel für die **App-Pfade** wird beim Berechnen des dll-Suchpfades nicht verwendet.

Wenn **SafeDllSearchMode** deaktiviert ist, sieht die Alternative Such Reihenfolge wie folgt aus:

1.  Das von *lpFileName* angegebene Verzeichnis.
2.  Das aktuelle Verzeichnis.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
4.  Das 16-Bit-System Verzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, sondern durchsucht wird.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind. Beachten Sie, dass dies nicht den pro Anwendung-Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der Schlüssel für die **App-Pfade** wird beim Berechnen des dll-Suchpfades nicht verwendet.

Die [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) -Funktion unterstützt eine Alternative Such Reihenfolge, wenn der *lppathname* -Parameter einen Pfad angibt. Die Alternative Such Reihenfolge lautet wie folgt:

1.  Das Verzeichnis, in dem die Anwendung geladen wurde.
2.  Das Verzeichnis, das durch den *lppathname* -Parameter von [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)angegeben wird.
3.  Das Systemverzeichnis Verwenden Sie die [**GetSystemDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getsystemdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten. Der Name dieses Verzeichnisses lautet "System32".
4.  Das 16-Bit-System Verzeichnis. Es gibt keine Funktion, die den Pfad dieses Verzeichnisses erhält, sondern durchsucht wird. Der Name dieses Verzeichnisses ist System.
5.  Das Windows-Verzeichnis. Verwenden Sie die [**GetWindowsDirectory**](/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getwindowsdirectorya) -Funktion, um den Pfad zu diesem Verzeichnis zu erhalten.
6.  Die Verzeichnisse, die in der PATH-Umgebungsvariablen aufgelistet sind. Beachten Sie, dass dies nicht den pro Anwendung-Pfad enthält, der durch den Registrierungsschlüssel für **App-Pfade** angegeben wird. Der Schlüssel für die **App-Pfade** wird beim Berechnen des dll-Suchpfades nicht verwendet.

Wenn der *lppathname* -Parameter eine leere Zeichenfolge ist, wird das aktuelle Verzeichnis aus der Such Reihenfolge entfernt.

[**Setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) deaktiviert den sicheren DLL-Suchmodus, während sich das angegebene Verzeichnis im Suchpfad befindet. Um den sicheren DLL-Suchmodus basierend auf dem Registrierungs Wert **SafeDllSearchMode** wiederherzustellen und das aktuelle Verzeichnis in der Such Reihenfolge wiederherzustellen, müssen Sie **setdlldirectory** mit *lppathname* als NULL aufrufen.

### <a name="search-order-using-load_library_search-flags"></a>Such Reihenfolge mithilfe von **\_ \_ Suchflags der Lade Bibliothek**

Eine Anwendung kann eine Such Reihenfolge mithilfe eines oder mehrerer **\_ \_ Suchflags für die Auslastungs Bibliothek** mit der [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion angeben. Eine Anwendung kann auch **Load \_ Library- \_ Suchflags** mit der [**setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) -Funktion verwenden, um eine DLL-Such Reihenfolge für einen Prozess einzurichten. Die Anwendung kann zusätzliche Verzeichnisse für die Such Reihenfolge der Prozess-DLL mithilfe der [**adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) -Funktion oder der [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) -Funktion angeben.

Die Verzeichnisse, die durchsucht werden, richten sich nach den Flags, die mit [**setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)angegeben werden. Wenn mehr als ein Flag verwendet wird, werden die entsprechenden Verzeichnisse in der folgenden Reihenfolge durchsucht:

1.  Das Verzeichnis, das die dll enthält (**Laden der \_ Bibliotheks \_ Suche \_ dll \_ Load \_ dir**). Dieses Verzeichnis wird nur nach Abhängigkeiten der zu ladenden DLL durchsucht.
2.  Das Anwendungsverzeichnis (**Anwendungsverzeichnis der \_ Bibliotheks \_ Suche \_ \_ Laden**).
3.  Pfade, die explizit mit der [**adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory) -Funktion hinzugefügt wurden (**Load \_ Library \_ Search \_ User \_ dirs**) oder die Funktion " [**setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya) ". Wenn mehr als ein Pfad hinzugefügt wurde, ist die Reihenfolge, in der die Pfade durchsucht werden, nicht angegeben.
4.  Das System Verzeichnis (**Laden der \_ Bibliotheks \_ Suche \_ system32**).

Wenn die Anwendung [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) nicht mit einem **\_ \_ Suchflags für die Auslastungs Bibliothek** aufruft oder eine DLL-Such Reihenfolge für den Prozess festlegt, sucht das System entweder mithilfe der Standard Such Reihenfolge oder der alternativen Such Reihenfolge nach DLLs.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Adddlldirectory**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-adddlldirectory)
</dt> <dt>

[Anwendungs Registrierung](/windows/desktop/shell/app-registration)
</dt> <dt>

[Umleitung von Dynamic Link Library](dynamic-link-library-redirection.md)
</dt> <dt>

[Dynamic Link Library-Sicherheit](dynamic-link-library-security.md)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa)
</dt> <dt>

[**LoadPackagedLibrary**](/windows/desktop/api/Winbase/nf-winbase-loadpackagedlibrary)
</dt> <dt>

[**Setdefaultdlldirectories**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-setdefaultdlldirectories)
</dt> <dt>

[**Setdlldirectory**](/windows/desktop/api/Winbase/nf-winbase-setdlldirectorya)
</dt> <dt>

[Parallele Komponenten](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)
</dt> </dl>

 

 