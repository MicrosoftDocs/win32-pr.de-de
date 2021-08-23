---
title: Aufzählen von Netzwerkressourcen
description: Das folgende Beispiel veranschaulicht eine anwendungsdefinierte Funktion (EnumerateFunc), die alle Ressourcen in einem Netzwerk aufzählt.
ms.assetid: f5872ee7-483d-406a-b7d8-4ce93613fd29
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633a8b03dd538853a0b339ee727c18fb05b2231b7690d89dea0a83264f7faf8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053329"
---
# <a name="enumerating-network-resources"></a>Aufzählen von Netzwerkressourcen

Das folgende Beispiel veranschaulicht eine anwendungsdefinierte Funktion (EnumerateFunc), die alle Ressourcen in einem Netzwerk aufzählt. Im Beispiel wird **NULL** für den Zeiger auf die [**NETRESOURCE-Struktur**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) angegeben, da [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) beim Empfangen eines **NULL-Zeigers** ein Handle zum Stamm des Netzwerks abruft.

Um mit der Enumeration einer Netzwerkcontainerressource zu beginnen, sollte Ihre Anwendung die folgenden Schritte ausführen:

1.  Übergeben Sie die Adresse einer [**NETRESOURCE-Struktur,**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) die die Ressource darstellt, an die [**WNetOpenEnum-Funktion.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma)
2.  Ordnen Sie einen Puffer zu, der groß genug ist, um das Array von [**NETRESOURCE-Strukturen**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) zu speichern, das die [**WNetEnumResource-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) zurückgibt, sowie die Zeichenfolgen, auf die ihre Member zeigen.
3.  Übergeben Sie das von [**WNetOpenEnum zurückgegebene**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) Ressourcenhand handle an die [**WNetEnumResource-Funktion.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)
4.  Schließen Sie das Ressourcenhand handle, wenn es nicht mehr benötigt wird, indem Sie die [**WNetCloseEnum-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) aufrufen.

Sie können mit dem Aufzählen einer Containerressource fortfahren, die im Array von [**NETRESOURCE-Strukturen**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) beschrieben wird, die von [**WNetEnumResource abgerufen werden.**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) Wenn **der dwUsage-Member** der **NETRESOURCE-Struktur** gleich RESOURCEUSAGE CONTAINER ist, übergeben Sie die Adresse der Struktur an die \_ [**WNetOpenEnum-Funktion,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) um den Container zu öffnen und die Enumeration fortzufahren. Wenn **dwUsage** gleich RESOURCEUSAGE CONNECTABLE ist, kann die Anwendung die Adresse der Struktur an die \_ [**WNetAddConnection2-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) oder die [**WNetAddConnection3-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) übergeben, um eine Verbindung mit der Ressource herzustellen.

Zuerst ruft das Beispiel die [**WNetOpenEnum-Funktion auf,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) um die Enumeration zu starten. Im Beispiel wird die [**GlobalAlloc-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalalloc) zum Zuordnen des erforderlichen Puffers und dann die [**ZeroMemory-Funktion**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) zum Festlegen des Pufferinhalts auf 0 (null) aufruft. Anschließend ruft das Beispiel die [**WNetEnumResource-Funktion**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) auf, um die Enumeration fortzufahren. Wenn das **dwUsage-Member** einer VON **WNetEnumResource** abgerufenen [**NETRESOURCE-Struktur**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) gleich RESOURCEUSAGE CONTAINER ist, ruft sich die EnumerateFunc-Funktion rekursiv auf und verwendet einen Zeiger auf diese Struktur im Aufruf von \_ **WNetOpenEnum.** Schließlich ruft das Beispiel die [**GlobalFree-Funktion**](/windows/desktop/api/winbase/nf-winbase-globalfree) auf, um den zugeordneten Arbeitsspeicher frei zu geben, und [**das WNetCloseEnum,**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) um die Enumeration zu beenden.


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



Weitere Informationen zur Verwendung eines anwendungsdefinierten Fehlerhandlers finden Sie unter [Retrieving Network Errors](retrieving-network-errors.md).

 

 