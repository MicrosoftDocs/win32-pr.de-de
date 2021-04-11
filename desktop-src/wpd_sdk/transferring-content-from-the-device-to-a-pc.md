---
description: Übertragen von Inhalt vom Gerät an einen PC
ms.assetid: 76069097-a513-42f7-bdcc-a65714e95f0a
title: Übertragen von Inhalt vom Gerät an einen PC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de06861ba74b4b7883c8d96e25cebe3fbb64e21c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217504"
---
# <a name="transferring-content-from-the-device-to-a-pc"></a><span data-ttu-id="a97bc-103">Übertragen von Inhalt vom Gerät an einen PC</span><span class="sxs-lookup"><span data-stu-id="a97bc-103">Transferring Content from the Device to a PC</span></span>

<span data-ttu-id="a97bc-104">Ein gängiger Vorgang, der von einer WPD-Anwendung ausgeführt wird, ist die Übertragung von Inhalt von einem verbundenen Gerät auf den PC.</span><span class="sxs-lookup"><span data-stu-id="a97bc-104">One common operation accomplished by a WPD application is the transfer of content from a connected device to the PC.</span></span>

<span data-ttu-id="a97bc-105">Inhalts Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.</span><span class="sxs-lookup"><span data-stu-id="a97bc-105">Content transfers are accomplished using the interfaces described in the following table.</span></span>



| <span data-ttu-id="a97bc-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a97bc-106">Interface</span></span>                                                                | <span data-ttu-id="a97bc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a97bc-107">Description</span></span>                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="a97bc-108">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-108">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | <span data-ttu-id="a97bc-109">Bietet Zugriff auf die **iportabledeviceproperties** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="a97bc-109">Provides access to the **IPortableDeviceProperties** interface.</span></span> |
| [<span data-ttu-id="a97bc-110">**Iportabledeviceproperties-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-110">**IPortableDeviceProperties Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | <span data-ttu-id="a97bc-111">Ermöglicht den Zugriff auf Eigenschaften spezifische Methoden.</span><span class="sxs-lookup"><span data-stu-id="a97bc-111">Provides access to property-specific methods.</span></span>                   |
| [<span data-ttu-id="a97bc-112">**Iportabledeviceresources-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-112">**IPortableDeviceResources Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | <span data-ttu-id="a97bc-113">Wird verwendet, um die Eigenschafts Schlüssel für das angegebene Profil zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a97bc-113">Used to store the property keys for the given profile.</span></span>          |
| <span data-ttu-id="a97bc-114">IStream-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a97bc-114">IStream Interface</span></span>                                                        | <span data-ttu-id="a97bc-115">Wird verwendet, um die Daten zu lesen und zu schreiben.</span><span class="sxs-lookup"><span data-stu-id="a97bc-115">Used to read and write the data.</span></span>                                |



 

<span data-ttu-id="a97bc-116">Die `TransferContentFromDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Kontaktinformationen von einem verbundenen Gerät an einen PC übertragen könnte.</span><span class="sxs-lookup"><span data-stu-id="a97bc-116">The `TransferContentFromDevice` function in the sample application's ContentTransfer.cpp module demonstrates how an application could transfer contact information from a connected device to a PC.</span></span>

<span data-ttu-id="a97bc-117">Die erste Aufgabe, die von der- `TransferContentFromDevice` Funktion ausgeführt wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das übergeordnete Objekt auf dem Gerät aufzufordern (unter dem der Inhalt übertragen wird).</span><span class="sxs-lookup"><span data-stu-id="a97bc-117">The first task accomplished by the `TransferContentFromDevice` function is to prompt the user to enter an object identifier for the parent object on the device (under which the content will be transferred).</span></span>


```C++
HRESULT                            hr                   = S_OK;
WCHAR                              szSelection[81]      = {0};
CComPtr<IPortableDeviceContent>    pContent;
CComPtr<IPortableDeviceResources>  pResources;
CComPtr<IPortableDeviceProperties> pProperties;
CComPtr<IStream>                   pObjectDataStream;
CComPtr<IStream>                   pFinalFileStream;
DWORD                              cbOptimalTransferSize = 0;
CAtlStringW                        strOriginalFileName;

if (pDevice == NULL)
{
    printf("! A NULL IPortableDevice interface pointer was received\n");
    return;
}


// Prompt user to enter an object identifier on the device to transfer.
printf("Enter the identifer of the object you wish to transfer.\n>");
hr = StringCbGetsW(szSelection,sizeof(szSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting content transfer\n");
}
```



<span data-ttu-id="a97bc-118">Der nächste Schritt ist das Abrufen eines **iportabledevicecontent** -Objekts, das im Beispiel für den Zugriff auf die Inhalts spezifischen Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a97bc-118">The next step is the retrieval of an **IPortableDeviceContent** object that the sample uses to access the content-specific methods.</span></span>


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



<span data-ttu-id="a97bc-119">Der nächste Schritt ist das Abrufen eines **iportabledeviceresources** -Objekts, das im Beispiel für den Zugriff auf die Ressourcen spezifischen Methoden verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a97bc-119">The next step is the retrieval of an **IPortableDeviceResources** object that the sample uses to access the resource-specific methods.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="a97bc-120">Der nächste Schritt ist das Abrufen eines IStream-Objekts, das im Beispiel verwendet wird, um die Daten zu lesen, die es vom Gerät überträgt.</span><span class="sxs-lookup"><span data-stu-id="a97bc-120">The next step is the retrieval of an IStream object that the sample uses to read the data it is transferring from the device.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pResources->GetStream(szSelection,             // Identifier of the object we want to transfer
                               WPD_RESOURCE_DEFAULT,    // We are transferring the default resource (which is the entire object's data)
                               STGM_READ,               // Opening a stream in READ mode, because we are reading data from the device.
                               &cbOptimalTransferSize,  // Driver supplied optimal transfer size
                               &pObjectDataStream);
    if (FAILED(hr))
    {
        printf("! Failed to get IStream (representing object data on the device) from IPortableDeviceResources, hr = 0x%lx\n",hr);
    }
}
```



<span data-ttu-id="a97bc-121">Der nächste Schritt ist das Abrufen des Datei namens des Objekts auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="a97bc-121">The next step is the retrieval of the object's file name on the device.</span></span> <span data-ttu-id="a97bc-122">Diese Zeichenfolge wird zum Erstellen des entsprechenden Datei namens auf dem PC verwendet.</span><span class="sxs-lookup"><span data-stu-id="a97bc-122">This string is used to create the corresponding file name on the PC.</span></span> <span data-ttu-id="a97bc-123">Wenn das Objekt keinen Dateinamen auf dem Gerät hat, wird der Bezeichner des Objekts in eine Zeichenfolge konvertiert und zum Erstellen des Ziel Dateinamens verwendet.</span><span class="sxs-lookup"><span data-stu-id="a97bc-123">If the object does not have a file name on the device, the object's identifier is converted to a string and used to create the destination file name.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = pContent->Properties(&pProperties);
    if (SUCCEEDED(hr))
    {
        hr = GetStringValue(pProperties,
                            szSelection,
                            WPD_OBJECT_ORIGINAL_FILE_NAME,
                            strOriginalFileName);
        if (FAILED(hr))
        {
            printf("! Failed to read WPD_OBJECT_ORIGINAL_FILE_NAME on object '%ws', hr = 0x%lx\n", szSelection, hr);
            strOriginalFileName.Format(L"%ws.data", szSelection);
            printf("* Creating a filename '%ws' as a default.\n", (PWSTR)strOriginalFileName.GetString());
            // Set the HRESULT to S_OK, so we can continue with our newly generated
            // temporary file name.
            hr = S_OK;
        }
    }
    else
    {
        printf("! Failed to get IPortableDeviceProperties from IPortableDeviceContent, hr = 0x%lx\n", hr);
    }
}
```



<span data-ttu-id="a97bc-124">Danach erstellt das Beispiel ein IStream-Zielobjekt.</span><span class="sxs-lookup"><span data-stu-id="a97bc-124">After this, the sample creates a destination IStream object.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = SHCreateStreamOnFile(strOriginalFileName, STGM_CREATE|STGM_WRITE, &pFinalFileStream);
    if (FAILED(hr))
    {
        printf("! Failed to create a temporary file named (%ws) to transfer object (%ws), hr = 0x%lx\n",(PWSTR)strOriginalFileName.GetString(), szSelection, hr);
    }
}
```



<span data-ttu-id="a97bc-125">Schließlich wird das Quell-IStream-Objekt in das Ziel auf dem PC kopiert.</span><span class="sxs-lookup"><span data-stu-id="a97bc-125">Finally, the source IStream object is copied to the destination on the PC.</span></span>


```C++
if (SUCCEEDED(hr))
{
    DWORD cbTotalBytesWritten = 0;

    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    hr = StreamCopy(pFinalFileStream,       // Destination (The Final File to transfer to)
                    pObjectDataStream,      // Source (The Object's data to transfer from)
                    cbOptimalTransferSize,  // The driver specified optimal transfer buffer size
                    &cbTotalBytesWritten);  // The total number of bytes transferred from device to the finished file
    if (FAILED(hr))
    {
        printf("! Failed to transfer object from device, hr = 0x%lx\n",hr);
    }
    else
    {
        printf("* Transferred object '%ws' to '%ws'.\n", szSelection, (PWSTR)strOriginalFileName.GetString());
    }
}
```



## <a name="related-topics"></a><span data-ttu-id="a97bc-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a97bc-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a97bc-127">**Iportabledevice-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-127">**IPortableDevice Interface**</span></span>](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[<span data-ttu-id="a97bc-128">**Iportabledevicecontent-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-128">**IPortableDeviceContent Interface**</span></span>](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[<span data-ttu-id="a97bc-129">**Iportabledebug-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="a97bc-129">**IPortableDeviceValues Interface**</span></span>](iportabledevicevalues.md)
</dt> <dt>

[<span data-ttu-id="a97bc-130">**Programmierhandbuch**</span><span class="sxs-lookup"><span data-stu-id="a97bc-130">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 



