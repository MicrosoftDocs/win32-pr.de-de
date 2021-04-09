---
title: Verwalten von DHCP-Leases mit ipreleaseaddress, iprenewaddress
description: Die Funktionen ipreleaseaddress und iprenewaddress werden zum Freigeben und erneuern der aktuellen DHCP-Lease (Dynamic Host Configuration Protocol) verwendet.
ms.assetid: 0ed699dd-0bfb-4581-900d-7f5bc1e8acff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8a450d5e9a54fd4818f01bdc1eb7893609261ab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862439"
---
# <a name="manage-dhcp-leases-with-ipreleaseaddress-iprenewaddress"></a><span data-ttu-id="5dc01-103">Verwalten von DHCP-Leases mit ipreleaseaddress, iprenewaddress</span><span class="sxs-lookup"><span data-stu-id="5dc01-103">Manage DHCP leases with IpReleaseAddress, IpRenewAddress</span></span>

<span data-ttu-id="5dc01-104">Die Funktionen [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) und [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) werden zum Freigeben und erneuern der aktuellen DHCP-Lease (Dynamic Host Configuration Protocol) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5dc01-104">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions are used to release and renew the current Dynamic Host Configuration Protocol (DHCP) lease.</span></span> <span data-ttu-id="5dc01-105">Die **ipreleaseaddress** -Funktion gibt eine IPv4-Adresse frei, die zuvor über DHCP abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5dc01-105">The **IpReleaseAddress** function releases an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="5dc01-106">Die **iprenewaddress** -Funktion erneuert eine Lease für eine IPv4-Adresse, die zuvor über DHCP abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="5dc01-106">The **IpRenewAddress** function renews a lease on an IPv4 address previously obtained through DHCP.</span></span> <span data-ttu-id="5dc01-107">Es ist üblich, diese beiden Funktionen gemeinsam zu verwenden, zuerst die Lease mit einem **ipreleaseaddress**-Befehl freizugeben und dann die Lease mit einem-Rückruf der **iprenewaddress** -Funktion zu erneuern.</span><span class="sxs-lookup"><span data-stu-id="5dc01-107">It is common to use these two functions together, first releasing the lease with a call to **IpReleaseAddress**, and then renewing the lease with a call to the **IpRenewAddress** function.</span></span>

<span data-ttu-id="5dc01-108">Wenn ein DHCP-Client zuvor eine DHCP-Lease abgerufen hat und [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) vor der [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion nicht aufgerufen wird, wird die DHCP-Client Anforderung an den DHCP-Server gesendet, der die anfängliche DHCP-Lease ausgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5dc01-108">When a DHCP client has previously obtained a DHCP lease and [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) is not called before the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, the DHCP client request is sent to the DHCP server that issued the initial DHCP lease.</span></span> <span data-ttu-id="5dc01-109">Dieser DHCP-Server ist möglicherweise nicht verfügbar, oder die DHCP-Anforderung schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="5dc01-109">This DHCP server may not available or the DHCP request may fail.</span></span> <span data-ttu-id="5dc01-110">Wenn ein Host zuvor eine DHCP-Lease abgerufen hat und **ipreleaseaddress** vor der **iprenewaddress** -Funktion aufgerufen wird, gibt der DHCP-Client zunächst die erhaltene IP-Adresse frei und sendet eine DHCP-Client Anforderung für eine Antwort von einem beliebigen verfügbaren DHCP-Server.</span><span class="sxs-lookup"><span data-stu-id="5dc01-110">When a host has previously obtained a DHCP lease and **IpReleaseAddress** is called before the **IpRenewAddress** function, the DHCP client first releases the IP address obtained and sends a DHCP client request for a response from any available DHCP server.</span></span>

> [!Note]  
> <span data-ttu-id="5dc01-111">Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion und die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion erfordern, dass DHCP ordnungsgemäß ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5dc01-111">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) and [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) functions require that DHCP be enabled to perform correctly.</span></span>

 

<span data-ttu-id="5dc01-112">Die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion nimmt einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_ Struktur-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur als einzigen Parameter an.</span><span class="sxs-lookup"><span data-stu-id="5dc01-112">The [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function takes a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure as its only parameter.</span></span> <span data-ttu-id="5dc01-113">Rufen Sie zum Abrufen dieses Parameters zuerst [**getinterfacetten Info**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo)auf.</span><span class="sxs-lookup"><span data-stu-id="5dc01-113">To obtain this parameter, first call [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo).</span></span> <span data-ttu-id="5dc01-114">Hilfe zur Funktion **getinterfacetten** Info finden Sie unter Verwalten von [Schnittstellen mithilfe von getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info.</span><span class="sxs-lookup"><span data-stu-id="5dc01-114">For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md).</span></span>

<span data-ttu-id="5dc01-115">**So verwenden Sie ipreleaseaddress**</span><span class="sxs-lookup"><span data-stu-id="5dc01-115">**To use IpReleaseAddress**</span></span>

1.  <span data-ttu-id="5dc01-116">Rufen Sie mithilfe der [**getinterfaceinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="5dc01-116">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="5dc01-117">(Hilfe zur getinterfacetten-Funktion finden Sie unter Verwalten von [Schnittstellen mit getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info).</span><span class="sxs-lookup"><span data-stu-id="5dc01-117">(For help with the GetInterfaceInfo function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="5dc01-118">Erstellen Sie ein **DWORD** -Objekt `dwRetVal` (für die Fehlerüberprüfung verwendet).</span><span class="sxs-lookup"><span data-stu-id="5dc01-118">Create a **DWORD** object `dwRetVal` (used for error checking).</span></span> <span data-ttu-id="5dc01-119">Es wird davon ausgegangen, dass die von **getinterfacetten Info** zurückgegebene Variable aufgerufen wird `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="5dc01-119">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="5dc01-120">Wenn DHCP aktiviert ist, rufen Sie die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion auf, und übergeben Sie dabei die [**IP- \_ Adapter \_ Index \_ map-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Variable `Adapter` als Parameter.</span><span class="sxs-lookup"><span data-stu-id="5dc01-120">If DHCP is enabled, call the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="5dc01-121">Überprüfen Sie, ob allgemeine Fehler auftreten, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="5dc01-121">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    > [!Note]  
    > <span data-ttu-id="5dc01-122">Die [**getadaptersinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) -Funktion gibt einen Parameter zurück, der verwendet werden kann, um zu überprüfen, ob DHCP aktiviert ist, bevor diese Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="5dc01-122">The [**GetAdaptersInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getadaptersinfo) function returns a parameter that can be used to check whether DHCP is enabled before calling these functions.</span></span> <span data-ttu-id="5dc01-123">Hilfe zu **getadaptersinfo** finden Sie unter [Verwalten von Netzwerkadaptern mit "getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)".</span><span class="sxs-lookup"><span data-stu-id="5dc01-123">For help with **GetAdaptersInfo**, see [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md).</span></span>

     

    ```C++
    if ((dwRetVal = IpReleaseAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Release succeeded.\n");
    }
    
    ```

    

> [!Note]  
> <span data-ttu-id="5dc01-124">Es ist üblich, diese beiden Funktionen gemeinsam zu verwenden, die [**ipreleaseaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) -Funktion aufzurufen und dann die [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion aufzurufen und die gleiche Struktur wie der Parameter an beide Funktionen zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="5dc01-124">It is common to use these two functions together, calling the [**IpReleaseAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-ipreleaseaddress) function and then calling the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the same structure as the parameter to both functions.</span></span> <span data-ttu-id="5dc01-125">Bei der folgenden Prozedur wird davon ausgegangen, dass die Funktionen nicht gleichzeitig verwendet werden. Wenn die Funktionen jedoch gleichzeitig verwendet werden, überspringen Sie Schritt 1.</span><span class="sxs-lookup"><span data-stu-id="5dc01-125">The following procedure assumes that the functions are not used together; however, if the functions are used together, skip step 1.</span></span>

 

<span data-ttu-id="5dc01-126">**So verwenden Sie iprenewaddress**</span><span class="sxs-lookup"><span data-stu-id="5dc01-126">**To use IpRenewAddress**</span></span>

1.  <span data-ttu-id="5dc01-127">Rufen Sie mithilfe der [**getinterfaceinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion einen Zeiger auf eine [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="5dc01-127">Obtain a pointer to an [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure using the [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function.</span></span> <span data-ttu-id="5dc01-128">(Hilfe zur **getinterfacetten** -Funktion finden Sie unter Verwalten von [Schnittstellen mit getinterfacetten](managing-interfaces-using-getinterfaceinfo.md)Info).</span><span class="sxs-lookup"><span data-stu-id="5dc01-128">(For help with the **GetInterfaceInfo** function, see [Managing Interfaces Using GetInterfaceInfo](managing-interfaces-using-getinterfaceinfo.md)).</span></span> <span data-ttu-id="5dc01-129">Deklarieren Sie ein **DWORD** -Objekt `dwRetVal` (für die Fehlerüberprüfung verwendet), wenn diese Variable nicht deklariert wurde.</span><span class="sxs-lookup"><span data-stu-id="5dc01-129">Declare a **DWORD** object `dwRetVal` (used for error checking) if this variable has not been declared.</span></span> <span data-ttu-id="5dc01-130">Es wird davon ausgegangen, dass die von **getinterfacetten Info** zurückgegebene Variable aufgerufen wird `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="5dc01-130">It is assumed that the variable returned by **GetInterfaceInfo** is called `pInfo`.</span></span>
    ```C++
    DWORD dwRetVal;
    
    ```

    

2.  <span data-ttu-id="5dc01-131">Aufrufen der [**iprenewaddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) -Funktion, wobei die [**IP- \_ Adapter \_ Index \_ map-**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Variable `Adapter` als Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5dc01-131">Call the [**IpRenewAddress**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-iprenewaddress) function, passing the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) variable `Adapter` as its parameter.</span></span> <span data-ttu-id="5dc01-132">Überprüfen Sie, ob allgemeine Fehler auftreten, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine umfassendere Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="5dc01-132">Check for general errors and return its value to the **DWORD** variable `dwRetVal` (for more extensive error checking).</span></span>
    ```C++
    if ((dwRetVal = IpRenewAddress(&pInfo->Adapter[0])) == NO_ERROR) {
        printf("Ip Renew succeeded.\n");
    }
    ```

    

<span data-ttu-id="5dc01-133">Nächster Schritt: [Verwalten von IP-Adressen mit addipaddress und deleteipaddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span><span class="sxs-lookup"><span data-stu-id="5dc01-133">Next Step: [Managing IP Addresses Using AddIPAddress and DeleteIPAddress](managing-ip-addresses-using-addipaddress-and-deleteipaddress.md)</span></span>

<span data-ttu-id="5dc01-134">Vorheriger Schritt: [Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="5dc01-134">Previous Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

 

 



