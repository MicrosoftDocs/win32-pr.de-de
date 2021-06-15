---
title: Aufzählen von Geräten (WPD)
description: Erfahren Sie, wie eine Anwendung Geräte mithilfe der Funktion EnumerateAllDevices aufzählt, die die Anzahl der verbundenen Geräte und gerätespezifische Informationen ruft.
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6465b04e6f1a18a0bdb74f0ce883cf9161371fb6
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068596"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="3240b-103">Aufzählen von Geräten (WPD)</span><span class="sxs-lookup"><span data-stu-id="3240b-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="3240b-104">Die erste Aufgabe, die von den meisten Anwendungen abgeschlossen wird, ist die Enumeration der Geräte, die mit dem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="3240b-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="3240b-105">Diese Aufgabe und das Abrufen von Geräteinformationen (z. B. Hersteller, Angezeigter Name und Beschreibung) wird von der [**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3240b-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="3240b-106">Die Funktion EnumerateAllDevices im Modul DeviceEnumeration.cpp enthält Code, der das Abrufen der Anzahl verbundener Geräte veranschaulicht und nach dem Abrufen der Anzahl gerätespezifische Informationen für jedes verbundene Gerät abruft.</span><span class="sxs-lookup"><span data-stu-id="3240b-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="3240b-107">Die EnumerateAllDevices-Funktion erfüllt vier primäre Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="3240b-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="3240b-108">Erstellt das Portable Device Manager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3240b-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="3240b-109">Ruft die Anzahl der verbundenen Geräte ab.</span><span class="sxs-lookup"><span data-stu-id="3240b-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="3240b-110">Ruft Geräteinformationen ab (für die verbundenen Geräte).</span><span class="sxs-lookup"><span data-stu-id="3240b-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="3240b-111">Gibt den beim Abrufen der Geräteinformationen verwendeten Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="3240b-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="3240b-112">Jede dieser vier Aufgaben wird in den folgenden Abschnitten ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3240b-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="3240b-113">Der erste Schritt des Geräteenumerationsprozesses ist die Erstellung eines portablen Geräte-Manager-Objekts.</span><span class="sxs-lookup"><span data-stu-id="3240b-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="3240b-114">Dies erfolgt durch Aufrufen der CoCreateInstance-Funktion und Übergeben des Klassenbezeichners (CLSID) für das Objekt, Angeben des Kontexts, in dem der Code ausgeführt wird, Angabe eines Verweisbezeichners für die IPortableDeviceManager-Schnittstelle und anschließendes Angeben einer Zeigervariable, die den IPortableDeviceManager-Schnittstellenzeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="3240b-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


```C++
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceManager,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_PPV_ARGS(&pPortableDeviceManager));
if (FAILED(hr))
{
    printf("! Failed to CoCreateInstance CLSID_PortableDeviceManager, hr = 0x%lx\n",hr);
}
```



<span data-ttu-id="3240b-115">Nachdem Sie einen [**IPortableDeviceManager-Schnittstellenzeiger**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) erhalten haben, können Sie mit dem Aufrufen von Methoden für diese Schnittstelle beginnen.</span><span class="sxs-lookup"><span data-stu-id="3240b-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="3240b-116">Die erste Methode, die in der EnumerateAllDevices-Funktion aufgerufen wird, ist [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span><span class="sxs-lookup"><span data-stu-id="3240b-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="3240b-117">Wenn diese Methode aufgerufen wird und das erste Argument auf **NULL** festgelegt ist, wird die Anzahl der verbundenen Geräte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3240b-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pPortableDeviceManager->GetDevices(NULL, &cPnPDeviceIDs);
    if (FAILED(hr))
    {
        printf("! Failed to get number of devices on the system, hr = 0x%lx\n",hr);
    }
}

// Report the number of devices found.  NOTE: we will report 0, if an error
// occured.

printf("\n%d Windows Portable Device(s) found on the system\n\n", cPnPDeviceIDs);
```



<span data-ttu-id="3240b-118">Nachdem Sie die Anzahl der verbundenen Geräte abgerufen haben, können Sie diesen Wert verwenden, um Geräteinformationen für jedes verbundene Gerät abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3240b-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="3240b-119">Dieser Prozess beginnt mit der Übergabe eines Arrays von Zeichenfolgenze0ern als erstes Argument und der Anzahl der Elemente, die dieses Array als zweites Argument enthalten kann (diese Anzahl sollte mindestens der Anzahl der verfügbaren Geräte entspricht).</span><span class="sxs-lookup"><span data-stu-id="3240b-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="3240b-120">Die von dieser Methode zurückgegebenen Zeichenfolgen sind Plug & Play Namen der verbundenen Geräte.</span><span class="sxs-lookup"><span data-stu-id="3240b-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="3240b-121">Diese Namen werden wiederum an andere Methoden auf der [**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) übergeben, um gerätespezifische Informationen abzurufen, z. B. den Benutzernamen, den Herstellernamen und die Gerätebeschreibung.</span><span class="sxs-lookup"><span data-stu-id="3240b-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="3240b-122">(Diese Namen werden auch verwendet, um eine Verbindung mit dem Gerät zu öffnen, wenn eine Anwendung die [**IPortableDevice::Open-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) aufruft.)</span><span class="sxs-lookup"><span data-stu-id="3240b-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


```C++
if (SUCCEEDED(hr) && (cPnPDeviceIDs > 0))
{
    pPnpDeviceIDs = new (std::nothrow) PWSTR[cPnPDeviceIDs];
    if (pPnpDeviceIDs != NULL)
    {
        DWORD dwIndex = 0;

        hr = pPortableDeviceManager->GetDevices(pPnpDeviceIDs, &cPnPDeviceIDs);
        if (SUCCEEDED(hr))
        {
            // For each device found, display the devices friendly name,
            // manufacturer, and description strings.
            for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
            {
                printf("[%d] ", dwIndex);
                DisplayFriendlyName(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayManufacturer(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
                printf("    ");
                DisplayDescription(pPortableDeviceManager, pPnpDeviceIDs[dwIndex]);
            }
        }
        else
        {
            printf("! Failed to get the device list from the system, hr = 0x%lx\n",hr);
        }
```



<span data-ttu-id="3240b-123">Nachdem Sie die Geräteinformationen abgerufen haben, müssen Sie den Arbeitsspeicher, der den Zeichenfolgen zugeordnet ist, auf die durch das Array von Zeichenfolgenzedern verwiesen wird, frei geben.</span><span class="sxs-lookup"><span data-stu-id="3240b-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="3240b-124">Sie müssen auch dieses Array löschen.</span><span class="sxs-lookup"><span data-stu-id="3240b-124">You will also need to delete this array.</span></span>


```C++
for (dwIndex = 0; dwIndex < cPnPDeviceIDs; dwIndex++)
{
    CoTaskMemFree(pPnpDeviceIDs[dwIndex]);
    pPnpDeviceIDs[dwIndex] = NULL;
}

// Delete the array of PWSTR pointers
delete [] pPnpDeviceIDs;
pPnpDeviceIDs = NULL;
```



## <a name="related-topics"></a><span data-ttu-id="3240b-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3240b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3240b-126">**IPortableDeviceManager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="3240b-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="3240b-127">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="3240b-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



