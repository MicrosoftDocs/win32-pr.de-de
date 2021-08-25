---
description: Verschieben von Inhalten auf dem Gerät
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Verschieben von Inhalten auf dem Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0830dab93b4ac0cd11f988c34edef24b1eb11b8869f63efdc4b0b518fc9380b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928370"
---
# <a name="moving-content-on-the-device"></a>Verschieben von Inhalten auf dem Gerät

Ein weiterer gängiger Vorgang, der von einer WPD-Anwendung durchgeführt wird, ist die Übertragung von Inhalten von einem Standort auf dem Gerät an einen anderen.

Vorgänge zum Verschieben von Inhalten werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen durchgeführt.



| Schnittstelle                                                                                      | BESCHREIBUNG                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.  |
| [**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md) | Ermöglicht den Zugriff auf die eigenschaftenspezifischen Methoden. |



 

Die MoveContentAlreadyOnDevice-Funktion im ContentTransfer.cpp-Modul der Beispielanwendung veranschaulicht, wie eine Anwendung Inhalte von einem Speicherort an einen anderen verschieben kann.

Die erste Aufgabe, die von der MoveContentAlreadyOnDevice-Funktion ausgeführt wird, besteht darin, den Gerätetreiber abzufragen, um festzustellen, ob er die Inhaltsbewegung unterstützt. Dies wird erreicht, indem die SupportsCommand-Hilfsfunktion aufgerufen und WPD COMMAND OBJECT MANAGEMENT MOVE OBJECTS als zweites Argument übergeben \_ \_ \_ \_ \_ wird.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SupportsCommand(pDevice, WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS) == FALSE)
{
    printf("! This device does not support the move operation (i.e. The WPD_COMMAND_OBJECT_MANAGEMENT_MOVE_OBJECTS command)\n");
    return;
}
```



Der nächste Schritt umfasst die Aufforderung des Benutzers, zwei Objektbezeichner einzugeben. Der erste ist der Bezeichner für den Inhalt, der verschoben wird. Die zweite ist der Bezeichner für den Speicherort, an den die Anwendung diesen Inhalt verschieben soll.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
printf("Enter the identifer of the object you wish to move.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}

// Prompt user to enter an object identifier on the device to move.
printf("Enter the identifer of the object you wish to move '%ws' to.\n>", wszSelection);
hr = StringCbGetsW(wszDestinationFolderObjectID,sizeof(wszDestinationFolderObjectID));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content moving\n");
}
```



Als Nächstes ruft das Beispiel ein [**IPortableDeviceContent-Objekt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) ab, das für den Zugriff auf die [**IPortableDeviceContent::Move-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) verwendet wird.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



Schließlich wird der Inhalt verschoben. Dieser Prozess umfasst Folgendes:

1.  Erstellen eines [**IPortableDevicePropVariantCollection-Objekts,**](iportabledevicepropvariantcollection.md) das eine PROPVARIANT-Struktur für das zu verschiebende Objekt empfängt.
2.  Hinzufügen von PROPVARIANT zum IPortableDevicePropVariantCollection-Objekt.
3.  Aufrufen der IPortableDeviceContent::Move-Methode.


```C++
HRESULT                                       hr                               = S_OK;
WCHAR                                         wszSelection[81]                 = {0};
WCHAR                                         wszDestinationFolderObjectID[81] = {0};
CComPtr<IPortableDeviceContent>               pContent;
CComPtr<IPortableDevicePropVariantCollection> pObjectsToMove;
CComPtr<IPortableDevicePropVariantCollection> pObjectsFailedToMove;
if (SUCCEEDED(hr))
{
    hr = CoCreateInstance(CLSID_PortableDevicePropVariantCollection,
                          NULL,
                          CLSCTX_INPROC_SERVER,
                          IID_IPortableDevicePropVariantCollection,
                          (VOID**) &pObjectsToMove);
    if (SUCCEEDED(hr))
    {
        if (pObjectsToMove != NULL)
        {
            PROPVARIANT pv = {0};
            PropVariantInit(&pv);

            // Initialize a PROPVARIANT structure with the object identifier string
            // that the user selected above. Notice we are allocating memory for the
            // LPWSTR value.  This memory will be freed when PropVariantClear() is
            // called below.
            pv.vt      = VT_LPWSTR;
            pv.pwszVal = AtlAllocTaskWideString(wszSelection);
            if (pv.pwszVal != NULL)
            {
                // Add the object identifier to the objects-to-move list
                // (We are only moving 1 in this example)
                hr = pObjectsToMove->Add(&pv);
                if (SUCCEEDED(hr))
                {
                    // Attempt to move the object on the device
                    hr = pContent->Move(pObjectsToMove,               // Object(s) to move
                                        wszDestinationFolderObjectID, // Folder to move to
                                        NULL);                        // Object(s) that failed to delete (we are only moving 1, so we can pass NULL here)
                    if (SUCCEEDED(hr))
                    {
                        // An S_OK return lets the caller know that the deletion was successful
                        if (hr == S_OK)
                        {
                            printf("The object '%ws' was moved on the device.\n", wszSelection);
                        }

                        // An S_FALSE return lets the caller know that the move failed.
                        // The caller should check the returned IPortableDevicePropVariantCollection
                        // for a list of object identifiers that failed to be moved.
                        else
                        {
                            printf("The object '%ws' failed to be moved on the device.\n", wszSelection);
                        }
                    }
                    else
                    {
                        printf("! Failed to move an object on the device, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to move an object on the device because we could no add the object identifier string to the IPortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
                }
            }
            else
            {
                hr = E_OUTOFMEMORY;
                printf("! Failed to move an object on the device because we could no allocate memory for the object identifier string, hr = 0x%lx\n",hr);
            }

            // Free any allocated values in the PROPVARIANT before exiting
            PropVariantClear(&pv);
        }
        else
        {
            printf("! Failed to move an object from the device because we were returned a NULL IPortableDevicePropVariantCollection interface pointer, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to CoCreateInstance CLSID_PortableDevicePropVariantCollection, hr = 0x%lx\n",hr);
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDevicePropVariantCollection-Schnittstelle**](iportabledevicepropvariantcollection.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



