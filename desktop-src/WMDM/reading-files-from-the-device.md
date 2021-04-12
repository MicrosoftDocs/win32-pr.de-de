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
# <a name="reading-files-from-the-device"></a>Lesen von Dateien vom Gerät

Wenn Sie eine Datei gefunden haben, die Sie vom Gerät kopieren möchten, können Sie die Datei mit einem einzigen-Befehl vom Gerät auf den Computer kopieren oder einen Rückruf verwenden, damit die Datei Bytes direkt in die Anwendung gelesen werden. auf diese Weise können die Daten nach Bedarf verarbeitet oder gespeichert werden.

Die folgenden Schritte zeigen die grundlegende Methode zum Kopieren einer Datei von einem Gerät in einem einzelnen-Befehl:

1.  Erhalten Sie ein Handle für die Datei auf dem Gerät. Sie können das Handle über eine rekursive Dateisuche oder, wenn Sie die persistente ID des Speichers kennen, durch Aufrufen von [**IWMDMDevice3:: findstorage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage)abrufen. In beiden Fällen benötigen Sie die [**iwmdmstorage**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) -Schnittstelle des-Objekts.
2.  Bestimmen Sie, ob es sich beim Speicher um eine Datei oder einen Ordner handelt. Nur Dateien können vom Gerät kopiert werden. Aufrufen von [**iwmdmstorage:: GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) zum Abrufen von Speicher Attributen, die Aufschluss darüber geben, ob es sich bei dem Speicher um eine Datei oder einen Ordner handelt.
3.  Fragen Sie **iwmdmstorage** nach [**iwmdmstoragecontrol**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)ab, und nennen Sie [**iwmdmstoragecontrol:: Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) , um die Datei vom Gerät zu lesen und an einem angegebenen Speicherort zu speichern.

Wenn Sie stattdessen den File Block by-Block vom Gerät lesen möchten, müssen Sie die [**iwmdmoperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) -Rückruf Schnittstelle implementieren. Übergeben Sie diese Schnittstelle an den **iwmdmstoragecontrol:: Read** -Befehl, und der Windows Media-Device Manager sendet Teilmengen von Datei Daten sequenziell an Ihren Rückruf. Die folgenden Schritte zeigen, wie ein Gerätedatei Block nach Block gelesen wird:

1.  Holen Sie sich die **iwmdmstorage** -Schnittstelle für den Speicher, und bestimmen Sie, ob es sich um eine Datei handelt, wie zuvor beschrieben
2.  Bereiten Sie alle Datei Handles oder anderen Handles vor, die Sie zum Speichern der empfangenen Daten benötigen.
3.  Abfrage für die **iwmdmstoragecontrol** -Schnittstelle des Speichers
4.  Nennen Sie **iwmdmstoragecontrol:: Read** , um den Lesevorgang zu starten, und übergeben Sie die von Ihnen implementierte **iwmdmoperation** -Schnittstelle.
5.  Windows Media Device Manager sendet den Datenblock nach Block an Ihr Gerät, wie unter [Manuelles Verarbeiten von Dateiübertragungen](handling-file-transfers-manually.md)beschrieben.

Die folgende C++-Beispiel Funktion liest ein Speicher Objekt von einem Gerät. Die Funktion akzeptiert einen optionalen **iwmdmoperation** -Schnittstellen Zeiger. Wenn Sie übermittelt wird, erstellt die Funktion eine Datei explizit und verarbeitet das Schreiben der Daten in die Datei bei der Implementierung von **iwmdmoperation:: transferobjectdata**; Wenn dies nicht der Fall ist, wird die Datei gelesen und in dem durch *pwszdestname* angegebenen Ziel gespeichert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen einer Windows Media Device Manager-Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




