---
title: Auflisten von Netzwerkressourcen
description: Das folgende Beispiel veranschaulicht eine Anwendungs definierte Funktion (enumeratefunc), die alle Ressourcen in einem Netzwerk auflistet.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2313e679746b09603d2514b418abf281fefa9bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390659"
---
# <a name="enumerating-network-resources"></a>Auflisten von Netzwerkressourcen

Das folgende Beispiel veranschaulicht eine Anwendungs definierte Funktion (enumeratefunc), die alle Ressourcen in einem Netzwerk auflistet. Im Beispiel wird **null** für den Zeiger auf die Struktur " [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) " angegeben, denn wenn " [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) " einen **null** -Zeiger empfängt, ruft er ein Handle an den Stamm des Netzwerks ab.

Um mit der Enumeration einer Netzwerk Container Ressource zu beginnen, sollte Ihre Anwendung die folgenden Schritte ausführen:

1.  Übergeben Sie die Adresse einer [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Struktur, die die Ressource darstellt, an die Funktion [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .
2.  Weisen Sie einen Puffer zu, der groß genug ist, um das Array von [**artresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Strukturen aufzunehmen, die von der [**wnettenumschlag**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion zurückgegeben werden, sowie die Zeichen folgen, auf die ihre Elemente
3.  Übergeben Sie das von [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) zurückgegebene Ressourcen Handle an die [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion.
4.  Schließen Sie das Ressourcen handle, wenn es nicht mehr benötigt wird, indem Sie die [**wnetcloseenum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) -Funktion aufrufen.

Sie können fortfahren, indem Sie eine Container Ressource auflisten, die im Array der von [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)abgerufenen [**artresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Strukturen beschrieben wird. Wenn der **dwusage** -Member der Struktur " **nettresource** " gleich dem ResourceUsage \_ -Container ist, übergeben Sie die Adresse der Struktur an die Funktion " [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) ", um den Container zu öffnen und die Enumeration fortzusetzen. Wenn **dwusage** gleich ResourceUsage \_ Connectable ist, kann die Anwendung die Adresse der Struktur an die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion oder die [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) -Funktion übergeben, um eine Verbindung mit der Ressource herzustellen.

Zuerst Ruft das Beispiel die [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) -Funktion auf, um die-Enumeration zu starten. Das Beispiel ruft die [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion auf, um den erforderlichen Puffer zuzuordnen, und ruft dann die [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) -Funktion auf, um den Pufferinhalt auf 0 (null) festzulegen. Im Beispiel wird die [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion aufgerufen, um die-Enumeration fortzusetzen. Immer wenn der **dwusage** -Member einer von **wnettenumresource** abgerufenen [**Struktur gleich**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) dem ResourceUsage \_ -Container ist, ruft die enumeratefunc-Funktion sich selbst rekursiv auf und verwendet einen Zeiger auf diese Struktur in dem Aufruf von **WNetOpenEnum**. Zum Schluss ruft das Beispiel die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion auf, um den zugeordneten Arbeitsspeicher freizugeben, und die [**wnetcloseenum-Klasse**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) zum Beenden der Enumeration.


```C++
#ifndef UNICODE
#define UNICODE
#endif
#pragma comment(lib, "mpr.lib")

#include <windows.h>
#include <stdio.h>
#include <winnetwk.h>

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr);
void DisplayStruct(int i, LPNETRESOURCE lpnrLocal);

int main()
{

    LPNETRESOURCE lpnr = NULL;

    if (EnumerateFunc(lpnr) == FALSE) {
        printf("Call to EnumerateFunc failed\n");
        return 1;
    } else
        return 0;

}

BOOL WINAPI EnumerateFunc(LPNETRESOURCE lpnr)
{
    DWORD dwResult, dwResultEnum;
    HANDLE hEnum;
    DWORD cbBuffer = 16384;     // 16K is a good size
    DWORD cEntries = -1;        // enumerate all possible entries
    LPNETRESOURCE lpnrLocal;    // pointer to enumerated structures
    DWORD i;
    //
    // Call the WNetOpenEnum function to begin the enumeration.
    //
    dwResult = WNetOpenEnum(RESOURCE_GLOBALNET, // all network resources
                            RESOURCETYPE_ANY,   // all resources
                            0,  // enumerate all resources
                            lpnr,       // NULL first time the function is called
                            &hEnum);    // handle to the resource

    if (dwResult != NO_ERROR) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
        return FALSE;
    }
    //
    // Call the GlobalAlloc function to allocate resources.
    //
    lpnrLocal = (LPNETRESOURCE) GlobalAlloc(GPTR, cbBuffer);
    if (lpnrLocal == NULL) {
        printf("WnetOpenEnum failed with error %d\n", dwResult);
//      NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetOpenEnum");
        return FALSE;
    }

    do {
        //
        // Initialize the buffer.
        //
        ZeroMemory(lpnrLocal, cbBuffer);
        //
        // Call the WNetEnumResource function to continue
        //  the enumeration.
        //
        dwResultEnum = WNetEnumResource(hEnum,  // resource handle
                                        &cEntries,      // defined locally as -1
                                        lpnrLocal,      // LPNETRESOURCE
                                        &cbBuffer);     // buffer size
        //
        // If the call succeeds, loop through the structures.
        //
        if (dwResultEnum == NO_ERROR) {
            for (i = 0; i < cEntries; i++) {
                // Call an application-defined function to
                //  display the contents of the NETRESOURCE structures.
                //
                DisplayStruct(i, &lpnrLocal[i]);

                // If the NETRESOURCE structure represents a container resource, 
                //  call the EnumerateFunc function recursively.

                if (RESOURCEUSAGE_CONTAINER == (lpnrLocal[i].dwUsage
                                                & RESOURCEUSAGE_CONTAINER))
//          if(!EnumerateFunc(hwnd, hdc, &lpnrLocal[i]))
                    if (!EnumerateFunc(&lpnrLocal[i]))
                        printf("EnumerateFunc returned FALSE\n");
//            TextOut(hdc, 10, 10, "EnumerateFunc returned FALSE.", 29);
            }
        }
        // Process errors.
        //
        else if (dwResultEnum != ERROR_NO_MORE_ITEMS) {
            printf("WNetEnumResource failed with error %d\n", dwResultEnum);

//      NetErrorHandler(hwnd, dwResultEnum, (LPSTR)"WNetEnumResource");
            break;
        }
    }
    //
    // End do.
    //
    while (dwResultEnum != ERROR_NO_MORE_ITEMS);
    //
    // Call the GlobalFree function to free the memory.
    //
    GlobalFree((HGLOBAL) lpnrLocal);
    //
    // Call WNetCloseEnum to end the enumeration.
    //
    dwResult = WNetCloseEnum(hEnum);

    if (dwResult != NO_ERROR) {
        //
        // Process errors.
        //
        printf("WNetCloseEnum failed with error %d\n", dwResult);
//    NetErrorHandler(hwnd, dwResult, (LPSTR)"WNetCloseEnum");
        return FALSE;
    }

    return TRUE;
}

void DisplayStruct(int i, LPNETRESOURCE lpnrLocal)
{
    printf("NETRESOURCE[%d] Scope: ", i);
    switch (lpnrLocal->dwScope) {
    case (RESOURCE_CONNECTED):
        printf("connected\n");
        break;
    case (RESOURCE_GLOBALNET):
        printf("all resources\n");
        break;
    case (RESOURCE_REMEMBERED):
        printf("remembered\n");
        break;
    default:
        printf("unknown scope %d\n", lpnrLocal->dwScope);
        break;
    }

    printf("NETRESOURCE[%d] Type: ", i);
    switch (lpnrLocal->dwType) {
    case (RESOURCETYPE_ANY):
        printf("any\n");
        break;
    case (RESOURCETYPE_DISK):
        printf("disk\n");
        break;
    case (RESOURCETYPE_PRINT):
        printf("print\n");
        break;
    default:
        printf("unknown type %d\n", lpnrLocal->dwType);
        break;
    }

    printf("NETRESOURCE[%d] DisplayType: ", i);
    switch (lpnrLocal->dwDisplayType) {
    case (RESOURCEDISPLAYTYPE_GENERIC):
        printf("generic\n");
        break;
    case (RESOURCEDISPLAYTYPE_DOMAIN):
        printf("domain\n");
        break;
    case (RESOURCEDISPLAYTYPE_SERVER):
        printf("server\n");
        break;
    case (RESOURCEDISPLAYTYPE_SHARE):
        printf("share\n");
        break;
    case (RESOURCEDISPLAYTYPE_FILE):
        printf("file\n");
        break;
    case (RESOURCEDISPLAYTYPE_GROUP):
        printf("group\n");
        break;
    case (RESOURCEDISPLAYTYPE_NETWORK):
        printf("network\n");
        break;
    default:
        printf("unknown display type %d\n", lpnrLocal->dwDisplayType);
        break;
    }

    printf("NETRESOURCE[%d] Usage: 0x%x = ", i, lpnrLocal->dwUsage);
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONNECTABLE)
        printf("connectable ");
    if (lpnrLocal->dwUsage & RESOURCEUSAGE_CONTAINER)
        printf("container ");
    printf("\n");

    printf("NETRESOURCE[%d] Localname: %S\n", i, lpnrLocal->lpLocalName);
    printf("NETRESOURCE[%d] Remotename: %S\n", i, lpnrLocal->lpRemoteName);
    printf("NETRESOURCE[%d] Comment: %S\n", i, lpnrLocal->lpComment);
    printf("NETRESOURCE[%d] Provider: %S\n", i, lpnrLocal->lpProvider);
    printf("\n");
}

```



Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).

 

 