---
description: Eine DLL kann optional eine Einstiegspunktfunktion angeben.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Dynamic-Link Library Entry-Point Function
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6289f705a11dad58eca8b047ba469ee07320dedef762024cbfa04046a0677f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117815838"
---
# <a name="dynamic-link-library-entry-point-function"></a>Dynamic-Link Library Entry-Point Function

Eine DLL kann optional eine Einstiegspunktfunktion angeben. Falls vorhanden, ruft das System die Einstiegspunktfunktion auf, wenn ein Prozess oder Thread die DLL lädt oder entlädt. Sie kann verwendet werden, um einfache Initialisierungs- und Bereinigungsaufgaben auszuführen. Beispielsweise kann er lokalen Threadspeicher einrichten, wenn ein neuer Thread erstellt wird, und ihn bereinigen, wenn der Thread beendet wird.

Wenn Sie Ihre DLL mit der C-Laufzeitbibliothek verknüpfen, stellt sie möglicherweise eine Einstiegspunktfunktion für Sie zur Verfügung und ermöglicht es Ihnen, eine separate Initialisierungsfunktion zur Verfügung zu stellen. Weitere Informationen finden Sie in der Dokumentation zu Ihrer Laufzeitbibliothek.

Wenn Sie einen eigenen Einstiegspunkt bereitstellen, lesen Sie die [**DllMain-Funktion.**](dllmain.md) Der Name **DllMain** ist ein Platzhalter für eine benutzerdefinierte Funktion. Sie müssen den tatsächlichen Namen angeben, den Sie beim Erstellen der DLL verwenden. Weitere Informationen finden Sie in der Dokumentation zu Ihren Entwicklungstools.

## <a name="calling-the-entry-point-function"></a>Aufrufen der Entry-Point-Funktion

Das System ruft die Einstiegspunktfunktion auf, wenn eines der folgenden Ereignisse eintritt:

-   Ein Prozess lädt die DLL. Bei Prozessen, die dynamische Verknüpfungen zur Ladezeit verwenden, wird die DLL während der Prozessin initialisierung geladen. Bei Prozessen mit Laufzeitverknüpfung wird die DLL geladen, bevor [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx zurückgegeben**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) wird.
-   Ein Prozess entlädt die DLL. Die DLL wird entladen, wenn der Prozess die [**FreeLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) beendet oder aufruft und der Verweiszähler 0 (null) wird. Wenn der Prozess als Ergebnis der [**TerminateProcess-**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) oder [**TerminateThread-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) beendet wird, wird die DLL-Einstiegspunktfunktion nicht vom System aufruft.
-   Ein neuer Thread wird in einem Prozess erstellt, der die DLL geladen hat. Sie können die [**Funktion DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) verwenden, um die Benachrichtigung zu deaktivieren, wenn Threads erstellt werden.
-   Ein Thread eines Prozesses, der die DLL geladen hat, wird normal beendet, ohne [**TerminateThread oder**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) [**TerminateProcess zu verwenden.**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) Wenn ein Prozess die DLL entlädt, wird die Einstiegspunktfunktion nur einmal für den gesamten Prozess und nicht einmal für jeden vorhandenen Thread des Prozesses aufgerufen. Sie können [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) verwenden, um Benachrichtigungen zu deaktivieren, wenn Threads beendet werden.

Die Einstiegspunktfunktion kann nur von einem Thread gleichzeitig aufgerufen werden.

Das System ruft die Einstiegspunktfunktion im Kontext des Prozesses oder Threads auf, der den Aufruf der Funktion verursacht hat. Dadurch kann eine DLL ihre Einstiegspunktfunktion verwenden, um Arbeitsspeicher im virtuellen Adressraum des aufrufenden Prozesses zu zuordnen oder Handles zu öffnen, auf die der Prozess zugriff kann. Die Einstiegspunktfunktion kann einem neuen Thread auch privaten Speicher mithilfe des lokalen Threadspeichers (THREAD Local Storage, TLS) zuordnen. Weitere Informationen zum lokalen Threadspeicher finden Sie unter [Thread Local Storage](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Entry-Point Funktionsdefinition

Die DLL-Einstiegspunktfunktion muss mit der Standardaufrufaufrufkonvention deklariert werden. Wenn der DLL-Einstiegspunkt nicht ordnungsgemäß deklariert ist, wird die DLL nicht geladen, und das System zeigt eine Meldung an, die angibt, dass der DLL-Einstiegspunkt mit WINAPI deklariert werden muss.

Im Text der Funktion können Sie eine beliebige Kombination der folgenden Szenarien behandeln, in denen der DLL-Einstiegspunkt aufgerufen wurde:

-   Ein Prozess lädt die DLL (**DLL \_ PROCESS \_ ATTACH**).
-   Der aktuelle Prozess erstellt einen neuen Thread (**DLL \_ THREAD \_ ATTACH**).
-   Ein Thread wird normal beendet (**DLL \_ THREAD \_ DETACH**).
-   Ein Prozess entlädt die DLL (**DLL \_ PROCESS \_ DETACH**).

Die Einstiegspunktfunktion sollte nur einfache Initialisierungsaufgaben ausführen. Es darf nicht die [**LoadLibrary-**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) (oder eine Funktion, die diese Funktionen aufruft) aufrufen, da dies Abhängigkeitsschleifen in der DLL-Lade reihenfolge erstellen kann. Dies kann dazu führen, dass eine DLL verwendet wird, bevor das System seinen Initialisierungscode ausgeführt hat. Ebenso darf die Einstiegspunktfunktion die [**FreeLibrary-Funktion**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) (oder eine Funktion, die **FreeLibrary** aufruft) während der Prozessbeendigung nicht aufrufen, da dies dazu führen kann, dass eine DLL verwendet wird, nachdem das System seinen Beendigungscode ausgeführt hat.

Da Kernel32.dll beim Aufruf der Einstiegspunktfunktion garantiert in den Prozessadressenbereich geladen wird, führt das Aufrufen von Funktionen in Kernel32.dll nicht dazu, dass die DLL verwendet wird, bevor ihr Initialisierungscode ausgeführt wurde. Daher kann die Einstiegspunktfunktion [](/windows/desktop/Sync/synchronization-objects) Synchronisierungsobjekte wie kritische Abschnitte und Mutexe erstellen und TLS verwenden, da sich diese Funktionen in Kernel32.dll. Es ist beispielsweise nicht sicher, die Registrierungsfunktionen auf aufruft, da sie sich in Advapi32.dll.

Das Aufrufen anderer Funktionen kann zu Problemen führen, die schwer zu diagnostizieren sind. Beispielsweise kann das Aufrufen von User-, Shell- und COM-Funktionen zu Zugriffsverletzungsfehlern führen, da einige Funktionen in ihren DLLs [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufrufen, um andere Systemkomponenten zu laden. Umgekehrt kann das Aufrufen dieser Funktionen während der Beendigung zu Zugriffsverletzungsfehlern führen, da die entsprechende Komponente möglicherweise bereits entladen oder nicht initialisiert wurde.

Im folgenden Beispiel wird veranschaulicht, wie die DLL-Einstiegspunktfunktion strukturiert wird.

``` syntax
BOOL WINAPI DllMain(
    HINSTANCE hinstDLL,  // handle to DLL module
    DWORD fdwReason,     // reason for calling function
    LPVOID lpReserved )  // reserved
{
    // Perform actions based on the reason for calling.
    switch( fdwReason ) 
    { 
        case DLL_PROCESS_ATTACH:
         // Initialize once for each new process.
         // Return FALSE to fail DLL load.
            break;

        case DLL_THREAD_ATTACH:
         // Do thread-specific initialization.
            break;

        case DLL_THREAD_DETACH:
         // Do thread-specific cleanup.
            break;

        case DLL_PROCESS_DETACH:
         // Perform any necessary cleanup.
            break;
    }
    return TRUE;  // Successful DLL_PROCESS_ATTACH.
}
```

## <a name="entry-point-function-return-value"></a>Entry-Point-Rückgabewert der Funktion

Wenn eine DLL-Einstiegspunktfunktion aufgerufen wird, weil ein Prozess geladen wird, gibt die Funktion **TRUE** zurück, um den Erfolg anzugeben. Bei Prozessen, die die Verknüpfung zur Ladezeit verwenden, führt der Rückgabewert **FALSE** dazu, dass die Prozessin initialisierung fehlschlägt und der Prozess beendet wird. Bei Prozessen, die die Laufzeitverknüpfung verwenden, bewirkt der Rückgabewert FALSE, dass die [**LoadLibrary-**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx-Funktion**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) **NULL** zurückgibt, was auf einen Fehler hinweist. (Das System ruft sofort ihre Einstiegspunktfunktion mit **DLL \_ PROCESS \_ DETACH** auf und entlädt die DLL.) Der Rückgabewert der Einstiegspunktfunktion wird ignoriert, wenn die Funktion aus einem anderen Grund aufgerufen wird.

 

 
