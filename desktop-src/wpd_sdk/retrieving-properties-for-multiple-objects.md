---
description: Abrufen von Eigenschaften für mehrere Objekte
ms.assetid: 0d0c6b3d-23bc-4628-a684-14bb9e18967f
title: Abrufen von Eigenschaften für mehrere Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c069f6a28b923339f66f8423f211eff4704ef6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366142"
---
# <a name="retrieving-properties-for-multiple-objects"></a>Abrufen von Eigenschaften für mehrere Objekte

Einige Gerätetreiber unterstützen das Abrufen von Eigenschaften für mehrere Objekte in einem einzelnen Funktionsaufrufs. Dies wird als Massen Abruf bezeichnet. Es gibt zwei Arten von Massen Abruf Vorgängen: mit dem ersten Typ werden Eigenschaften für eine Liste von Objekten abgerufen, und der zweite Typ Ruft Eigenschaften für alle Objekte eines angegebenen Formats ab. Das in diesem Abschnitt beschriebene Beispiel veranschaulicht das erste.

Die Anwendung kann einen Massen Abruf mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausführen.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                        |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.                   |
| [**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)                 | Wird verwendet, um die abzurufenden Eigenschaften zu identifizieren.                   |
| [**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                       | Wird verwendet, um zu bestimmen, ob ein bestimmter Treiber Massen Vorgänge unterstützt. |
| [**Iportabledevicepropertiesbulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)               | Unterstützt den Massen Abruf Vorgang.                             |
| [**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Wird zum Speichern der Objekt Bezeichner für den Massen Vorgang verwendet.       |



 

Die Funktion "lesecontentpropertiesbulk" im Modul "contentproperties. cpp" der Beispielanwendung veranschaulicht einen Massen Abruf Vorgang.

Die erste Aufgabe, die in diesem Beispiel ausgeführt wird, besteht darin, zu bestimmen, ob der angegebene Treiber Massen Vorgänge unterstützt. Dies wird erreicht, indem QueryInterface auf der iportabledeviceproperties-Schnittstelle aufgerufen und das vorhanden sein von iportabledevicepropertiesbulk überprüft wird.


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



Wenn der Treiber Massen Vorgänge unterstützt, besteht der nächste Schritt darin, eine Instanz der [**iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md) zu erstellen und die Schlüssel anzugeben, die den Eigenschaften entsprechen, die von der Anwendung abgerufen werden. Eine Beschreibung dieses Prozesses finden Sie im Thema [Abrufen von Eigenschaften für ein einzelnes Objekt](retrieving-properties-for-a-single-object.md) .

Nachdem die entsprechenden Schlüssel angegeben wurden, erstellt die Beispielanwendung eine Instanz der [**iportabledevicepropertiesbulkcallback-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk). Die Anwendung verwendet die Methoden in dieser Schnittstelle, um den Fortschritt des asynchronen Massen Abruf Vorgangs zu verfolgen.


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



Die nächste Funktion, die von der Beispielanwendung aufgerufen wird, ist die "samateiportabledevicepropvariantcollectionwithzugewiesene"-Hilfsfunktion. Diese Funktion erstellt beispielsweise eine Liste aller verfügbaren Objekt Bezeichner. (Eine reale Anwendung schränkt die Liste der Bezeichner auf einen bestimmten Satz von Objekten ein. Beispielsweise kann eine Anwendung eine Liste von Bezeichnernamen für alle Objekte erstellen, die sich derzeit in einer bestimmten Ordneransicht befinden.)

Wie bereits erwähnt, listet die Hilfsfunktion rekursiv alle Objekte auf einem bestimmten Gerät auf. Diese Liste wird in einer [**iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md) zurückgegeben, die einen Bezeichner für jedes gefundene Objekt enthält. Die Hilfsfunktion ist im Modul "contentenumeration. cpp" definiert.


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



Sobald die vorherigen Schritte ausgeführt wurden, initiiert die Beispielanwendung den Abruf der asynchronen Eigenschaften. Gehen Sie hierzu wie folgt vor:

1.  Aufrufen von iportabledevicepropertiesbulk:: queuegetvaluesbyobjectlist, die eine Anforderung für den Abruf der Massen Eigenschaft in die Warteschlange eingereiht. (Beachten Sie, dass die Anforderung zwar in die Warteschlange eingereiht ist, aber nicht gestartet wird.)
2.  Iportabledevicepropertiesbulk:: Start wird aufgerufen, um die Anforderung in der Warteschlange zu initiieren.

Diese Schritte werden im folgenden Code Ausschnitt aus der Beispielanwendung veranschaulicht.


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

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledevicekeycollection-Schnittstelle**](iportabledevicekeycollection.md)
</dt> <dt>

[**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)
</dt> <dt>

[**Iportabledevicepropertiesbulk-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)
</dt> <dt>

[**Iportabledevicepropvariantcollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



