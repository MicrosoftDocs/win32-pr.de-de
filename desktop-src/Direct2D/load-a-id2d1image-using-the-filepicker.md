---
title: Laden eines Bilds in Direct2D-Effekte mit filePicker
description: Zeigt, wie Sie die dateiopenPicker-Datei der Windows Storage verwenden, um ein Bild in Direct2D-Effekte zu laden.
ms.assetid: 42158EF0-2FC8-45F3-8C92-E12318D4724F
keywords:
- FileOpenPicker
- FilePicker
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05bb23faf2b9d50f12219f3b99c07ec835558addc55e67d4843dee049946a60d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160531"
---
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a>Laden eines Bilds in Direct2D-Effekte mit filePicker

Zeigt, wie sie den [**Windows::Storage::P schlüssels::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) verwenden, um ein Bild in [Direct2D-Effekte](effects-overview.md)zu laden. Wenn Sie dem Benutzer erlauben möchten, eine Bilddatei aus dem Speicher in einer Windows Store-App auszuwählen, wird empfohlen, [**fileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)zu verwenden.

## <a name="what-you-need-to-know"></a>Wichtige Informationen

### <a name="technologies"></a>Technologien

-   [Direct2D](./direct2d-portal.md)
-   [Direct2D-Effekte](effects-overview.md)
-   [**Windows::Storage::P anzeigen::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen ein [**ID2D1DeviceContext-Objekt**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) zum Erstellen von Effekten.
-   Sie benötigen ein [**IWICImagingFactory-Objekt**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) zum Erstellen von WIC-Objekten.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-open-the-file-picker"></a>Schritt 1: Öffnen der Dateiauswahl

Erstellen Sie ein [**FileOpenPicker-Objekt,**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) und legen *Sie viewMode,* *SuggestedStartLocation* und *FileTypeFilter* zum Auswählen von Bildern fest. Rufen Sie die [**PickSingleFileAsync-Methode**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) auf.


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



Nachdem [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) abgeschlossen ist, erhalten Sie einen Dateistream von der [**IAsyncOperation-Schnittstelle,**](/previous-versions//bb776309(v=vs.85)) die zurückgegeben wird.

### <a name="step-2-get-a-file-stream"></a>Schritt 2: Abrufen eines Dateistreams

Deklarieren Sie einen Vervollständigungshandler, der ausgeführt werden soll, nachdem der asynchrone Vorgang der Dateiauswahl zurückgegeben wurde. Verwenden Sie die [**GetResults-Methode,**](/previous-versions//br205815(v=vs.85)) um die Datei abzurufen und das Dateistreamobjekt abzurufen.


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



Im nächsten Schritt konvertieren Sie das [**IRandomAccessStream-Objekt**](/previous-versions//hh438400(v=vs.85)) in einen [**IStream,**](/windows/desktop/api/objidl/nn-objidl-istream) den Sie an [WIC](/windows/desktop/wic/-wic-api)übergeben können.

### <a name="step-3-convert-the-file-stream"></a>Schritt 3: Konvertieren des Dateistreams

Verwenden Sie die [**CreateStreamOverRandomAccessStream-Funktion,**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) um den Dateistream zu konvertieren. Windows Laufzeit-APIs stellen Streams mit [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85))dar, während [WIC](/windows/desktop/wic/-wic-api) [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream)nutzt.


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
> Um die [**CreateStreamOverRandomAccessStream-Funktion**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) zu verwenden, sollten Sie *shcore.h* in Ihr Projekt einschließen.

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a>Schritt 4: Erstellen eines WIC-Decoders und Abrufen des Frames

Erstellen Sie ein [**IWICBitmapDecoder-Objekt**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) mithilfe der [**IWICImagingFactory::CreateDecoderFromStream-Methode.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)


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



Abrufen des ersten Bildrahmens aus dem Decoder mithilfe der [**IWICBitmapDecoder::GetFrame-Methode.**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a>Schritt 5: Erstellen eines WIC-Konverters und Initialisieren

Konvertieren Sie das Bild mithilfe von [WIC](/windows/desktop/wic/-wic-api)in das BGRA-Farbformat. [IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) gibt das systemeigene Pixelformat des Bilds zurück, wie JPEGs in GUID \_ WICPixelFormat24bppBGR gespeichert werden. Als Leistungsoptimierung mit Direct2D wird jedoch empfohlen, in WICPixelFormat32bppPBGRA zu konvertieren.

1.  Erstellen Sie ein [**IWICFormatConverter-Objekt**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) mithilfe der [**IWICImagingFactory::CreateFormatConverter-Methode.**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter)

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  Initialisieren Sie den Formatkonverter, um WICPixelFormat32bppPBGRA zu verwenden, und übergeben Sie den Bitmaprahmen.

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

    

Die [**IWICFormatConverter-Schnittstelle**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) wird von der [**IWICBitmapSource-Schnittstelle**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) abgeleitet, sodass Sie den Konverter an den [Bitmap-Quelleffekt](bitmap-source.md) übergeben können.

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a>Schritt 6: Erstellen eines Effekts und Übergeben einer IWICBitmapSource

Verwenden Sie die [**CreateEffect-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) um mithilfe des Direct2D-Gerätekontexts ein [Bitmapquell-ID2D1Effect-Objekt](bitmap-source.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) zu erstellen. [](getting-started-with-direct2d.md) [](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

Verwenden Sie die [**ID2D1Effect::SetValue-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) um die *EIGENSCHAFT D2D1 \_ BITMAPSOURCE \_ PROP \_ WIC BITMAP \_ \_ SOURCE* auf den WIC-Formatkonverter festzulegen. [](/windows/desktop/wic/-wic-api) [](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)

> [!Note]  
> Der [Bitmapquelleffekt](bitmap-source.md) nimmt keine Eingabe von der [**SetInput-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) wie viele [Direct2D-Effekte](effects-overview.md)an. Stattdessen wird das [**IWICBitmapSource-Objekt**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) als -Eigenschaft angegeben.

 


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



Nachdem Sie nun über den [Bitmap-Quelleffekt](bitmap-source.md) verfügen, können Sie ihn als Eingabe für jeden [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) verwenden und ein Effektdiagramm erstellen.

## <a name="complete-example"></a>Vollständiges Beispiel

Hier ist der vollständige Code für dieses Beispiel.


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



 

 