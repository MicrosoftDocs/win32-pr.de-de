---
title: Abrufen von Informationen zu einer Netzwerkressource
description: Um den Netzwerkanbieter zu identifizieren, der Besitzer einer Ressource ist, kann eine Anwendung die wnetgetresourceinformation-Funktion wie im folgenden Codebeispiel veranschaulicht aufruft.
ms.assetid: 4bddb55c-181d-4c6f-bd92-9c27d6b894bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf21e48be540f5307fc1ebd2359aea7ff03cbe0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104101967"
---
# <a name="retrieving-information-about-a-network-resource"></a><span data-ttu-id="52f6c-103">Abrufen von Informationen zu einer Netzwerkressource</span><span class="sxs-lookup"><span data-stu-id="52f6c-103">Retrieving Information About a Network Resource</span></span>

<span data-ttu-id="52f6c-104">Um den Netzwerkanbieter zu identifizieren, der Besitzer einer Ressource ist, kann eine Anwendung die [**wnetgetresourceinformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) -Funktion wie im folgenden Codebeispiel veranschaulicht aufruft.</span><span class="sxs-lookup"><span data-stu-id="52f6c-104">To identify the network provider that owns a resource, an application can call the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, as illustrated in the following code sample.</span></span>

<span data-ttu-id="52f6c-105">Das folgende Beispiel ist eine Funktion (checkserver), die einen Servernamen als Parameter annimmt und Informationen zu diesem Server zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="52f6c-105">The following sample is a function (CheckServer) that takes a server name as a parameter and returns information about that server.</span></span> <span data-ttu-id="52f6c-106">Zuerst Ruft die Funktion die [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) -Funktion auf, um den Inhalt eines Speicherblocks auf 0 (null) zu initialisieren.</span><span class="sxs-lookup"><span data-stu-id="52f6c-106">First the function calls the [**ZeroMemory**](/previous-versions/windows/desktop/legacy/aa366920(v=vs.85)) function to initialize the contents of a block of memory to zero.</span></span> <span data-ttu-id="52f6c-107">Anschließend ruft das Beispiel die [**wnetgetresourceinformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) -Funktion auf und gibt einen Puffer an, der groß genug ist, um nur eine [**nettresource**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) -Struktur zu speichern.</span><span class="sxs-lookup"><span data-stu-id="52f6c-107">Then the sample calls the [**WNetGetResourceInformation**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetresourceinformationa) function, specifying a buffer large enough to hold only a [**NETRESOURCE**](/windows/desktop/api/Winnetwk/ns-winnetwk-netresourcea) structure.</span></span> <span data-ttu-id="52f6c-108">Die-Routine schließt die Fehler Verarbeitung ein, um den Fall zu behandeln, dass ein Puffer dieser Größe nicht ausreicht, um die Zeichen folgen variabler Länge zu speichern, auf die Elemente **der Struktur der Struktur der Struktur** zeigen.</span><span class="sxs-lookup"><span data-stu-id="52f6c-108">The routine includes error processing to handle the case when a buffer of this size is insufficient to hold the variable-length strings to which members of the **NETRESOURCE** structure point.</span></span> <span data-ttu-id="52f6c-109">Wenn dieser Fehler auftritt, ordnet das Beispiel ausreichend Arbeitsspeicher zu und ruft **wnetgetresourceinformation** erneut auf.</span><span class="sxs-lookup"><span data-stu-id="52f6c-109">If this error occurs, the sample allocates sufficient memory and calls **WNetGetResourceInformation** again.</span></span> <span data-ttu-id="52f6c-110">Schließlich gibt das Beispiel den zugewiesenen Speicher frei.</span><span class="sxs-lookup"><span data-stu-id="52f6c-110">Finally, the sample frees the allocated memory.</span></span>

<span data-ttu-id="52f6c-111">Beachten Sie, dass im Beispiel davon ausgegangen wird, dass der *pszserver* -Parameter auf einen Servernamen verweist, der von einem der Netzwerkanbieter auf dem lokalen Computer erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="52f6c-111">Note that the sample assumes that the *pszServer* parameter points to a server name that one of the network providers on the local computer recognizes.</span></span>


```C++
#include <Windows.h>
#include <Winnetwk.h >

// Need to link with Mpr.lib
#pragma comment(lib, "Mpr.lib")
//
// Verify a server on the network. 
//
DWORD
CheckServer( LPTSTR pszServer )
{  
    DWORD dwBufferSize = sizeof(NETRESOURCE);
    LPBYTE lpBuffer;                  // buffer
    NETRESOURCE nr;
    LPTSTR pszSystem = NULL;          // variable-length strings

    //
    // Set the block of memory to zero; then initialize
    // the NETRESOURCE structure. 
    //
    ZeroMemory(&nr, sizeof(nr));

    nr.dwScope       = RESOURCE_GLOBALNET;
    nr.dwType        = RESOURCETYPE_ANY;
    nr.lpRemoteName  = pszServer;

    //
    // First call the WNetGetResourceInformation function with 
    // memory allocated to hold only a NETRESOURCE structure. This 
    // method can succeed if all the NETRESOURCE pointers are NULL.
    // If the call fails because the buffer is too small, allocate
    // a larger buffer.
    //
    lpBuffer = (LPBYTE) malloc( dwBufferSize );
    if (lpBuffer == NULL) 
        return FALSE;

    while ( WNetGetResourceInformation(&nr, lpBuffer, &dwBufferSize, 
                &pszSystem) == ERROR_MORE_DATA)
    {
        lpBuffer = (LPBYTE) realloc(lpBuffer, dwBufferSize);
    }

    // Process the contents of the NETRESOURCE structure and the
    // variable-length strings in lpBuffer and set dwValue. When
    // finished, free the memory.

    free(lpBuffer);

    return TRUE;
}
```



 

 