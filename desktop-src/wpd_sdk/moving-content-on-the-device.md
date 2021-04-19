---
description: Verschieben von Inhalt auf dem Gerät
ms.assetid: 5072d308-d376-4141-96df-dbef23fb9f9b
title: Verschieben von Inhalt auf dem Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eb4a9638e656d5cab8437448d64b79947df337b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363546"
---
# <a name="moving-content-on-the-device"></a><span data-ttu-id="ca353-103">Verschieben von Inhalt auf dem Gerät</span><span class="sxs-lookup"><span data-stu-id="ca353-103">Moving Content on the Device</span></span>

<span data-ttu-id="ca353-104">Ein weiterer häufiger Vorgang, der von einer WPD-Anwendung ausgeführt wird, ist die Übertragung von Inhalt von einem Speicherort auf dem Gerät zu einem anderen.</span><span class="sxs-lookup"><span data-stu-id="ca353-104">Another common operation accomplished by a WPD application is the transfer of content from one location on the device to another.</span></span>

<span data-ttu-id="ca353-105">Vorgänge zum Verschieben von Inhalten werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca353-105">Content move operations are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="ca353-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ca353-106">Interface</span></span>                                                                                      | <span data-ttu-id="ca353-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ca353-107">Description</span></span>                                       |
|------------------------------------------------------------------------------------------------|---------------------------------------------------|
| [<span data-ttu-id="ca353-108">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca353-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                             | <span data-ttu-id="ca353-109">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="ca353-109">Provides access to the content-specific methods.</span></span>  |
| [<span data-ttu-id="ca353-110">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca353-110">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md) | <span data-ttu-id="ca353-111">Bietet Zugriff auf die Eigenschaften spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="ca353-111">Provides access to the property-specific methods.</span></span> |



 

<span data-ttu-id="ca353-112">Die Funktion movecontentalleseyondevice im Modul contenttransfer. cpp der Beispielanwendung veranschaulicht, wie eine Anwendung Inhalte von einem Speicherort zu einem anderen verschieben kann.</span><span class="sxs-lookup"><span data-stu-id="ca353-112">The MoveContentAlreadyOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application can move content from one location to another.</span></span>

<span data-ttu-id="ca353-113">Die erste Aufgabe, die von der Funktion "muvecontentalleseyondevice" durchgeführt wird, besteht darin, den Gerätetreiber abzufragen, um festzustellen, ob die Inhalts Verschiebung</span><span class="sxs-lookup"><span data-stu-id="ca353-113">The first task accomplished by the MoveContentAlreadyOnDevice function is to query the device driver to see whether it supports content movement.</span></span> <span data-ttu-id="ca353-114">Dies wird erreicht, indem die Hilfsfunktion supportscommand aufgerufen und WPD \_ Command \_ Object \_ Management \_ Move \_ Objects als zweites Argument übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="ca353-114">This is accomplished by calling the SupportsCommand helper function and passing WPD\_COMMAND\_OBJECT\_MANAGEMENT\_MOVE\_OBJECTS as the second argument.</span></span>


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



<span data-ttu-id="ca353-115">Der nächste Schritt erfordert, dass der Benutzer aufgefordert wird, zwei Objekt Bezeichner einzugeben.</span><span class="sxs-lookup"><span data-stu-id="ca353-115">The next step entails prompting the user to enter two object identifiers.</span></span> <span data-ttu-id="ca353-116">Der erste ist der Bezeichner für den Inhalt, der verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ca353-116">The first is the identifier for the content that will be moved.</span></span> <span data-ttu-id="ca353-117">Die zweite ist der Bezeichner für den Speicherort, an den die Anwendung diesen Inhalt verschieben soll.</span><span class="sxs-lookup"><span data-stu-id="ca353-117">The second is the identifier for the location to which the application should move this content.</span></span>


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



<span data-ttu-id="ca353-118">Als nächstes Ruft das Beispiel ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt ab, das für den Zugriff auf die [**iportabledevicecontent:: Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) -Methode verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ca353-118">Next, the sample retrieves an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object that is used to access the [**IPortableDeviceContent::Move**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-move) method.</span></span>


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



<span data-ttu-id="ca353-119">Schließlich wird der Inhalt verschoben.</span><span class="sxs-lookup"><span data-stu-id="ca353-119">Finally, the content is moved.</span></span> <span data-ttu-id="ca353-120">Dieser Vorgang umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ca353-120">This process involves the following:</span></span>

1.  <span data-ttu-id="ca353-121">Erstellen eines [**iportabledevicepropvariantcollection**](iportabledevicepropvariantcollection.md) -Objekts, das eine PROPVARIANT-Struktur für das zu bewegende Objekt empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca353-121">Creating an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) object that receives a PROPVARIANT structure for the object to be moved.</span></span>
2.  <span data-ttu-id="ca353-122">Das PROPVARIANT-Objekt wird dem iportabledevicepropvariantcollection-Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ca353-122">Adding the PROPVARIANT to the IPortableDevicePropVariantCollection object.</span></span>
3.  <span data-ttu-id="ca353-123">Aufrufen der iportabledevicecontent:: Move-Methode.</span><span class="sxs-lookup"><span data-stu-id="ca353-123">Invoking the IPortableDeviceContent::Move method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="ca353-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca353-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca353-125">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca353-125">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="ca353-126">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca353-126">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="ca353-127">**Iportabledevicepropvariantcollection-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="ca353-127">**IPortableDevicePropVariantCollection Interface**</span></span>](iportabledevicepropvariantcollection.md)
</dt> <dt>

[<span data-ttu-id="ca353-128">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="ca353-128">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



