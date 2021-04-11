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
# <a name="transferring-content-from-the-device-to-a-pc"></a>Übertragen von Inhalt vom Gerät an einen PC

Ein gängiger Vorgang, der von einer WPD-Anwendung ausgeführt wird, ist die Übertragung von Inhalt von einem verbundenen Gerät auf den PC.

Inhalts Übertragungen werden mithilfe der in der folgenden Tabelle beschriebenen Schnittstellen erreicht.



| Schnittstelle                                                                | BESCHREIBUNG                                                     |
|--------------------------------------------------------------------------|-----------------------------------------------------------------|
| [**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)       | Bietet Zugriff auf die **iportabledeviceproperties** -Schnittstelle. |
| [**Iportabledeviceproperties-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties) | Ermöglicht den Zugriff auf Eigenschaften spezifische Methoden.                   |
| [**Iportabledeviceresources-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)   | Wird verwendet, um die Eigenschafts Schlüssel für das angegebene Profil zu speichern.          |
| IStream-Schnittstelle                                                        | Wird verwendet, um die Daten zu lesen und zu schreiben.                                |



 

Die `TransferContentFromDevice` Funktion im Modul "contenttransfer. cpp" der Beispielanwendung veranschaulicht, wie eine Anwendung Kontaktinformationen von einem verbundenen Gerät an einen PC übertragen könnte.

Die erste Aufgabe, die von der- `TransferContentFromDevice` Funktion ausgeführt wird, besteht darin, den Benutzer zur Eingabe eines Objekt Bezeichners für das übergeordnete Objekt auf dem Gerät aufzufordern (unter dem der Inhalt übertragen wird).


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



Der nächste Schritt ist das Abrufen eines **iportabledevicecontent** -Objekts, das im Beispiel für den Zugriff auf die Inhalts spezifischen Methoden verwendet wird.


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



Der nächste Schritt ist das Abrufen eines **iportabledeviceresources** -Objekts, das im Beispiel für den Zugriff auf die Ressourcen spezifischen Methoden verwendet wird.


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



Der nächste Schritt ist das Abrufen eines IStream-Objekts, das im Beispiel verwendet wird, um die Daten zu lesen, die es vom Gerät überträgt.


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



Der nächste Schritt ist das Abrufen des Datei namens des Objekts auf dem Gerät. Diese Zeichenfolge wird zum Erstellen des entsprechenden Datei namens auf dem PC verwendet. Wenn das Objekt keinen Dateinamen auf dem Gerät hat, wird der Bezeichner des Objekts in eine Zeichenfolge konvertiert und zum Erstellen des Ziel Dateinamens verwendet.


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



Danach erstellt das Beispiel ein IStream-Zielobjekt.


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



Schließlich wird das Quell-IStream-Objekt in das Ziel auf dem PC kopiert.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iportabledevice-Schnittstelle**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)
</dt> <dt>

[**Iportabledevicecontent-Schnittstelle**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)
</dt> <dt>

[**Iportabledebug-Schnittstelle**](iportabledevicevalues.md)
</dt> <dt>

[**Programmierhandbuch**](programming-guide.md)
</dt> </dl>

 

 



