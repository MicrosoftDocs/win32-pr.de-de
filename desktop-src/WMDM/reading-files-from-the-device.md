---
title: Lesen von Dateien vom Gerät
description: Lesen von Dateien vom Gerät
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Media Device Manager, Lesen von Dateien von Geräten
- Device Manager, Lesen von Dateien von Geräten
- Programmier Handbuch, Lesen von Dateien von Geräten
- Desktop Anwendungen, Lesen von Dateien von Geräten
- Erstellen von Windows Media Device Manager-Anwendungen, Lesen von Dateien von Geräten
- Lesen von Dateien von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0b80cf820e889b29e612206f90b07e1cb02c4c7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104206401"
---
# <a name="reading-files-from-the-device"></a><span data-ttu-id="f60a8-109">Lesen von Dateien vom Gerät</span><span class="sxs-lookup"><span data-stu-id="f60a8-109">Reading Files from the Device</span></span>

<span data-ttu-id="f60a8-110">Wenn Sie eine Datei gefunden haben, die Sie vom Gerät kopieren möchten, können Sie die Datei mit einem einzigen-Befehl vom Gerät auf den Computer kopieren oder einen Rückruf verwenden, damit die Datei Bytes direkt in die Anwendung gelesen werden. auf diese Weise können die Daten nach Bedarf verarbeitet oder gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f60a8-110">When you have found a file you would like to copy from the device, you can then copy the file from the device to the computer in a single call, or use a callback to have the file bytes read directly to your application, which can then process or store the data as it sees fits.</span></span>

<span data-ttu-id="f60a8-111">Die folgenden Schritte zeigen die grundlegende Methode zum Kopieren einer Datei von einem Gerät in einem einzelnen-Befehl:</span><span class="sxs-lookup"><span data-stu-id="f60a8-111">The following steps show the basic way to copy a file from a device in a single call:</span></span>

1.  <span data-ttu-id="f60a8-112">Erhalten Sie ein Handle für die Datei auf dem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f60a8-112">Get a handle to the file on the device.</span></span> <span data-ttu-id="f60a8-113">Sie können das Handle über eine rekursive Dateisuche oder, wenn Sie die persistente ID des Speichers kennen, durch Aufrufen von [**IWMDMDevice3:: findstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage)abrufen.</span><span class="sxs-lookup"><span data-stu-id="f60a8-113">You might obtain the handle by using a recursive file search or, if you know the persistent ID of the storage, by calling [**IWMDMDevice3::FindStorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage).</span></span> <span data-ttu-id="f60a8-114">In beiden Fällen benötigen Sie die [**iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) -Schnittstelle des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="f60a8-114">In either case, you need the [**IWMDMStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) interface of the object.</span></span>
2.  <span data-ttu-id="f60a8-115">Bestimmen Sie, ob es sich beim Speicher um eine Datei oder einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="f60a8-115">Determine whether the storage is a file or a folder.</span></span> <span data-ttu-id="f60a8-116">Nur Dateien können vom Gerät kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="f60a8-116">Only files can be copied from the device.</span></span> <span data-ttu-id="f60a8-117">Aufrufen von [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) zum Abrufen von Speicher Attributen, die Aufschluss darüber geben, ob es sich bei dem Speicher um eine Datei oder einen Ordner handelt.</span><span class="sxs-lookup"><span data-stu-id="f60a8-117">Call [**IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) to get storage attributes, which will tell you whether the storage is a file or a folder.</span></span>
3.  <span data-ttu-id="f60a8-118">Fragen Sie **iwmdmstorage** nach [**iwmdmstoragecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)ab, und nennen Sie [**iwmdmstoragecontrol:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) , um die Datei vom Gerät zu lesen und an einem angegebenen Speicherort zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f60a8-118">Query **IWMDMStorage** for [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol), and call [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) to read the file from the device and save it to a specified location.</span></span>

<span data-ttu-id="f60a8-119">Wenn Sie stattdessen den File Block by-Block vom Gerät lesen möchten, müssen Sie die [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) -Rückruf Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="f60a8-119">If, instead, you want to read the file block by block from the device, you must implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) callback interface.</span></span> <span data-ttu-id="f60a8-120">Übergeben Sie diese Schnittstelle an den **iwmdmstoragecontrol:: Read** -Befehl, und der Windows Media-Device Manager sendet Teilmengen von Datei Daten sequenziell an Ihren Rückruf.</span><span class="sxs-lookup"><span data-stu-id="f60a8-120">Pass this interface into the **IWMDMStorageControl::Read** call, and Windows Media Device Manager will send chunks of file data sequentially to your callback.</span></span> <span data-ttu-id="f60a8-121">Die folgenden Schritte zeigen, wie ein Gerätedatei Block nach Block gelesen wird:</span><span class="sxs-lookup"><span data-stu-id="f60a8-121">The following steps show how to read a device file block by block:</span></span>

1.  <span data-ttu-id="f60a8-122">Holen Sie sich die **iwmdmstorage** -Schnittstelle für den Speicher, und bestimmen Sie, ob es sich um eine Datei handelt, wie zuvor beschrieben</span><span class="sxs-lookup"><span data-stu-id="f60a8-122">Get the **IWMDMStorage** interface for the storage and determine whether it is a file, as described previously.</span></span>
2.  <span data-ttu-id="f60a8-123">Bereiten Sie alle Datei Handles oder anderen Handles vor, die Sie zum Speichern der empfangenen Daten benötigen.</span><span class="sxs-lookup"><span data-stu-id="f60a8-123">Prepare any file handles or other handles you need to hold the received data.</span></span>
3.  <span data-ttu-id="f60a8-124">Abfrage für die **iwmdmstoragecontrol** -Schnittstelle des Speichers</span><span class="sxs-lookup"><span data-stu-id="f60a8-124">Query for the storage's **IWMDMStorageControl** interface</span></span>
4.  <span data-ttu-id="f60a8-125">Nennen Sie **iwmdmstoragecontrol:: Read** , um den Lesevorgang zu starten, und übergeben Sie die von Ihnen implementierte **iwmdmoperation** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f60a8-125">Call **IWMDMStorageControl::Read** to begin the read operation, passing in the **IWMDMOperation** interface you have implemented.</span></span>
5.  <span data-ttu-id="f60a8-126">Windows Media Device Manager sendet den Datenblock nach Block an Ihr Gerät, wie unter [Manuelles Verarbeiten von Dateiübertragungen](handling-file-transfers-manually.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f60a8-126">Windows Media Device Manager will send the data block by block to your device as described in [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>

<span data-ttu-id="f60a8-127">Die folgende C++-Beispiel Funktion liest ein Speicher Objekt von einem Gerät.</span><span class="sxs-lookup"><span data-stu-id="f60a8-127">The following C++ example function reads a storage object from a device.</span></span> <span data-ttu-id="f60a8-128">Die Funktion akzeptiert einen optionalen **iwmdmoperation** -Schnittstellen Zeiger. Wenn Sie übermittelt wird, erstellt die Funktion eine Datei explizit und verarbeitet das Schreiben der Daten in die Datei bei der Implementierung von **iwmdmoperation:: transferobjectdata**; Wenn dies nicht der Fall ist, wird die Datei gelesen und in dem durch *pwszdestname* angegebenen Ziel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f60a8-128">The function accepts an optional **IWMDMOperation** interface pointer; if submitted, the function will create a file explicitly and handle writing the data to file on its implementation of **IWMDMOperation::TransferObjectData**; if not, it will read the file and save to the destination specified by *pwszDestName*.</span></span>


```C++
HANDLE m_File = NULL;

HRESULT myFileRead(IWMDMStorage pStorage, LPWSTR pwszDestName, IWMDMOperation* pOperation)
{
    HRESULT hr = S_OK;
    if ((pStorage == NULL) || (pwszDestName == NULL)) 
    {
        return E_INVALIDPARAM;
    }

    // Check that the storage is readable.
    DWORD attributes = 0;
    UINT flags = 0;
    hr = pStorage->GetAttributes(&attributes, NULL); 
    if (FAILED(hr))
    {
        return hr;
    }

    // Check that content is readable.
    if ((attributes & WMDM_FILE_ATTR_CANREAD) == 0)
    {
        return E_FAIL;
    }
    // Check that it is not abstract (such as an abstract playlist).
    else if (attributes & WMDM_STORAGE_ATTR_VIRTUAL)
    {
        return E_FAIL;
    }

    // Set some flag values for the read operation.
    flags |= WMDM_MODE_BLOCK;
    if (attributes & WMDM_FILE_ATTR_FOLDER)
    {
        flags |= WMDM_CONTENT_FOLDER;
    }
    if (attributes & WMDM_FILE_ATTR_FILE)
    {
        flags |= WMDM_CONTENT_FILE;
    }

    // Get the IWMDMStorageControl interface.
    CComQIPtr<IWMDMStorageControl> pStgControl(pStorage);
    
    // Extra steps if we want to read the file ourselves using IWMDMOperation3.
    if (pOperation != NULL)
    {
        // Create a new file and get the handle. m_File is a global variable
        // that we will use in IWMDMOperation::TransferObjectData.
        // This can also be done when IWMDMOperation::BeginRead is called.
        m_File = CreateFile(
            pwszDestName,   // Destination file name.
            GENERIC_WRITE,  // Write and append writes
            NULL,           // File can't be shared while using, and must be closed.
            NULL,           // Handle can't be inherited.
            CREATE_ALWAYS,  // Overwrite existing files.
            FILE_ATTRIBUTE_NORMAL, // No special attributes.
            NULL            // No template file supplied.
           );
        if (m_File == INVALID_HANDLE_VALUE) return E_FAIL;
        // Modify the Read() method flag. WMDM_CONTENT_FILE and WMDM_CONTENT_FOLDER 
        // are not valid flags when pOperation != NULL.
        flags |= WMDM_CONTENT_OPERATIONINTERFACE;
    }

    // Read the file.
    hr = pStgControl->Read(
             flags,        // Synchronous call specified.
             pwszDestName, // Ignored if pOperation is not NULL.
             NULL,         // No progress callback sent.
             pOperation);  // IWMDMOperation interface, if provided.
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="f60a8-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f60a8-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f60a8-130">**Erstellen einer Windows Media Device Manager-Anwendung**</span><span class="sxs-lookup"><span data-stu-id="f60a8-130">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




