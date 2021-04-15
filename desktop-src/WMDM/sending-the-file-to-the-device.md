---
title: Senden der Datei an das Gerät
description: Senden der Datei an das Gerät
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Media Device Manager, Senden von Dateien an Geräte
- Device Manager, Senden von Dateien an Geräte
- Programmier Handbuch, Senden von Dateien an Geräte
- Desktop Anwendungen, Senden von Dateien an Geräte
- Erstellen von Windows Media Device Manager-Anwendungen, Senden von Dateien an Geräte
- Schreiben von Dateien auf Geräte, Senden von Dateien an Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65be0c18a6022538dc5573d936f63392234e9c15
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515806"
---
# <a name="sending-the-file-to-the-device"></a><span data-ttu-id="ee540-109">Senden der Datei an das Gerät</span><span class="sxs-lookup"><span data-stu-id="ee540-109">Sending the File to the Device</span></span>

<span data-ttu-id="ee540-110">Nachdem die Datei bei Bedarf transcodiert wurde und alle Metadaten, einschließlich des Formats, festgelegt wurden, kann die Anwendung die Datei an das Gerät senden.</span><span class="sxs-lookup"><span data-stu-id="ee540-110">After the file has been transcoded if necessary, and all metadata including the format has been set, your application can send the file to the device.</span></span> <span data-ttu-id="ee540-111">Um dies zu erreichen, müssen Sie zuerst eine **iwmdmstoragecontrol** -Schnittstelle (oder eine höhere Version) für einen Zielort auf dem Gerät erhalten.</span><span class="sxs-lookup"><span data-stu-id="ee540-111">In order to do so, you must first get an **IWMDMStorageControl** interface (or a later version) for a target location on the device.</span></span> <span data-ttu-id="ee540-112">Die **einfügeflags** geben an, ob der neue Speicher ein gleich geordnetes oder untergeordnetes Element des Ziels sein soll.</span><span class="sxs-lookup"><span data-stu-id="ee540-112">The **Insert** flags specify whether the new storage should be a sibling or child of the target.</span></span> <span data-ttu-id="ee540-113">Nachdem Sie das Ziel abgerufen haben, können Sie [**iwmdmstoragecontrol:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)oder [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) zum Übertragen der Datei verwenden.</span><span class="sxs-lookup"><span data-stu-id="ee540-113">Once you have gotten the target, you can call [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2), or [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) to transfer the file.</span></span> <span data-ttu-id="ee540-114">Die Anwendung kann das Lesen der Datei Daten selbst durch Implementieren von [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)verarbeiten, oder Sie kann es der **Insert** -Methode ermöglichen, die Datei automatisch zu lesen und zu übertragen, indem Sie keinen Zeiger auf einen von der Anwendung implementierten **iwmdmoperation-Vorgang** bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="ee540-114">The application can handle reading the file data itself by implementing [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation), or it can allow the **Insert** method to read and transfer the file automatically by not providing a pointer to an application-implemented **IWMDMOperation**.</span></span>

<span data-ttu-id="ee540-115">Der folgende C++-Code veranschaulicht das Aufrufen von **Insert3** zum Schreiben einer Datei auf ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="ee540-115">The following C++ code demonstrates calling **Insert3** to write a file to a device.</span></span> <span data-ttu-id="ee540-116">Wenn der an **Insert3** weiter gegebene *poperation* -Zeiger **null** ist, wird die Datei in einem Schritt gesendet. Wenn dieser Zeiger ein gültiger Schnittstellen Zeiger ist, ruft Windows Media Device Manager die Rückruf Methode auf, um Daten in Blöcken abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee540-116">If the *pOperation* pointer passed to **Insert3** is **NULL**, the file will be sent in one step; if this pointer is a valid interface pointer, Windows Media Device Manager will call your callback method to get data in blocks.</span></span> <span data-ttu-id="ee540-117">Ausführliche Informationen zum Implementieren von **iwmdmoperation** finden Sie unter [Manuelles Verarbeiten von Dateiübertragungen](handling-file-transfers-manually.md).</span><span class="sxs-lookup"><span data-stu-id="ee540-117">For details on how to implement **IWMDMOperation**, see [Handling File Transfers Manually](handling-file-transfers-manually.md).</span></span>


```C++
// Set the flags for the operation
UINT flags = WMDM_MODE_BLOCK | // Synchronous call. 
    WMDM_STORAGECONTROL_INSERTINTO | // Insert it into the destination folder.
    WMDM_CONTENT_FILE | // We're inserting a file.
    WMDM_FILE_CREATE_OVERWRITE; // Overwrite existing files.
if (pOperation != NULL)
    flags |= WMDM_CONTENT_OPERATIONINTERFACE;

// Send the file and metadata.
hr = pStgCtl3->Insert3(
    flags,
    WMDM_FILE_ATTR_FOLDER, // The current storage is a folder.
    const_cast<WCHAR*>(pwszFileName), // Source file.
    L"My New File.wma",//NULL, // Destination file name.
    pOperation, // NULL to allow the SDK to read the file; 
                // non-NULL to present raw data bytes to the SDK.
    pProgress, // Interface to send simple progress notifications.
    pMetadata, // IWMDMMetaData interface previously created and filled.
    NULL, 
    &pNewStorage); // Out: handle to the new storage, if the method succeeds.
```



## <a name="related-topics"></a><span data-ttu-id="ee540-118">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ee540-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee540-119">**Schreiben von Dateien auf das Gerät**</span><span class="sxs-lookup"><span data-stu-id="ee540-119">**Writing Files to the Device**</span></span>](writing-files-to-the-device.md)
</dt> </dl>

 

 




