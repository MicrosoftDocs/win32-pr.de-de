---
description: Hinzufügen einer Ressource zu einem Objekt
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: Hinzufügen einer Ressource zu einem Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 869b5cdcf172c4b8f27f7081bfce8e6f05073789
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346588"
---
# <a name="adding-a-resource-to-an-object"></a><span data-ttu-id="165a3-103">Hinzufügen einer Ressource zu einem Objekt</span><span class="sxs-lookup"><span data-stu-id="165a3-103">Adding a Resource to an Object</span></span>

<span data-ttu-id="165a3-104">Zusätzlich zum Übertragen von Objekten an ein Gerät ist es auch möglich, Ressourcen zu Objekten hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="165a3-104">In addition to transferring objects to a device, it's also possible to add resources to objects.</span></span> <span data-ttu-id="165a3-105">Beispielsweise könnte eine Anwendung vorhandenen Informationen für einen bestimmten Kontakt ein Foto hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="165a3-105">For example, an application could add a photo to existing information for a given contact.</span></span>

<span data-ttu-id="165a3-106">Ressourcen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="165a3-106">Resources are added using the interfaces described in the following table.</span></span>



| <span data-ttu-id="165a3-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="165a3-107">Interface</span></span>                                                              | <span data-ttu-id="165a3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="165a3-108">Description</span></span>                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="165a3-109">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-109">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | <span data-ttu-id="165a3-110">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="165a3-110">Provides access to the content-specific methods.</span></span>                  |
| [<span data-ttu-id="165a3-111">**Iportabledeviceresources-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-111">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | <span data-ttu-id="165a3-112">Wird beim Schreiben der Ressourcen Eigenschaften und-Daten auf das Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="165a3-112">Used when writing the resource properties and data to the device.</span></span> |
| [<span data-ttu-id="165a3-113">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-113">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)       | <span data-ttu-id="165a3-114">Wird zum Schreiben von Eigenschaften verwendet, die die Ressource beschreiben.</span><span class="sxs-lookup"><span data-stu-id="165a3-114">Used to write properties that describe the resource.</span></span>              |
| <span data-ttu-id="165a3-115">IStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="165a3-115">IStream Interface</span></span>                                                      | <span data-ttu-id="165a3-116">Wird verwendet, um das Schreiben der Ressource auf das Gerät zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="165a3-116">Used to simplify writing the resource to the device.</span></span>              |



 

<span data-ttu-id="165a3-117">Die Funktion "Funktion" in der Funktion "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung einem Kontakt Objekt eine Foto Ressource hinzufügen kann.</span><span class="sxs-lookup"><span data-stu-id="165a3-117">The CreateContactPhotoResourceOnDevice function in the sample application's ContentTransfer.cpp module demonstrates how an application could add a photo resource to a contact object.</span></span> <span data-ttu-id="165a3-118">Diese Funktion fordert den Benutzer zur Eingabe des Objekt Bezeichners des Kontakts auf dem Gerät auf, dem die Foto Ressource hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="165a3-118">This function prompts the user for the object identifier of the contact on the device, to which the photo resource will be added.</span></span> <span data-ttu-id="165a3-119">Daraufhin wird das Dialogfeld FileOpen angezeigt, in dem der Benutzer das hinzu zufügende Bild auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="165a3-119">Then it displays a FileOpen dialog box so that the user can select the image to be added.</span></span> <span data-ttu-id="165a3-120">Nachdem diese Daten gesammelt wurden, schreibt die Anwendung die Ressource auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="165a3-120">Once this data is collected, the application writes the resource to the device.</span></span>

<span data-ttu-id="165a3-121">Die erste Aufgabe, die von der Funktion "" mit der Funktion "" mit der Funktion "" erstellt wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für den Kontakt aufzufordern, dem das Foto hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="165a3-121">The first task accomplished by the CreateContactPhotoResourceOnDevice function is to prompt the user to enter an object identifier for the contact to which the photo will be added.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



<span data-ttu-id="165a3-122">Der nächste Schritt ist das Abrufen eines [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekts, das wiederum zum Abrufen eines [**iportabledeviceresources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) -Objekts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="165a3-122">The next step is the retrieval of an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object, which in turn is used to obtain an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object.</span></span> <span data-ttu-id="165a3-123">(Die Anwendung verwendet dieses letztere Objekt, um die neue Ressource zu erstellen und zu schreiben.)</span><span class="sxs-lookup"><span data-stu-id="165a3-123">(The application uses this latter object to create and write the new resource.)</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
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
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="165a3-124">Anschließend wird im Beispiel das Dialogfeld **FileOpen** angezeigt, das es dem Benutzer ermöglicht, den Namen der Bilddatei anzugeben, die das Foto enthält, das Sie den Kontaktinformationen hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="165a3-124">After this, the sample displays the **FileOpen** dialog box, which allows the user to specify the name of the image file that contains the photo they want to add to the contact information.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="165a3-125">Wenn das Beispiel ein [**iportabledeviceresources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) -Objekt und den Namen der Bilddatei enthält, werden die folgenden Schritte in Vorbereitung für die eigentliche Übertragung von Daten auf das Gerät durchführen.</span><span class="sxs-lookup"><span data-stu-id="165a3-125">Once the sample has an [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) object and the name of the image file, it does the following in preparation for actually transferring data to the device.</span></span>

1.  <span data-ttu-id="165a3-126">Er öffnet ein IStream-Objekt für die ausgewählte Datei für Lesevorgänge.</span><span class="sxs-lookup"><span data-stu-id="165a3-126">It opens an IStream object on the selected file for read operations.</span></span>
2.  <span data-ttu-id="165a3-127">Es wird ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt erstellt, das Informationen wie die Bildgröße und das Bildformat enthält.</span><span class="sxs-lookup"><span data-stu-id="165a3-127">It creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, which will contain information such as the image size and format.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



<span data-ttu-id="165a3-128">Nach der Vorbereitung der IStream-und [**iportabledevicevalues**](iportabledevicevalues.md) -Objekte für den Schreibvorgang überträgt das Beispiel das Image auf das Gerät.</span><span class="sxs-lookup"><span data-stu-id="165a3-128">After preparing the IStream and [**IPortableDeviceValues**](iportabledevicevalues.md) objects for the write operation, the sample transfers the image to the device.</span></span> <span data-ttu-id="165a3-129">Im Beispiel wird die Übertragung in drei Schritten wie folgt abgeschlossen:</span><span class="sxs-lookup"><span data-stu-id="165a3-129">The sample completes the transfer in three steps, as follows:</span></span>

1.  <span data-ttu-id="165a3-130">Die Ressource wird auf dem Gerät erstellt, indem die [**iportabledeviceresources:: CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="165a3-130">It creates the resource on the device by calling the [**IPortableDeviceResources::CreateResource**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource) method.</span></span>
2.  <span data-ttu-id="165a3-131">Er ruft eine streamcopy-Hilfsfunktion auf, um den Quelldaten Strom in den Zielstream zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="165a3-131">It calls a StreamCopy helper function to copy the source stream to the destination stream.</span></span>
3.  <span data-ttu-id="165a3-132">Der Gerätetreiber wird informiert, dass die Übertragung durch Aufrufen der iportabledevicedatastream:: Commit-Methode beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="165a3-132">It informs the device driver that the transfer is complete by calling the IPortableDeviceDataStream::Commit method.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
                        pFileStream,            // Source (The File data to transfer from)
                        cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                        &cbTotalBytesWritten);  // The total number of bytes transferred from file to the device
        if (FAILED(hr))
        {
            printf("! Failed to transfer object to device, hr = 0x%lx\n",hr);
        }
    }
    else
    {
        printf("! Failed to get IStream (representing destination object data on the device) from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }

    // After transferring content to the device, the client is responsible for letting the
    // driver know that the transfer is complete by calling the Commit() method
    // on the IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="165a3-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="165a3-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="165a3-134">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-134">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="165a3-135">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-135">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="165a3-136">**Iportabledeviceresources-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-136">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[<span data-ttu-id="165a3-137">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="165a3-137">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="165a3-138">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="165a3-138">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



