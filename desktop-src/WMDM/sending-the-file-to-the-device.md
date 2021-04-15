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
# <a name="sending-the-file-to-the-device"></a>Senden der Datei an das Gerät

Nachdem die Datei bei Bedarf transcodiert wurde und alle Metadaten, einschließlich des Formats, festgelegt wurden, kann die Anwendung die Datei an das Gerät senden. Um dies zu erreichen, müssen Sie zuerst eine **iwmdmstoragecontrol** -Schnittstelle (oder eine höhere Version) für einen Zielort auf dem Gerät erhalten. Die **einfügeflags** geben an, ob der neue Speicher ein gleich geordnetes oder untergeordnetes Element des Ziels sein soll. Nachdem Sie das Ziel abgerufen haben, können Sie [**iwmdmstoragecontrol:: Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2:: Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)oder [**IWMDMStorageControl3:: Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) zum Übertragen der Datei verwenden. Die Anwendung kann das Lesen der Datei Daten selbst durch Implementieren von [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)verarbeiten, oder Sie kann es der **Insert** -Methode ermöglichen, die Datei automatisch zu lesen und zu übertragen, indem Sie keinen Zeiger auf einen von der Anwendung implementierten **iwmdmoperation-Vorgang** bereitstellt.

Der folgende C++-Code veranschaulicht das Aufrufen von **Insert3** zum Schreiben einer Datei auf ein Gerät. Wenn der an **Insert3** weiter gegebene *poperation* -Zeiger **null** ist, wird die Datei in einem Schritt gesendet. Wenn dieser Zeiger ein gültiger Schnittstellen Zeiger ist, ruft Windows Media Device Manager die Rückruf Methode auf, um Daten in Blöcken abzurufen. Ausführliche Informationen zum Implementieren von **iwmdmoperation** finden Sie unter [Manuelles Verarbeiten von Dateiübertragungen](handling-file-transfers-manually.md).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Schreiben von Dateien auf das Gerät**](writing-files-to-the-device.md)
</dt> </dl>

 

 




