---
description: Angeben von Clientinformationen
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Angeben von Clientinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b437c4d0c0ce9d04f55bb00a1fd4b666d30cf29228050151072e43f87edb11a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119445500"
---
# <a name="specifying-client-information"></a>Angeben von Clientinformationen

Die im zweiten Argument angegebenen Clientinformationen werden von einigen Gerätetreibern verwendet, um die Geräteleistung zu optimieren. Ihre Anwendung sollte mindestens eine Zeichenfolge mit ihrem Namen, einer Hauptversionsnummer, einer Nebenversionsnummer und einer Revisionsnummer bereitstellen. Dies sind die Felder, die von der Beispielanwendung bereitgestellt werden.


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



Die `GetClientInformation` Funktion in der Beispielanwendung erstellt eine **IPortableDeviceValues-Schnittstelle** und füllt sie mit Clientinformationen auf. Diese Funktion besteht aus zwei Hauptteilen. Der erste Teil erstellt eine Instanz eines portablen Gerätewertobjekts durch Aufrufen der CoCreateInstance-Funktion.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



Der zweite Teil legt die Clientinformationen im portablen Device Values-Objekt fest.


```C++
if (SUCCEEDED(hr))
{
    // Attempt to set all bits of client information
    hr = (*ppClientInformation)->SetStringValue(WPD_CLIENT_NAME, CLIENT_NAME);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_NAME, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MAJOR_VERSION, CLIENT_MAJOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MAJOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_MINOR_VERSION, CLIENT_MINOR_VER);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_MINOR_VERSION, hr = 0x%lx\n",hr);
    }

    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_REVISION, CLIENT_REVISION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_REVISION, hr = 0x%lx\n",hr);
    }

    //  Some device drivers need to impersonate the caller in order to function correctly.  Since our application does not
    //  need to restrict its identity, specify SECURITY_IMPERSONATION so that we work with all devices.
    hr = (*ppClientInformation)->SetUnsignedIntegerValue(WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, SECURITY_IMPERSONATION);
    if (FAILED(hr))
    {
        printf("! Failed to set WPD_CLIENT_SECURITY_QUALITY_OF_SERVICE, hr = 0x%lx\n",hr);
    }
}
else
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceValues, hr = 0x%lx\n",hr);
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



