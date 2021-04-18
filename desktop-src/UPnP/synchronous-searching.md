---
title: Synchrone Suche
description: Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge. Synchrone Suchvorgänge sind abgeschlossen und geben die Steuerung nur dann an die aufrufenden Anwendung zurück, nachdem alle verfügbaren Geräte gefunden wurden.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1890829dfe8386cd79627dde039264dc81e473c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340642"
---
# <a name="synchronous-searching"></a><span data-ttu-id="5fa51-104">Synchrone Suche</span><span class="sxs-lookup"><span data-stu-id="5fa51-104">Synchronous Searching</span></span>

<span data-ttu-id="5fa51-105">Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge.</span><span class="sxs-lookup"><span data-stu-id="5fa51-105">The Device Finder object enables both synchronous and asynchronous searches.</span></span> <span data-ttu-id="5fa51-106">Synchrone Suchvorgänge sind abgeschlossen und geben die Steuerung nur dann an die aufrufenden Anwendung zurück, nachdem alle verfügbaren Geräte gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="5fa51-106">Synchronous searches are completed and return control to the calling application only after all available devices are found.</span></span> <span data-ttu-id="5fa51-107">Um eine synchrone Suche auszuführen, verwenden Sie eine der synchronen Suchmethoden der [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="5fa51-107">To perform a synchronous search, use one of the synchronous search methods of the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface.</span></span>

> [!Note]  
> <span data-ttu-id="5fa51-108">Die Rückgabe synchroner Suchvorgänge dauert mindestens neun Sekunden.</span><span class="sxs-lookup"><span data-stu-id="5fa51-108">Synchronous searches take at least nine seconds to return.</span></span> <span data-ttu-id="5fa51-109">Die Verzögerung ist darauf zurückzuführen, dass die anfängliche UDP-Such Nachricht mehrmals gesendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="5fa51-109">The delay is caused because the initial UDP search message must be sent multiple times.</span></span> <span data-ttu-id="5fa51-110">Diese Duplizierung berücksichtigt die Unzuverlässigkeit des zugrunde liegenden Netzwerk Protokolls.</span><span class="sxs-lookup"><span data-stu-id="5fa51-110">This duplication accounts for the unreliability of the underlying network protocol.</span></span> <span data-ttu-id="5fa51-111">Synchrone Suchvorgänge eignen sich am besten für Befehlszeilen Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="5fa51-111">Synchronous searches are best for command-line interfaces.</span></span> <span data-ttu-id="5fa51-112">Sie werden nicht für grafische Benutzeroberflächen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5fa51-112">They are not recommended for graphical user interfaces.</span></span>

 

<span data-ttu-id="5fa51-113">Die [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode sucht nach Gerät oder Diensttyp.</span><span class="sxs-lookup"><span data-stu-id="5fa51-113">The [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method searches by device or service type.</span></span> <span data-ttu-id="5fa51-114">Diese Methode nimmt einen Typ-Uri als Eingabeparameter an und gibt eine Auflistung von Geräte Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="5fa51-114">This method takes a type URI as an input parameter and returns a collection of Device objects.</span></span> <span data-ttu-id="5fa51-115">Ein Geräte Objekt stellt ein einzelnes Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="5fa51-115">A Device object represents an individual device.</span></span>

<span data-ttu-id="5fa51-116">In den folgenden Beispielen wird veranschaulicht, wie eine synchrone Suche nach Geräten in VBScript ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5fa51-116">The following examples demonstrate how to perform a synchronous search for devices in VBScript.</span></span> <span data-ttu-id="5fa51-117">Jedes Skript verwendet [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), das mit dem Typ-Uri (Dienst-ID) für den Media Player-Gerätetyp, *urn: Schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*, aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="5fa51-117">Each script uses [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), called with the type URI (service ID) for the media player device type, *urn:schemas-upnp-org:device:mediaplayer.v1.00.00*.</span></span> <span data-ttu-id="5fa51-118">Die-Methode gibt eine Auflistung von Geräte Objekten zurück, die den gefundenen Media Player-Geräten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5fa51-118">The method returns a collection of Device objects that corresponds to media player devices that were found.</span></span> <span data-ttu-id="5fa51-119">Informationen zum Extrahieren einzelner Geräte Objekte aus einer Sammlung finden Sie unter [von synchronen Such Vorgängen zurückgegebene Geräte](device-collections-returned-by-synchronous-searches.md)Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="5fa51-119">For information on extracting individual device objects from a collection, see [Device Collections Returned By Synchronous Searches](device-collections-returned-by-synchronous-searches.md).</span></span>

## <a name="search-for-devices-by-type-in-vbscript"></a><span data-ttu-id="5fa51-120">Suchen nach Geräten nach Typ in VBScript</span><span class="sxs-lookup"><span data-stu-id="5fa51-120">Search for Devices by Type in VBScript</span></span>


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a><span data-ttu-id="5fa51-121">Suchen nach einem Gerät nach Typ in C++</span><span class="sxs-lookup"><span data-stu-id="5fa51-121">Search for Device by Type in C++</span></span>

<span data-ttu-id="5fa51-122">Im folgenden Beispiel wird eine synchrone Suche nach Media Player-Geräten mithilfe von C++ veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5fa51-122">The following example demonstrates a synchronous search for media player devices using C++.</span></span> <span data-ttu-id="5fa51-123">Die Funktion nimmt einen Zeiger auf die [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle als Eingabe an und gibt den [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Schnittstellen Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="5fa51-123">The function takes a pointer to the [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) interface as input, and returns the [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) interface pointer.</span></span>

<span data-ttu-id="5fa51-124">Das Beispiel ordnet zuerst einen **BSTR** zu, der den Gerätetyp-URI darstellt, und übergibt ihn dann an die [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode.</span><span class="sxs-lookup"><span data-stu-id="5fa51-124">The example first allocates a **BSTR** to represent the device type URI and then passes this to the [**IUPnPDeviceFinder::FindByType**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) method.</span></span> <span data-ttu-id="5fa51-125">Außerdem wird die Adresse eines lokalen [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Zeigers in dem Puffer übergeben, in dem die-Methode die gefundene Geräte Auflistung speichert.</span><span class="sxs-lookup"><span data-stu-id="5fa51-125">It also passes the address of a local [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) pointer in the buffer in which the method then stores the collection of devices found.</span></span> <span data-ttu-id="5fa51-126">Wenn der Funktions Aufrufvorgang erfolgreich ist, wird der Zeiger auf diese Auflistung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5fa51-126">If the function call is successful, it returns the pointer to this collection.</span></span>


```C++
#include <windows.h>
#include <upnp.h>
#include <stdio.h>

#pragma comment(lib, "oleaut32.lib")

IUPnPDevices *FindMediaPlayerDevices(IUPnPDeviceFinder *pDeviceFinder)
{
    HRESULT         hr = S_OK;
    IUPnPDevices    * pFoundDevices = NULL;
    BSTR            bstrTypeURI = NULL;

    bstrTypeURI = 
        SysAllocString(L"urn:schemas-upnp-org:device:multidisk-dvd");

    if (bstrTypeURI)
    {
        hr = pDeviceFinder->FindByType(bstrTypeURI, 
                                       0,
                                       &pFoundDevices);

        if (SUCCEEDED(hr))
        {
            wprintf(L"FindMediaPlayerDevices(): "
                    L"Search returned successfully\n");
        }
        else
        {
            fwprintf(stderr, L"FindMediaPlayerDevices(): "
                     L"FindByType search failed - returned "
                     L"HRESULT 0x%x\n",
                     hr);
            pFoundDevices = NULL;
        }
        SysFreeString(bstrTypeURI);
    }
    else
    {
        fwprintf(stderr, L"FindMediaPlayerDevices(): "
                 L"Could not allocate BSTR for type URI\n");
    }

    return pFoundDevices;
}
```



 

 




