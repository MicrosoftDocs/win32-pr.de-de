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
# <a name="transferring-an-image-or-music-file-to-the-device"></a>Übertragen einer Bild-oder Musikdatei auf das Gerät

Eine der gängigsten Vorgänge, die von einer Anwendung durchgeführt werden, ist die Übertragung von Inhalt auf ein verbundenes Gerät.

Inhalts Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.



| Schnittstelle                                                                | BESCHREIBUNG                                                    |
|--------------------------------------------------------------------------|----------------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Ermöglicht den Zugriff auf die Inhalts spezifischen Methoden.               |
| [**Iportabledevicedatastream-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) | Wird beim Schreiben des Inhalts auf das Gerät verwendet.                   |
| [**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)         | Dient zum Abrufen von Eigenschaften, die den Inhalt beschreiben.         |
| IStream-Schnittstelle                                                        | Wird verwendet, um das Lesen von Inhalten und das Schreiben auf das Gerät zu vereinfachen. |



 

Die `TransferContentToDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Inhalte von einem PC an ein verbundenes Gerät übertragen könnte. In diesem speziellen Beispiel kann der übertragene Inhalt eine Datei sein, die ein Bild, eine Musik oder Kontaktinformationen enthält.

Die erste Aufgabe, die von der-Funktion durchgeführt wird, besteht darin, `TransferContentToDevice` den Benutzer zur Eingabe eines Objekt Bezeichners aufzufordern, der das zu übertragende Objekt identifiziert.


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



Die zweite Aufgabe, die von der-Funktion durchgeführt `TransferContentToDevice` wird, besteht darin, ein [**iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) -Objekt durch Aufrufen der [**iportabledevice:: Content**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-content) -Methode zu erstellen.


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



Die nächste Aufgabe, die von der-Funktion durchgeführt `TransferContentToDevice` wird, ist die Erstellung eines **FileOpen** -Dialog Felds, in dem der Benutzer den Speicherort und den Namen der zu übertragenden Datei angeben kann.


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



Die- `TransferContentToDevice` Funktion übergibt eine Filter Zeichenfolge ( `wszFileTypeFilter` ) an die GetOpenFileName-Methode, die den Typ der Dateien bestimmt, die der Benutzer auswählen kann. `DoMenu`Im Modul wpdapisample. cpp finden Sie Beispiele für die drei verschiedenen Filter, die im Beispiel zulässig sind.

Nachdem der Benutzer eine bestimmte Datei für die Übertragung an das Gerät identifiziert hat, `TransferContentToDevice` öffnet die Funktion diese Datei als IStream-Objekt und ruft die zum Abschluss der Übertragung erforderlichen Eigenschaften ab.


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



Die erforderlichen Eigenschaften werden abgerufen, indem die `GetRequiredPropertiesForContentType` Hilfsfunktion aufgerufen wird, die für das IStream-Objekt gilt. Die `GetRequiredPropertiesForContentType` -Hilfsfunktion erstellt ein [**iportabledevicevalues**](iportabledevicevalues.md) -Objekt, ruft die Eigenschaften in der folgenden Liste ab und fügt diese diesem-Objekt hinzu.

-   Übergeordnete Objekt Kennung
-   Streamgröße in Bytes
-   Name der Inhalts Datei
-   Inhalts Name (der Dateiname ohne Erweiterung)
-   Inhaltstyp (Bild, Audiodatei oder Kontakt)
-   Inhalts Format (jff, WMA oder vCard2)

Die Beispielanwendung verwendet die abgerufenen Eigenschaften, um den neuen Inhalt auf dem Gerät zu erstellen. Dies erfolgt in drei Phasen:

1.  Die Anwendung ruft die [**iportabledevicecontent:: | ateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) -Methode auf, um ein neues IStream-Objekt auf dem Gerät zu erstellen.
2.  Die Anwendung verwendet dieses Objekt, um ein [**iportabledevicedatastream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream) -Objekt aus dem WPD-Treiber abzurufen.
3.  Die Anwendung verwendet das neue **iportabledevicedatastream** -Objekt, um den Inhalt auf das Gerät zu schreiben (über die streamcopy-Hilfsfunktion). Die Hilfsfunktion schreibt die Daten aus der Quelldatei in den Datenstrom, der von [**iportabledevicecontent:: | ateobjectwithpropertiesanddata**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata)zurückgegeben wurde.
4.  Die Anwendung schließt den Vorgang ab, indem Sie die Commit-Methode für den Zielstream aufruft.


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

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledevicedatastream-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



