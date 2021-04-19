---
description: Übertragen einer Bild-oder Musikdatei auf das Gerät
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Übertragen einer Bild-oder Musikdatei auf das Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f3308212825f6c67ea79a40873fc466164d62f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362616"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a><span data-ttu-id="e2c6b-103">Übertragen einer Bild-oder Musikdatei auf das Gerät</span><span class="sxs-lookup"><span data-stu-id="e2c6b-103">Transferring an Image or Music File to the Device</span></span>

<span data-ttu-id="e2c6b-104">Eine der gängigsten Vorgänge, die von einer Anwendung durchgeführt werden, ist die Übertragung von Inhalt auf ein verbundenes Gerät.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-104">One of the most common operations accomplished by an application is the transfer of content to a connected device.</span></span>

<span data-ttu-id="e2c6b-105">Inhalts Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="e2c6b-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e2c6b-106">Interface</span></span>                                                                | <span data-ttu-id="e2c6b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e2c6b-107">Description</span></span>                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="e2c6b-108">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="e2c6b-109">Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-109">Provides access to the content-specific methods.</span></span>               |
| [<span data-ttu-id="e2c6b-110">**Iportabledevicedatastream-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-110">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | <span data-ttu-id="e2c6b-111">Wird beim Schreiben des Inhalts auf das Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-111">Used when writing the content to the device.</span></span>                   |
| [<span data-ttu-id="e2c6b-112">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-112">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)         | <span data-ttu-id="e2c6b-113">Dient zum Abrufen von Eigenschaften, die den Inhalt beschreiben.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-113">Used to retrieve properties that describe the content.</span></span>         |
| <span data-ttu-id="e2c6b-114">IStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e2c6b-114">IStream Interface</span></span>                                                        | <span data-ttu-id="e2c6b-115">Wird verwendet, um das Lesen von Inhalten und das Schreiben auf das Gerät zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-115">Used to simplify reading of content and writing to the device.</span></span> |



 

<span data-ttu-id="e2c6b-116">Die `TransferContentToDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Inhalte von einem PC an ein verbundenes Gerät übertragen könnte.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-116">The `TransferContentToDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer content from a PC to a connected device.</span></span> <span data-ttu-id="e2c6b-117">In diesem speziellen Beispiel kann der übertragene Inhalt eine Datei sein, die ein Bild, eine Musik oder Kontaktinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-117">In this particular sample, the transferred content can be a file containing an image, music, or contact information.</span></span>

<span data-ttu-id="e2c6b-118">Die erste Aufgabe, die von der-Funktion durchgeführt wird, besteht darin, `TransferContentToDevice` den Benutzer zur Eingabe eines Objekt Bezeichners aufzufordern, der das zu übertragende Objekt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-118">The first task accomplished by the `TransferContentToDevice` function is to prompt the user to enter an object identifier, which identifies the object to be transferred.</span></span>


```C++
HRESULT                             hr = S_OK;
WCHAR                               szSelection[81]        = {0};
WCHAR                               szFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IPortableDeviceDataStream>  pFinalObjectDataStream;
CComPtr<IPortableDeviceValues>      pFinalObjectProperties;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IStream>                    pTempStream;  // Temporary IStream which we use to QI for IPortableDeviceDataStream

// Prompt user to enter an object identifier for the parent object on the device to transfer.
printf("Enter the identifer of the parent object which the file will be transferred under.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="e2c6b-119">Die zweite Aufgabe, die von der-Funktion durchgeführt `TransferContentToDevice` wird, besteht darin, ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt durch Aufrufen der [**iportabledevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) -Methode zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-119">The second task accomplished by the `TransferContentToDevice` function is to create an [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) object by calling the [**IPortableDevice::Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) method.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="e2c6b-120">Die nächste Aufgabe, die von der-Funktion durchgeführt `TransferContentToDevice` wird, ist die Erstellung eines **FileOpen** -Dialog Felds, in dem der Benutzer den Speicherort und den Namen der zu übertragenden Datei angeben kann.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-120">The next task accomplished by the `TransferContentToDevice` function is the creation of a **FileOpen** dialog with which the user can specify the location and name of the file to be transferred.</span></span>


```C++
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = szFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(szFilePath);
    OpenFileNameInfo.lpstrFilter    = pszFileTypeFilter;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = pszDefaultFileExtension;

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was canceled.\n");
        hr = E_ABORT;
    }
}
```



<span data-ttu-id="e2c6b-121">Die- `TransferContentToDevice` Funktion übergibt eine Filter Zeichenfolge ( `wszFileTypeFilter` ) an die GetOpenFileName-Methode, die den Typ der Dateien bestimmt, die der Benutzer auswählen kann.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-121">The `TransferContentToDevice` function passes a filter string (`wszFileTypeFilter`) to the GetOpenFileName method, which determines the type of files that the user can choose.</span></span> <span data-ttu-id="e2c6b-122">`DoMenu`Im Modul wpdapisample. cpp finden Sie Beispiele für die drei verschiedenen Filter, die im Beispiel zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-122">Refer to the `DoMenu` function in the WpdApiSample.cpp module for examples of the three different filters allowed by the sample.</span></span>

<span data-ttu-id="e2c6b-123">Nachdem der Benutzer eine bestimmte Datei für die Übertragung an das Gerät identifiziert hat, `TransferContentToDevice` öffnet die Funktion diese Datei als IStream-Objekt und ruft die zum Abschluss der Übertragung erforderlichen Eigenschaften ab.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-123">After the user identifies a particular file for transfer to the device, the `TransferContentToDevice` function opens that file as an IStream object and retrieves properties that are required to complete the transfer.</span></span>


```C++
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(szFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // Get the required properties needed to properly describe the data being
        // transferred to the device.
        hr = GetRequiredPropertiesForContentType(guidContentType,           // Content type of the data
                                                 szSelection,              // Parent to transfer the data under
                                                 szFilePath,               // Full file path to the data file
                                                 pFileStream,               // Open IStream that contains the data
                                                 &pFinalObjectProperties);  // Returned properties describing the data
        if (FAILED(hr))
        {
            printf("! Failed to get required properties needed to transfer a file to the device, hr = 0x%lx\n", hr);
        }
    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",szFilePath, hr);
    }
}
```



<span data-ttu-id="e2c6b-124">Die erforderlichen Eigenschaften werden abgerufen, indem die `GetRequiredPropertiesForContentType` Hilfsfunktion aufgerufen wird, die für das IStream-Objekt gilt.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-124">The required properties are retrieved by calling the`GetRequiredPropertiesForContentType` helper-function, which operates on the IStream object.</span></span> <span data-ttu-id="e2c6b-125">Die `GetRequiredPropertiesForContentType` -Hilfsfunktion erstellt ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, ruft die Eigenschaften in der folgenden Liste ab und fügt diese diesem-Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-125">The `GetRequiredPropertiesForContentType` helper-function creates an [**IPortableDeviceValues**](iportabledevicevalues.md) object, retrieves the properties in the following list, and adds them to this object.</span></span>

-   <span data-ttu-id="e2c6b-126">Übergeordnete Objekt Kennung</span><span class="sxs-lookup"><span data-stu-id="e2c6b-126">Parent-object identifier</span></span>
-   <span data-ttu-id="e2c6b-127">Streamgröße in Bytes</span><span class="sxs-lookup"><span data-stu-id="e2c6b-127">Stream size in bytes</span></span>
-   <span data-ttu-id="e2c6b-128">Name der Inhalts Datei</span><span class="sxs-lookup"><span data-stu-id="e2c6b-128">Content file name</span></span>
-   <span data-ttu-id="e2c6b-129">Inhalts Name (der Dateiname ohne Erweiterung)</span><span class="sxs-lookup"><span data-stu-id="e2c6b-129">Content name (the file name without the extension)</span></span>
-   <span data-ttu-id="e2c6b-130">Inhaltstyp (Bild, Audiodatei oder Kontakt)</span><span class="sxs-lookup"><span data-stu-id="e2c6b-130">Content type (image, audio, or contact)</span></span>
-   <span data-ttu-id="e2c6b-131">Inhalts Format (jff, WMA oder vCard2)</span><span class="sxs-lookup"><span data-stu-id="e2c6b-131">Content format (JFIF, WMA, or vCard2)</span></span>

<span data-ttu-id="e2c6b-132">Die Beispielanwendung verwendet die abgerufenen Eigenschaften, um den neuen Inhalt auf dem Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-132">The sample application uses the retrieved properties to create the new content on the device.</span></span> <span data-ttu-id="e2c6b-133">Dies erfolgt in drei Phasen:</span><span class="sxs-lookup"><span data-stu-id="e2c6b-133">This is done in three phases:</span></span>

1.  <span data-ttu-id="e2c6b-134">Die Anwendung ruft die [**iportabledevicecontent:: | ateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) -Methode auf, um ein neues IStream-Objekt auf dem Gerät zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-134">The application calls [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) method to create a new IStream object on the device.</span></span>
2.  <span data-ttu-id="e2c6b-135">Die Anwendung verwendet dieses Objekt, um ein [**iportabledevicedatastream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) -Objekt aus dem WPD-Treiber abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-135">The application uses this object to obtain an [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) object from the WPD driver.</span></span>
3.  <span data-ttu-id="e2c6b-136">Die Anwendung verwendet das neue **iportabledevicedatastream** -Objekt, um den Inhalt auf das Gerät zu schreiben (über die streamcopy-Hilfsfunktion).</span><span class="sxs-lookup"><span data-stu-id="e2c6b-136">The application uses the new **IPortableDeviceDataStream** object to write the content to the device (via the StreamCopy helper function).</span></span> <span data-ttu-id="e2c6b-137">Die Hilfsfunktion schreibt die Daten aus der Quelldatei in den Datenstrom, der von [**iportabledevicecontent:: | ateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-137">The helper function writes the data from the source file to the stream returned by [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span>
4.  <span data-ttu-id="e2c6b-138">Die Anwendung schließt den Vorgang ab, indem Sie die Commit-Methode für den Zielstream aufruft.</span><span class="sxs-lookup"><span data-stu-id="e2c6b-138">The application completes the operation by calling the Commit method on the destination stream.</span></span>


```C++
// 4) Transfer for the content to the device
if (SUCCEEDED(hr))
{
    hr = pContent->CreateObjectWithPropertiesAndData(pFinalObjectProperties,    // Properties describing the object data
                                                     &pTempStream,              // Returned object data stream (to transfer the data to)
                                                     &cbOptimalTransferSize,    // Returned optimal buffer size to use during transfer
                                                     NULL);

    // Once we have a the IStream returned from CreateObjectWithPropertiesAndData,
    // QI for IPortableDeviceDataStream so we can use the additional methods
    // to get more information about the object (i.e. The newly created object
    // identifier on the device)
    if (SUCCEEDED(hr))
    {
        hr = pTempStream->QueryInterface(IID_PPV_ARGS(&pFinalObjectDataStream));
        if (FAILED(hr))
        {
            printf("! Failed to QueryInterface for IPortableDeviceDataStream, hr = 0x%lx\n",hr);
        }
    }

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pFinalObjectDataStream, // Destination (The Object to transfer to)
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
        hr = pFinalObjectDataStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit object to device, hr = 0x%lx\n",hr);
        }
    }

    // Some clients may want to know the object identifier of the newly created
    // object.  This is done by calling GetObjectID() method on the
    // IPortableDeviceDataStream interface.
    if (SUCCEEDED(hr))
    {
        PWSTR pszNewlyCreatedObject = NULL;
        hr = pFinalObjectDataStream->GetObjectID(&pszNewlyCreatedObject);
        if (SUCCEEDED(hr))
        {
            printf("The file '%ws' was transferred to the device.\nThe newly created object's ID is '%ws'\n",szFilePath ,pszNewlyCreatedObject);
        }

        if (FAILED(hr))
        {
            printf("! Failed to get the newly transferred object's identifier from the device, hr = 0x%lx\n",hr);
        }

        // Free the object identifier string returned from the GetObjectID() method.
        CoTaskMemFree(pszNewlyCreatedObject);
        pszNewlyCreatedObject = NULL;
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="e2c6b-139">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2c6b-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c6b-140">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-140">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="e2c6b-141">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-141">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="e2c6b-142">**Iportabledevicedatastream-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-142">**IPortableDeviceDataStream Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[<span data-ttu-id="e2c6b-143">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-143">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="e2c6b-144">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="e2c6b-144">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



