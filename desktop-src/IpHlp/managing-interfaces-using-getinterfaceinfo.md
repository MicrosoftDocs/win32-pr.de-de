---
description: Die getinterfakeinfo-Funktion füllt einen Zeiger auf eine IP- \_ Schnittstellen \_ Informationsstruktur mit Informationen zu den dem System zugeordneten Schnittstellen.
ms.assetid: 0cc18e14-7329-49b0-bb07-912fa403db46
title: Verwalten von Schnittstellen mithilfe von getinterfacetten Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39a8ad420f8a2d4fdbacc2bf01e65f5d9fbc9d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354460"
---
# <a name="managing-interfaces-using-getinterfaceinfo"></a><span data-ttu-id="70f61-103">Verwalten von Schnittstellen mithilfe von getinterfacetten Info</span><span class="sxs-lookup"><span data-stu-id="70f61-103">Managing Interfaces Using GetInterfaceInfo</span></span>

<span data-ttu-id="70f61-104">Die [**getinterfakeinfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) -Funktion füllt einen Zeiger auf eine [**IP- \_ Schnittstellen \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) Informationsstruktur mit Informationen zu den dem System zugeordneten Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="70f61-104">The [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) function fills a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) structure with information about the interfaces associated with the system.</span></span>

<span data-ttu-id="70f61-105">**So verwenden Sie getinterfacetten Info**</span><span class="sxs-lookup"><span data-stu-id="70f61-105">**To use GetInterfaceInfo**</span></span>

1.  <span data-ttu-id="70f61-106">Deklarieren Sie einen Zeiger auf ein [**IP- \_ Schnittstellen \_ Info**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) Objekt mit `pInfo` dem Namen und ein **ulong** -Objekt mit dem Namen `ulOutBufLen` .</span><span class="sxs-lookup"><span data-stu-id="70f61-106">Declare a pointer to an [**IP\_INTERFACE\_INFO**](/windows/desktop/api/Ipexport/ns-ipexport-ip_interface_info) object called `pInfo`, and a **ULONG** object called `ulOutBufLen`.</span></span> <span data-ttu-id="70f61-107">Deklarieren Sie auch ein **DWORD** -Objekt mit dem Namen `dwRetVal` (für die Fehlerüberprüfung verwendet).</span><span class="sxs-lookup"><span data-stu-id="70f61-107">Also declare a **DWORD** object called `dwRetVal` (used for error checking).</span></span>
    ```C++
        ULONG               ulOutBufLen;
        DWORD               dwRetVal;
        unsigned int       i;

        IP_INTERFACE_INFO*  pInterfaceInfo;
    ```

    

2.  <span data-ttu-id="70f61-108">Zuweisen von Arbeitsspeicher für die Strukturen.</span><span class="sxs-lookup"><span data-stu-id="70f61-108">Allocate memory for the structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="70f61-109">Die Größe von `ulOutBufLen` reicht nicht aus, um die Informationen zu speichern.</span><span class="sxs-lookup"><span data-stu-id="70f61-109">The size of `ulOutBufLen` is not sufficient to hold the information.</span></span> <span data-ttu-id="70f61-110">Weitere Informationen finden Sie im nächsten Schritt.</span><span class="sxs-lookup"><span data-stu-id="70f61-110">See the next step.</span></span>

     

    ```C++
        pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(sizeof (IP_INTERFACE_INFO));
        ulOutBufLen = sizeof(IP_INTERFACE_INFO);
    
    ```

    

3.  <span data-ttu-id="70f61-111">Erstellen Sie zunächst [**getinterfacetten**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) Info, um die benötigte Größe in der `ulOutBufLen` Variablen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="70f61-111">Make an initial call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) to get the size needed into the `ulOutBufLen` variable.</span></span>
    > [!Note]  
    > <span data-ttu-id="70f61-112">Dieser Aufrufe der-Funktion soll fehlschlagen, und wird verwendet, um sicherzustellen, dass die `ulOutBufLen` Variable eine ausreichende Größe für alle Informationen angibt, die an zurückgegeben werden `pInfo` .</span><span class="sxs-lookup"><span data-stu-id="70f61-112">This call to the function is meant to fail, and is used to ensure that the `ulOutBufLen` variable specifies a size sufficient for holding all the information returned to `pInfo`.</span></span> <span data-ttu-id="70f61-113">Dies ist ein gängiges Programmiermodell im IP-Hilfsprogramm für Datenstrukturen und Funktionen dieses Typs.</span><span class="sxs-lookup"><span data-stu-id="70f61-113">This is a common programming model in IP Helper for data structures and functions of this type.</span></span>

     

    ```C++
        if (GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen) ==
            ERROR_INSUFFICIENT_BUFFER) {
            free(pInterfaceInfo);
            pInterfaceInfo = (IP_INTERFACE_INFO *) malloc(ulOutBufLen);
        }
    ```

    

4.  <span data-ttu-id="70f61-114">Erstellen Sie einen zweiten get-Befehl für " [**getinterfacetten Info**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) " mit allgemeiner Fehlerüberprüfung, und geben Sie den Wert an die **DWORD** -Variable zurück `dwRetVal` (für eine erweiterte Fehlerüberprüfung).</span><span class="sxs-lookup"><span data-stu-id="70f61-114">Make a second call to [**GetInterfaceInfo**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getinterfaceinfo) with general error checking and return its value to the **DWORD** variable `dwRetVal` (for more advanced error checking).</span></span>
    ```C++
        if ((dwRetVal = GetInterfaceInfo(pInterfaceInfo, &ulOutBufLen)) != NO_ERROR) {
            printf("  GetInterfaceInfo failed with error: %d\n", dwRetVal);
        }
    ```

    

5.  <span data-ttu-id="70f61-115">Wenn der-Befehl erfolgreich ausgeführt wurde, greifen Sie auf die Daten aus der `pInfo` Datenstruktur zu.</span><span class="sxs-lookup"><span data-stu-id="70f61-115">If the call was successful, access the data from the `pInfo` data structure.</span></span>

    ```C++
            printf("  GetInterfaceInfo succeeded.\n");

            printf("  Num Adapters: %ld\n\n", pInterfaceInfo->NumAdapters);
            for (i = 0; i < (unsigned int) pInterfaceInfo->NumAdapters; i++) {
                printf("  Adapter Index[%d]: %ld\n", i,
                       pInterfaceInfo->Adapter[i].Index);
                printf("  Adapter Name[%d]:  %ws\n\n", i,
                       pInterfaceInfo->Adapter[i].Name);
            }
        }
    ```

    

    > [!Note]  
    > <span data-ttu-id="70f61-116">Das% WS in der ersten Zeile bezeichnet eine Breite Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="70f61-116">The %ws in the first line denotes a wide string.</span></span> <span data-ttu-id="70f61-117">Dies wird verwendet, da das **namens** Attribut der [**IP- \_ Adapter \_ Index \_**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) Struktur `Adapter` ein **WCHAR**-Zeichen ist, bei dem es sich um eine Unicode-Zeichenfolge handelt.</span><span class="sxs-lookup"><span data-stu-id="70f61-117">This is used because the **Name** attribute of the [**IP\_ADAPTER\_INDEX\_MAP**](/windows/desktop/api/Ipexport/ns-ipexport-ip_adapter_index_map) structure `Adapter` is a **WCHAR**, which is a Unicode string.</span></span>

     

6.  <span data-ttu-id="70f61-118">Gibt den für die *pinfo* -Struktur zugeordneten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="70f61-118">Free any memory allocated for the *pInfo* structure.</span></span>
    ```C++
        if (pInterfaceInfo) {
            free(pInterfaceInfo);
            pInterfaceInfo = NULL;
        }
    ```

    

<span data-ttu-id="70f61-119">Nächster Schritt: [Verwalten von IP-Adressen mit getipaddrtable](managing-ip-addresses-using-getipaddrtable.md)</span><span class="sxs-lookup"><span data-stu-id="70f61-119">Next Step: [Managing IP Addresses Using GetIpAddrTable](managing-ip-addresses-using-getipaddrtable.md)</span></span>

<span data-ttu-id="70f61-120">Vorheriger Schritt: [Verwalten von Netzwerkadaptern mit getadaptersinfo](managing-network-adapters-using-getadaptersinfo.md)</span><span class="sxs-lookup"><span data-stu-id="70f61-120">Previous Step: [Managing Network Adapters Using GetAdaptersInfo](managing-network-adapters-using-getadaptersinfo.md)</span></span>

 

 



