---
description: Hinzufügen einer Ressource zu einem Objekt
ms.assetid: 81476f50-5ea0-4e02-9e38-2b1dfcc32c4f
title: Hinzufügen einer Ressource zu einem Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34f95cd4b11182a8cc6bc3d249f2065744ba0f6d8efe1be204e47ad321429a88
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930240"
---
# <a name="adding-a-resource-to-an-object"></a>Hinzufügen einer Ressource zu einem Objekt

Zusätzlich zum Übertragen von Objekten auf ein Gerät ist es auch möglich, Objekten Ressourcen hinzuzufügen. Beispielsweise könnte eine Anwendung vorhandenen Informationen für einen bestimmten Kontakt ein Foto hinzufügen.

Ressourcen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen hinzugefügt.



| Schnittstelle                                                              | BESCHREIBUNG                                                       |
|------------------------------------------------------------------------|-------------------------------------------------------------------|
| [**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)     | Ermöglicht den Zugriff auf die inhaltsspezifischen Methoden.                  |
| [**IPortableDeviceResources-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) | Wird verwendet, wenn die Ressourceneigenschaften und -daten auf das Gerät geschrieben werden. |
| [**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)       | Wird verwendet, um Eigenschaften zu schreiben, die die Ressource beschreiben.              |
| IStream-Schnittstelle                                                      | Wird verwendet, um das Schreiben der Ressource auf das Gerät zu vereinfachen.              |



 

Die Funktion CreateContactPhotoResourceOnDevice im ContentTransfer.cpp-Modul der Beispielanwendung veranschaulicht, wie eine Anwendung einem Kontaktobjekt eine Fotoressource hinzufügen kann. Diese Funktion fordert den Benutzer zur Eingabe des Objektbezeichners des Kontakts auf dem Gerät auf, dem die Fotoressource hinzugefügt wird. Anschließend wird ein Dialogfeld Datei Öffnen angezeigt, damit der Benutzer das bild auswählen kann, das hinzugefügt werden soll. Nachdem diese Daten gesammelt wurden, schreibt die Anwendung die Ressource auf das Gerät.

Die erste Aufgabe, die von der CreateContactPhotoResourceOnDevice-Funktion ausgeführt wird, besteht darin, den Benutzer zur Eingabe eines Objektbezeichners für den Kontakt aufforderungen, dem das Foto hinzugefügt wird.


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
printf("Enter the identifer of the object to which we will add an Audio annotation.\n>");
hr = StringCbGetsW(wszSelection,sizeof(wszSelection));
if (FAILED(hr))
{
    printf("An invalid object identifier was specified, aborting resource creation\n");
}do
```



Der nächste Schritt ist das Abrufen eines [**IPortableDeviceContent-Objekts,**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent) das wiederum zum Abrufen eines [**IPortableDeviceResources-Objekts verwendet**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) wird. (Die Anwendung verwendet dieses zweite Objekt, um die neue Ressource zu erstellen und zu schreiben.)


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pDevice->Content(&pContent);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceContent from IPortableDevice, hr = 0x%lx\n",hr);
    }
}





if (SUCCEEDED(hr))
{
    hr = pContent->Transfer(&pResources);
    if (FAILED(hr))
    {
        printf("! Failed to get IPortableDeviceResources from IPortableDeviceContent, hr = 0x%lx\n",hr);
    }
}
```



Danach wird im Beispiel das Dialogfeld **Datei Öffnen** angezeigt, mit dem der Benutzer den Namen der Bilddatei angeben kann, die das Foto enthält, das er den Kontaktinformationen hinzufügen möchte.


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    OPENFILENAME OpenFileNameInfo   = {0};

    OpenFileNameInfo.lStructSize    = sizeof(OPENFILENAME);
    OpenFileNameInfo.hwndOwner      = NULL;
    OpenFileNameInfo.lpstrFile      = wszFilePath;
    OpenFileNameInfo.nMaxFile       = ARRAYSIZE(wszFilePath);
    OpenFileNameInfo.lpstrFilter    = L"JPEG (*.JPG)\0*.JPG\0JPEG (*.JPEG)\0*.JPEG\0JPG (*.JPE)\0*.JPE\0JPG (*.JFIF)\0*.JFIF\0\0";;
    OpenFileNameInfo.nFilterIndex   = 1;
    OpenFileNameInfo.Flags          = OFN_PATHMUSTEXIST | OFN_FILEMUSTEXIST;
    OpenFileNameInfo.lpstrDefExt    = L"JPG";

    if (GetOpenFileName(&OpenFileNameInfo) == FALSE)
    {
        printf("The transfer operation was cancelled.\n");
        hr = E_ABORT;
    }
}
```



Sobald das Beispiel über ein [**IPortableDeviceResources-Objekt**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources) und den Namen der Bilddatei verfügt, wird folgendes als Vorbereitung für die übertragung von Daten an das Gerät verwendet.

1.  Es wird ein IStream-Objekt in der ausgewählten Datei für Lesevorgänge geöffnet.
2.  Es erstellt ein [**IPortableDeviceValues-Objekt,**](iportabledevicevalues.md) das Informationen wie Bildgröße und -format enthält.


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    // Open the selected file as an IStream.  This will simplify reading the
    // data and writing to the device.
    hr = SHCreateStreamOnFile(wszFilePath, STGM_READ, &pFileStream);
    if (SUCCEEDED(hr))
    {
        // CoCreate the IPortableDeviceValues to hold the resource attributes
        hr = CoCreateInstance(CLSID_PortableDeviceValues,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IPortableDeviceValues,
                              (VOID**) &pResourceAttributes);
        if (SUCCEEDED(hr))
        {
            // Fill in the necessary information regarding this resource

            // Set the WPD_OBJECT_ID.  This informs the driver which object this request is intended for.
            hr = pResourceAttributes->SetStringValue(WPD_OBJECT_ID, wszSelection);
            if (FAILED(hr))
            {
                printf("! Failed to set WPD_OBJECT_ID when creating a resource, hr = 0x%lx\n",hr);
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetKeyValue(WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY, WPD_RESOURCE_CONTACT_PHOTO);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_RESOURCE_KEY to WPD_RESOURCE_CONTACT_PHOTO, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE by requesting the total size of the
            // data stream.
            if (SUCCEEDED(hr))
            {
                STATSTG statstg = {0};
                hr = pFileStream->Stat(&statstg, STATFLAG_NONAME);
                if (SUCCEEDED(hr))
                {
                    hr = pResourceAttributes->SetUnsignedLargeIntegerValue(WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, statstg.cbSize.QuadPart);
                    if (FAILED(hr))
                    {
                        printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_TOTAL_SIZE, hr = 0x%lx\n",hr);
                    }
                }
                else
                {
                    printf("! Failed to get file's total size, hr = 0x%lx\n",hr);
                }
            }

            // Set the WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF because we are
            // creating a contact photo resource with JPG image data.
            if (SUCCEEDED(hr))
            {
                hr = pResourceAttributes->SetGuidValue(WPD_RESOURCE_ATTRIBUTE_FORMAT, WPD_OBJECT_FORMAT_JFIF);
                if (FAILED(hr))
                {
                    printf("! Failed to set WPD_RESOURCE_ATTRIBUTE_FORMAT to WPD_OBJECT_FORMAT_JFIF, hr = 0x%lx\n",hr);
                }
            }
        }

    }

    if (FAILED(hr))
    {
        printf("! Failed to open file named (%ws) to transfer to device, hr = 0x%lx\n",wszFilePath, hr);
    }
}
```



Nachdem die IStream- und [**IPortableDeviceValues-Objekte**](iportabledevicevalues.md) für den Schreibvorgang vorbereitet wurden, überträgt das Beispiel das Bild auf das Gerät. Im Beispiel wird die Übertragung wie folgt in drei Schritten abgeschlossen:

1.  Sie erstellt die Ressource auf dem Gerät durch Aufrufen der [**IPortableDeviceResources::CreateResource-Methode.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledeviceresources-createresource)
2.  Sie ruft eine StreamCopy-Hilfsfunktion auf, um den Quellstream in den Zielstream zu kopieren.
3.  Er informiert den Gerätetreiber, dass die Übertragung abgeschlossen ist, indem die IPortableDeviceDataStream::Commit-Methode aufruft.


```C++
HRESULT                             hr = S_OK;
WCHAR                               wszSelection[81]        = {0};
WCHAR                               wszFilePath[MAX_PATH]   = {0};
DWORD                               cbOptimalTransferSize   = 0;
CComPtr<IStream>                    pFileStream;
CComPtr<IStream>                    pResourceStream;
CComPtr<IPortableDeviceValues>      pResourceAttributes;
CComPtr<IPortableDeviceContent>     pContent;
CComPtr<IPortableDeviceResources>   pResources;
if (SUCCEEDED(hr))
{
    hr = pResources->CreateResource(pResourceAttributes,    // Properties describing this resource
                                    &pResourceStream,       // Returned resource data stream (to transfer the data to)
                                    &cbOptimalTransferSize, // Returned optimal buffer size to use during transfer
                                    NULL);


    // Since we have IStream-compatible interfaces, call our helper function
    // that copies the contents of a source stream into a destination stream.
    if (SUCCEEDED(hr))
    {
        DWORD cbTotalBytesWritten = 0;

        hr = StreamCopy(pResourceStream,        // Destination (The resource to transfer to)
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
        hr = pResourceStream->Commit(0);
        if (FAILED(hr))
        {
            printf("! Failed to commit resource to device, hr = 0x%lx\n",hr);
        }
    }
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IPortableDevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**IPortableDeviceContent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**IPortableDeviceResources-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)
</dt> <dt>

[**IPortableDeviceValues-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



