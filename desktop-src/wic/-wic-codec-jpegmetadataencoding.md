---
description: Im folgenden Beispiel wird veranschaulicht, wie ein Bild und seine Metadaten erneut in eine neue Datei mit demselben Format codiert werden.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: 'Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c023defb760faeab2bc6ea92232fcc916ef15126
ms.sourcegitcommit: af120ad5c30da2fc5eb717ca2a1c4c45878efd71
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/20/2021
ms.locfileid: "106365146"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Gewusst wie: Erneutes Codieren eines JPEG-Bilds mit Metadaten

Im folgenden Beispiel wird veranschaulicht, wie ein Bild und seine Metadaten erneut in eine neue Datei mit demselben Format codiert werden. Außerdem werden in diesem Beispiel Metadaten hinzugefügt, um einen einzelnen Element Ausdruck zu veranschaulichen, der von einem Abfrage-Writer verwendet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Teil 1: Decodieren eines Bilds](#part-1-decode-an-image)
-   [Teil 2: Erstellen und Initialisieren des Image Encoders](#part-2-create-and-initialize-the-image-encoder)
-   [Teil 3: Kopieren von decodierten Frame Informationen](#part-3-copy-decoded-frame-information)
-   [Teil 4: Kopieren der Metadaten](#part-4-copy-the-metadata)
-   [Teil 5: Hinzufügen zusätzlicher Metadaten](#part-5-add-additional-metadata)
-   [Teil 6: Finalisieren des codierten Bilds](#part-6-finalize-the-encoded-image)
-   [JPEG Umcodieren von Beispiel Code](#jpeg-re-encode-example-code)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie sich mit dem Metadatensystem der Windows Imaging Component (WIC) vertraut machen, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)beschrieben. Sie sollten auch mit den WIC-Codec-Komponenten vertraut sein, wie in der [Übersicht über Windows Imaging](-wic-about-windows-imaging-codec.md)-Komponenten beschrieben.

## <a name="part-1-decode-an-image"></a>Teil 1: Decodieren eines Bilds

Bevor Sie Bilddaten oder Metadaten in eine neue Bilddatei kopieren können, müssen Sie zuerst einen Decoder für das vorhandene Abbild erstellen, das Sie erneut codieren möchten. Der folgende Code veranschaulicht, wie ein WIC-Decoder für die Bilddatei test.jpg erstellt wird.


```C++
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }
```



Beim Aufrufen von " **anatedecoderfromfilename** " wurde der Wert WICDecodeMetadataCacheOnDemand aus der [**wicdecodeoptions**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) -Enumeration als vierter Parameter verwendet. Dadurch wird der Decoder aufgefordert, die Metadaten zwischenzuspeichern, wenn die Metadaten benötigt werden, entweder durch Abrufen eines Abfrage Readers oder durch Verwendung des zugrunde liegenden metadatenreaders. Wenn Sie diese Option verwenden, können Sie den Datenstrom in den Metadaten beibehalten. Dies ist für die schnelle metadatencodierung erforderlich und ermöglicht die Verlust lose Decodierung und Codierung von JPEG-Bildern. Alternativ können Sie auch den anderen **wicdecodeoptions** -Wert, WICDecodeMetadataCacheOnLoad, verwenden, der die eingebetteten Bild Metadaten zwischenspeichert, sobald das Bild geladen wird.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Teil 2: Erstellen und Initialisieren des Image Encoders

Der folgende Code veranschaulicht die Erstellung des Encoders, den Sie verwenden, um das Image zu codieren, das Sie zuvor decodiert haben.


```C++
    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }
```



Ein WIC-Datei Datenstrom: pifilestream wird erstellt und zum Schreiben in die Bilddatei "test2.jpg" initialisiert. pifilestream wird dann verwendet, um den Encoder zu initialisieren und den Encoder darüber zu informieren, wo die Abbild Bits geschrieben werden sollen, wenn die Codierung beendet ist.

## <a name="part-3-copy-decoded-frame-information"></a>Teil 3: Kopieren von decodierten Frame Informationen

Der folgende Code kopiert jeden Frame eines Bilds in einen neuen Frame des Encoders. Diese Kopie umfasst Größe, Auflösung und Pixel Format. Alle sind erforderlich, um einen gültigen Frame zu erstellen.

> [!Note]  
> JPEG-Bilder verfügen nur über einen Frame, und die nachfolgende Schleife ist technisch nicht erforderlich, ist jedoch enthalten, um die Multi-Frame-Verwendung für Formate zu veranschaulichen, die diese unterstützen.

 


```C++
    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }
```



Der folgende Code führt eine schnelle Überprüfung durch, um zu bestimmen, ob die Quell-und Ziel Bildformate identisch sind. Dies ist erforderlich, da Teil 4 einen Vorgang anzeigt, der nur unterstützt wird, wenn das Quell-und Zielformat identisch sind.


```C++
            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }
```



## <a name="part-4-copy-the-metadata"></a>Teil 4: Kopieren der Metadaten

> [!Note]  
> Der Code in diesem Abschnitt ist nur gültig, wenn die Quell-und Ziel Image Formate identisch sind. Wenn Sie in ein anderes Bildformat codieren, können Sie nicht alle Metadaten eines Bilds in einem einzelnen Vorgang kopieren.

 

Zum Beibehalten von Metadaten beim erneuten Codieren eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzelnen Vorgang zur Verfügung. Jeder dieser Vorgänge folgt einem ähnlichen Muster: jede legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird. Beachten Sie, dass dies für jeden einzelnen Bild Rahmen erfolgt.

Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den blockwriter des neuen Frames mit dem Block Reader des decodierten Frames zu initialisieren. Der folgende Code veranschaulicht diese Methode.


```C++
            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }
```



In diesem Beispiel rufen Sie einfach den Block Reader und den blockwriter aus dem Quellframe bzw. dem Zielframe ab. Der blockwriter wird dann vom Block Reader initialisiert. Dadurch wird der blockwriter mit den vorab aufgefüllten Metadaten des Block Readers initialisiert. Weitere Methoden zum Kopieren von Metadaten finden Sie im Abschnitt Schreiben von Metadaten in der [Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md).

Auch dieser Vorgang funktioniert nur, wenn die Quell-und Ziel Images das gleiche Format aufweisen. Dies liegt daran, dass unterschiedliche Bildformate die Metadatenblöcke an verschiedenen Speicherorten speichern. Beispielsweise unterstützen sowohl JPEG als auch Tagged Image File Format (TIFF) Extensible Metadata Platform (XMP)-Metadatenblöcke. In JPEG-Bildern befindet sich der XMP-Block im stammmetadatenblock, wie in der [WIC-Metadatenübersicht](-wic-about-metadata.md)veranschaulicht. In einem TIFF-Bild wird der XMP-Block jedoch in den IFD-Stammblock eingebettet.

## <a name="part-5-add-additional-metadata"></a>Teil 5: Hinzufügen zusätzlicher Metadaten

Im folgenden Beispiel wird veranschaulicht, wie dem Zielbild Metadaten hinzugefügt werden. Dies erfolgt durch Aufrufen der **SetMetadataByName** -Methode des Abfrage Writers mithilfe eines Abfrage Ausdrucks und der in einem [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)gespeicherten Daten.


```C++
            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
```



Weitere Informationen zum Abfrage Ausdruck finden Sie in der [Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md).

## <a name="part-6-finalize-the-encoded-image"></a>Teil 6: Finalisieren des codierten Bilds

Die abschließenden Schritte zum Kopieren des Bilds sind das Schreiben der Pixeldaten für den Frame, das Ausführen eines Commit für den Frame an den Encoder und das Ausführen eines Commit für den Encoder. Durch das committen des Encoders wird der Bildstream in die Datei geschrieben.


```C++
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
```



Die "Write **tesource** "-Methode des Frames dient zum Schreiben der Pixeldaten für das Bild. Beachten Sie, dass dies geschieht, nachdem die Metadaten geschrieben wurden. Dies ist erforderlich, um sicherzustellen, dass die Metadaten über ausreichend Speicherplatz innerhalb der Bilddatei verfügen. Nachdem die Pixeldaten geschrieben wurden, wird der Frame mithilfe der **Commit** -Methode von Frame in den Stream geschrieben. Nachdem alle Frames verarbeitet wurden, wird der Encoder (und damit das Bild) mithilfe der **Commit** -Methode des Encoders fertiggestellt.

Nachdem Sie einen Commit für den Frame durchgeführt haben, müssen Sie die in der-Schleife erstellten COM-Objekte freigeben.

## <a name="jpeg-re-encode-example-code"></a>JPEG Umcodieren von Beispiel Code

Im folgenden finden Sie den Code von den Teilen 1 bis 6 in einem convienient-Block.


```C++
#include <Windows.h>
#include <Wincodecsdk.h>

int main()
{
    // Initialize COM.
    HRESULT hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    IWICImagingFactory *piFactory = NULL;
    IWICBitmapDecoder *piDecoder = NULL;

    // Create the COM imaging factory.
    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(CLSID_WICImagingFactory,
        NULL, CLSCTX_INPROC_SERVER,
        IID_PPV_ARGS(&piFactory));
    }

    // Create the decoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateDecoderFromFilename(L"test.jpg", NULL, GENERIC_READ,
            WICDecodeMetadataCacheOnDemand, //For JPEG lossless decoding/encoding.
            &piDecoder);
    }

    // Variables used for encoding.
    IWICStream *piFileStream = NULL;
    IWICBitmapEncoder *piEncoder = NULL;
    IWICMetadataBlockWriter *piBlockWriter = NULL;
    IWICMetadataBlockReader *piBlockReader = NULL;

    WICPixelFormatGUID pixelFormat = { 0 };
    UINT count = 0;
    double dpiX, dpiY = 0.0;
    UINT width, height = 0;

    // Create a file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateStream(&piFileStream);
    }

    // Initialize our new file stream.
    if (SUCCEEDED(hr))
    {
        hr = piFileStream->InitializeFromFilename(L"test2.jpg", GENERIC_WRITE);
    }

    // Create the encoder.
    if (SUCCEEDED(hr))
    {
        hr = piFactory->CreateEncoder(GUID_ContainerFormatJpeg, NULL, &piEncoder);
    }
    // Initialize the encoder
    if (SUCCEEDED(hr))
    {
        hr = piEncoder->Initialize(piFileStream,WICBitmapEncoderNoCache);
    }

    if (SUCCEEDED(hr))
    {
        hr = piDecoder->GetFrameCount(&count);
    }

    if (SUCCEEDED(hr))
    {
        // Process each frame of the image.
        for (UINT i=0; i<count && SUCCEEDED(hr); i++)
        {
            // Frame variables.
            IWICBitmapFrameDecode *piFrameDecode = NULL;
            IWICBitmapFrameEncode *piFrameEncode = NULL;
            IWICMetadataQueryReader *piFrameQReader = NULL;
            IWICMetadataQueryWriter *piFrameQWriter = NULL;

            // Get and create the image frame.
            if (SUCCEEDED(hr))
            {
                hr = piDecoder->GetFrame(i, &piFrameDecode);
            }
            if (SUCCEEDED(hr))
            {
                hr = piEncoder->CreateNewFrame(&piFrameEncode, NULL);
            }

            // Initialize the encoder.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Initialize(NULL);
            }
            // Get and set the size.
            if (SUCCEEDED(hr))
            {
                hr = piFrameDecode->GetSize(&width, &height);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetSize(width, height);
            }
            // Get and set the resolution.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetResolution(&dpiX, &dpiY);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetResolution(dpiX, dpiY);
            }
            // Set the pixel format.
            if (SUCCEEDED(hr))
            {
                piFrameDecode->GetPixelFormat(&pixelFormat);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->SetPixelFormat(&pixelFormat);
            }

            // Check that the destination format and source formats are the same.
            bool formatsEqual = FALSE;
            if (SUCCEEDED(hr))
            {
                GUID srcFormat;
                GUID destFormat;

                hr = piDecoder->GetContainerFormat(&srcFormat);
                if (SUCCEEDED(hr))
                {
                    hr = piEncoder->GetContainerFormat(&destFormat);
                }
                if (SUCCEEDED(hr))
                {
                    if (srcFormat == destFormat)
                        formatsEqual = true;
                    else
                        formatsEqual = false;
                }
            }

            if (SUCCEEDED(hr) && formatsEqual)
            {
                // Copy metadata using metadata block reader/writer.
                if (SUCCEEDED(hr))
                {
                    piFrameDecode->QueryInterface(IID_PPV_ARGS(&piBlockReader));
                }
                if (SUCCEEDED(hr))
                {
                    piFrameEncode->QueryInterface(IID_PPV_ARGS(&piBlockWriter));
                }
                if (SUCCEEDED(hr))
                {
                    piBlockWriter->InitializeFromBlockReader(piBlockReader);
                }
            }

            if(SUCCEEDED(hr))
            {
                hr = piFrameEncode->GetMetadataQueryWriter(&piFrameQWriter);
            }
            if (SUCCEEDED(hr))
            {
                // Add additional metadata.
                PROPVARIANT    value;
                value.vt = VT_LPWSTR;
                value.pwszVal= L"Metadata Test Image.";
                hr = piFrameQWriter->SetMetadataByName(L"/xmp/dc:title", &value);
            }
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->WriteSource(
                    static_cast<IWICBitmapSource*> (piFrameDecode),
                    NULL); // Using NULL enables JPEG loss-less encoding.
            }

            // Commit the frame.
            if (SUCCEEDED(hr))
            {
                hr = piFrameEncode->Commit();
            }

            if (piFrameDecode)
            {
                piFrameDecode->Release();
            }

            if (piFrameEncode)
            {
                piFrameEncode->Release();
            }

            if (piFrameQReader)
            {
                piFrameQReader->Release();
            }

            if (piFrameQWriter)
            {
                piFrameQWriter->Release();
            }
        }
    }

    if (SUCCEEDED(hr))
    {
        piEncoder->Commit();
    }

    if (SUCCEEDED(hr))
    {
        piFileStream->Commit(STGC_DEFAULT);
    }

    if (piFileStream)
    {
        piFileStream->Release();
    }
    if (piEncoder)
    {
        piEncoder->Release();
    }
    if (piBlockWriter)
    {
        piBlockWriter->Release();
    }
    if (piBlockReader)
    {
        piBlockReader->Release();
    }
    return 0;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadaten-Abfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bild Metadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
