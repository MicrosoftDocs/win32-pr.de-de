---
description: Die getipaddrtable-Funktion füllt einen Zeiger auf eine MIB \_ ipaddrtable-Struktur mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.
ms.assetid: f041cb37-926d-4eeb-835c-f8b9d5ee4d2e
title: Verwalten von IP-Adressen mit getipaddrtable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a3d94eb4de22a428e20a4cb0fdc8970d7f65fed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864875"
---
# <a name="managing-ip-addresses-using-getipaddrtable"></a><span data-ttu-id="dcca6-103">Verwalten von IP-Adressen mit getipaddrtable</span><span class="sxs-lookup"><span data-stu-id="dcca6-103">Managing IP Addresses Using GetIpAddrTable</span></span>

<span data-ttu-id="dcca6-104">Die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion füllt einen Zeiger auf eine [**MIB \_ ipaddrtable**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) -Struktur mit Informationen zu den aktuellen IP-Adressen, die dem System zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="dcca6-104">The [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function fills a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) structure with information about the current IP addresses associated with the system.</span></span>

<span data-ttu-id="dcca6-105">**So verwenden Sie "getipaddrtable"**</span><span class="sxs-lookup"><span data-stu-id="dcca6-105">**To use GetIpAddrTable**</span></span>

1.  <span data-ttu-id="dcca6-106">Deklarieren Sie einen Zeiger auf ein [**MIB \_ ipaddrtable**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) -Objekt namens *pipaddrtable* und ein **DWORD** -Objekt mit dem Namen *dwSize*.</span><span class="sxs-lookup"><span data-stu-id="dcca6-106">Declare a pointer to an [**MIB\_IPADDRTABLE**](/windows/win32/api/ipmib/ns-ipmib-mib_ipaddrtable) object called *pIPAddrTable*, and a **DWORD** object called *dwSize*.</span></span> <span data-ttu-id="dcca6-107">Diese Variablen werden als Parameter an die [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion übermittelt.</span><span class="sxs-lookup"><span data-stu-id="dcca6-107">These variables are passed as parameters to the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="dcca6-108">Erstellen Sie außerdem eine **DWORD** -Variable mit dem Namen *dwretval* (für die Fehlerüberprüfung verwendet).</span><span class="sxs-lookup"><span data-stu-id="dcca6-108">Also create a **DWORD** variable called *dwRetVal* (used for error checking).</span></span>
    ```C++
    MIB_IPADDRTABLE  *pIPAddrTable;
    DWORD            dwSize = 0;
    DWORD            dwRetVal;
    
    ```

    

2.  <span data-ttu-id="dcca6-109">Zuweisen von Speicher für die Struktur.</span><span class="sxs-lookup"><span data-stu-id="dcca6-109">Allocate memory for the structure.</span></span>
    > [!Note]  
    > <span data-ttu-id="dcca6-110">Die Größe von *dwSize* reicht nicht aus, um die Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dcca6-110">The size of *dwSize* is not sufficient to hold the information.</span></span> <span data-ttu-id="dcca6-111">Weitere Informationen finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="dcca6-111">See the next step.</span></span>

     

    ```C++
    pIPAddrTable = (MIB_IPADDRTABLE*) malloc( sizeof(MIB_IPADDRTABLE) );
    
    ```

    

3.  <span data-ttu-id="dcca6-112">Führen Sie einen anfänglichen Aufrufen von [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) aus, um die benötigte Größe in die *dwSize* -Variable zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="dcca6-112">Make an initial call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) to get the size needed into the *dwSize* variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="dcca6-113">Dieser Aufrufen der-Funktion soll fehlschlagen und wird verwendet, um sicherzustellen, dass die *dwSize* -Variable eine ausreichende Größe angibt, um alle an *pipaddrtable* zurückgegebenen Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dcca6-113">This call to the function is meant to fail, and is used to ensure that the *dwSize* variable specifies a size sufficient for holding all the information returned to *pIPAddrTable*.</span></span> <span data-ttu-id="dcca6-114">Dies ist ein gängiges Programmiermodell für Datenstrukturen und Funktionen dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="dcca6-114">This is a common programming model for data structures and functions of this type.</span></span>

     

    ```C++
    if (GetIpAddrTable(pIPAddrTable, &dwSize, 0) == ERROR_INSUFFICIENT_BUFFER) {
        free( pIPAddrTable );
        pIPAddrTable = (MIB_IPADDRTABLE *) malloc ( dwSize );
    }
    
    ```

    

4.  <span data-ttu-id="dcca6-115">Erstellen Sie einen zweiten Aufrufen von [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) mit allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable *dwretval* zurück (für eine erweiterte Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="dcca6-115">Make a second call to [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) with general error checking and return its value to the **DWORD** variable *dwRetVal* (for more advanced error checking).</span></span>
    ```C++
    if ( (dwRetVal = GetIpAddrTable( pIPAddrTable, &dwSize, 0 )) != NO_ERROR ) { 
        printf("GetIpAddrTable call failed with %d\n", dwRetVal);
    }
    
    ```

    

5.  <span data-ttu-id="dcca6-116">Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten aus der *pipaddrtable* -Datenstruktur zu.</span><span class="sxs-lookup"><span data-stu-id="dcca6-116">If the call was successful, access the data from the *pIPAddrTable* data structure.</span></span>
    ```C++
    printf("IP Address:         %ld\n", pIPAddrTable->table[0].dwAddr);
    printf("IP Mask:            %ld\n", pIPAddrTable->table[0].dwMask);
    printf("IF Index:           %ld\n", pIPAddrTable->table[0].dwIndex);
    printf("Broadcast Addr:     %ld\n", pIPAddrTable->table[0].dwBCastAddr);
    printf("Re-assembly size:   %ld\n", pIPAddrTable->table[0].dwReasmSize);
    
    ```

    

6.  <span data-ttu-id="dcca6-117">Gibt den für die *pipaddrtable* -Struktur zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="dcca6-117">Free any memory allocated for the *pIPAddrTable* structure.</span></span>
    ```C++
    if (pIPAddrTable)
            free(pIPAddrTable);
    
    ```

    

> [!Note]  
> <span data-ttu-id="dcca6-118">Die **DWORD** -Objekte *dwaddr* und *dwMask* werden als numerische Werte in der Host-Byte Reihenfolge und nicht in der netzwerkbyte Reihenfolge zurückgegeben</span><span class="sxs-lookup"><span data-stu-id="dcca6-118">The **DWORD** objects *dwAddr* and *dwMask* are returned as numerical values in host byte order, not network byte order.</span></span> <span data-ttu-id="dcca6-119">Diese Werte sind keine gepunkteten IP-Adressen.</span><span class="sxs-lookup"><span data-stu-id="dcca6-119">These values are not dotted IP addresses.</span></span>

 

<span data-ttu-id="dcca6-120">Nächster Schritt: [Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="dcca6-120">Next Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

<span data-ttu-id="dcca6-121">Vorheriger Schritt: [Verwalten von Schnittstellen mithilfe von getinterfakeinfo](managing-interfaces-using-getinterfaceinfo.md)</span><span class="sxs-lookup"><span data-stu-id="dcca6-121">Previous Step: [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)</span></span>

 

 
