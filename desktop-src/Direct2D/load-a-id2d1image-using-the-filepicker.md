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
# <a name="how-to-load-an-image-into-direct2d-effects-using-the-filepicker"></a><span data-ttu-id="691ab-105">Laden eines Bilds in Direct2D Effekte mithilfe der Dateiauswahl</span><span class="sxs-lookup"><span data-stu-id="691ab-105">How to load an image into Direct2D effects using the FilePicker</span></span>

<span data-ttu-id="691ab-106">Veranschaulicht die Verwendung von [**Windows:: Storage::P icker:: fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) zum Laden eines Bilds in [Direct2D-Effekte](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="691ab-106">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="691ab-107">Wenn Sie zulassen möchten, dass der Benutzer eine Bilddatei aus dem Speicher in einer Windows Store-App auswählt, wird die Verwendung von [**fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)empfohlen.</span><span class="sxs-lookup"><span data-stu-id="691ab-107">If you want to let the user select an image file from storage in a Windows Store app, we recommend that you use the [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="691ab-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="691ab-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="691ab-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="691ab-109">Technologies</span></span>

-   [<span data-ttu-id="691ab-110">Direct2D</span><span class="sxs-lookup"><span data-stu-id="691ab-110">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="691ab-111">Direct2D Effekte</span><span class="sxs-lookup"><span data-stu-id="691ab-111">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="691ab-112">**Windows:: Storage::P ickers:: fileopenpicker**</span><span class="sxs-lookup"><span data-stu-id="691ab-112">**Windows::Storage::Pickers::FileOpenPicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileOpenPicker)

### <a name="prerequisites"></a><span data-ttu-id="691ab-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="691ab-113">Prerequisites</span></span>

-   <span data-ttu-id="691ab-114">Zum Erstellen von Effekten benötigen Sie ein [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="691ab-114">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object for creating effects.</span></span>
-   <span data-ttu-id="691ab-115">Sie benötigen ein [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) -Objekt zum Erstellen von WIC-Objekten.</span><span class="sxs-lookup"><span data-stu-id="691ab-115">You need an [**IWICImagingFactory**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory) object for creating WIC objects.</span></span>

## <a name="instructions"></a><span data-ttu-id="691ab-116">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="691ab-116">Instructions</span></span>

### <a name="step-1-open-the-file-picker"></a><span data-ttu-id="691ab-117">Schritt 1: Öffnen der Dateiauswahl</span><span class="sxs-lookup"><span data-stu-id="691ab-117">Step 1: Open the file picker</span></span>

<span data-ttu-id="691ab-118">Erstellen Sie ein [**fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) -Objekt, und legen Sie *ViewMode*, Vorschlags *Plan Start Location* und den *filetypefilter* für die Auswahl von Images fest.</span><span class="sxs-lookup"><span data-stu-id="691ab-118">Create a [**FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) object and set the *ViewMode*, *SuggestedStartLocation*, and the *FileTypeFilter* for selecting images.</span></span> <span data-ttu-id="691ab-119">Aufrufen der [**picksinglefileasync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) -Methode.</span><span class="sxs-lookup"><span data-stu-id="691ab-119">Call the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) method.</span></span>


```C++
    FileOpenPicker^ openPicker = ref new FileOpenPicker();
    openPicker->ViewMode = PickerViewMode::Thumbnail;
    openPicker->SuggestedStartLocation = PickerLocationId::PicturesLibrary;
    openPicker->FileTypeFilter->Append(".jpg");
    auto pickOperation = openPicker->PickSingleFileAsync();
```



<span data-ttu-id="691ab-120">Nachdem [**picksinglefileasync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) abgeschlossen ist, erhalten Sie einen Dateistream von der [**iasyncoperation**](/previous-versions//bb776309(v=vs.85)) -Schnittstelle, die zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="691ab-120">After the [**PickSingleFileAsync**](/uwp/api/windows.storage.pickers.fileopenpicker.picksinglefileasync) completes, you get a file stream from the [**IAsyncOperation**](/previous-versions//bb776309(v=vs.85)) interface it returns.</span></span>

### <a name="step-2-get-a-file-stream"></a><span data-ttu-id="691ab-121">Schritt 2: erhalten eines Datei Datenstroms</span><span class="sxs-lookup"><span data-stu-id="691ab-121">Step 2: Get a file stream</span></span>

<span data-ttu-id="691ab-122">Deklarieren Sie einen Vervollständigungs Handler, der ausgeführt wird, nachdem der asynchrone Vorgang für die Dateiauswahl</span><span class="sxs-lookup"><span data-stu-id="691ab-122">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="691ab-123">Verwenden Sie die [**GetResults**](/previous-versions//br205815(v=vs.85)) -Methode, um die Datei abzurufen und das Dateistream-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="691ab-123">Use the [**GetResults**](/previous-versions//br205815(v=vs.85)) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="691ab-124">Im nächsten Schritt konvertieren Sie das [**jeandomaccessstream**](/previous-versions//hh438400(v=vs.85)) -Objekt in ein [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) , das Sie an [WIC](/windows/desktop/wic/-wic-api)übergeben können.</span><span class="sxs-lookup"><span data-stu-id="691ab-124">In the next step you convert the [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) object to an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) that you can pass to [WIC](/windows/desktop/wic/-wic-api).</span></span>

### <a name="step-3-convert-the-file-stream"></a><span data-ttu-id="691ab-125">Schritt 3: Konvertieren des Datei Datenstroms</span><span class="sxs-lookup"><span data-stu-id="691ab-125">Step 3: Convert the file stream</span></span>

<span data-ttu-id="691ab-126">Verwenden Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) ", um den Dateistream zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="691ab-126">Use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function to convert the file stream.</span></span> <span data-ttu-id="691ab-127">Windows-Runtime-APIs stellen Streams mit " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85))" dar, während [WIC](/windows/desktop/wic/-wic-api) [**IStream verwendet**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="691ab-127">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while [WIC](/windows/desktop/wic/-wic-api) consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


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
> <span data-ttu-id="691ab-128">Wenn Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) " verwenden möchten, sollten Sie " *shcore. h* " in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="691ab-128">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include *shcore.h* in your project.</span></span>

 

### <a name="step-4-create-a-wic-decoder-and-get-the-frame"></a><span data-ttu-id="691ab-129">Schritt 4: Erstellen eines WIC-Decoders und des Abbilds</span><span class="sxs-lookup"><span data-stu-id="691ab-129">Step 4: Create a WIC decoder and get the frame</span></span>

<span data-ttu-id="691ab-130">Erstellen Sie ein [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) -Objekt mithilfe der [**IWICImagingFactory:: | atedecoderfromstream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) -Methode.</span><span class="sxs-lookup"><span data-stu-id="691ab-130">Create an [**IWICBitmapDecoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapdecoder) object using the [**IWICImagingFactory::CreateDecoderFromStream**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream) method.</span></span>


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



<span data-ttu-id="691ab-131">Verwenden Sie die [**IWICBitmapDecoder:: GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) -Methode, um den ersten Frame des Bilds vom Decoder zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="691ab-131">Get the first frame of the image from the decoder using the [**IWICBitmapDecoder::GetFrame**](/windows/desktop/api/wincodec/nf-wincodec-iwicbitmapdecoder-getframecount) method.</span></span>


```C++
    ComPtr<IWICBitmapFrameDecode> frame;
    DX::ThrowIfFailed(
        decoder->GetFrame(0, &frame)
        );
```



### <a name="step-5-create-a-wic-converter-and-initialize"></a><span data-ttu-id="691ab-132">Schritt 5: Erstellen eines WIC-Konverters und initialisieren</span><span class="sxs-lookup"><span data-stu-id="691ab-132">Step 5: Create a WIC converter and initialize</span></span>

<span data-ttu-id="691ab-133">Konvertieren Sie das Bild mit [WIC](/windows/desktop/wic/-wic-api)in das BGRA-Farb Format.</span><span class="sxs-lookup"><span data-stu-id="691ab-133">Convert the image to the BGRA color format using [WIC](/windows/desktop/wic/-wic-api).</span></span> <span data-ttu-id="691ab-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) gibt das systemeigene Pixel Format des Bilds zurück, z. b. jpeer-Daten werden in GUID- \_ WICPixelFormat24bppBGR gespeichert.</span><span class="sxs-lookup"><span data-stu-id="691ab-134">[IWICBitmapFrameDecode](/windows/desktop/wic/-wic-imp-iwicbitmapframedecode) will return the native pixel format of the image, like JPEGs are stored in GUID\_WICPixelFormat24bppBGR.</span></span> <span data-ttu-id="691ab-135">Als Leistungsoptimierung mit Direct2D wird jedoch empfohlen, dass Sie in WICPixelFormat32bppPBGRA konvertieren.</span><span class="sxs-lookup"><span data-stu-id="691ab-135">However, as a performance optimization with Direct2D we recommend that you convert to WICPixelFormat32bppPBGRA.</span></span>

1.  <span data-ttu-id="691ab-136">Erstellen Sie ein [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) -Objekt mithilfe der [**IWICImagingFactory:: deateformatconverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) -Methode.</span><span class="sxs-lookup"><span data-stu-id="691ab-136">Create a [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) object using the [**IWICImagingFactory::CreateFormatConverter**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory-createformatconverter) method.</span></span>

    ```C++
        ComPtr<IWICFormatConverter> converter;
        DX::ThrowIfFailed(
            m_wicFactory->CreateFormatConverter(&converter)
            ); 
     
    ```

    

2.  <span data-ttu-id="691ab-137">Initialisieren Sie den Format Konverter, um das WICPixelFormat32bppPBGRA zu verwenden, und übergeben Sie den BitmapFrame.</span><span class="sxs-lookup"><span data-stu-id="691ab-137">Initialize the format converter to use the WICPixelFormat32bppPBGRA and pass in the bitmap frame.</span></span>

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

    

<span data-ttu-id="691ab-138">Die [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) -Schnittstelle wird von der [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) -Schnittstelle abgeleitet, sodass Sie den Konverter an den [bitmapquelleffekt](bitmap-source.md) übergeben können.</span><span class="sxs-lookup"><span data-stu-id="691ab-138">The [**IWICFormatConverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter) interface is derived from the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) interface, so you can pass the converter to the [bitmap source](bitmap-source.md) effect.</span></span>

### <a name="step-6-create-effect-and-pass-in-an-iwicbitmapsource"></a><span data-ttu-id="691ab-139">Schritt 6: Erstellen eines Effekts und übergeben in eine IWICBitmapSource</span><span class="sxs-lookup"><span data-stu-id="691ab-139">Step 6: Create effect and pass in an IWICBitmapSource</span></span>

<span data-ttu-id="691ab-140">Verwenden Sie die Methode " [**kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) ", um mit dem [Direct2D](getting-started-with-direct2d.md) [**-Gerätekontext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)ein [Bitmap-Quell](bitmap-source.md) - [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekt zu erstellen</span><span class="sxs-lookup"><span data-stu-id="691ab-140">Use the [**CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method to create a [bitmap source](bitmap-source.md) [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object using the [Direct2D](getting-started-with-direct2d.md) [**device context**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext).</span></span>

<span data-ttu-id="691ab-141">Verwenden Sie die [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode, um die *\_ \_ \_ \_ BitmapSource \_ -Eigenschaft der D2D1 BitmapSource* -Eigenschaft auf den [WIC](/windows/desktop/wic/-wic-api) - [**Format Konverter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter)festzulegen.</span><span class="sxs-lookup"><span data-stu-id="691ab-141">Use the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method to set the *D2D1\_BITMAPSOURCE\_PROP\_WIC\_BITMAP\_SOURCE* property to the [WIC](/windows/desktop/wic/-wic-api) [**format converter**](/windows/desktop/api/wincodec/nn-wincodec-iwicformatconverter).</span></span>

> [!Note]  
> <span data-ttu-id="691ab-142">Der [Bitmap-Quell](bitmap-source.md) Effekt nimmt keine Eingabe der [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) -Methode auf, wie viele [Direct2D Effekte](effects-overview.md).</span><span class="sxs-lookup"><span data-stu-id="691ab-142">The [bitmap source](bitmap-source.md) effect doesn't take an input from the [**SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method like many [Direct2D effects](effects-overview.md).</span></span> <span data-ttu-id="691ab-143">Stattdessen wird das [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) -Objekt als Eigenschaft angegeben.</span><span class="sxs-lookup"><span data-stu-id="691ab-143">Instead, the [**IWICBitmapSource**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapsource) object is specified as a property.</span></span>

 


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



<span data-ttu-id="691ab-144">Nun, da Sie den [Bitmap-Quell](bitmap-source.md) Effekt haben, können Sie ihn als Eingabe für beliebige [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) verwenden und ein Effekt Diagramm erstellen.</span><span class="sxs-lookup"><span data-stu-id="691ab-144">Now that you have the [bitmap source](bitmap-source.md) effect, you can use it as input to any [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) and create an effect graph.</span></span>

## <a name="complete-example"></a><span data-ttu-id="691ab-145">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="691ab-145">Complete example</span></span>

<span data-ttu-id="691ab-146">Im folgenden finden Sie den vollständigen Code für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="691ab-146">Here is the full code for this example.</span></span>


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



 

 