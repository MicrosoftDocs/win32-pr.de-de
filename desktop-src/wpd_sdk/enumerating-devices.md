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
# <a name="enumerating-devices-wpd"></a>Auflisten von Geräten (WPD)

Die erste Aufgabe, die von den meisten Anwendungen abgeschlossen wird, ist die Enumeration der Geräte, die mit dem Computer verbunden sind. Diese Aufgabe und das Abrufen von Geräteinformationen (z. b. Hersteller, Anzeige Name und Beschreibung) werden von der [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle unterstützt.

Die Funktion "enumeratealldevices" im deviceenumeration. cpp-Modul enthält Code, der das Abrufen der Anzahl verbundener Geräte und nach dem Abrufen der Anzahl den Abruf Geräte spezifischer Informationen für jedes verbundene Gerät veranschaulicht.

Die Funktion "enumeratealldevices" führt vier Hauptaufgaben aus:

1.  Erstellt das portablen Geräte-Manager-Objekt.
2.  Ruft die Anzahl verbundener Geräte ab.
3.  Ruft Geräteinformationen (für die verbundenen Geräte) ab.
4.  Gibt den Arbeitsspeicher frei, der beim Abrufen der Geräteinformationen verwendet wurde.

Diese vier Aufgaben werden in den folgenden Abschnitten ausführlicher beschrieben.

Der erste Schritt im Geräte Aufzählungs Prozess ist die Erstellung eines portablen Geräte-Manager-Objekts. Dies erfolgt durch Aufrufen der CoCreateInstance-Funktion und durch übergeben der Klassen-ID (CLSID) für das Objekt. dabei wird der Kontext angegeben, in dem der Code ausgeführt wird, und es wird ein Verweis Bezeichner für die iportabledevicemanager-Schnittstelle angegeben


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



Sobald Sie einen [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstellen Zeiger erhalten haben, können Sie mit dem Aufrufen von Methoden für diese Schnittstelle beginnen. Die erste Methode, die in der Funktion "enumeratealldevices" aufgerufen wird, ist [**iportabledevicemanager:: GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices). Wenn diese Methode aufgerufen wird, wobei das erste Argument auf **null** festgelegt ist, wird die Anzahl der verbundenen Geräte zurückgegeben.


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



Nachdem Sie die Anzahl der verbundenen Geräte abgerufen haben, können Sie mit diesem Wert Geräteinformationen für jedes verbundene Gerät abrufen. Dieser Prozess beginnt mit dem Übergeben eines Arrays von Zeichen folgen Zeigern als erstes Argument und der Anzahl der Elemente, die dieses Array als zweites Argument enthalten kann (diese Anzahl sollte mindestens der Anzahl der verfügbaren Geräte entsprechen).

Die von dieser Methode zurückgegebenen Zeichen folgen sind die Plug & Play Namen der verbundenen Geräte. Diese Namen werden wiederum an andere Methoden der [**iportabledevicemanager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) -Schnittstelle übergeben, um gerätespezifische Informationen wie den anzeigen Amen, den Namen des Herstellers und die Geräte Beschreibung abzurufen. (Diese Namen werden auch verwendet, um eine Verbindung mit dem Gerät zu öffnen, wenn eine Anwendung die [**iportabledevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) -Methode aufruft.)


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



Nachdem Sie die Geräteinformationen abgerufen haben, müssen Sie den Arbeitsspeicher freigeben, der den Zeichen folgen zugeordnet ist, auf die durch das Array von Zeichen folgen Zeigern verwiesen wird. Außerdem müssen Sie dieses Array löschen.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledebug Manager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



