---
title: Senden der Datei an das Gerät
description: Senden der Datei an das Gerät
ms.assetid: 202185b8-f10e-4108-a950-60658c006cec
keywords:
- Windows Medien Geräte-Manager, Senden von Dateien an Geräte
- Geräte-Manager,Senden von Dateien an Geräte
- Programmierhandbuch,Senden von Dateien an Geräte
- Desktopanwendungen, Senden von Dateien an Geräte
- Erstellen Windows Media Geräte-Manager-Anwendungen, Senden von Dateien an Geräte
- Schreiben von Dateien auf Geräte, Senden von Dateien an Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 974a47de872d03d42701ff6e95516a9ead59f1206729ae9ca70d6dd9e5f1260f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120124140"
---
# <a name="sending-the-file-to-the-device"></a>Senden der Datei an das Gerät

Nachdem die Datei bei Bedarf transcodiert und alle Metadaten einschließlich des Formats festgelegt wurden, kann Ihre Anwendung die Datei an das Gerät senden. Hierzu müssen Sie zunächst eine **IWMDMStorageControl-Schnittstelle** (oder eine höhere Version) für einen Zielspeicherort auf dem Gerät abrufen. Die **Insert-Flags** geben an, ob der neue Speicher ein gleichgeordnetes oder untergeordnetes Element des Ziels sein soll. Nachdem Sie das Ziel erhalten haben, können Sie [**IWMDMStorageControl::Insert**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-insert), [**IWMDMStorageControl2::Insert2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol2-insert2)oder [**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) aufrufen, um die Datei zu übertragen. Die Anwendung kann das Lesen der Dateidaten selbst verarbeiten, indem [**sie IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation)implementiert, oder sie kann es der **Insert-Methode** ermöglichen, die Datei automatisch zu lesen und zu übertragen, indem sie keinen Zeiger auf eine von der Anwendung implementierte **IWMDMOperation** bereitstellt.

Der folgende C++-Code veranschaulicht das Aufrufen von **Insert3,** um eine Datei auf ein Gerät zu schreiben. Wenn der an **Insert3** übergebene *pOperation-Zeiger* **NULL** ist, wird die Datei in einem Schritt gesendet. Wenn dieser Zeiger ein gültiger Schnittstellenzeiger ist, ruft Windows Media Geräte-Manager Ihre Rückrufmethode auf, um Daten in Blöcken abzurufen. Ausführliche Informationen zum Implementieren von **IWMDMOperation** finden Sie unter [Manuelles Behandeln von Dateiübertragungen.](handling-file-transfers-manually.md)


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

 

 




