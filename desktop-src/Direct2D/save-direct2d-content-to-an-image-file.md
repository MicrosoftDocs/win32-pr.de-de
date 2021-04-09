---
title: Speichern von Direct2D-Inhalten in einer Bilddatei
description: In diesem Thema wird gezeigt, wie iwicimageencoder verwendet wird, um Inhalt in Form einer ID2D1Image in einer codierten Bilddatei (z. b. JPEG) zu speichern.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b19146d838474046fd634cb5524ddf2367fd1d6c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858301"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Speichern von Direct2D-Inhalten in einer Bilddatei

In diesem Thema wird gezeigt, wie [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) verwendet wird, um Inhalt in Form einer [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei (z. b. JPEG) zu speichern. Wenn Sie eine Windows Store-App schreiben, können Sie den Benutzer mithilfe von [**Windows:: Storage::P icker:: filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)eine Zieldatei auswählen lassen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D Effekte](effects-overview.md)
-   [**Windows:: Storage::P icker:: filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen ein [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Objekt und ein Objekt, das [Direct2D](./direct2d-portal.md) -Inhalt enthält, der [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) wie z. b. [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) oder [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)implementiert.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-get-a-destination-file-and-stream"></a>Schritt 1: eine Zieldatei und einen Stream

Wenn Sie dem Benutzer die Auswahl einer Zieldatei gestatten möchten, können Sie [**filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)verwenden, die zurückgegebene Datei öffnen und einen [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) für die Verwendung mit WIC Abrufen.

Erstellen Sie einen [**Windows:: Storage::P ickers:: filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) , und legen Sie dessen Parameter für Bilddateien fest. Aufrufen der [**picksavefileasync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) -Methode.


```C++
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    savePicker->DefaultFileExtension = ".jpg";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
```



Deklarieren Sie einen Vervollständigungs Handler, der ausgeführt wird, nachdem der asynchrone Vorgang für die Dateiauswahl Verwenden Sie die [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) -Methode, um die Datei abzurufen und das Dateistream-Objekt abzurufen.


```C++
    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }
```



Rufen Sie einen " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85)) " ab, indem Sie [**openasync**](/uwp/api/windows.storage.storagefile.openasync) für die Datei aufrufen und das Ergebnis des asynchronen Vorgangs erhalten.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Verwenden Sie abschließend die [**Methode "**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) Methode", um den Dateistream zu konvertieren. Windows-Runtime-APIs stellen Streams mit " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85))" dar, während WIC [**IStream verwendet**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Wenn Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) " verwenden möchten, sollten Sie " **shcore. h** " in Ihr Projekt einschließen.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Schritt 2: erhalten der WIC-Bitmap und des Frame Encoders

[Iwicbitmapcoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) stellen die Funktionalität bereit, um Abbild Erstellungs Daten in einem codierten Dateiformat zu speichern.

Erstellen und initialisieren Sie die Encoderobjekte.


```C++
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );
```



### <a name="step-3-get-an-iwicimageencoder"></a>Schritt 3: Holen Sie sich einen iwicimageencoder

[**Iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) ist eine neue Schnittstelle in Windows 8. Sie kann über [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)erstellt werden, das **IWICImagingFactory** erweitert und auch für Windows 8 neu ist.


```C++
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );
```



Aufrufen von [**IWICImagingFactory2:: kreateimageencoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder). Der erste Parameter ist ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) und muss das Gerät sein, auf dem das zu codierende Image erstellt wurde – Sie können Bilder aus verschiedenen Ressourcen Domänen innerhalb eines einzelnen [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)nicht mischen.


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Schritt 4: Schreiben des Direct2D-Inhalts mit iwicimageencoder

[**Iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) kann ein [Direct2D](./direct2d-portal.md) -Bild in einen Bildframe, eine Frame-Miniaturansicht oder die Miniaturansicht des Containers schreiben. Anschließend können Sie [iwicbitmakcoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) verwenden, um die Abbild Erstellungs Daten in einer Datei als normal zu codieren.

Schreiben Sie das [Direct2D](./direct2d-portal.md) -Image in den Frame. In diesem Code Ausschnitt schreiben wir eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , die einen gerastertes Direct2D-Inhalt enthält. Allerdings können Sie jede beliebige Schnittstelle bereitstellen, die [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)implementiert.


```C++
    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );
```



> [!Note]  
> Der [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Parameter muss für den [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) erstellt worden sein, der an [**IWICImagingFactory2:: | ateimageencoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)übergeben wurde.

 

Commit der WIC-und Stream-Ressourcen, um den Vorgang abzuschließen.


```C++
    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
```



> [!Note]  
> Einige Implementierungen von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) implementieren die [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) -Methode nicht und geben **E \_ notimpl** zurück.

 

Nun verfügen Sie über eine Datei mit dem [Direct2D](./direct2d-portal.md) -Image.

## <a name="complete-example"></a>Vollständiges Beispiel

Hier der vollständige Code für dieses Beispiel.

```cpp
ComPtr<IWICImagingFactory2> m_wicFactory;

DX::ThrowIfFailed(
    CoCreateInstance(
        CLSID_WICImagingFactory,
        nullptr,
        CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&m_wicFactory)
        )
    );

void SaveAsImageFile::SaveBitmapToFile()
{
    // Prepare a file picker for customers to input image file name.
    Pickers::FileSavePicker^ savePicker = ref new Pickers::FileSavePicker();
    auto pngExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    pngExtensions->Append(".png");
    savePicker->FileTypeChoices->Insert("PNG file", pngExtensions);
    auto jpgExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    jpgExtensions->Append(".jpg");
    savePicker->FileTypeChoices->Insert("JPEG file", jpgExtensions);
    auto bmpExtensions = ref new Platform::Collections::Vector<Platform::String^>();
    bmpExtensions->Append(".bmp");
    savePicker->FileTypeChoices->Insert("BMP file", bmpExtensions);
    savePicker->DefaultFileExtension = ".png";
    savePicker->SuggestedFileName = "SaveScreen";
    savePicker->SuggestedStartLocation = Pickers::PickerLocationId::PicturesLibrary;

    task<StorageFile^> fileTask(savePicker->PickSaveFileAsync());
    fileTask.then([=](StorageFile^ file) {
        if (file != nullptr)
        {
            // User selects a file.
            m_imageFileName = file->Name;
            GUID wicFormat = GUID_ContainerFormatPng;
            if (file->FileType == ".bmp")
            {
                wicFormat = GUID_ContainerFormatBmp;
            }
            else if (file->FileType == ".jpg")
            {
                wicFormat = GUID_ContainerFormatJpeg;
            }

            // Retrieve a stream from the file.
            task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
            createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
                // Convert the RandomAccessStream to an IStream.
                ComPtr<IStream> stream;
                DX::ThrowIfFailed(
                    CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
                    );

                SaveBitmapToStream(m_d2dTargetBitmap, m_wicFactory, m_d2dContext, wicFormat, stream.Get());
            });
        }
    });
}

// Save render target bitmap to a stream using WIC.
void SaveAsImageFile::SaveBitmapToStream(
    _In_ ComPtr<ID2D1Bitmap1> d2dBitmap,
    _In_ ComPtr<IWICImagingFactory2> wicFactory2,
    _In_ ComPtr<ID2D1DeviceContext> d2dContext,
    _In_ REFGUID wicFormat,
    _In_ IStream* stream
    )
{
    // Create and initialize WIC Bitmap Encoder.
    ComPtr<IWICBitmapEncoder> wicBitmapEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateEncoder(
            wicFormat,
            nullptr,    // No preferred codec vendor.
            &wicBitmapEncoder
            )
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Initialize(
            stream,
            WICBitmapEncoderNoCache
            )
        );

    // Create and initialize WIC Frame Encoder.
    ComPtr<IWICBitmapFrameEncode> wicFrameEncode;
    DX::ThrowIfFailed(
        wicBitmapEncoder->CreateNewFrame(
            &wicFrameEncode,
            nullptr     // No encoder options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Initialize(nullptr)
        );

    // Retrieve D2D Device.
    ComPtr<ID2D1Device> d2dDevice;
    d2dContext->GetDevice(&d2dDevice);

    // Create IWICImageEncoder.
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );

    DX::ThrowIfFailed(
        imageEncoder->WriteFrame(
            d2dBitmap.Get(),
            wicFrameEncode.Get(),
            nullptr     // Use default WICImageParameter options.
            )
        );

    DX::ThrowIfFailed(
        wicFrameEncode->Commit()
        );

    DX::ThrowIfFailed(
        wicBitmapEncoder->Commit()
        );

    // Flush all memory buffers to the next-level storage object.
    DX::ThrowIfFailed(
        stream->Commit(STGC_DEFAULT)
        );
}

```



 

 