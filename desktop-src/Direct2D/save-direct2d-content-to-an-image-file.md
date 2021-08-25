---
title: Speichern von Direct2D-Inhalten in einer Bilddatei
description: In diesem Thema wird gezeigt, wie Sie IWICImageEncoder verwenden, um Inhalte in Form eines ID2D1Image in einer codierten Bilddatei wie JPEG zu speichern.
ms.assetid: F0D8BFC7-723A-4577-B2DF-4D656A18E2FC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c6020b29be3771575919ccb0200718e8e608afded584471625cfa922aee8da8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160366"
---
# <a name="how-to-save-direct2d-content-to-an-image-file"></a>Speichern von Direct2D-Inhalten in einer Bilddatei

In diesem Thema wird gezeigt, wie [**Sie IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) verwenden, um Inhalte in Form eines [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei wie JPEG zu speichern. Wenn Sie eine Windows Store-App schreiben, können Sie festlegen, dass der Benutzer mit [**Windows::Storage::P dos::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)eine Zieldatei auswählt.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D-Effekte](effects-overview.md)
-   [**Windows::Storage::P anzeigen::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen ein [**ID2D1DeviceContext-Objekt**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) und ein Objekt mit [Direct2D-Inhalt,](./direct2d-portal.md) das [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) implementiert, z.B. [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) oder [**ID2D1Bitmap1.**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)

## <a name="instructions"></a>Anweisungen

### <a name="step-1-get-a-destination-file-and-stream"></a>Schritt 1: Abrufen einer Zieldatei und eines Streams

Wenn Sie dem Benutzer die Auswahl einer Zieldatei gestatten möchten, können Sie [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)verwenden, die zurückgegebene Datei öffnen und einen [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) abrufen, der mit WIC verwendet werden soll.

Erstellen Sie einen [**Windows::Storage::P anzeigen::FileSavePicker,**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) und legen Sie dessen Parameter für Bilddateien fest. Rufen Sie die [**PickSaveFileAsync-Methode**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) auf.


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



Deklarieren Sie einen Vervollständigungshandler, der ausgeführt werden soll, nachdem der asynchrone Vorgang der Dateiauswahl zurückgegeben wurde. Verwenden Sie die [**GetResults-Methode,**](/windows/desktop/WinRT/iasyncaction-getresults) um die Datei abzurufen und das Dateistreamobjekt abzurufen.


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



Rufen Sie einen [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) ab, indem [**Sie OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) für die Datei aufrufen und das Ergebnis des asynchronen Vorgangs abrufen.


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



Verwenden Sie abschließend die [**CreateStreamOverRandomAccessStream-Methode,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) um den Dateistream zu konvertieren. Windows Laufzeit-APIs stellen Streams mit [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))dar, während WIC [**IStream nutzt.**](/windows/desktop/api/objidl/nn-objidl-istream)


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> Um die [**CreateStreamOverRandomAccessStream-Funktion**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) zu verwenden, sollten Sie **shcore.h** in Ihr Projekt einschließen.

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a>Schritt 2: Abrufen der WIC-Bitmap und des Frameencoders

[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) bieten die Funktionalität zum Speichern von Imagedaten in einem codierten Dateiformat.

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



### <a name="step-3-get-an-iwicimageencoder"></a>Schritt 3: Abrufen eines IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) ist eine neue Schnittstelle in Windows 8. Sie kann aus [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)erstellt werden, wodurch **IWICImagingFactory** erweitert wird und auch für Windows 8 neu ist.


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



Rufen Sie [**IWICImagingFactory2::CreateImageEncoder auf.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder) Der erste Parameter ist ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) und muss das Gerät sein, auf dem das Image erstellt wurde, das Sie codieren möchten. Sie können keine Images aus verschiedenen Ressourcendomänen innerhalb eines einzelnen [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)kombinieren.


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a>Schritt 4: Schreiben des Direct2D-Inhalts mit IWICImageEncoder

[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) kann ein [Direct2D-Bild](./direct2d-portal.md) in einen Bildrahmen, eine Frameminiatur oder die Containerminiatur schreiben. Anschließend können Sie [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) verwenden, um die Imagingdaten wie gewohnt in eine Datei zu codieren.

Schreiben Sie das [Direct2D-Bild](./direct2d-portal.md) in den Frame. In diesem Codeausschnitt schreiben wir eine [**ID2D1Bitmap,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) die gerasterte Direct2D-Inhalte enthält. Sie können jedoch eine beliebige Schnittstelle bereitstellen, die [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)implementiert.


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
> Der [**Id2D1Image-Parameter**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) muss auf dem [**ID2D1Device-Objekt**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) erstellt worden sein, das an [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)übergeben wurde.

 

Committen Sie die WIC- und Streamressourcen, um den Vorgang fertig zu stellen.


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
> Einige Implementierungen von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) implementieren nicht die [**Commit-Methode**](/windows/desktop/api/objidl/nf-objidl-istream-commit) und geben **E \_ NOTIMPL** zurück.

 

Nun verfügen Sie über eine Datei mit dem [Direct2D-Image.](./direct2d-portal.md)

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



 

 