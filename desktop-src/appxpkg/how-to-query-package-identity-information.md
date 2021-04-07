---
title: Abfragen von App-Paket Manifest-Informationen (C++)
description: Erfahren Sie, wie Sie mithilfe der Paket-API Informationen aus dem App-Paket Manifest für eine Windows-APP erhalten.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9940f92a4412be7731db2454d68b4429522b63f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038812"
---
# <a name="query-app-package-manifest-info-c"></a>Abfragen von App-Paket Manifest-Informationen (C++)

Erfahren Sie, wie Sie mithilfe der Paket- [API](interfaces.md)Informationen aus dem App-Paket Manifest für eine Windows-APP erhalten.

### <a name="create-a-package-manifest-reader"></a>Erstellen eines Paket Manifest-Readers

Zum Erstellen eines Paket Manifest-Readers rufen Sie [**iappxfactory:: kreatepackagereader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) zum Erstellen eines Paket Readers auf. Der erste Parameter ist ein Eingabestream für das Paket (AppX-Datei). Der zweite Parameter ist ein Ausgabeparameter, der einen Zeiger auf einen [**iappxpackagereader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) -Zeiger empfängt. Rufen Sie als nächstes [**iappxpackagereader:: getmanifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) auf, um den Manifest-Reader abzurufen. Der-Parameter ist ein Ausgabeparameter, der einen Zeiger auf einen [**iappxmanifestreader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) -Zeiger empfängt.


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
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



### <a name="read-package-identity-info"></a>Informationen zum Lesen von Paket Identitäten

Die Paket Identifizierung wird mithilfe des [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) -Elements im Manifest angegeben. Verwenden Sie [**iappxmanifestreader:: getpackageid**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) , um ein [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) -Element zum Lesen von Paket Identitätsinformationen zu erhalten, wie hier gezeigt.

In diesem Code wird [**IAppxManifestPackageId:: getpackagefullname**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) verwendet, um den vollständigen Paketnamen abzurufen, [**IAppxManifestPackageId:: GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) , um den Paketnamen abzurufen, und [**IAppxManifestPackageId:: GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) , um die Paketversion zu erhalten.


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a>Lesen von Metadaten, die das Paket für Benutzer beschreiben

Eigenschaften werden mit dem [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) -Element im Manifest angegeben. Verwenden Sie [**iappxmanifestreader:: GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) , um eine [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) zum Lesen dieses Knotens zu erhalten, wie hier gezeigt.

In diesem Code wird [**IAppxManifestProperties:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) verwendet, um den Paket anzeigen Amen und die Paketbeschreibung zu erhalten.


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a>Lesen von Metadaten zu den im Paket enthaltenen apps

Apps werden mit dem [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) -Element im Manifest angegeben. Verwenden Sie [**iappxmanifestreader:: GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) zum Aufrufen eines [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) zum Lesen dieses Knotens. Verwenden Sie [**IAppxManifestApplicationsEnumerator:: GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) und [**IAppxManifestApplicationsEnumerator:: apvenext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) , um eine [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) für jede APP im Paket zu erhalten.

In diesem Code wird [**IAppxManifestApplication:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) verwendet, um den anzeigen Amen für jede APP zu erhalten.


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a>Bereinigen des Paket Manifest-Readers

Bevor Sie von der-Funktion zurückgegeben `wmain` werden, müssen Sie die [**releasemethode**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) zum Bereinigen des Paket Manifest-Readers und zum Abrufen der Funktion " [**count**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) " abrufen.


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
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

[Beispiel für das Abfragen von App-Paketen und App-Manifest](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

**Verweis**
</dt> <dt>

[**Iappxmanifestreader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 