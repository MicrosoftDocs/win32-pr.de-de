---
title: Erstellen eines App-Pakets (C++)
description: Erfahren Sie, wie Sie mithilfe der Paketerstellungs-API ein App-Paket für eine Windows-App erstellen.
ms.assetid: FD677D75-50D5-4228-891F-73B5F40679B0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ac2e471443acd22a39128c046590eed29d320b75bafee0a65cb6d37fb4fb8d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119049058"
---
# <a name="how-to-create-an-app-package-c"></a>Erstellen eines App-Pakets (C++)

Erfahren Sie, wie Sie ein App-Paket für eine Windows-App mithilfe der [Paketerstellungs-API](interfaces.md)erstellen.

Wenn Sie ein Desktop-App-Paket manuell erstellen möchten, können Sie auch das MakeAppx.exe Tool verwenden, das die [Paketerstellungs-API](interfaces.md)verwendet. Weitere Informationen finden Sie unter [App Packager (MakeAppx.exe).](make-appx-package--makeappx-exe-.md)

Wenn Sie Visual Studio verwenden, wird empfohlen, die App mithilfe des Assistenten für die Visual Studio Paketierung zu verpacken. Weitere Informationen finden Sie unter [Packen einer UWP-App mit Visual Studio](/windows/msix/package/packaging-uwp-apps).

## <a name="instructions"></a>Anweisungen

### <a name="step-1-create-a-package-writer"></a>Schritt 1: Erstellen eines Paketwriters

Um einen Paketwriter zu erstellen, rufen Sie die [**IAppxFactory::CreatePackageWriter-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) auf. Der erste Parameter ist ein Ausgabestream, in den das Paket geschrieben wird. Der zweite Parameter ist ein Zeiger auf eine [**APPX \_ PACKAGE \_ SETTINGS-Struktur,**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) die Paketeinstellungen angibt. Der dritte Parameter ist ein Ausgabeparameter, der einen Zeiger auf einen [**IAppxPackageWriter-Zeiger**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) empfängt.


```C++
#include <windows.h>
#include <shlwapi.h>
#include <AppxPackaging.h>

// We store the produced package under this file name.
const LPCWSTR OutputPackagePath = L"HelloWorld.appx";

int wmain()
{
    HRESULT hr = S_OK;

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        // Create a package writer
        IAppxPackageWriter* packageWriter = NULL;

        hr = GetPackageWriter(OutputPackagePath, &packageWriter);
    }
}

//
// Creates an app package writer with default settings.
//
// Parameters:
//   outputFileName  
//     Fully qualified name of the app package (.appx file) to be created.
//   writer 
//     On success, receives the created instance of IAppxPackageWriter.
//
HRESULT GetPackageWriter(
    _In_ LPCWSTR outputFileName,
    _Outptr_ IAppxPackageWriter** writer)
{
    const LPCWSTR Sha256AlgorithmUri = L"https://www.w3.org/2001/04/xmlenc#sha256"; 
    HRESULT hr = S_OK;
    IStream* outputStream = NULL;
    IUri* hashMethod = NULL;
    APPX_PACKAGE_SETTINGS packageSettings = {0};
    IAppxFactory* appxFactory = NULL;

    // Create a stream over the output file for the package 
    hr = SHCreateStreamOnFileEx(
            outputFileName,
            STGM_CREATE | STGM_WRITE | STGM_SHARE_EXCLUSIVE,
            0,     // default file attributes
            TRUE,  // create file if it does not exist
            NULL,  // no template
            &outputStream);

    // Create default package writer settings, including hash algorithm URI
    // and Zip format.
    if (SUCCEEDED(hr))
    {        hr = CreateUri(
                Sha256AlgorithmUri,
                Uri_CREATE_CANONICALIZE,
                0, // reserved parameter
                &hashMethod);
    }

    if (SUCCEEDED(hr))
    {
        packageSettings.forceZip32 = TRUE;
        packageSettings.hashMethod = hashMethod;
    }

    // Create a new Appx factory
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(
                __uuidof(AppxFactory),
                NULL,
                CLSCTX_INPROC_SERVER,
                __uuidof(IAppxFactory),
                (LPVOID*)(&appxFactory));
    }

    // Create a new package writer using the factory
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageWriter(
                outputStream,
                &packageSettings,
                writer);
    }

    // Clean up allocated resources
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    if (hashMethod != NULL)
    {
        hashMethod->Release();
        hashMethod = NULL;
    }
    if (outputStream != NULL)
    {
        outputStream->Release();
        outputStream = NULL;
    }
    return hr;
}
```



### <a name="step-2-add-the-payload-files-for-your-app-to-the-package"></a>Schritt 2: Hinzufügen der Nutzlastdateien für Ihre App zum Paket

Rufen Sie die [**IAppxPackageWriter::AddPayloadFile-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) auf, um dem Paket Dateien hinzuzufügen. Der erste Parameter ist der relative Pfad der Datei. Der zweite Parameter gibt den Inhaltstyp der Datei an. Der dritte Parameter gibt Optionen aus der [**APPX \_ COMPRESSION \_ OPTION-Enumeration**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) an. Der vierte Parameter ist der Eingabestream für die Datei.


```C++
// Path where all input files are stored
const LPCWSTR DataPath = L"Data\\";

// Add all payload files to the package writer
for (int i = 0; SUCCEEDED(hr) && (i < PayloadFilesCount); i++)
{
    IStream* fileStream = NULL;

    hr = GetFileStream(DataPath, PayloadFilesName[i], &fileStream);

    if (SUCCEEDED(hr))
    {
        packageWriter->AddPayloadFile(
            PayloadFilesName[i],
            PayloadFilesContentType[i],
            PayloadFilesCompression[i],
            fileStream);
        }

        if (fileStream != NULL)
        {
            fileStream->Release();
            fileStream = NULL;
        }
    }
}
```



Im vorherigen Code werden diese Variablendefinitionen und `GetFileStream` hilfsfunktion verwendet.


```C++
#include <strsafe.h>
#include <shlwapi.h>

// The produced app package's content consists of these files, with
// corresponding content types and compression options.
const int PayloadFilesCount = 4;
const LPCWSTR PayloadFilesName[PayloadFilesCount] = {
    L"AppTile.png",
    L"Default.html",
    L"images\\smiley.jpg",
    L"Error.html",
};
const LPCWSTR PayloadFilesContentType[PayloadFilesCount] = {
    L"image/png",
    L"text/html",
    L"image/jpeg",
    L"text/html",
};
const APPX_COMPRESSION_OPTION PayloadFilesCompression[PayloadFilesCount] = {
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
    APPX_COMPRESSION_OPTION_NONE,
    APPX_COMPRESSION_OPTION_NORMAL,
};

//
// Creates a readable IStream over the specified file. For simplicity, we assume that the fully 
// qualified file name is 100 characters or less. Your code should 
// handle longer names, and allocate the buffer dynamically.
//
// Parameters:
//   path 
//      Path of the folder that contains the file to be opened; must end with a '\'
//   fileName 
//      Name, of the file to be opened, not including the path
//   stream 
//      On success, receives the created instance of IStream
//
HRESULT GetFileStream(
    _In_ LPCWSTR path,
    _In_ LPCWSTR fileName,
    _Outptr_ IStream** stream)
{
    HRESULT hr = S_OK;
    const int MaxFileNameLength = 100;
    WCHAR fullFileName[MaxFileNameLength + 1];

    // Create full file name by concatenating path and fileName
    hr = StringCchCopyW(fullFileName, MaxFileNameLength, path);
    if (SUCCEEDED(hr))
    {
        hr = StringCchCat(fullFileName, MaxFileNameLength, fileName);
    }

    // Create stream for reading the file
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                fullFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0,      // default file attributes
                FALSE,  // don't create new file
                NULL,   // no template
                stream);
    }
    return hr;
}
```



### <a name="step-3-add-the-package-manifest-to-the-package"></a>Schritt 3: Hinzufügen des Paketmanifests zum Paket

Jedes Paket muss über ein Paketmanifest verfügen. Um dem Paket das Paketmanifest hinzuzufügen, erstellen Sie einen Eingabestream für die Datei, und rufen Sie dann die [**IAppxPackageWriter::Close-Methode**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) auf, um das Manifest am Ende des Pakets zu schreiben und den Ausgabestream für den Paketwriter zu schließen.

In diesem Code wird die `GetFileStream` im vorherigen Schritt gezeigte Hilfsfunktion verwendet, um den Stream für das Paketmanifest zu erstellen.


```C++
// We read the app package's manifest from this file
const LPCWSTR ManifestFileName = L"AppxManifest.xml";

IStream* manifestStream = NULL;

hr = GetFileStream(DataPath, ManifestFileName, &manifestStream);

if (SUCCEEDED(hr))
{
    hr = packageWriter->Close(manifestStream);
}

if (manifestStream != NULL)
{
    manifestStream->Release();
    manifestStream = NULL;
}
```



### <a name="step-4-clean-up-the-package-writer"></a>Schritt 4: Bereinigen des Paketwriters

Rufen Sie vor dem Zurückgeben von der `wmain` Funktion die [**Release-Methode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf, um den Paketwriter zu bereinigen, und rufen Sie die [**CoUninitialize-Funktion**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) auf.


```C++
if (packageWriter != NULL)
{
    packageWriter->Release();
    packageWriter = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Beispiele**
</dt> <dt>

[Beispiel zum Erstellen eines App-Pakets](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

**Referenz**
</dt> <dt>

[**IAppxPackageWriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter)
</dt> </dl>

 

 