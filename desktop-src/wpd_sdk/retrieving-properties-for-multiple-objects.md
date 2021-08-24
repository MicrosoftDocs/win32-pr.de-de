---
description: Abrufen von Eigenschaften für mehrere Objekte
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Abrufen von Eigenschaften für mehrere Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1ad9ec397daa90c149fe950c1fc4777c407e3f5f3a359f46cf8bef56e18b9f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083514"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Abrufen von Eigenschaften für mehrere Objekte

Einige Gerätetreiber unterstützen das Abrufen von Eigenschaften für mehrere Objekte in einem einzelnen Funktionsaufruf. dies wird als Massenabruf bezeichnet. Es gibt zwei Arten von Massenabrufvorgängen: Der erste Typ ruft Eigenschaften für eine Liste von -Objekten ab, und der zweite Typ ruft Eigenschaften für alle Objekte eines bestimmten Formats ab. Das in diesem Abschnitt beschriebene Beispiel veranschaulicht erstere.

Ihre Anwendung kann einen Massenabruf mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausführen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.                   |
| [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)                 | Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.                   |
| [**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Wird verwendet, um zu bestimmen, ob ein angegebener Treiber Massenvorgänge unterstützt. |
| [**IPortableDevicePropertiesBulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Unterstützt den Massenabrufvorgang.                             |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Speichern der Objektbezeichner für den Massenvorgang verwendet.       |



 

Die ReadContentPropertiesBulk-Funktion im ContentProperties.cpp-Modul der Beispielanwendung veranschaulicht einen Massenabrufvorgang.

Die erste Aufgabe, die in diesem Beispiel ausgeführt wird, besteht darin, zu bestimmen, ob der gegebene Treiber Massenvorgänge unterstützt. Dies wird erreicht, indem QueryInterface auf der IPortableDeviceProperties-Schnittstelle aufruft und das Vorhandensein von IPortableDevicePropertiesBulk überprüft wird.


```C++
HRESULT                                       hr                = S_OK;
GUID                                          guidContext       = GUID_NULL;
CGetBulkValuesCallback*                       pCallback         = NULL;
CComPtr<IPortableDeviceProperties>            pProperties;
CComPtr<IPortableDevicePropertiesBulk>        pPropertiesBulk;
CComPtr<IPortableDeviceValues>                pObjectProperties;
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDeviceKeyCollection>         pPropertiesToRead;
CComPtr<IPortableDevicePropVariantCollection> pObjectIDs;


if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDevice, hr = 0x%lx\n",hr);
    }
}



if (SUCCEEDED(hr))
{
    hr = pProperties->QueryInterface(IID_PPV_ARGS(&pPropertiesBulk));
    if (FAILED(hr))
    {
        printf("This driver does not support BULK property operations.\n");
    }
}
```



Wenn der Treiber Massenvorgänge unterstützt, besteht der nächste Schritt im Erstellen einer Instanz der [**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md) und dem Angeben der Schlüssel, die den Eigenschaften entsprechen, die die Anwendung abruft. Eine Beschreibung dieses Prozesses finden Sie im Thema [Abrufen von Eigenschaften für ein einzelnes Objekt.](retrieving-properties-for-a-single-object.md)

Nachdem die entsprechenden Schlüssel angegeben wurden, erstellt die Beispielanwendung eine Instanz der [**IPortableDevicePropertiesBulkCallback-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). Die Anwendung verwendet die Methoden in dieser Schnittstelle, um den Fortschritt des asynchronen Massenabrufs zu verfolgen.


```C++
if (SUCCEEDED(hr))
{
    pCallback = new CGetBulkValuesCallback();
    if (pCallback == NULL)
    {
        hr = E_OUTOFMEMORY;
        printf("! Failed to allocate CGetBulkValuesCallback, hr = 0x%lx\n", hr);
    }
}
```



Die nächste Funktion, die die Beispielanwendung aufruft, ist die Hilfsfunktion CreateIPortableDevicePropVariantCollectionWithAllObjectIDs. Diese Funktion erstellt eine Liste aller verfügbaren Objektbezeichner für Beispielzwecke. (Eine reale Anwendung würde die Liste der Bezeichner auf einen bestimmten Satz von Objekten beschränken. Beispielsweise kann eine Anwendung eine Liste von Bezeichnern für alle Objekte erstellen, die sich derzeit in einer bestimmten Ordneransicht befinden.)

Wie bereits erwähnt, werden mit der Hilfsfunktion alle Objekte auf einem bestimmten Gerät rekursiv aufzählt. Diese Liste wird in einer [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) zurückgegeben, die einen Bezeichner für jedes gefundene Objekt enthält. Die Hilfsfunktion wird im Modul ContentEnumeration.cpp definiert.


```C++
// 7) Call our helper function CreateIPortableDevicePropVariantCollectionWithAllObjectIDs
// to enumerate and create an IPortableDevicePropVariantCollection with the object
// identifiers needed to perform the bulk operation on.
if (SUCCEEDED(hr))
{
    hr = CreateIPortableDevicePropVariantCollectionWithAllObjectIDs(pDevice,
                                                                    pContent,
                                                                    &pObjectIDs);
}
```



Nachdem die vorherigen Schritte ausgeführt wurden, initiiert die Beispielanwendung den asynchronen Eigenschaftenabruf. Dies wird wie folgt erreicht:

1.  Aufrufen von IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, wodurch eine Anforderung für den Massenabruf von Eigenschaften in die Warteschlange gestellt wird. (Beachten Sie, dass die Anforderung zwar in der Warteschlange steht, aber nicht gestartet wird.)
2.  Aufrufen von IPortableDevicePropertiesBulk::Start, um die Anforderung in der Warteschlange zu initiieren.

Diese Schritte werden im folgenden Codeausschnitt aus der Beispielanwendung gezeigt.


```C++
   if (SUCCEEDED(hr))
   {
       hr = pPropertiesBulk->QueueGetValuesByObjectList(pObjectIDs,
                                                        pPropertiesToRead,
                                                        pCallback,
                                                        &guidContext);


       if(SUCCEEDED(hr))
       {
           // Cleanup any previously created global event handles.
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               CloseHandle(g_hBulkPropertyOperationEvent);
               g_hBulkPropertyOperationEvent = NULL;
           }

           // In order to create a simpler to follow example we create and wait infinitly
           // for the bulk property operation to complete and ignore any errors.
           // Production code should be written in a more robust manner.
           // Create the global event handle to wait on for the bulk operation
           // to complete.
           g_hBulkPropertyOperationEvent = CreateEvent(NULL, FALSE, FALSE, NULL);
           if (g_hBulkPropertyOperationEvent != NULL)
           {
               // Call Start() to actually being the Asynchronous bulk operation.
               hr = pPropertiesBulk->Start(guidContext);
               if(FAILED(hr))
               {
                   printf("! Failed to start property operation, hr = 0x%lx\n", hr);
               }
           }
           else
           {
               printf("! Failed to create the global event handle to wait on for the bulk operation. Aborting operation.\n");
           }
       }
       else
       {
           printf("! QueueGetValuesByObjectList Failed, hr = 0x%lx\n", hr);
       }
   }
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceKeyCollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**IPortableDeviceProperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**IPortableDevicePropertiesBulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



