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
# <a name="how-to-save-direct2d-content-to-an-image-file"></a><span data-ttu-id="ea813-103">Speichern von Direct2D-Inhalten in einer Bilddatei</span><span class="sxs-lookup"><span data-stu-id="ea813-103">How to save Direct2D content to an image file</span></span>

<span data-ttu-id="ea813-104">In diesem Thema wird gezeigt, wie [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) verwendet wird, um Inhalt in Form einer [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei (z. b. JPEG) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea813-104">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span> <span data-ttu-id="ea813-105">Wenn Sie eine Windows Store-App schreiben, können Sie den Benutzer mithilfe von [**Windows:: Storage::P icker:: filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)eine Zieldatei auswählen lassen.</span><span class="sxs-lookup"><span data-stu-id="ea813-105">If you are writing a Windows Store app, you can have the user select a destination file using [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker).</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="ea813-106">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="ea813-106">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="ea813-107">Technologien</span><span class="sxs-lookup"><span data-stu-id="ea813-107">Technologies</span></span>

-   [<span data-ttu-id="ea813-108">Direct2D</span><span class="sxs-lookup"><span data-stu-id="ea813-108">Direct2D</span></span>](./direct2d-portal.md)
-   [<span data-ttu-id="ea813-109">Direct2D Effekte</span><span class="sxs-lookup"><span data-stu-id="ea813-109">Direct2D effects</span></span>](effects-overview.md)
-   [<span data-ttu-id="ea813-110">**Windows:: Storage::P icker:: filesavepicker**</span><span class="sxs-lookup"><span data-stu-id="ea813-110">**Windows::Storage::Pickers::FileSavePicker**</span></span>](/uwp/api/Windows.Storage.Pickers.FileSavePicker)

### <a name="prerequisites"></a><span data-ttu-id="ea813-111">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="ea813-111">Prerequisites</span></span>

-   <span data-ttu-id="ea813-112">Sie benötigen ein [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Objekt und ein Objekt, das [Direct2D](./direct2d-portal.md) -Inhalt enthält, der [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) wie z. b. [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) oder [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1)implementiert.</span><span class="sxs-lookup"><span data-stu-id="ea813-112">You need an [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) object and an object containing [Direct2D](./direct2d-portal.md) content that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) such as [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) or [**ID2D1Bitmap1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1bitmap1).</span></span>

## <a name="instructions"></a><span data-ttu-id="ea813-113">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="ea813-113">Instructions</span></span>

### <a name="step-1-get-a-destination-file-and-stream"></a><span data-ttu-id="ea813-114">Schritt 1: eine Zieldatei und einen Stream</span><span class="sxs-lookup"><span data-stu-id="ea813-114">Step 1: Get a destination file and stream</span></span>

<span data-ttu-id="ea813-115">Wenn Sie dem Benutzer die Auswahl einer Zieldatei gestatten möchten, können Sie [**filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker)verwenden, die zurückgegebene Datei öffnen und einen [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) für die Verwendung mit WIC Abrufen.</span><span class="sxs-lookup"><span data-stu-id="ea813-115">If you want to allow the user to select a destination file, you can use [**FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker), open the returned file, and obtain an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) to use with WIC.</span></span>

<span data-ttu-id="ea813-116">Erstellen Sie einen [**Windows:: Storage::P ickers:: filesavepicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) , und legen Sie dessen Parameter für Bilddateien fest.</span><span class="sxs-lookup"><span data-stu-id="ea813-116">Create a [**Windows::Storage::Pickers::FileSavePicker**](/uwp/api/Windows.Storage.Pickers.FileSavePicker) and set its parameters for image files.</span></span> <span data-ttu-id="ea813-117">Aufrufen der [**picksavefileasync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ea813-117">Call the [**PickSaveFileAsync**](/uwp/api/windows.storage.pickers.filesavepicker.picksavefileasync) method.</span></span>


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



<span data-ttu-id="ea813-118">Deklarieren Sie einen Vervollständigungs Handler, der ausgeführt wird, nachdem der asynchrone Vorgang für die Dateiauswahl</span><span class="sxs-lookup"><span data-stu-id="ea813-118">Declare a completion handler to run after the file picker async operation returns.</span></span> <span data-ttu-id="ea813-119">Verwenden Sie die [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) -Methode, um die Datei abzurufen und das Dateistream-Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="ea813-119">Use the [**GetResults**](/windows/desktop/WinRT/iasyncaction-getresults) method to retrieve the file and to get the file stream object.</span></span>


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



<span data-ttu-id="ea813-120">Rufen Sie einen " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85)) " ab, indem Sie [**openasync**](/uwp/api/windows.storage.storagefile.openasync) für die Datei aufrufen und das Ergebnis des asynchronen Vorgangs erhalten.</span><span class="sxs-lookup"><span data-stu-id="ea813-120">Obtain an [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)) by calling [**OpenAsync**](/uwp/api/windows.storage.storagefile.openasync) on the file and getting the result of the async operation.</span></span>


```C++
    task<Streams::IRandomAccessStream^> createStreamTask(file->OpenAsync(FileAccessMode::ReadWrite));
    createStreamTask.then([=](Streams::IRandomAccessStream^ randomAccessStream) {
```



<span data-ttu-id="ea813-121">Verwenden Sie abschließend die [**Methode "**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) Methode", um den Dateistream zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="ea813-121">Finally, use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) method to convert the file stream.</span></span> <span data-ttu-id="ea813-122">Windows-Runtime-APIs stellen Streams mit " [**unandomaccessstream**](/previous-versions//hh438400(v=vs.85))" dar, während WIC [**IStream verwendet**](/windows/desktop/api/objidl/nn-objidl-istream).</span><span class="sxs-lookup"><span data-stu-id="ea813-122">Windows Runtime APIs represent streams with [**IRandomAccessStream**](/previous-versions//hh438400(v=vs.85)), while WIC consumes [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream).</span></span>


```C++
    ComPtr<IStream> stream;
    DX::ThrowIfFailed(
        CreateStreamOverRandomAccessStream(randomAccessStream, IID_PPV_ARGS(&stream))
        );
```



> [!Note]  
> <span data-ttu-id="ea813-123">Wenn Sie die Funktion " [**kreatestreamoverrandomaccessstream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) " verwenden möchten, sollten Sie " **shcore. h** " in Ihr Projekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="ea813-123">To use the [**CreateStreamOverRandomAccessStream**](/windows/desktop/api/shcore/nf-shcore-createstreamoverrandomaccessstream) function, you should include **shcore.h** in your project.</span></span>

 

### <a name="step-2-get-the-wic-bitmap-and-frame-encoder"></a><span data-ttu-id="ea813-124">Schritt 2: erhalten der WIC-Bitmap und des Frame Encoders</span><span class="sxs-lookup"><span data-stu-id="ea813-124">Step 2: Get the WIC bitmap and frame encoder</span></span>

<span data-ttu-id="ea813-125">[Iwicbitmapcoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) stellen die Funktionalität bereit, um Abbild Erstellungs Daten in einem codierten Dateiformat zu speichern.</span><span class="sxs-lookup"><span data-stu-id="ea813-125">[IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) provide the functionality to save imaging data to an encoded file format.</span></span>

<span data-ttu-id="ea813-126">Erstellen und initialisieren Sie die Encoderobjekte.</span><span class="sxs-lookup"><span data-stu-id="ea813-126">Create and initialize the encoder objects.</span></span>


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



### <a name="step-3-get-an-iwicimageencoder"></a><span data-ttu-id="ea813-127">Schritt 3: Holen Sie sich einen iwicimageencoder</span><span class="sxs-lookup"><span data-stu-id="ea813-127">Step 3: Get an IWICImageEncoder</span></span>

<span data-ttu-id="ea813-128">[**Iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) ist eine neue Schnittstelle in Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ea813-128">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) is a new interface in Windows 8.</span></span> <span data-ttu-id="ea813-129">Sie kann über [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2)erstellt werden, das **IWICImagingFactory** erweitert und auch für Windows 8 neu ist.</span><span class="sxs-lookup"><span data-stu-id="ea813-129">It can be created from [**IWICImagingFactory2**](/windows/desktop/api/wincodec/nn-wincodec-iwicimagingfactory2), which extends **IWICImagingFactory** and is also new for Windows 8.</span></span>


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



<span data-ttu-id="ea813-130">Aufrufen von [**IWICImagingFactory2:: kreateimageencoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span><span class="sxs-lookup"><span data-stu-id="ea813-130">Call [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span> <span data-ttu-id="ea813-131">Der erste Parameter ist ein [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) und muss das Gerät sein, auf dem das zu codierende Image erstellt wurde – Sie können Bilder aus verschiedenen Ressourcen Domänen innerhalb eines einzelnen [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder)nicht mischen.</span><span class="sxs-lookup"><span data-stu-id="ea813-131">The first parameter is an [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) and must be the device on which the image you want to encode was created – you cannot mix images from different resource domains within a single [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder).</span></span>


```C++
    ComPtr<IWICImageEncoder> imageEncoder;
    DX::ThrowIfFailed(
        wicFactory2->CreateImageEncoder(
            d2dDevice.Get(),
            &imageEncoder
            )
       );
```



### <a name="step-4-write-the-direct2d-content-using-iwicimageencoder"></a><span data-ttu-id="ea813-132">Schritt 4: Schreiben des Direct2D-Inhalts mit iwicimageencoder</span><span class="sxs-lookup"><span data-stu-id="ea813-132">Step 4: Write the Direct2D content using IWICImageEncoder</span></span>

<span data-ttu-id="ea813-133">[**Iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) kann ein [Direct2D](./direct2d-portal.md) -Bild in einen Bildframe, eine Frame-Miniaturansicht oder die Miniaturansicht des Containers schreiben.</span><span class="sxs-lookup"><span data-stu-id="ea813-133">[**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) can write a [Direct2D](./direct2d-portal.md) image into an image frame, a frame thumbnail, or the container thumbnail.</span></span> <span data-ttu-id="ea813-134">Anschließend können Sie [iwicbitmakcoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) und [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) verwenden, um die Abbild Erstellungs Daten in einer Datei als normal zu codieren.</span><span class="sxs-lookup"><span data-stu-id="ea813-134">You can then use [IWICBitmapEncoder](/windows/desktop/wic/-wic-imp-iwicbitmapencoder) and [IWICBitmapFrameEncode](/windows/desktop/wic/-wic-imp-iwicbitmapframeencode) to encode the imaging data to a file as normal.</span></span>

<span data-ttu-id="ea813-135">Schreiben Sie das [Direct2D](./direct2d-portal.md) -Image in den Frame.</span><span class="sxs-lookup"><span data-stu-id="ea813-135">Write the [Direct2D](./direct2d-portal.md) image to the frame.</span></span> <span data-ttu-id="ea813-136">In diesem Code Ausschnitt schreiben wir eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) , die einen gerastertes Direct2D-Inhalt enthält.</span><span class="sxs-lookup"><span data-stu-id="ea813-136">In this snippet we write an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) that contains rasterized Direct2D content.</span></span> <span data-ttu-id="ea813-137">Allerdings können Sie jede beliebige Schnittstelle bereitstellen, die [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image)implementiert.</span><span class="sxs-lookup"><span data-stu-id="ea813-137">However, you can provide any interface that implements [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image).</span></span>


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
> <span data-ttu-id="ea813-138">Der [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Parameter muss für den [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) erstellt worden sein, der an [**IWICImagingFactory2:: | ateimageencoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder)übergeben wurde.</span><span class="sxs-lookup"><span data-stu-id="ea813-138">The [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) parameter must have been created on the [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device) that was passed into [**IWICImagingFactory2::CreateImageEncoder**](/windows/desktop/api/wincodec/nf-wincodec-iwicimagingfactory2-createimageencoder).</span></span>

 

<span data-ttu-id="ea813-139">Commit der WIC-und Stream-Ressourcen, um den Vorgang abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ea813-139">Commit the WIC and stream resources to finalize the operation.</span></span>


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
> <span data-ttu-id="ea813-140">Einige Implementierungen von [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) implementieren die [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) -Methode nicht und geben **E \_ notimpl** zurück.</span><span class="sxs-lookup"><span data-stu-id="ea813-140">Some implementations of [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) do not implement the [**Commit**](/windows/desktop/api/objidl/nf-objidl-istream-commit) method and return **E\_NOTIMPL**.</span></span>

 

<span data-ttu-id="ea813-141">Nun verfügen Sie über eine Datei mit dem [Direct2D](./direct2d-portal.md) -Image.</span><span class="sxs-lookup"><span data-stu-id="ea813-141">Now you have a file containing the [Direct2D](./direct2d-portal.md) image.</span></span>

## <a name="complete-example"></a><span data-ttu-id="ea813-142">Vollständiges Beispiel</span><span class="sxs-lookup"><span data-stu-id="ea813-142">Complete example</span></span>

<span data-ttu-id="ea813-143">Hier der vollständige Code für dieses Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ea813-143">Here the full code for this example.</span></span>

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



 

 