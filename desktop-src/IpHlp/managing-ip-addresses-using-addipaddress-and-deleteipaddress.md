---
title: Verwalten von IP-Adressen mit addipaddress, deleteipaddress
description: Die addipaddress-Funktion fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu.
ms.assetid: 71cf6b4d-192c-4b2a-b534-be0b3da552f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 259a18effd95acaa6c0773c07e44088e448f48d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106351668"
---
# <a name="manage-ip-addresses-with-addipaddress-deleteipaddress"></a><span data-ttu-id="b598d-103">Verwalten von IP-Adressen mit addipaddress, deleteipaddress</span><span class="sxs-lookup"><span data-stu-id="b598d-103">Manage IP addresses with AddIPAddress, DeleteIPAddress</span></span>

<span data-ttu-id="b598d-104">Die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion fügt dem angegebenen Adapter die angegebene IPv4-Adresse hinzu.</span><span class="sxs-lookup"><span data-stu-id="b598d-104">The [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function adds the specified IPv4 address to the specified adapter.</span></span> <span data-ttu-id="b598d-105">Die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion löscht die angegebene IPv4-Adresse aus dem angegebenen Adapter.</span><span class="sxs-lookup"><span data-stu-id="b598d-105">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function deletes the specified IPv4 address from the specified adapter.</span></span> <span data-ttu-id="b598d-106">Diese Funktionen können zum Hinzufügen und Löschen von IPv4-Adressen zu einem Netzwerkadapter verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b598d-106">These functions can be used to add and delete IPv4 addresses to a network adapter.</span></span>

<span data-ttu-id="b598d-107">Eine von der [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion hinzugefügte IPv4-Adresse ist nicht persistent.</span><span class="sxs-lookup"><span data-stu-id="b598d-107">An IPv4 address added by the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function is not persistent.</span></span> <span data-ttu-id="b598d-108">Die IPv4-Adresse ist nur so lange vorhanden, wie das Adapter Objekt vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b598d-108">The IPv4 address exists only as long as the adapter object exists.</span></span> <span data-ttu-id="b598d-109">Durch einen Neustart des Computers wird die IPv4-Adresse zerstört, da die Netzwerkschnittstellenkarte (NIC) manuell zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b598d-109">Restarting the computer destroys the IPv4 address, as does manually resetting the network interface card (NIC).</span></span>

<span data-ttu-id="b598d-110">Nachdem [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) erfolgreich aufgerufen wurde, wird DHCP für die hinzugefügte IP-Adresse deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b598d-110">After [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) has been called successfully, DHCP will be disabled for the IP address that was added.</span></span> <span data-ttu-id="b598d-111">Daher sind Funktionen wie [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), die DHCP aktivieren müssen, für die hinzugefügte IP-Adresse nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="b598d-111">Therefore, functions such as [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress), which require DHCP to be enabled, will not be functional on the added IP address.</span></span> <span data-ttu-id="b598d-112">Die [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion kann verwendet werden, um die hinzugefügte IPv4-Adresse zu löschen.</span><span class="sxs-lookup"><span data-stu-id="b598d-112">The [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function can be used to delete the added IPv4 address.</span></span>

> [!Note]  
> <span data-ttu-id="b598d-113">Gruppenrichtlinien, Unternehmensrichtlinien und andere Einschränkungen im Netzwerk verhindern möglicherweise, dass diese Funktionen erfolgreich abgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="b598d-113">Group policies, enterprise policies, and other restrictions on the network may prevent these functions from completing successfully.</span></span> <span data-ttu-id="b598d-114">Stellen Sie sicher, dass die Anwendung über die erforderlichen Netzwerk Berechtigungen verfügt, bevor Sie versuchen, diese Funktionen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b598d-114">Ensure that the application has the necessary network permissions before attempting to use these functions.</span></span>

 

<span data-ttu-id="b598d-115">**So verwenden Sie addipaddress**</span><span class="sxs-lookup"><span data-stu-id="b598d-115">**To use AddIPAddress**</span></span>

1.  <span data-ttu-id="b598d-116">Deklarieren Sie **ulong** `NTEContext` -Variablen `NTEInstance` mit dem Namen und, beide werden auf NULL initialisiert.</span><span class="sxs-lookup"><span data-stu-id="b598d-116">Declare **ULONG** variables named `NTEContext` and `NTEInstance`, both initialized to zero.</span></span>
    > [!Note]  
    > <span data-ttu-id="b598d-117">Die `NTEContext` -Variable ist der einzige Parameter der [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion. zum Löschen der hinzugefügten IP-Adresse `NTEContext` muss gespeichert und unverändert sein.</span><span class="sxs-lookup"><span data-stu-id="b598d-117">The `NTEContext` variable is the only parameter to the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function; to delete the IP address that is added, `NTEContext` must be stored and unchanged.</span></span>

     

    ```C++
        ULONG NTEContext = 0;
        ULONG NTEInstance = 0;
    
    ```

    

    > [!Note]  

     

2.  <span data-ttu-id="b598d-118">Deklarieren Sie Variablen für die ipaddr-und ipmask-Strukturen mit den Namen `iaIPAddress` `iaIPMask` bzw..</span><span class="sxs-lookup"><span data-stu-id="b598d-118">Declare variables for the IPAddr and IPMask structures named `iaIPAddress` and `iaIPMask`, respectively.</span></span> <span data-ttu-id="b598d-119">Diese Werte sind einfach ganze Zahlen ohne Vorzeichen.</span><span class="sxs-lookup"><span data-stu-id="b598d-119">These values are simply unsigned integers.</span></span> <span data-ttu-id="b598d-120">Initialisieren `iaIPAddress` Sie die `iaIPMask` Variablen und mithilfe der Funktion " [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) ".</span><span class="sxs-lookup"><span data-stu-id="b598d-120">Initialize the `iaIPAddress` and `iaIPMask` variables using the [**inet\_addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) function.</span></span>
    ```C++
    UINT iaIPAddress;
    UINT iaIPMask;

    iaIPAddress = inet_addr("192.168.0.5");
    iaIPMask    = inet_addr("255.255.255.0");
    ```

    

3.  <span data-ttu-id="b598d-121">Ruft die [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) -Funktion auf, um die IPv4-Adresse hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b598d-121">Call the [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) function to add the IPv4 address.</span></span> <span data-ttu-id="b598d-122">Überprüfen Sie, ob Fehler vorliegen, und geben Sie den Fehlerwert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="b598d-122">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = AddIPAddress(iaIPAddress, iaIPMask, pIPAddrTable->table[0].dwIndex, 
                                 &NTEContext, &NTEInstance);
    if (dwRetVal != NO_ERROR) {
        printf("AddIPAddress call failed with %d\n", dwRetVal);
    }
    ```

    

    > [!Note]  
    > <span data-ttu-id="b598d-123">Der dritte Parameter ist der Adapter Index, der durch Aufrufen der [**getipaddrtable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) -Funktion abgerufen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b598d-123">The third parameter is the adapter index, which can be obtained by calling the [**GetIpAddrTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipaddrtable) function.</span></span> <span data-ttu-id="b598d-124">Es wird davon ausgegangen, dass die von dieser Funktion zurückgegebene Variable den Namen hat `pIPAddrTable` .</span><span class="sxs-lookup"><span data-stu-id="b598d-124">It is assumed that the variable returned by this function is named `pIPAddrTable`.</span></span> <span data-ttu-id="b598d-125">Hilfe zur **getipaddrtable** -Funktion finden Sie unter [Verwalten der IP-Adresse mithilfe von getipaddrtable](managing-ip-addresses-using-getipaddrtable.md).</span><span class="sxs-lookup"><span data-stu-id="b598d-125">For help with the **GetIpAddrTable** function, see [Managing IP Address Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md).</span></span>

     

<span data-ttu-id="b598d-126">**So verwenden Sie deleteipaddress**</span><span class="sxs-lookup"><span data-stu-id="b598d-126">**To use DeleteIpAddress**</span></span>

-   <span data-ttu-id="b598d-127">Aufrufen der [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) -Funktion, wobei die `NTEContext` Variable als Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="b598d-127">Call the [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress) function, passing the `NTEContext` variable as its parameter.</span></span> <span data-ttu-id="b598d-128">Überprüfen Sie, ob Fehler vorliegen, und geben Sie den Fehlerwert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="b598d-128">Check for errors and return the error value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    dwRetVal = DeleteIPAddress(NTEContext);
    if (dwRetVal != NO_ERROR) {
            printf("\tDeleteIPAddress failed with error: %d\n", dwRetVal);
    } 
    ```

    

> [!Note]  
> <span data-ttu-id="b598d-129">Um [**deleteipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress)zu verwenden, muss [**addipaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) zuerst aufgerufen werden, um das Handle zu erhalten `NTEContext` .</span><span class="sxs-lookup"><span data-stu-id="b598d-129">To use [**DeleteIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipaddress), [**AddIPAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-addipaddress) must first be called to get the handle `NTEContext`.</span></span> <span data-ttu-id="b598d-130">Bei der vorherigen Prozedur wird davon ausgegangen, dass **addipaddress** bereits irgendwo im Code aufgerufen wurde und `NTEContext` gespeichert wurde und unbeschädigt ist.</span><span class="sxs-lookup"><span data-stu-id="b598d-130">The previous procedure assumes that **AddIPAddress** has already been called somewhere in the code, and `NTEContext` has been saved and remains uncorrupted.</span></span>

 

<span data-ttu-id="b598d-131">Nächster Schritt: [Abrufen von Informationen mithilfe von GetIpStatistics](retrieving-information-using-getipstatistics.md)</span><span class="sxs-lookup"><span data-stu-id="b598d-131">Next Step: [Retrieving Information Using GetIpStatistics](retrieving-information-using-getipstatistics.md)</span></span>

<span data-ttu-id="b598d-132">Vorheriger Schritt: [Verwalten von DHCP-Leases mithilfe von ipreleaseaddress und iprenewaddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span><span class="sxs-lookup"><span data-stu-id="b598d-132">Previous Step: [Managing DHCP Leases Using IpReleaseAddress and IpRenewAddress](managing-dhcp-leases-using-ipreleaseaddress-and-iprenewaddress.md)</span></span>

 

 
