---
title: Synchrone Suche
description: Das Device Finder-Objekt ermöglicht sowohl synchrone als auch asynchrone Suchvorgänge. Synchrone Suchvorgänge werden abgeschlossen und geben die Steuerung erst an die aufrufende Anwendung zurück, nachdem alle verfügbaren Geräte gefunden wurden.
ms.assetid: fa22cd53-6468-4958-b4e3-b1a41b3cb2f6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f852957bed4bb73d9b31d0e26e099eb545b804953718d8cfd4e3cb44ea5f6c62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999500"
---
# <a name="synchronous-searching"></a>Synchrone Suche

Das Device Finder-Objekt ermöglicht sowohl synchrone als auch asynchrone Suchvorgänge. Synchrone Suchvorgänge werden abgeschlossen und geben die Steuerung erst an die aufrufende Anwendung zurück, nachdem alle verfügbaren Geräte gefunden wurden. Um eine synchrone Suche durchzuführen, verwenden Sie eine der synchronen Suchmethoden der [**IUPnPDeviceSynchron-Schnittstelle.**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)

> [!Note]  
> Die Rückgabe synchroner Suchvorgänge dauert mindestens neun Sekunden. Die Verzögerung wird dadurch verursacht, dass die erste UDP-Suchnachricht mehrmals gesendet werden muss. Diese Duplizierung ist für die Nichtzuverlässigkeit des zugrunde liegenden Netzwerkprotokolls verantwortlich. Synchrone Suchvorgänge sind am besten für Befehlszeilenschnittstellen. Sie werden für grafische Benutzeroberflächen nicht empfohlen.

 

Die [**IUPnPDevice Wiesn::FindByType-Methode**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) durchsucht nach Geräte- oder Diensttyp. Diese Methode verwendet einen Typ-URI als Eingabeparameter und gibt eine Auflistung von Geräteobjekten zurück. Ein Device-Objekt stellt ein einzelnes Gerät dar.

In den folgenden Beispielen wird veranschaulicht, wie sie eine synchrone Suche nach Geräten in VBScript ausführen. Jedes Skript verwendet [**IUPnPDeviceGramm::FindByType,**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype)der mit dem Typ-URI (Dienst-ID) für den Media *Player-Gerätetyp urn:schemas-upnp-org:device:mediaplayer.v1.00.00 aufgerufen wird.* Die -Methode gibt eine Sammlung von Geräteobjekten zurück, die gefundenen Media Player-Geräten entsprechen. Informationen zum Extrahieren einzelner Geräteobjekte aus einer Sammlung finden Sie unter Gerätesammlungen, die [von synchronen Suchvorgängen zurückgegeben werden.](device-collections-returned-by-synchronous-searches.md)

## <a name="search-for-devices-by-type-in-vbscript"></a>Suchen nach Geräten nach Typ in VBScript


```VB
Dim deviceFinder

Set deviceFinder = CreateObject( "UPnP.UPnPDeviceFinder" )

Dim devices

Set devices = deviceFinder.FindByType( "urn:schemas-upnp-org:device:multidisk-dvd", 0 )
```



## <a name="search-for-device-by-type-in-c"></a>Suchen nach Gerät nach Typ in C++

Im folgenden Beispiel wird eine synchrone Suche nach Media Player-Geräten mit C++ veranschaulicht. Die -Funktion verwendet einen Zeiger auf die [**IUPnPDeviceGrad-Schnittstelle**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) als Eingabe und gibt den [**IUPnPDevices-Schnittstellenzeiger**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) zurück.

Im Beispiel wird zuerst ein **BSTR** zur Darstellung des Gerätetyp-URI zuteilen, und anschließend wird dieser an die [**IUPnPDeviceViceVic::FindByType-Methode**](/windows/desktop/api/Upnp/nf-upnp-iupnpdevicefinder-findbytype) übertragen. Außerdem wird die Adresse eines lokalen [**IUPnPDevices-Zeigers**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices) in den Puffer übergibt, in dem die -Methode dann die Sammlung der gefundenen Geräte speichert. Wenn der Funktionsaufruf erfolgreich ist, wird der Zeiger auf diese Auflistung zurückgegeben.


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



 

 




