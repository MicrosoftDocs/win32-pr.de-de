---
description: Ein optionaler Einstiegspunkt in eine Dynamic Link Library (dll). Wenn das System einen Prozess oder Thread startet oder beendet, ruft es die Einstiegspunkt Funktion für jede geladene DLL mit dem ersten Thread des Prozesses auf.
ms.assetid: 0c3e3083-9297-4626-b2a7-0062d1c2cf9e
title: DllMain-Einstiegspunkt (Process. h)
ms.topic: reference
ms.date: 07/22/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: ee182fd54f11909e54e98f827904f1da5e46f557
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347417"
---
# <a name="dllmain-entry-point"></a>DllMain-Einstiegspunkt

Ein optionaler Einstiegspunkt in eine Dynamic Link Library (dll). Wenn das System einen Prozess oder Thread startet oder beendet, ruft es die Einstiegspunkt Funktion für jede geladene DLL mit dem ersten Thread des Prozesses auf. Das System ruft auch die Einstiegspunkt Funktion für eine DLL auf, wenn Sie mit den Funktionen [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) geladen oder entladen wird.

## <a name="example"></a>Beispiel

```cpp
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

Dies ist ein Beispiel aus der [Funktion "Dynamic-Link Library Entry-Point](dynamic-link-library-entry-point-function.md)".


> [!WARNING]
> Es gibt erhebliche Einschränkungen bei den Aktionen, die Sie sicher in einem DLL-Einstiegspunkt durchführen können. Weitere Informationen finden Sie unter [allgemeine bewährte Methoden](dynamic-link-library-best-practices.md) für bestimmte Windows-APIs, die in DllMain nicht sicher aufgerufen werden können. Wenn Sie mehr als nur die einfachste Initialisierung durchführen müssen, führen Sie dies in einer Initialisierungsfunktion für die DLL durch. Sie können festlegen, dass Anwendungen die Initialisierungsfunktion nach dem Ausführen von DllMain und vor dem Abrufen anderer Funktionen in der DLL aufruft.

 

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI DllMain(
  _In_ HINSTANCE hinstDLL,
  _In_ DWORD     fdwReason,
  _In_ LPVOID    lpvReserved
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstDll* \[ in\]
</dt> <dd>

Ein Handle für das dll-Modul. Der Wert ist die Basisadresse der dll. Die **HINSTANCE** einer dll ist mit dem **HMODULE** der dll identisch, sodass *hinstDll* in Aufrufen von Funktionen verwendet werden kann, die ein Modul handle erfordern.

</dd> <dt>

*Grundursache* \[ in\]
</dt> <dd>

Der Ursachen Code, der angibt, warum die DLL-Einstiegspunkt Funktion aufgerufen wird. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                | Bedeutung                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DLL_PROCESS_ATTACH"></span><span id="dll_process_attach"></span><dl> <dt>**Dll \_ Prozess \_ Anfügen**</dt> <dt>1</dt> </dl> | Die dll wird in den virtuellen Adressraum des aktuellen Prozesses als Ergebnis des Startvorgangs oder als Ergebnis eines Aufrufes von [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)geladen. DLLs können diese Gelegenheit nutzen, um beliebige Instanzdaten zu initialisieren oder die [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) -Funktion zu verwenden, um einen Thread lokalen Speicher (TLS)-Index zuzuordnen.<br/> Der *lbeibehaltene* Parameter gibt an, ob die DLL statisch oder dynamisch geladen wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="DLL_PROCESS_DETACH"></span><span id="dll_process_detach"></span><dl> <dt>**Dll \_ Prozess \_**</dt> Trennung <dt>0</dt> </dl> | Die dll wird aus dem virtuellen Adressraum des aufrufenden Prozesses entladen, weil Sie nicht erfolgreich geladen wurde oder der Verweis Zähler Null erreicht hat (die Prozesse wurden entweder für jedes Mal, wenn Sie [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)aufgerufen haben, entweder beendet oder als " [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) " bezeichnet).<br/> Der *lbeibehaltene* Parameter gibt an, ob die dll aufgrund eines [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Aufrufes, eines Fehlers beim Laden oder eines Prozess Beendens entladen wird.<br/> Die dll kann diese Möglichkeit zum Abrufen der [**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree) -Funktion verwenden, um alle TLS-Indizes freizugeben, die mithilfe von [**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc) zugeordnet werden, und um beliebige Thread lokale Daten freizugeben.<br/> Beachten Sie, dass der Thread, der die **dll- \_ Prozess \_** Trennungs Benachrichtigung empfängt, nicht notwendigerweise derselbe Thread ist, der die **dll- \_ Prozess \_ Anfüge** Benachrichtigung empfangen hat.<br/> |
| <span id="DLL_THREAD_ATTACH"></span><span id="dll_thread_attach"></span><dl> <dt>**Dll \_ Thread \_ Anfügen**</dt> <dt>2</dt> </dl>    | Beim aktuellen Prozess wird ein neuer Thread erstellt. Wenn dies auftritt, ruft das System die Einstiegspunkt Funktion aller DLLs auf, die derzeit an den Prozess angefügt sind. Der-Rückruf erfolgt im Kontext des neuen Threads. DLLs können diese Gelegenheit nutzen, um einen TLS-Slot für den Thread zu initialisieren. Ein Thread, der die DLL-Einstiegspunkt Funktion mit **dll- \_ Prozess \_ Anfügen** aufruft, ruft die DLL-Einstiegspunkt Funktion nicht mit **dll- \_ Thread \_ Anfügen** auf. <br/> Beachten Sie, dass die Einstiegspunkt Funktion einer DLL mit diesem Wert nur von Threads aufgerufen wird, die nach dem Laden der dll durch den Prozess erstellt werden. Wenn eine DLL mit [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)geladen wird, wird die Einstiegspunkt Funktion der neu geladenen DLL von vorhandenen Threads nicht aufgerufen.<br/>                                                                                                                                                                       |
| <span id="DLL_THREAD_DETACH"></span><span id="dll_thread_detach"></span><dl> <dt>**Dll \_ Thread \_**</dt> Trennung <dt>3</dt> </dl>    | Ein Thread wird ordnungsgemäß beendet. Wenn die dll einen Zeiger auf den zugeordneten Speicher in einem TLS-Slot gespeichert hat, sollte diese Gelegenheit genutzt werden, um den Arbeitsspeicher freizugeben. Das System ruft die Einstiegspunkt Funktion aller aktuell geladenen DLLs mit diesem Wert auf. Der-Befehl wird im Kontext des enden Threads durchgeführt.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |



 

</dd> <dt>

*lpvreserved* \[ in\]
</dt> <dd>

Wenn *fdwreason* **dll- \_ Prozess \_ Anfügen** ist, ist *lpvreserved* bei dynamischen Ladevorgängen **null** und ungleich NULL für statische Ladevorgänge.

Wenn *fdwreason* eine **dll- \_ Prozess \_** Trennung ist, ist *lpvreserved* **null** , wenn " [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) " aufgerufen wurde oder wenn der dll-Ladevorgang fehlgeschlagen ist und nicht **null** ist, wenn der Prozess beendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn das System die **DllMain** -Funktion mit dem **\_ \_ Anfüge** Wert des dll-Prozesses aufruft, gibt die Funktion **true** zurück, wenn Sie erfolgreich ist oder **false** , wenn die Initialisierung fehlschlägt. Wenn der Rückgabewert **false** ist, wenn **DllMain** aufgerufen wird, da der Prozess die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion verwendet, gibt **LoadLibrary** NULL zurück. (Das System ruft sofort die Einstiegspunkt Funktion mit dem **dll \_ - \_ Prozess** ab und entlädt die dll.) Wenn der Rückgabewert **false** ist, wenn **DllMain** während der Prozess Initialisierung aufgerufen wird, wird der Prozess mit einem Fehler beendet. Um erweiterte Fehlerinformationen zu erhalten, rufen Sie [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf.

Wenn das System die **DllMain** -Funktion mit einem anderen Wert als dem **dll- \_ Prozess \_ Anfügen** aufruft, wird der Rückgabewert ignoriert.

## <a name="remarks"></a>Bemerkungen

**DllMain** ist ein Platzhalter für den Namen der Bibliothek definierten Funktion. Sie müssen den tatsächlichen Namen angeben, den Sie beim Erstellen der DLL verwenden. Weitere Informationen finden Sie in der Dokumentation, die in ihren Entwicklungs Tools enthalten ist.

Während des anfänglichen Prozess Starts oder nach einem [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)-Aufrufvorgang scannt das System die Liste der geladenen DLLs für den Prozess. Für jede DLL, die nicht bereits mit dem **\_ \_ Anfüge** Wert des dll-Prozesses aufgerufen wurde, ruft das System die Einstiegspunkt Funktion der dll auf. Dieser Aufruf erfolgt im Kontext des Threads, der bewirkt hat, dass sich der Prozess Adressraum geändert hat, z. b. der primäre Thread des Prozesses oder der Thread, der **LoadLibrary** aufgerufen hat. Der Zugriff auf den Einstiegspunkt wird vom System Prozess weit serialisiert. Threads in *DllMain* enthalten die Loadersperre, sodass keine weiteren DLLs dynamisch geladen oder initialisiert werden können.

Wenn die Einstiegspunkt Funktion der DLL nach einer **dll- \_ Prozess \_ Anfüge** Benachrichtigung false zurückgibt, empfängt Sie eine **dll- \_ Prozess \_** Trennungs Benachrichtigung, und die dll wird sofort entladen. Wenn jedoch der **dll- \_ Prozess \_ Anfüge** Code eine Ausnahme auslöst, empfängt die Einstiegspunkt Funktion nicht die **dll- \_ Prozess- \_ detachbenachrichtigung** .

Es gibt Fälle, in denen die Einstiegspunkt Funktion für einen abschließenden Thread aufgerufen wird, auch wenn die Einstiegspunkt Funktion nie mit dem **dll- \_ Thread \_ Attach** für den Thread aufgerufen wurde:

-   Der Thread war der erste Thread im Prozess, sodass das System die Einstiegspunkt Funktion mit dem **\_ \_ Anfüge** Wert des dll-Prozesses aufgerufen hat.
-   Der Thread wurde bereits ausgeführt, als ein Aufruf der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion erfolgt ist, sodass das System nie die Einstiegspunkt Funktion aufgerufen hat.

Wenn eine DLL aus einem Prozess aufgrund einer nicht erfolgreichen Last der dll, Beendigung des Prozesses oder eines Aufrufs von " [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)" entladen wird, ruft das System die Einstiegspunkt Funktion der dll nicht mit dem **dll- \_ Thread \_** Trennungs Wert für die einzelnen Threads des Prozesses auf. Der dll wird nur eine **dll- \_ Prozess- \_ Detach** -Benachrichtigung gesendet. DLLs können diese Gelegenheit nutzen, um alle Ressourcen für alle Threads zu bereinigen, die der dll bekannt sind.

Wenn die DLL- **Prozess Trennung behandelt \_ \_** wird, sollte eine DLL Ressourcen wie z. b. Heap Speicher nur dann freigeben, wenn die DLL dynamisch entladen wird (der *lbeibehaltene* Parameter ist **null**). Wenn der Prozess beendet wird (der *lpvreserved* -Parameter ist nicht **null**), werden alle Threads im Prozess, außer dem aktuellen Thread, entweder bereits beendet oder durch einen Aufrufen der [**ExitProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-exitprocess) -Funktion explizit beendet, was einige Prozess Ressourcen wie Heaps in einem inkonsistenten Zustand belassen kann. In diesem Fall ist es nicht sicher, dass die dll die Ressourcen bereinigen kann. Stattdessen sollte die dll dem Betriebssystem ermöglichen, den Speicher freizugeben.

Wenn Sie einen Prozess beenden, indem Sie [**TerminateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess) oder [**terminatejobobject**](/windows/desktop/api/jobapi2/nf-jobapi2-terminatejobobject)aufrufen, empfangen die DLLs dieses Prozesses keine **dll- \_ Prozess \_** Trennungs Benachrichtigungen. Wenn Sie einen Thread beenden, indem Sie [**TerminateThread**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminatethread)aufrufen, empfangen die DLLs dieses Threads keine **dll- \_ Thread \_** Trennungs Benachrichtigungen.

Die Einstiegspunkt Funktion sollte nur einfache Initialisierungs-oder Beendigungs Aufgaben ausführen. Die [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion oder die [**LoadLibraryEx**](/windows/desktop/api/LibLoaderAPI/nf-libloaderapi-loadlibraryexa) -Funktion (oder eine Funktion, die diese Funktionen aufruft) darf nicht aufgerufen werden, da dadurch Abhängigkeits Schleifen in der dll-Lade Reihenfolge erstellt werden können. Dies kann dazu führen, dass eine DLL verwendet wird, bevor das System den Initialisierungs Code ausgeführt hat. Ebenso darf die Einstiegspunkt Funktion die [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) -Funktion (oder eine Funktion, die **FreeLibrary** aufruft) während der Prozess Beendigung nicht aufrufen, da dies dazu führen kann, dass eine DLL verwendet wird, nachdem das System den Beendigungs Code ausgeführt hat.

Da Kernel32.dll im Prozess Adressraum garantiert geladen wird, wenn die Einstiegspunkt Funktion aufgerufen wird, führt das Aufrufen von Funktionen in Kernel32.dll nicht dazu, dass die dll verwendet wird, bevor Ihr Initialisierungs Code ausgeführt wurde. Daher kann die Einstiegspunkt Funktion Funktionen in Kernel32.dll aufzurufen, die keine anderen DLLs laden. *DllMain* kann z. b. [Synchronisierungs Objekte](/windows/desktop/Sync/synchronization-objects) erstellen, z. b. kritische Abschnitte und Mutexen, und TLS verwenden. Leider gibt es keine umfassende Liste der sicheren Funktionen in Kernel32.dll.

Das Aufrufen von Funktionen, die andere DLLs als Kernel32.dll erfordern, kann zu Problemen führen, die schwer zu diagnostizieren sind. Das Aufrufen von Benutzer-, Shell-und com-Funktionen kann z. b. zu Zugriffs Verletzungs Fehlern führen, da einige Funktionen andere Systemkomponenten laden. Umgekehrt kann das Aufrufen von Funktionen wie diesen während der Beendigung zu Zugriffs Verletzungs Fehlern führen, da die entsprechende Komponente möglicherweise bereits entladen oder nicht initialisiert wurde.

Da dll-Benachrichtigungen serialisiert werden, sollten die Einstiegspunkt Funktionen nicht versuchen, mit anderen Threads oder Prozessen zu kommunizieren. Deadlocks können als Ergebnis auftreten.

Informationen zu bewährten Methoden beim Schreiben einer DLL finden Sie unter https://docs.microsoft.com/windows/win32/dlls/dynamic-link-library-best-practices .

Wenn die DLL mit der C-Lauf Zeit Bibliothek (CRT) verknüpft ist, ruft der von der CRT bereitgestellte Einstiegspunkt die Konstruktoren und Dekonstruktoren für globale und statische C++-Objekte auf. Daher gelten diese Einschränkungen für *DllMain* auch für Konstruktoren und decoditoren und sämtlicher Code, der von Ihnen aufgerufen wird.

Wenn die dll nicht mit der statischen C-Lauf Zeit Bibliothek (CRT) verknüpft **ist, sollten \_ \_** Sie den Aufruf von [**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls) in Erwägung erhalten.


## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| Header<br/>                   | <dl> <dt>Process. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Dynamic-Link Library Entry-Point-Funktion](dynamic-link-library-entry-point-function.md)
</dt> <dt>

[Dynamic Link Library-Funktionen](dynamic-link-library-functions.md)
</dt> <dt>

[**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary)
</dt> <dt>

[**Fehler bei GetModuleFileName**](/windows/win32/api/libloaderapi/nf-libloaderapi-getmodulefilenamea)
</dt> <dt>

[**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> <dt>

[**TlsAlloc**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsalloc)
</dt> <dt>

[**TlsFree**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-tlsfree)
</dt> <dt>

[**DisableThreadLibraryCalls**](/windows/win32/api/libloaderapi/nf-libloaderapi-disablethreadlibrarycalls)





</dt> </dl>
