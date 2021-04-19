---
title: Auflisten von Geräten (WPD)
description: Auflisten von Geräten
ms.assetid: 28ded3cf-b0c8-4c90-ab39-efc879adb6e7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2738398de7f3bfb6aa1ea88175ff30241b4dbb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106361697"
---
# <a name="enumerating-devices-wpd"></a><span data-ttu-id="00263-103">Auflisten von Geräten (WPD)</span><span class="sxs-lookup"><span data-stu-id="00263-103">Enumerating devices (WPD)</span></span>

<span data-ttu-id="00263-104">Die erste Aufgabe, die von den meisten Anwendungen abgeschlossen wird, ist die Enumeration der Geräte, die mit dem Computer verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="00263-104">The first task completed by most applications is the enumeration of the devices connected to the computer.</span></span> <span data-ttu-id="00263-105">Diese Aufgabe und das Abrufen von Geräteinformationen (z. b. Hersteller, Anzeige Name und Beschreibung) werden von der [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle unterstützt.</span><span class="sxs-lookup"><span data-stu-id="00263-105">This task, and the retrieval of device information (such as manufacturer, friendly name, and description), is supported by the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span>

<span data-ttu-id="00263-106">Die Funktion "enumeratealldevices" im deviceenumeration. cpp-Modul enthält Code, der das Abrufen der Anzahl verbundener Geräte und nach dem Abrufen der Anzahl den Abruf Geräte spezifischer Informationen für jedes verbundene Gerät veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="00263-106">The EnumerateAllDevices function in the DeviceEnumeration.cpp module contains code that demonstrates the retrieval of the count of connected devices and, once the count is retrieved, the retrieval of device-specific information for each connected device.</span></span>

<span data-ttu-id="00263-107">Die Funktion "enumeratealldevices" führt vier Hauptaufgaben aus:</span><span class="sxs-lookup"><span data-stu-id="00263-107">The EnumerateAllDevices function accomplishes four primary tasks:</span></span>

1.  <span data-ttu-id="00263-108">Erstellt das portablen Geräte-Manager-Objekt.</span><span class="sxs-lookup"><span data-stu-id="00263-108">Creates the portable device manager object.</span></span>
2.  <span data-ttu-id="00263-109">Ruft die Anzahl verbundener Geräte ab.</span><span class="sxs-lookup"><span data-stu-id="00263-109">Retrieves a count of connected devices.</span></span>
3.  <span data-ttu-id="00263-110">Ruft Geräteinformationen (für die verbundenen Geräte) ab.</span><span class="sxs-lookup"><span data-stu-id="00263-110">Retrieves device information (for the connected devices).</span></span>
4.  <span data-ttu-id="00263-111">Gibt den Arbeitsspeicher frei, der beim Abrufen der Geräteinformationen verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="00263-111">Frees the memory used when retrieving the device information.</span></span>

<span data-ttu-id="00263-112">Diese vier Aufgaben werden in den folgenden Abschnitten ausführlicher beschrieben.</span><span class="sxs-lookup"><span data-stu-id="00263-112">Each of these four tasks is described in more detail in the following sections.</span></span>

<span data-ttu-id="00263-113">Der erste Schritt im Geräte Aufzählungs Prozess ist die Erstellung eines portablen Geräte-Manager-Objekts.</span><span class="sxs-lookup"><span data-stu-id="00263-113">The first step in the device enumeration process is the creation of a portable device manager object.</span></span> <span data-ttu-id="00263-114">Dies erfolgt durch Aufrufen der CoCreateInstance-Funktion und durch übergeben der Klassen-ID (CLSID) für das Objekt. dabei wird der Kontext angegeben, in dem der Code ausgeführt wird, und es wird ein Verweis Bezeichner für die iportabledevicemanager-Schnittstelle angegeben</span><span class="sxs-lookup"><span data-stu-id="00263-114">This is done by calling the CoCreateInstance function and passing the class identifier (CLSID) for the object, specifying the context in which the code will run, specifying a reference identifier for the IPortableDeviceManager interface, and then supplying a pointer variable that receives the IPortableDeviceManager interface pointer.</span></span>


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



<span data-ttu-id="00263-115">Sobald Sie einen [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstellen Zeiger erhalten haben, können Sie mit dem Aufrufen von Methoden für diese Schnittstelle beginnen.</span><span class="sxs-lookup"><span data-stu-id="00263-115">Once you obtain an [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface pointer, you can begin calling methods on this interface.</span></span> <span data-ttu-id="00263-116">Die erste Methode, die in der Funktion "enumeratealldevices" aufgerufen wird, ist [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span><span class="sxs-lookup"><span data-stu-id="00263-116">The first method called in the EnumerateAllDevices function is [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices).</span></span> <span data-ttu-id="00263-117">Wenn diese Methode aufgerufen wird, wobei das erste Argument auf **null** festgelegt ist, wird die Anzahl der verbundenen Geräte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00263-117">When this method is called with the first argument set to **NULL**, it returns the count of connected devices.</span></span>


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



<span data-ttu-id="00263-118">Nachdem Sie die Anzahl der verbundenen Geräte abgerufen haben, können Sie mit diesem Wert Geräteinformationen für jedes verbundene Gerät abrufen.</span><span class="sxs-lookup"><span data-stu-id="00263-118">After you have retrieved the count of connected devices, you can use this value to retrieve device information for each connected device.</span></span> <span data-ttu-id="00263-119">Dieser Prozess beginnt mit dem Übergeben eines Arrays von Zeichen folgen Zeigern als erstes Argument und der Anzahl der Elemente, die dieses Array als zweites Argument enthalten kann (diese Anzahl sollte mindestens der Anzahl der verfügbaren Geräte entsprechen).</span><span class="sxs-lookup"><span data-stu-id="00263-119">This process begins by passing an array of string pointers as the first argument and a count of the number of elements that this array can hold as the second argument (this count should at least be equal to the number of available devices).</span></span>

<span data-ttu-id="00263-120">Die von dieser Methode zurückgegebenen Zeichen folgen sind die Plug & Play Namen der verbundenen Geräte.</span><span class="sxs-lookup"><span data-stu-id="00263-120">The strings returned by this method are the Plug and Play names of the connected devices.</span></span> <span data-ttu-id="00263-121">Diese Namen werden wiederum an andere Methoden der [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle übergeben, um gerätespezifische Informationen wie den anzeigen Amen, den Namen des Herstellers und die Geräte Beschreibung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="00263-121">These names, in turn, are passed to other methods on the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface to retrieve device-specific information such as the friendly name, the manufacturer's name, and the device description.</span></span> <span data-ttu-id="00263-122">(Diese Namen werden auch verwendet, um eine Verbindung mit dem Gerät zu öffnen, wenn eine Anwendung die [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode aufruft.)</span><span class="sxs-lookup"><span data-stu-id="00263-122">(These names are also used to open a connection to the device when an application calls the [**IPortableDevice::Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) method.)</span></span>


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



<span data-ttu-id="00263-123">Nachdem Sie die Geräteinformationen abgerufen haben, müssen Sie den Arbeitsspeicher freigeben, der den Zeichen folgen zugeordnet ist, auf die durch das Array von Zeichen folgen Zeigern verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="00263-123">Once you've retrieved the device information, you will need to free the memory associated with the strings pointed to by the array of string pointers.</span></span> <span data-ttu-id="00263-124">Außerdem müssen Sie dieses Array löschen.</span><span class="sxs-lookup"><span data-stu-id="00263-124">You will also need to delete this array.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="00263-125">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="00263-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00263-126">**Iportabledebug Manager-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="00263-126">**IPortableDeviceManager Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[<span data-ttu-id="00263-127">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="00263-127">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



