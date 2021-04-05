---
description: Eine DLL kann optional eine Einstiegspunkt Funktion angeben.
ms.assetid: ec035fc6-0a6f-4e52-a4cc-8d7a25a94366
title: Entry-Point Funktion der Dynamic-Link-Bibliothek
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b62bff557bfa2aa792b420e8fe1856bbe0726921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753776"
---
# <a name="dynamic-link-library-entry-point-function"></a>Entry-Point Funktion der Dynamic-Link-Bibliothek

Eine DLL kann optional eine Einstiegspunkt Funktion angeben. Falls vorhanden, ruft das System die Einstiegspunkt Funktion immer dann auf, wenn ein Prozess oder Thread die dll lädt oder entlädt. Sie kann verwendet werden, um einfache Initialisierungs-und Bereinigungs Aufgaben auszuführen. So kann beispielsweise ein lokaler Thread Speicher eingerichtet werden, wenn ein neuer Thread erstellt wird, und bereinigt, wenn der Thread beendet wird.

Wenn Sie die DLL mit der C-Lauf Zeit Bibliothek verknüpfen, stellt Sie möglicherweise eine Einstiegspunkt Funktion bereit und ermöglicht es Ihnen, eine separate Initialisierungsfunktion bereitzustellen. Weitere Informationen finden Sie in der Dokumentation zur Lauf Zeit Bibliothek.

Wenn Sie einen eigenen Einstiegspunkt bereitstellen, finden Sie weitere Informationen unter der [**DllMain**](dllmain.md) -Funktion. Der Name **DllMain** ist ein Platzhalter für eine benutzerdefinierte Funktion. Sie müssen den tatsächlichen Namen angeben, den Sie beim Erstellen der DLL verwenden. Weitere Informationen finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.

## <a name="calling-the-entry-point-function"></a>Aufrufen der Entry-Point-Funktion

Das System ruft die Einstiegspunkt Funktion immer dann auf, wenn eines der folgenden Ereignisse eintritt:

-   Ein Prozess lädt die dll. Für Prozesse, die dynamische Verknüpfungen zur Ladezeit verwenden, wird die dll während der Prozess Initialisierung geladen. Für Prozesse, die Lauf Zeit Verknüpfungen verwenden, wird die dll vor der Rückgabe von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) oder [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) geladen.
-   Ein Prozess entlädt die dll. Die dll wird entladen, wenn der Prozess beendet wird oder die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion aufruft und der Verweis Zähler 0 (null) ist. Wenn der Prozess aufgrund der [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) -oder [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) -Funktion beendet wird, ruft das System die DLL-Einstiegspunkt Funktion nicht auf.
-   Ein neuer Thread wird in einem Prozess erstellt, der die dll geladen hat. Sie können die [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) -Funktion verwenden, um die Benachrichtigung zu deaktivieren, wenn Threads erstellt werden.
-   Ein Thread eines Prozesses, der die dll geladen hat, wird normal beendet, nicht mithilfe von [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread) oder [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess). Wenn ein Prozess die dll entlädt, wird die Einstiegspunkt Funktion nur einmal für den gesamten Prozess und nicht für jeden vorhandenen Thread des Prozesses aufgerufen. Sie können [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) verwenden, um die Benachrichtigung zu deaktivieren, wenn Threads beendet werden.

Die Einstiegspunkt Funktion kann jeweils nur von einem Thread aufgerufen werden.

Das System ruft die Einstiegspunkt Funktion im Kontext des Prozesses oder Threads auf, der bewirkt hat, dass die Funktion aufgerufen wird. Dadurch kann eine DLL die Einstiegspunkt Funktion verwenden, um Speicher im virtuellen Adressraum des aufrufenden Prozesses zuzuweisen, oder um Handles zu öffnen, auf die der Prozess Zugriff hat. Die Einstiegspunkt Funktion kann auch Arbeitsspeicher zuweisen, der einem neuen Thread mithilfe von Thread lokalem Speicher (TLS) privat ist. Weitere Informationen zum lokalen Thread Speicher finden Sie unter [Thread lokaler Speicher](/windows/desktop/ProcThread/thread-local-storage).

## <a name="entry-point-function-definition"></a>Definition der Entry-Point Funktion

Die DLL-Einstiegspunkt Funktion muss mit der Standard Aufruf Konvention deklariert werden. Wenn der DLL-Einstiegspunkt nicht ordnungsgemäß deklariert ist, wird die dll nicht geladen, und das System zeigt eine Meldung an, die angibt, dass der DLL-Einstiegspunkt mit WinAPI deklariert werden muss.

Im Hauptteil der-Funktion können Sie eine beliebige Kombination der folgenden Szenarien verarbeiten, in denen der DLL-Einstiegspunkt aufgerufen wurde:

-   Ein Prozess lädt die dll (**dll- \_ Prozess \_ Anfügen**).
-   Der aktuelle Prozess erstellt einen neuen Thread (**\_ \_ Anfügen eines dll-Threads**).
-   Ein Thread wird normal beendet **( \_ \_ Trennen des dll-Threads**).
-   Ein Prozess entlädt die dll (**dll \_ - \_ Prozess** Trennung).

Die Einstiegspunkt Funktion sollte nur einfache Initialisierungs Tasks ausführen. Die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion oder die [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion (oder eine Funktion, die diese Funktionen aufruft) darf nicht aufgerufen werden, da dadurch Abhängigkeits Schleifen in der dll-Lade Reihenfolge erstellt werden können. Dies kann dazu führen, dass eine DLL verwendet wird, bevor das System den Initialisierungs Code ausgeführt hat. Ebenso darf die Einstiegspunkt Funktion die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion (oder eine Funktion, die **FreeLibrary** aufruft) während der Prozess Beendigung nicht aufrufen, da dies dazu führen kann, dass eine DLL verwendet wird, nachdem das System den Beendigungs Code ausgeführt hat.

Da Kernel32.dll im Prozess Adressraum garantiert geladen wird, wenn die Einstiegspunkt Funktion aufgerufen wird, führt das Aufrufen von Funktionen in Kernel32.dll nicht dazu, dass die dll verwendet wird, bevor Ihr Initialisierungs Code ausgeführt wurde. Daher kann die Einstiegspunkt Funktion [Synchronisierungs Objekte](/windows/desktop/Sync/synchronization-objects) erstellen, z. b. kritische Abschnitte und Mutexen, und TLS verwenden, da sich diese Funktionen in Kernel32.dll befinden. Es ist z. b. nicht sicher, die Registrierungsfunktionen aufzurufen, da Sie sich in Advapi32.dll befinden.

Das Aufrufen anderer Funktionen kann zu Problemen führen, die schwer zu diagnostizieren sind. Das Aufrufen von Benutzer-, Shell-und com-Funktionen kann z. b. zu Zugriffs Verletzungs Fehlern führen, da einige Funktionen in ihren DLLs [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) aufrufen, um andere Systemkomponenten zu laden. Umgekehrt kann das Aufrufen dieser Funktionen während der Beendigung zu Zugriffs Verletzungs Fehlern führen, da die entsprechende Komponente möglicherweise bereits entladen oder nicht initialisiert wurde.

Im folgenden Beispiel wird veranschaulicht, wie die-DLL-Einstiegspunkt Funktion strukturiert wird.

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

## <a name="entry-point-function-return-value"></a>Rückgabewert der Entry-Point Funktion

Wenn eine DLL-Einstiegspunkt Funktion aufgerufen wird, weil ein Prozess geladen wird, gibt die Funktion **true** zurück, um den Erfolg anzugeben. Bei Prozessen, die das Lade Zeit Verknüpfungen verwenden, bewirkt der Rückgabewert **false** , dass die Prozess Initialisierung fehlschlägt und der Prozess beendet wird. Für Prozesse, die Lauf Zeit Verknüpfungen verwenden, bewirkt der Rückgabewert FALSE, dass die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion oder die [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion **null** zurückgibt, was auf einen Fehler hinweist. (Das System ruft sofort die Einstiegspunkt Funktion mit dem **dll \_ - \_ Prozess** ab und entlädt die dll.) Der Rückgabewert der Einstiegspunkt Funktion wird ignoriert, wenn die Funktion aus einem anderen Grund aufgerufen wird.

 

 
