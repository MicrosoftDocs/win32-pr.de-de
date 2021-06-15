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
# <a name="enumerating-devices-wpd"></a>Aufzählen von Geräten (WPD)

Die erste Aufgabe, die von den meisten Anwendungen abgeschlossen wird, ist die Enumeration der Geräte, die mit dem Computer verbunden sind. Diese Aufgabe und das Abrufen von Geräteinformationen (z. B. Hersteller, Angezeigter Name und Beschreibung) wird von der [**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) unterstützt.

Die Funktion EnumerateAllDevices im Modul DeviceEnumeration.cpp enthält Code, der das Abrufen der Anzahl verbundener Geräte veranschaulicht und nach dem Abrufen der Anzahl gerätespezifische Informationen für jedes verbundene Gerät abruft.

Die EnumerateAllDevices-Funktion erfüllt vier primäre Aufgaben:

1.  Erstellt das Portable Device Manager-Objekt.
2.  Ruft die Anzahl der verbundenen Geräte ab.
3.  Ruft Geräteinformationen ab (für die verbundenen Geräte).
4.  Gibt den beim Abrufen der Geräteinformationen verwendeten Arbeitsspeicher frei.

Jede dieser vier Aufgaben wird in den folgenden Abschnitten ausführlicher beschrieben.

Der erste Schritt des Geräteenumerationsprozesses ist die Erstellung eines portablen Geräte-Manager-Objekts. Dies erfolgt durch Aufrufen der CoCreateInstance-Funktion und Übergeben des Klassenbezeichners (CLSID) für das Objekt, Angeben des Kontexts, in dem der Code ausgeführt wird, Angabe eines Verweisbezeichners für die IPortableDeviceManager-Schnittstelle und anschließendes Angeben einer Zeigervariable, die den IPortableDeviceManager-Schnittstellenzeiger empfängt.


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



Nachdem Sie einen [**IPortableDeviceManager-Schnittstellenzeiger**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) erhalten haben, können Sie mit dem Aufrufen von Methoden für diese Schnittstelle beginnen. Die erste Methode, die in der EnumerateAllDevices-Funktion aufgerufen wird, ist [**IPortableDeviceManager::GetDevices**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicemanager-getdevices). Wenn diese Methode aufgerufen wird und das erste Argument auf **NULL** festgelegt ist, wird die Anzahl der verbundenen Geräte zurückgegeben.


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



Nachdem Sie die Anzahl der verbundenen Geräte abgerufen haben, können Sie diesen Wert verwenden, um Geräteinformationen für jedes verbundene Gerät abzurufen. Dieser Prozess beginnt mit der Übergabe eines Arrays von Zeichenfolgenze0ern als erstes Argument und der Anzahl der Elemente, die dieses Array als zweites Argument enthalten kann (diese Anzahl sollte mindestens der Anzahl der verfügbaren Geräte entspricht).

Die von dieser Methode zurückgegebenen Zeichenfolgen sind Plug & Play Namen der verbundenen Geräte. Diese Namen werden wiederum an andere Methoden auf der [**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) übergeben, um gerätespezifische Informationen abzurufen, z. B. den Benutzernamen, den Herstellernamen und die Gerätebeschreibung. (Diese Namen werden auch verwendet, um eine Verbindung mit dem Gerät zu öffnen, wenn eine Anwendung die [**IPortableDevice::Open-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) aufruft.)


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



Nachdem Sie die Geräteinformationen abgerufen haben, müssen Sie den Arbeitsspeicher, der den Zeichenfolgen zugeordnet ist, auf die durch das Array von Zeichenfolgenzedern verwiesen wird, frei geben. Sie müssen auch dieses Array löschen.


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

[**IPortableDeviceManager-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



