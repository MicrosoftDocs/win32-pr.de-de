---
title: Extrahieren von App-Paketinhalten (C++)
description: Erfahren Sie, wie Sie Dateien aus dem App-Paket für eine Windows-App mithilfe der Paket-API extrahieren.
ms.assetid: 72C368F9-2EBA-4930-81CF-9B85717CC0AA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4960a2b30ad7946f1f68e11df5170ae5246f3c36564a7e5e9bc27595be0b7903
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049048"
---
# <a name="extract-app-package-contents-c"></a>Extrahieren von App-Paketinhalten (C++)

Erfahren Sie, wie Sie Dateien aus dem App-Paket für eine Windows-App mithilfe der [Paket-API extrahieren.](interfaces.md)

Sie können auch das tool MakeAppx.exe verwenden, um Dateien aus einem App-Paket oder -Paket zu extrahieren. Weitere [Informationen finden Sie unter Extrahieren von Dateien](/windows/msix/package/create-app-package-with-makeappx-tool#extract-files-from-a-package-or-bundle) aus einem Paket oder Paket.

### <a name="create-a-package-reader"></a>Erstellen eines Paketlesers

Um einen Paketreader zu erstellen, rufen Sie die [**IAppxFactory::CreatePackageReader-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) auf. Der erste Parameter ist ein Eingabestream für das Paket (APPX-Datei). Der zweite Parameter ist ein Ausgabeparameter, der einen Zeiger auf einen [**IAppxPackageReader-Zeiger**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) empfängt.


```C++
#include <windows.h>
#include <shlwapi.h>
#include <AppxPackaging.h>

int wmain(
    _In_ int argc,
    _In_count_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;

    if (argc != 3)
    {
        wprintf(L"Usage:  ExtractAppx.exe inputFile outputPath\n");
        wprintf(L"    inputFile: Path to the appx package\n");
        wprintf(L"    outputPath: Path to the folder for the extracted package contents\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        // Create a package reader using the file name in argv[1] 
        IAppxPackageReader* packageReader = NULL;
        hr = GetPackageReader(argv[1], &packageReader);

        // Print information about all footprint files, and extract them to disk
        if (SUCCEEDED(hr))
        {
            hr = ExtractFootprintFiles(packageReader, argv[2]);
        }

        // Print information about all payload files, and extract them to disk
        if (SUCCEEDED(hr))
        {
            hr = ExtractPayloadFiles(packageReader, argv[2]);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName  
//     The fully-qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="extract-footprint-files"></a>Extrahieren von Speicherbedarfsdateien

Rufen Sie die [**IAppxPackageReader::GetFootprintFile-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getfootprintfile) auf, um jede Speicherabdruckdatei zu erhalten. Jede Speicherabdruckdatei wird durch eine [**IAppxFile-Schnittstelle**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxfile) dargestellt. Die Funktion in diesem Beispiel verwendet die `ExtractFile` [**Methoden GetName,**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getname) [**GetContentType**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getcontenttype)und [**GetSize**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getsize) von **IAppxFile,** um grundlegende Informationen zur Speicherbedarfsdatei anzuzeigen.


```C++
//
// Extracts all footprint files from a package.
//
// Parameters:
//   packageReader 
//      The package reader for the app package.
//   outputPath 
//      The path of the folder for the extracted footprint files.
//
// Types of footprint files in an app package
const int FootprintFilesCount = 4;
const APPX_FOOTPRINT_FILE_TYPE FootprintFilesType[FootprintFilesCount] = {
APPX_FOOTPRINT_FILE_TYPE_MANIFEST,
APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP,
APPX_FOOTPRINT_FILE_TYPE_SIGNATURE,
APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY
};
const LPCWSTR FootprintFilesName[FootprintFilesCount] = {
L"manifest",
L"block map",
L"digital signature",
L"CI catalog"
}; 
//

HRESULT ExtractFootprintFiles(
    _In_ IAppxPackageReader* packageReader,
    _In_ LPCWSTR outputPath)
{
    HRESULT hr = S_OK;
    wprintf(L"\nExtracting footprint files from the package...\n");

    for (int i = 0; SUCCEEDED(hr) && (i < FootprintFilesCount); i++)
    {
        IAppxFile* footprintFile = NULL;

        hr = packageReader->GetFootprintFile(FootprintFilesType[i], &footprintFile);

        if (hr == HRESULT_FROM_WIN32(ERROR_FILE_NOT_FOUND))
        {
            // Some footprint files are optional. It is normal for the GetFootprintFile
            // call to fail when there is no file.
            wprintf(L"\nThe package does not contain a %s.\n", FootprintFilesName[i]);
            hr = S_OK;
        }
        else if (SUCCEEDED(hr))
        {
            hr = ExtractFile(footprintFile, outputPath);
        }

        if (footprintFile != NULL)
        {
            footprintFile->Release();
            footprintFile = NULL;
        }
    }
    return hr;
}

//
// Prints basic info about a footprint or payload file and writes the file to disk.
//
// Parameters:
//   file 
//      The IAppxFile interface that represents a footprint or payload file in the package.
//   outputPath 
//      The path of the folder for the extracted files.
//
HRESULT ExtractFile(
    _In_ IAppxFile* file,
    _In_ LPCWSTR outputPath)
{
    HRESULT hr = S_OK;
    LPWSTR fileName = NULL;
    LPWSTR contentType = NULL;
    UINT64 fileSize = 0;
    IStream* fileStream = NULL;
    IStream* outputStream = NULL;
    ULARGE_INTEGER fileSizeLargeInteger = {0};

    // Get basic info about the file
    hr = file->GetName(&fileName);

    if (SUCCEEDED(hr))
    {
        hr = file->GetContentType(&contentType);
    }
    if (SUCCEEDED(hr))
    {
        hr = file->GetSize(&fileSize);
        fileSizeLargeInteger.QuadPart = fileSize;
    }
    if (SUCCEEDED(hr))
    {
        wprintf(L"\nFile name: %s\n", fileName);
        wprintf(L"Content type: %s\n", contentType);
        wprintf(L"Size: %llu bytes\n", fileSize);
    }

    // Write the file to disk
    if (SUCCEEDED(hr))
    {
        hr = file->GetStream(&fileStream);
    }
    if (SUCCEEDED(hr))
    {
        hr = GetOutputStream(outputPath, fileName, &outputStream);
    }
    if (SUCCEEDED(hr))
    {
        hr = fileStream->CopyTo(outputStream, fileSizeLargeInteger, NULL, NULL);
    }

    // You must free string buffers obtained from the packaging APIs
    CoTaskMemFree(fileName);
    CoTaskMemFree(contentType);

    // Clean up other allocated resources
    if (outputStream != NULL)
    {
        outputStream->Release();
        outputStream = NULL;
    }
    if (fileStream != NULL)
    {
        fileStream->Release();
        fileStream = NULL;
    }
    return hr;
}
```



Im vorherigen Code werden diese Variablendefinitionen und `GetOutputStream` Hilfsfunktionen verwendet.


```C++
// Creates a writable IStream for a file with the specified name under the specified path.  
// This function also creates intermediate subdirectories if necessary. For simplicity, 
// we keep file names including path to 200 characters or less. Make sure your appl 
// handles longer names. Allocate the necessary buffer dynamically.
//
// Parameters:
//    path 
//       The path of the folder containing the file to be opened. Make sure this does not end
//       with a '\' character.
//    fileName 
//       The name of the file to be opened, without the path.
//    stream 
//       On success, receives the created instance of IStream.
//
HRESULT GetOutputStream(
    _In_ LPCWSTR path,
    _In_ LPCWSTR fileName,
    _Outptr_ IStream** stream)
{
    HRESULT hr = S_OK;
    const int MaxFileNameLength = 200;
    WCHAR fullFileName[MaxFileNameLength + 1];

    // Create full file name by concatenating path and fileName
    hr = StringCchCopyW(fullFileName, MaxFileNameLength, path);

    if (SUCCEEDED(hr))
    {
        hr = StringCchCat(fullFileName, MaxFileNameLength, L"\\");
    }
    if (SUCCEEDED(hr))
    {
        hr = StringCchCat(fullFileName, MaxFileNameLength, fileName);
    }

    // Search through fullFileName for the '\' character which denotes
    // subdirectory and create each subdirectory in order of depth.
    for (int i = 0; SUCCEEDED(hr) && (i < MaxFileNameLength); i++)
    {
        if (fullFileName[i] == L'\0')
        {
            break;
        }
        else if (fullFileName[i] == L'\\')
        {
            // Temporarily set string to terminate at the '\' character
            // to obtain name of the subdirectory to create
            fullFileName[i] = L'\0';

            if (!CreateDirectory(fullFileName, NULL))
            {
                DWORD lastError = GetLastError();

                // It is normal for CreateDirectory to fail if the subdirectory
                // already exists.  Don't ignore other errors.
                if (lastError != ERROR_ALREADY_EXISTS)
                {
                    hr = HRESULT_FROM_WIN32(lastError);
                }
            }

            // Restore original string
            fullFileName[i] = L'\\';
        }
    }

    // Create stream for writing the file
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                fullFileName,
                STGM_CREATE | STGM_WRITE | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                TRUE, // create new file if it does not exist
                NULL, // no template
                stream);
    }
    return hr;
}
```



### <a name="extract-payload-files"></a>Extrahieren von Nutzlastdateien

Rufen Sie [**die IAppxPackageReader::GetPayloadFiles-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getpayloadfiles) auf, um die Nutzlastdateien aufzählen. Jede Nutzlastdatei wird durch eine [**IAppxFile-Schnittstelle**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxfile) dargestellt. Die Funktion in diesem Beispiel verwendet die `ExtractFile` [**Methoden GetName,**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getname) [**GetContentType**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getcontenttype)und [**GetSize**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfile-getsize) von **IAppxFile,** um grundlegende Informationen zur Nutzlastdatei anzuzeigen.

In diesem Code wird die im vorherigen Schritt gezeigte Hilfsfunktion `ExtractFile` verwendet, um den Stream für das Paketmanifest zu erstellen.


```C++
//
// Extracts all payload files from a package.
//
// Parameters:
//   packageReader 
//      The package reader for the app package.
//   outputPath 
//      The path of the folder for the extracted payload files.
//
HRESULT ExtractPayloadFiles(
    _In_ IAppxPackageReader* packageReader,
    _In_ LPCWSTR outputPath)
{
    HRESULT hr = S_OK;
    IAppxFilesEnumerator* payloadFiles = NULL;
    wprintf(L"\nExtracting payload files from the package...\n");

    // Get an enumerator of all payload files from the package reader and iterate
    // through all files.
    hr = packageReader->GetPayloadFiles(&payloadFiles);

    if (SUCCEEDED(hr))
    {
        BOOL hasCurrent = FALSE;
        hr = payloadFiles->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxFile* payloadFile = NULL;

            hr = payloadFiles->GetCurrent(&payloadFile);

            if (SUCCEEDED(hr))
            {
                hr = ExtractFile(payloadFile, outputPath);
            }
            if (SUCCEEDED(hr))
            {
                hr = payloadFiles->MoveNext(&hasCurrent);
            }

            if (payloadFile != NULL)
            {
                payloadFile->Release();
                payloadFile = NULL;
            }
        }
    }

    if (payloadFiles != NULL)
    {
        payloadFiles->Release();
        payloadFiles = NULL;
    }
    return hr;
}
```



### <a name="clean-up-the-package-reader"></a>Bereinigt den Paketleser.

Rufen Sie vor der Rückgabe von der Funktion die Release-Methode auf, um den Paketleser zu bereinigt und `wmain` die [**CoUninitialize-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) aufrufen. [](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release)


```C++
// Clean up allocated resources
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[Beispiel zum Extrahieren von App-Paketinhalten](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingExtractAppx)
</dt> <dt>

**Referenz**
</dt> <dt>

[**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader)
</dt> </dl>

 

 