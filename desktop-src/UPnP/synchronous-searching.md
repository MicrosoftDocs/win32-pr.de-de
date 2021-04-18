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
# <a name="synchronous-searching"></a>Synchrone Suche

Das Device Finder-Objekt ermöglicht synchrone und asynchrone Suchvorgänge. Synchrone Suchvorgänge sind abgeschlossen und geben die Steuerung nur dann an die aufrufenden Anwendung zurück, nachdem alle verfügbaren Geräte gefunden wurden. Um eine synchrone Suche auszuführen, verwenden Sie eine der synchronen Suchmethoden der [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle.

> [!Note]  
> Die Rückgabe synchroner Suchvorgänge dauert mindestens neun Sekunden. Die Verzögerung ist darauf zurückzuführen, dass die anfängliche UDP-Such Nachricht mehrmals gesendet werden muss. Diese Duplizierung berücksichtigt die Unzuverlässigkeit des zugrunde liegenden Netzwerk Protokolls. Synchrone Suchvorgänge eignen sich am besten für Befehlszeilen Schnittstellen. Sie werden nicht für grafische Benutzeroberflächen empfohlen.

 

Die [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode sucht nach Gerät oder Diensttyp. Diese Methode nimmt einen Typ-Uri als Eingabeparameter an und gibt eine Auflistung von Geräte Objekten zurück. Ein Geräte Objekt stellt ein einzelnes Gerät dar.

In den folgenden Beispielen wird veranschaulicht, wie eine synchrone Suche nach Geräten in VBScript ausgeführt wird. Jedes Skript verwendet [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype), das mit dem Typ-Uri (Dienst-ID) für den Media Player-Gerätetyp, *urn: Schemas-UPnP-org: Device: MediaPlayer. v 1.00.00*, aufgerufen wird. Die-Methode gibt eine Auflistung von Geräte Objekten zurück, die den gefundenen Media Player-Geräten entsprechen. Informationen zum Extrahieren einzelner Geräte Objekte aus einer Sammlung finden Sie unter [von synchronen Such Vorgängen zurückgegebene Geräte](device-collections-returned-by-synchronous-searches.md)Auflistungen.

## <a name="search-for-devices-by-type-in-vbscript"></a>Suchen nach Geräten nach Typ in VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Suchen nach einem Gerät nach Typ in C++

Im folgenden Beispiel wird eine synchrone Suche nach Media Player-Geräten mithilfe von C++ veranschaulicht. Die Funktion nimmt einen Zeiger auf die [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -Schnittstelle als Eingabe an und gibt den [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Schnittstellen Zeiger zurück.

Das Beispiel ordnet zuerst einen **BSTR** zu, der den Gerätetyp-URI darstellt, und übergibt ihn dann an die [**IUPnPDeviceFinder:: findbytype**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) -Methode. Außerdem wird die Adresse eines lokalen [**iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) -Zeigers in dem Puffer übergeben, in dem die-Methode die gefundene Geräte Auflistung speichert. Wenn der Funktions Aufrufvorgang erfolgreich ist, wird der Zeiger auf diese Auflistung zurückgegeben.


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



 

 




