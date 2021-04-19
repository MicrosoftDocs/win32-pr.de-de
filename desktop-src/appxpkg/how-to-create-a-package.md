---
title: Erstellen eines App-Pakets (C++)
description: Erfahren Sie, wie Sie mithilfe der Paket-API ein App-Paket für eine Windows-app erstellen.
ms.assetid: FD677D75-50D5-4228-891F-73B5F40679B0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f1808ebf57d4c7125f5509db68e22b78ce949f7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "106338251"
---
# <a name="how-to-create-an-app-package-c"></a><span data-ttu-id="ca6dd-103">Erstellen eines App-Pakets (C++)</span><span class="sxs-lookup"><span data-stu-id="ca6dd-103">How to create an app package (C++)</span></span>

<span data-ttu-id="ca6dd-104">Erfahren Sie, wie Sie mithilfe der [Paket-API](interfaces.md)ein App-Paket für eine Windows-app erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-104">Learn how to create an app package for a Windows app using the [packaging API](interfaces.md).</span></span>

<span data-ttu-id="ca6dd-105">Wenn Sie ein Desktop-App-Paket manuell erstellen möchten, können Sie auch das MakeAppx.exe Tool verwenden, das die [Paketierungs-API](interfaces.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-105">If you want to create a desktop app package manually, you can also use the MakeAppx.exe tool which utilizes the [packaging API](interfaces.md).</span></span> <span data-ttu-id="ca6dd-106">Weitere Informationen finden Sie unter [App Packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) .</span><span class="sxs-lookup"><span data-stu-id="ca6dd-106">See [App packager (MakeAppx.exe)](make-appx-package--makeappx-exe-.md) for more information.</span></span>

<span data-ttu-id="ca6dd-107">Wenn Sie Visual Studio verwenden, wird empfohlen, dass Sie den Visual Studio-Paketierungs-Assistenten verwenden, um Ihre APP zu verpacken.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-107">If you are using Visual Studio, it's recommended that you use the Visual Studio packaging wizard to package your app.</span></span> <span data-ttu-id="ca6dd-108">Weitere Informationen finden Sie unter [Packen einer UWP-App mithilfe von Visual Studio](/windows/msix/package/packaging-uwp-apps).</span><span class="sxs-lookup"><span data-stu-id="ca6dd-108">For more details, see [Package a UWP app using Visual Studio](/windows/msix/package/packaging-uwp-apps).</span></span>

## <a name="instructions"></a><span data-ttu-id="ca6dd-109">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ca6dd-109">Instructions</span></span>

### <a name="step-1-create-a-package-writer"></a><span data-ttu-id="ca6dd-110">Schritt 1: Erstellen eines paketwriters</span><span class="sxs-lookup"><span data-stu-id="ca6dd-110">Step 1: Create a package writer</span></span>

<span data-ttu-id="ca6dd-111">Um einen paketwriter zu erstellen, rufen Sie die [**iappxfactory:: kreatepackagewriter**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-111">To create a package writer, call the [**IAppxFactory::CreatePackageWriter**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagewriter) method.</span></span> <span data-ttu-id="ca6dd-112">Der erste Parameter ist ein Ausgabestream, in den das Paket geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-112">The first parameter is an output stream where the package will be written.</span></span> <span data-ttu-id="ca6dd-113">Der zweite Parameter ist ein Zeiger auf eine [**AppX- \_ Paket \_ Einstellungs**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) Struktur, die Paket Einstellungen angibt.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-113">The second parameter is a pointer to an [**APPX\_PACKAGE\_SETTINGS**](/windows/desktop/api/AppxPackaging/ns-appxpackaging-appx_package_settings) structure that specifies package settings.</span></span> <span data-ttu-id="ca6dd-114">Der dritte Parameter ist ein Ausgabeparameter, der einen Zeiger auf einen [**iappxpackagewriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) -Zeiger empfängt.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-114">The third parameter is an output parameter that receives a pointer to an [**IAppxPackageWriter**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter) pointer.</span></span>


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



### <a name="step-2-add-the-payload-files-for-your-app-to-the-package"></a><span data-ttu-id="ca6dd-115">Schritt 2: Hinzufügen der Nutz Last Dateien für Ihre APP zum Paket</span><span class="sxs-lookup"><span data-stu-id="ca6dd-115">Step 2: Add the payload files for your app to the package</span></span>

<span data-ttu-id="ca6dd-116">Rufen Sie die [**iappxpackagewriter:: addpayloadfile**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) -Methode auf, um dem Paketdateien hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-116">Call the [**IAppxPackageWriter::AddPayloadFile**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-addpayloadfile) method to add files to the package.</span></span> <span data-ttu-id="ca6dd-117">Der erste Parameter ist der relative Pfad der Datei.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-117">The first parameter is the relative path of the file.</span></span> <span data-ttu-id="ca6dd-118">Der zweite Parameter gibt den Inhaltstyp der Datei an.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-118">The second parameter indicates the content type of the file.</span></span> <span data-ttu-id="ca6dd-119">Der dritte Parameter gibt Optionen aus der [**AppX \_ - \_ komprimierungsoptionsenumeration**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) an.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-119">The third parameter specifies options from the [**APPX\_COMPRESSION\_OPTION**](/windows/desktop/api/AppxPackaging/ne-appxpackaging-appx_compression_option) enumeration.</span></span> <span data-ttu-id="ca6dd-120">Der vierte Parameter ist der Eingabestream für die Datei.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-120">The fourth parameter is the input stream for the file.</span></span>


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



<span data-ttu-id="ca6dd-121">Der vorherige Code verwendet diese Variablen Definitionen und `GetFileStream` Hilfsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-121">The previous code uses these variable definitions and `GetFileStream` helper function.</span></span>


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



### <a name="step-3-add-the-package-manifest-to-the-package"></a><span data-ttu-id="ca6dd-122">Schritt 3: Hinzufügen des Paket Manifests zum Paket</span><span class="sxs-lookup"><span data-stu-id="ca6dd-122">Step 3: Add the package manifest to the package</span></span>

<span data-ttu-id="ca6dd-123">Jedes Paket muss über ein Paket Manifest verfügen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-123">Every package must have a package manifest.</span></span> <span data-ttu-id="ca6dd-124">Um das Paket Manifest zum Paket hinzuzufügen, erstellen Sie einen Eingabestream für die Datei, und rufen Sie dann die [**iappxpackagewriter:: Close**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) -Methode auf, um das Manifest am Ende des Pakets zu schreiben und den Ausgabestream für den paketwriter zu schließen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-124">To add the package manifest to the package, create an input stream for the file, then call the [**IAppxPackageWriter::Close**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagewriter-close) method to write the manifest at the end of the package and close the output stream for package writer.</span></span>

<span data-ttu-id="ca6dd-125">In diesem Code wird die `GetFileStream` im vorherigen Schritt gezeigte Hilfsfunktion verwendet, um den Datenstrom für das Paket Manifest zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-125">This code uses the `GetFileStream` helper function shown in the previous step to create the stream for the package manifest.</span></span>


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



### <a name="step-4-clean-up-the-package-writer"></a><span data-ttu-id="ca6dd-126">Schritt 4: Bereinigen des paketwriters</span><span class="sxs-lookup"><span data-stu-id="ca6dd-126">Step 4: Clean up the package writer</span></span>

<span data-ttu-id="ca6dd-127">Bevor Sie von der-Funktion zurückgegeben `wmain` werden, müssen Sie die [**releasemethode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) zum Bereinigen des paketwriter und die Funktion " [**count Initialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="ca6dd-127">Before returning from the `wmain` function, call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method to clean up the package writer and call the [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
if (packageWriter != NULL)
{
    packageWriter->Release();
    packageWriter = NULL;
}
CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="ca6dd-128">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ca6dd-128">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ca6dd-129">**Beispiele**</span><span class="sxs-lookup"><span data-stu-id="ca6dd-129">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="ca6dd-130">App-Paket erstellen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="ca6dd-130">Create app package sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingCreateAppx)
</dt> <dt>

<span data-ttu-id="ca6dd-131">**Verweis**</span><span class="sxs-lookup"><span data-stu-id="ca6dd-131">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="ca6dd-132">**Iappxpackagewriter**</span><span class="sxs-lookup"><span data-stu-id="ca6dd-132">**IAppxPackageWriter**</span></span>](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagewriter)
</dt> </dl>

 

 