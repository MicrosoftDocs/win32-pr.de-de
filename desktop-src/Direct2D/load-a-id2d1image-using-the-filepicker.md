---
title: Laden eines Bilds in Direct2D Effekte mithilfe der Dateiauswahl
description: Zeigt, wie Sie die Windows-Speicher-Picker fileopenpicker zum Laden eines Bilds in Direct2D-Effekte verwenden.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4346cc0e337374fa41313cb77debf4faca781669
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337233"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Laden eines Bilds in Direct2D Effekte mithilfe der Dateiauswahl

Veranschaulicht die Verwendung von [**Windows:: Storage::P icker:: fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) zum Laden eines Bilds in [Direct2D-Effekte](effects-overview.md). Wenn Sie zulassen möchten, dass der Benutzer eine Bilddatei aus dem Speicher in einer Windows Store-App auswählt, wird die Verwendung von [**fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)empfohlen.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D Effekte](effects-overview.md)
-   [**Windows:: Storage::P ickers:: fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Voraussetzungen

-   Zum Erstellen von Effekten benötigen Sie ein [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Objekt.
-   Sie benötigen ein [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) -Objekt zum Erstellen von WIC-Objekten.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-open-the-file-picker"></a>Schritt 1: Öffnen der Dateiauswahl

Erstellen Sie ein [**fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) -Objekt, und legen Sie *ViewMode*, Vorschlags *Plan Start Location* und den *filetypefilter* für die Auswahl von Images fest. Aufrufen der [**picksinglefileasync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) -Methode.


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Nachdem [**picksinglefileasync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) abgeschlossen ist, erhalten Sie einen Dateistream von der [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) -Schnittstelle, die zurückgegeben wird.

### <a name="step-2-get-a-file-stream"></a>Schritt 2: erhalten eines Datei Datenstroms

Deklarieren Sie einen Vervollständigungs Handler, der ausgeführt wird, nachdem der asynchrone Vorgang für die Dateiauswahl Verwenden Sie die [**GetResults**](/previous-versions//br205815(v=vs.85)) -Methode, um die Datei abzurufen und das Dateistream-Objekt abzurufen.


```C++
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file) // If file == nullptr, the user did not select a file.
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
```



Im nächsten Schritt konvertieren Sie das [**jeandomaccessstream**](/previous-versions//hh438400(v=vs.85)) -Objekt in ein [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , das Sie an [WIC](/windows/desktop/wic/-wic-api)übergeben können.

### <a name="step-3-convert-the-file-stream"></a>Schritt 3: Konvertieren des Datei Datenstroms

Verwenden Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) ", um den Dateistream zu konvertieren. Windows-Runtime-APIs stellen Streams mit " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85))" dar, während [WIC](/windows/desktop/wic/-wic-api) [**IStream verwendet**](/windows/desktop/api/objidl/nn-objidl-istream).


```C++
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
        reinterpret_cast<IUnknown*>(fileStream),
        IID_PPV_ARGS(&istream)
        )
    );
```



> [!Note]  
> Wenn Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) " verwenden möchten, sollten Sie " *shcore. h* " in Ihr Projekt einschließen.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Schritt 4: Erstellen eines WIC-Decoders und des Abbilds

Erstellen Sie ein [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt mithilfe der [**IWICImagingFactory:: | atedecoderfromstream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) -Methode.


```C++
    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );
```



Verwenden Sie die [**IWICBitmapDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) -Methode, um den ersten Frame des Bilds vom Decoder zu erhalten.


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Schritt 5: Erstellen eines WIC-Konverters und initialisieren

Konvertieren Sie das Bild mit [WIC](/windows/desktop/wic/-wic-api)in das BGRA-Farb Format. [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) gibt das systemeigene Pixel Format des Bilds zurück, z. b. jpeer-Daten werden in GUID- \_ WICPixelFormat24bppBGR gespeichert. Als Leistungsoptimierung mit Direct2D wird jedoch empfohlen, dass Sie in WICPixelFormat32bppPBGRA konvertieren.

1.  Erstellen Sie ein [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) -Objekt mithilfe der [**IWICImagingFactory:: deateformatconverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) -Methode.

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Initialisieren Sie den Format Konverter, um das WICPixelFormat32bppPBGRA zu verwenden, und übergeben Sie den BitmapFrame.

    ```C++
       DX::ThrowIfFailed(
            converter->Initialize(
                frame.Get(),
                GUID_WICPixelFormat32bppPBGRA,
                WICBitmapDitherTypeNone,
                nullptr,
                0.0f,
                WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
                )
            );
    ```

    

Die [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) -Schnittstelle wird von der [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle abgeleitet, sodass Sie den Konverter an den [bitmapquelleffekt](bitmap-source.md) übergeben können.

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Schritt 6: Erstellen eines Effekts und übergeben in eine IWICBitmapSource

Verwenden Sie die Methode " [**kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ", um mit dem [Direct2D](getting-started-with-direct2d.md) [**-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)ein [Bitmap-Quell](bitmap-source.md) - [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekt zu erstellen

Verwenden Sie die [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode, um die *\_ \_ \_ \_ BitmapSource \_ -Eigenschaft der D2D1 BitmapSource* -Eigenschaft auf den [WIC](/windows/desktop/wic/-wic-api) - [**Format Konverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)festzulegen.

> [!Note]  
> Der [Bitmap-Quell](bitmap-source.md) Effekt nimmt keine Eingabe der [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) -Methode auf, wie viele [Direct2D Effekte](effects-overview.md). Stattdessen wird das [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) -Objekt als Eigenschaft angegeben.

 


```C++
    ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
```



Nun, da Sie den [Bitmap-Quell](bitmap-source.md) Effekt haben, können Sie ihn als Eingabe für beliebige [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) verwenden und ein Effekt Diagramm erstellen.

## <a name="complete-example"></a>Vollständiges Beispiel

Im folgenden finden Sie den vollständigen Code für dieses Beispiel.


```C++
ComPtr<ID2D1Effect> bitmapSourceEffect;

void OpenFilePicker()
{
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
    
    pickOperation->Completed = ref new AsyncOperationCompletedHandler<StorageFile^>(
          [=](IAsyncOperation<StorageFile^> ^operation, AsyncStatus status)
    {
        auto file = operation->GetResults();
        if (file)
        {
                             auto openOperation = file->OpenAsync(FileAccessMode::Read);
                             openOperation->Completed = ref new
                                      AsyncOperationCompletedHandler<IRandomAccessStream^>(
                                      [=](IAsyncOperation<IRandomAccessStream^> ^operation, AsyncStatus status)
                             {
                                      auto fileStream = operation->GetResults();

                                      // Pass IRandomAccessStream^ into DirectXApp for decoding/processing.
                                      OpenFile(fileStream);
                             });
        }
    });
}

void OpenFile(Windows::Storage::Streams::IRandomAccessStream^ fileStream)
{
    ComPtr<IStream> istream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(
            reinterpret_cast<IUnknown*>(fileStream),
            IID_PPV_ARGS(&istream)
            )
        );

    ComPtr<IWICBitmapDecoder> decoder;
    DX::ThrowIfFailed(
          m_wicFactory->CreateDecoderFromStream(
                    istream.Get(),
                    nullptr,
                    WICDecodeMetadataCacheOnDemand,
                    &decoder
                    )
          );

    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );

    ComPtr<IWICFormatConverter> converter;
    DX::ThrowIfFailed(
        m_wicFactory->CreateFormatConverter(&converter)
        );

    DX::ThrowIfFailed(
        converter->Initialize(
            frame.Get(),
            GUID_WICPixelFormat32bppPBGRA,
            WICBitmapDitherTypeNone,
            nullptr,
            0.0f,
            WICBitmapPaletteTypeCustom  // premultiplied BGRA has no paletting, so this is ignored
            )
        );

       ComPtr<ID2D1Effect> bitmapSourceEffect;

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect)
        );

    DX::ThrowIfFailed(
        bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, converter.Get())
        );

    // Insert code using the bitmap source in an effect graph.
}
```



 

 