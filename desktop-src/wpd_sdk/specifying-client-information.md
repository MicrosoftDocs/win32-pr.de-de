---
description: Angeben von Client Informationen
ms.assetid: 275fda71-61ef-4b50-96fe-bdc0c0266646
title: Angeben von Client Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f6ca094b627b6c2cee16ec587a8c850cd17f78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217510"
---
# <a name="specifying-client-information"></a>Angeben von Client Informationen

Die im zweiten Argument bereitgestellten Client Informationen werden von einigen Gerätetreibern verwendet, um die Geräteleistung zu optimieren. Die Anwendung sollte mindestens eine Zeichenfolge bereitstellen, die den Namen, eine Hauptversionsnummer, eine neben Versionsnummer und eine Revisionsnummer enthält. Dies sind die Felder, die von der Beispielanwendung bereitgestellt werden.


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



Die `GetClientInformation` -Funktion in der Beispielanwendung erstellt und füllt eine **iportabledevicevalues** -Schnittstelle mit Client Informationen. Diese Funktion verfügt über zwei primäre Teile. Der erste Teil erstellt eine Instanz eines portablen Geräte Wert Objekts durch Aufrufen der CoCreateInstance-Funktion.


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



Im zweiten Teil werden die Client Informationen im Objekt für tragbare Geräte Werte festgelegt.


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

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



