---
description: Übertragen einer Bild- oder Musik datei auf das Gerät
ms.assetid: bace274c-512a-46da-80a7-84734ee880b7
title: Übertragen einer Bild- oder Musik datei auf das Gerät
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cf16c4c95080b5479825bbc4a0f8dcfd131fdb603821edab0a2e9df4d03c41
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928060"
---
# <a name="transferring-an-image-or-music-file-to-the-device"></a>Übertragen einer Bild- oder Musik datei auf das Gerät

Einer der gängigsten Vorgänge, die von einer Anwendung durchgeführt werden, ist die Übertragung von Inhalten an ein verbundenes Gerät.

Inhaltsübertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen durchgeführt.



| Schnittstelle                                                                | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.               |
| [**IPortableDeviceDataStream-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | Wird beim Schreiben des Inhalts auf das Gerät verwendet.                   |
| [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)         | Wird verwendet, um Eigenschaften abzurufen, die den Inhalt beschreiben.         |
| IStream-Schnittstelle                                                        | Wird verwendet, um das Lesen von Inhalten und das Schreiben auf das Gerät zu vereinfachen. |



 

Die `TransferContentToDevice` Funktion im ContentTransfer.cpp-Modul der Beispielanwendung veranschaulicht, wie eine Anwendung Inhalte von einem PC auf ein verbundenes Gerät übertragen kann. In diesem speziellen Beispiel kann es sich bei dem übertragenen Inhalt um eine Datei mit einem Bild, musik oder Kontaktinformationen handelt.

Die erste Aufgabe der `TransferContentToDevice` Funktion besteht darin, den Benutzer zur Eingabe eines Objektbezeichners aufzufordern, der das zu übertragende Objekt identifiziert.


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



Die zweite Aufgabe der `TransferContentToDevice` Funktion besteht darin, ein [**IPortableDeviceContent-Objekt**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) durch Aufrufen der [**IPortableDevice::Content-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) zu erstellen.


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



Die nächste Aufgabe, die von der Funktion ausgeführt `TransferContentToDevice` wird, ist die Erstellung eines **Dateiöffnen-Dialogfelds,** mit dem der Benutzer den Speicherort und den Namen der zu übertragenden Datei angeben kann.


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



Die `TransferContentToDevice` Funktion übergibt eine Filterzeichenfolge ( `wszFileTypeFilter` ) an die GetOpenFileName-Methode, die den Typ der Dateien bestimmt, die der Benutzer auswählen kann. Beispiele für die drei verschiedenen Filter, die im Beispiel zulässig sind, finden Sie `DoMenu` in der Funktion im WpdApiSample.cpp-Modul.

Nachdem der Benutzer eine bestimmte Datei für die Übertragung auf das Gerät identifiziert hat, öffnet die `TransferContentToDevice` Funktion diese Datei als IStream-Objekt und ruft Eigenschaften ab, die zum Abschließen der Übertragung erforderlich sind.


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



Die erforderlichen Eigenschaften werden durch Aufrufen der `GetRequiredPropertiesForContentType` Hilfsfunktion abgerufen, die auf das IStream-Objekt angewendet wird. Die `GetRequiredPropertiesForContentType` Hilfsfunktion erstellt ein [**IPortableDeviceValues-Objekt,**](iportabledevicevalues.md) ruft die Eigenschaften in der folgenden Liste ab und fügt sie diesem Objekt hinzu.

-   Bezeichner des übergeordneten Objekts
-   Streamgröße in Bytes
-   Name der Inhaltsdatei
-   Inhaltsname (der Dateiname ohne Erweiterung)
-   Inhaltstyp (Bild, Audio oder Kontakt)
-   Inhaltsformat (JFIF, WMA oder vCard2)

Die Beispielanwendung verwendet die abgerufenen Eigenschaften, um den neuen Inhalt auf dem Gerät zu erstellen. Dies erfolgt in drei Phasen:

1.  Die Anwendung ruft die [**IPortableDeviceContent::CreateObjectWithPropertiesAndData-Methode**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) auf, um ein neues IStream-Objekt auf dem Gerät zu erstellen.
2.  Die Anwendung verwendet dieses Objekt, um ein [**IPortableDeviceDataStream-Objekt**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) vom WPD-Treiber abzurufen.
3.  Die Anwendung verwendet das neue **IPortableDeviceDataStream-Objekt,** um den Inhalt auf das Gerät zu schreiben (über die StreamCopy-Hilfsfunktion). Die Hilfsfunktion schreibt die Daten aus der Quelldatei in den Stream, der von [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegeben wird.
4.  Die Anwendung schließt den Vorgang ab, indem sie die Commit-Methode im Zielstream aufruft.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceDataStream-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



