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
# <a name="enumerating-network-resources"></a><span data-ttu-id="74099-103">Auflisten von Netzwerkressourcen</span><span class="sxs-lookup"><span data-stu-id="74099-103">Enumerating Network Resources</span></span>

<span data-ttu-id="74099-104">Das folgende Beispiel veranschaulicht eine Anwendungs definierte Funktion (enumeratefunc), die alle Ressourcen in einem Netzwerk auflistet.</span><span class="sxs-lookup"><span data-stu-id="74099-104">The following example illustrates an application-defined function (EnumerateFunc) that enumerates all the resources on a network.</span></span> <span data-ttu-id="74099-105">Im Beispiel wird **null** für den Zeiger auf die Struktur " [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) " angegeben, denn wenn " [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) " einen **null** -Zeiger empfängt, ruft er ein Handle an den Stamm des Netzwerks ab.</span><span class="sxs-lookup"><span data-stu-id="74099-105">The sample specifies **NULL** for the pointer to the [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure because when [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) receives a **NULL** pointer, it retrieves a handle to the root of the network.</span></span>

<span data-ttu-id="74099-106">Um mit der Enumeration einer Netzwerk Container Ressource zu beginnen, sollte Ihre Anwendung die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="74099-106">To begin the enumeration of a network container resource, your application should perform the following steps:</span></span>

1.  <span data-ttu-id="74099-107">Übergeben Sie die Adresse einer [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Struktur, die die Ressource darstellt, an die Funktion [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) .</span><span class="sxs-lookup"><span data-stu-id="74099-107">Pass the address of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure that represents the resource to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function.</span></span>
2.  <span data-ttu-id="74099-108">Weisen Sie einen Puffer zu, der groß genug ist, um das Array von [**artresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Strukturen aufzunehmen, die von der [**wnettenumschlag**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion zurückgegeben werden, sowie die Zeichen folgen, auf die ihre Elemente</span><span class="sxs-lookup"><span data-stu-id="74099-108">Allocate a buffer large enough to hold the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures that the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function returns, plus the strings to which their members point.</span></span>
3.  <span data-ttu-id="74099-109">Übergeben Sie das von [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) zurückgegebene Ressourcen Handle an die [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="74099-109">Pass the resource handle returned by [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) to the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function.</span></span>
4.  <span data-ttu-id="74099-110">Schließen Sie das Ressourcen handle, wenn es nicht mehr benötigt wird, indem Sie die [**wnetcloseenum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="74099-110">Close the resource handle when it is no longer needed by calling the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) function.</span></span>

<span data-ttu-id="74099-111">Sie können fortfahren, indem Sie eine Container Ressource auflisten, die im Array der von [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea)abgerufenen [**artresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Strukturen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="74099-111">You can continue enumerating a container resource described in the array of [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structures retrieved by [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea).</span></span> <span data-ttu-id="74099-112">Wenn der **dwusage** -Member der Struktur " **nettresource** " gleich dem ResourceUsage \_ -Container ist, übergeben Sie die Adresse der Struktur an die Funktion " [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) ", um den Container zu öffnen und die Enumeration fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="74099-112">If the **dwUsage** member of the **NETRESOURCE** structure is equal to RESOURCEUSAGE\_CONTAINER, pass the address of the structure to the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to open the container and continue the enumeration.</span></span> <span data-ttu-id="74099-113">Wenn **dwusage** gleich ResourceUsage \_ Connectable ist, kann die Anwendung die Adresse der Struktur an die [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) -Funktion oder die [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) -Funktion übergeben, um eine Verbindung mit der Ressource herzustellen.</span><span class="sxs-lookup"><span data-stu-id="74099-113">If **dwUsage** is equal to RESOURCEUSAGE\_CONNECTABLE, the application can pass the structure's address to the [**WNetAddConnection2**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection2a) function or the [**WNetAddConnection3**](/windows/win32/api/winnetwk/nf-winnetwk-wnetaddconnection3a) function to connect to the resource.</span></span>

<span data-ttu-id="74099-114">Zuerst Ruft das Beispiel die [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) -Funktion auf, um die-Enumeration zu starten.</span><span class="sxs-lookup"><span data-stu-id="74099-114">First the sample calls the [**WNetOpenEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetopenenuma) function to begin the enumeration.</span></span> <span data-ttu-id="74099-115">Das Beispiel ruft die [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) -Funktion auf, um den erforderlichen Puffer zuzuordnen, und ruft dann die [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) -Funktion auf, um den Pufferinhalt auf 0 (null) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="74099-115">The sample calls the [**GlobalAlloc**](/windows/desktop/api/winbase/nf-winbase-globalalloc) function to allocate the required buffer, and then calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to set the buffer contents to zero.</span></span> <span data-ttu-id="74099-116">Im Beispiel wird die [**wnettenumresource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) -Funktion aufgerufen, um die-Enumeration fortzusetzen.</span><span class="sxs-lookup"><span data-stu-id="74099-116">Then the sample calls the [**WNetEnumResource**](/windows/win32/api/winnetwk/nf-winnetwk-wnetenumresourcea) function to continue the enumeration.</span></span> <span data-ttu-id="74099-117">Immer wenn der **dwusage** -Member einer von **wnettenumresource** abgerufenen [**Struktur gleich**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) dem ResourceUsage \_ -Container ist, ruft die enumeratefunc-Funktion sich selbst rekursiv auf und verwendet einen Zeiger auf diese Struktur in dem Aufruf von **WNetOpenEnum**.</span><span class="sxs-lookup"><span data-stu-id="74099-117">Whenever the **dwUsage** member of a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure retrieved by **WNetEnumResource** is equal to RESOURCEUSAGE\_CONTAINER, the EnumerateFunc function calls itself recursively and uses a pointer to that structure in its call to **WNetOpenEnum**.</span></span> <span data-ttu-id="74099-118">Zum Schluss ruft das Beispiel die [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) -Funktion auf, um den zugeordneten Arbeitsspeicher freizugeben, und die [**wnetcloseenum-Klasse**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) zum Beenden der Enumeration.</span><span class="sxs-lookup"><span data-stu-id="74099-118">Finally, the sample calls the [**GlobalFree**](/windows/desktop/api/winbase/nf-winbase-globalfree) function to free the allocated memory, and the [**WNetCloseEnum**](/windows/win32/api/winnetwk/nf-winnetwk-wnetcloseenum) to end the enumeration.</span></span>


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



<span data-ttu-id="74099-119">Weitere Informationen zum Verwenden eines Anwendungs definierten Fehler Handlers finden Sie unter [Abrufen von Netzwerkfehlern](retrieving-network-errors.md).</span><span class="sxs-lookup"><span data-stu-id="74099-119">For more information about using an application-defined error handler, see [Retrieving Network Errors](retrieving-network-errors.md).</span></span>

 

 