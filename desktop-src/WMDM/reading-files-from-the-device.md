---
title: Lesen von Dateien vom Gerät
description: Lesen von Dateien vom Gerät
ms.assetid: adb87b53-39e2-4f83-ab6d-7e2f7c0bd5d3
keywords:
- Windows Medien Geräte-Manager,Lesen von Dateien von Geräten
- Geräte-Manager,Lesen von Dateien von Geräten
- Programmierhandbuch,Lesen von Dateien von Geräten
- Desktopanwendungen,Lesen von Dateien von Geräten
- Erstellen Windows Media Geräte-Manager-Anwendungen,Lesen von Dateien von Geräten
- Lesen von Dateien von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4352be59a335461f46bfc722146e4c51d31f72c1559e9ad8631e80cb6752c241
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119904000"
---
# <a name="reading-files-from-the-device"></a>Lesen von Dateien vom Gerät

Wenn Sie eine Datei gefunden haben, die Sie vom Gerät kopieren möchten, können Sie die Datei in einem einzigen Aufruf vom Gerät auf den Computer kopieren oder einen Rückruf verwenden, um die Dateibytes direkt in Ihre Anwendung lesen zu lassen, die dann die Daten nach Ihren Anforderungen verarbeiten oder speichern kann.

Die folgenden Schritte zeigen die grundlegende Methode zum Kopieren einer Datei von einem Gerät in einem einzigen Aufruf:

1.  Erhalten Sie ein Handle für die Datei auf dem Gerät. Sie können das Handle mithilfe einer rekursiven Dateisuche oder, wenn Sie die persistente ID des Speichers kennen, durch Aufrufen [**von IWMDMDevice3::FindStorage abrufen.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-findstorage) In beiden Fällen benötigen Sie die [**IWMDMStorage-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstorage) des Objekts.
2.  Bestimmen Sie, ob der Speicher eine Datei oder ein Ordner ist. Nur Dateien können vom Gerät kopiert werden. Rufen [**Sie IWMDMStorage::GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage-getattributes) auf, um Speicherattribute zu erhalten, die Ihnen mitteilen, ob es sich bei dem Speicher um eine Datei oder einen Ordner handelt.
3.  Fragen **Sie IWMDMStorage** nach [**IWMDMStorageControl**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmstoragecontrol)ab, und rufen Sie [**IWMDMStorageControl::Read**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol-read) auf, um die Datei vom Gerät zu lesen und an einem angegebenen Speicherort zu speichern.

Wenn Sie stattdessen den Dateiblock block by block vom Gerät lesen möchten, müssen Sie die [**IWMDMOperation-Rückrufschnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) implementieren. Übergeben Sie diese Schnittstelle an **den IWMDMStorageControl::Read-Aufruf,** und Windows Media Geräte-Manager sendet Sequenzen von Dateidaten an Ihren Rückruf. Die folgenden Schritte zeigen, wie Sie einen Gerätedateiblock nach Block lesen:

1.  Ermitteln Sie **die IWMDMStorage-Schnittstelle** für den Speicher, und bestimmen Sie, ob es sich um eine Datei handelt, wie zuvor beschrieben.
2.  Bereiten Sie alle Dateihandles oder andere Handles vor, die Sie zum Speichern der empfangenen Daten benötigen.
3.  Abfragen der **IWMDMStorageControl-Schnittstelle des** Speichers
4.  Rufen **Sie IWMDMStorageControl::Read** auf, um den Lesevorgang zu starten, und übergeben Sie dabei die von Ihnen implementierte **IWMDMOperation-Schnittstelle.**
5.  Windows Media Geräte-Manager sendet den Datenblock block by block an Ihr Gerät, wie unter Manuelles Verarbeiten von [Dateiübertragungen beschrieben.](handling-file-transfers-manually.md)

Die folgende C++-Beispielfunktion liest ein Speicherobjekt von einem Gerät. Die Funktion akzeptiert einen optionalen **IWMDMOperation-Schnittstellenzeiger.** wenn übermittelt, erstellt die Funktion explizit eine Datei und verarbeitet das Schreiben der Daten in die Datei bei der Implementierung **von IWMDMOperation::TransferObjectData**; Wenn dies nicht der Wert ist, wird die Datei gelesen und an dem von *pwszDestName angegebenen Ziel gespeichert.*


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

[**Erstellen einer Windows Media Geräte-Manager Anwendung**](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 




