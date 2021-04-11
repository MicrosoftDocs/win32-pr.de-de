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
# <a name="specifying-client-information"></a><span data-ttu-id="b3134-103">Angeben von Client Informationen</span><span class="sxs-lookup"><span data-stu-id="b3134-103">Specifying Client Information</span></span>

<span data-ttu-id="b3134-104">Die im zweiten Argument bereitgestellten Client Informationen werden von einigen Gerätetreibern verwendet, um die Geräteleistung zu optimieren.</span><span class="sxs-lookup"><span data-stu-id="b3134-104">The client information supplied in the second argument is used by some device drivers to optimize device performance.</span></span> <span data-ttu-id="b3134-105">Die Anwendung sollte mindestens eine Zeichenfolge bereitstellen, die den Namen, eine Hauptversionsnummer, eine neben Versionsnummer und eine Revisionsnummer enthält.</span><span class="sxs-lookup"><span data-stu-id="b3134-105">At a minimum, your application should provide a string containing its name, a major version number, a minor version number, and a revision number.</span></span> <span data-ttu-id="b3134-106">Dies sind die Felder, die von der Beispielanwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b3134-106">These are the fields supplied by the sample application.</span></span>


```C++
#define CLIENT_NAME         L"WPD Sample Application"
#define CLIENT_MAJOR_VER    1
#define CLIENT_MINOR_VER    0
#define CLIENT_REVISION     2
```



<span data-ttu-id="b3134-107">Die `GetClientInformation` -Funktion in der Beispielanwendung erstellt und füllt eine **iportabledevicevalues** -Schnittstelle mit Client Informationen.</span><span class="sxs-lookup"><span data-stu-id="b3134-107">The `GetClientInformation` function in the sample application creates and populates an **IPortableDeviceValues** interface with client information.</span></span> <span data-ttu-id="b3134-108">Diese Funktion verfügt über zwei primäre Teile.</span><span class="sxs-lookup"><span data-stu-id="b3134-108">This function has two primary parts.</span></span> <span data-ttu-id="b3134-109">Der erste Teil erstellt eine Instanz eines portablen Geräte Wert Objekts durch Aufrufen der CoCreateInstance-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b3134-109">The first part creates an instance of a portable device-values object by calling the CoCreateInstance function.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(ppClientInformation));
```



<span data-ttu-id="b3134-110">Im zweiten Teil werden die Client Informationen im Objekt für tragbare Geräte Werte festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b3134-110">The second part sets the client information in the portable device-values object.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="b3134-111">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b3134-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3134-112">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b3134-112">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="b3134-113">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="b3134-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="b3134-114">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="b3134-114">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



