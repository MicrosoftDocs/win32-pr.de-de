---
description: Im folgenden Beispiel wird veranschaulicht, wie ein Bild und dessen Metadaten in eine neue Datei im gleichen Format neu codiert werden.
ms.assetid: a7cfaa6d-e17d-458a-ae63-72963615bef8
title: Erneutes Codieren eines JPEG-Bilds mit Metadaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13851af04c6af742dbc68acc31fd674c3602ebeb16bec6903a3570f8cb1e0400
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119088162"
---
# <a name="how-to-re-encode-a-jpeg-image-with-metadata"></a>Erneutes Codieren eines JPEG-Bilds mit Metadaten

Im folgenden Beispiel wird veranschaulicht, wie ein Bild und dessen Metadaten in eine neue Datei im gleichen Format neu codiert werden. Darüber hinaus werden in diesem Beispiel Metadaten hinzugefügt, um einen ausdruck mit einem einzelnen Element zu veranschaulichen, der von einem Abfragewriter verwendet wird.

Dieses Thema enthält folgende Abschnitte:

-   [Voraussetzungen](#prerequisites)
-   [Teil 1: Decodieren eines Bilds](#part-1-decode-an-image)
-   [Teil 2: Erstellen und Initialisieren des Imageencoders](#part-2-create-and-initialize-the-image-encoder)
-   [Teil 3: Kopieren von decodierten Frameinformationen](#part-3-copy-decoded-frame-information)
-   [Teil 4: Kopieren der Metadaten](#part-4-copy-the-metadata)
-   [Teil 5: Hinzufügen zusätzlicher Metadaten](#part-5-add-additional-metadata)
-   [Teil 6: Finalisieren des codierten Bilds](#part-6-finalize-the-encoded-image)
-   [Beispielcode für die neu codierte JPEG-Datei](#jpeg-re-encode-example-code)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Um dieses Thema zu verstehen, sollten Sie mit dem WIC-Metadatensystem (Windows Imaging Component) vertraut sein, wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)beschrieben. Sie sollten auch mit den WIC-Codeckomponenten vertraut sein, wie in der [Übersicht über Windows Imaging Component](-wic-about-windows-imaging-codec.md)beschrieben.

## <a name="part-1-decode-an-image"></a>Teil 1: Decodieren eines Bilds

Bevor Sie Bilddaten oder Metadaten in eine neue Bilddatei kopieren können, müssen Sie zunächst einen Decoder für das vorhandene Bild erstellen, das Sie neu codieren möchten. Der folgende Code veranschaulicht das Erstellen eines WIC-Decoders für die Imagedatei test.jpg.


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



Beim Aufruf von **CreateDecoderFromFilename** wurde der Wert WICDecodeMetadataCacheOnDemand aus der [**WICDecodeOptions-Enumeration**](/windows/desktop/api/Wincodec/ne-wincodec-wicdecodeoptions) als vierter Parameter verwendet. Dadurch wird der Decoder angewiesen, die Metadaten zwischenzuspeichern, wenn die Metadaten benötigt werden, indem entweder ein Abfrageleser oder der zugrunde liegende Metadatenreader verwendet wird. Mit dieser Option können Sie den Datenstrom in den Metadaten beibehalten, was für die schnelle Metadatencodierung erforderlich ist und die verlustfreie Decodierung und Codierung von JPEG-Bildern ermöglicht. Alternativ können Sie den anderen **WICDecodeOptions-Wert** WICDecodeMetadataCacheOnLoad verwenden, der die eingebetteten Bildmetadaten zwischenspeichert, sobald das Image geladen wird.

## <a name="part-2-create-and-initialize-the-image-encoder"></a>Teil 2: Erstellen und Initialisieren des Imageencoders

Der folgende Code veranschaulicht die Erstellung des Encoders, den Sie zum Codieren des zuvor decodierten Bilds verwenden.


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



Ein WIC-Dateistream piFileStream wird zum Schreiben in die Imagedatei "test2.jpg" erstellt und initialisiert. piFileStream wird dann verwendet, um den Encoder zu initialisieren und den Encoder darüber zu informieren, wo die Bildbits geschrieben werden sollen, wenn die Codierung abgeschlossen ist.

## <a name="part-3-copy-decoded-frame-information"></a>Teil 3: Kopieren von decodierten Frameinformationen

Der folgende Code kopiert jeden Frame eines Bilds in einen neuen Frame des Encoders. Diese Kopie enthält Größe, Auflösung und Pixelformat. alle sind erforderlich, um einen gültigen Frame zu erstellen.

> [!Note]  
> JPEG-Bilder verfügen nur über einen Frame, und die folgende Schleife ist technisch nicht erforderlich, ist jedoch enthalten, um die Verwendung mehrerer Frames für Formate zu veranschaulichen, die sie unterstützen.

 


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



Der folgende Code führt eine schnelle Überprüfung durch, um zu ermitteln, ob die Quell- und Zielbildformate identisch sind. Dies ist erforderlich, da Teil 4 einen Vorgang anzeigt, der nur unterstützt wird, wenn das Quell- und das Zielformat identisch sind.


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
> Der Code in diesem Abschnitt ist nur gültig, wenn die Quell- und Zielbildformate identisch sind. Sie können nicht alle Metadaten eines Bilds in einem einzigen Vorgang kopieren, wenn sie in ein anderes Bildformat codieren.

 

Zum Beibehalten von Metadaten während der erneuten Codierung eines Bilds in dasselbe Bildformat stehen Methoden zum Kopieren aller Metadaten in einem einzigen Vorgang zur Verfügung. Jeder dieser Vorgänge folgt einem ähnlichen Muster. legt die Metadaten des decodierten Frames direkt in den neuen Frame fest, der codiert wird. Beachten Sie, dass dies für jeden einzelnen Bildrahmen erfolgt.

Die bevorzugte Methode zum Kopieren von Metadaten besteht darin, den Blockwriter des neuen Frames mit dem Blockreader des decodierten Frames zu initialisieren. Der folgende Code veranschaulicht diese Methode.


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



In diesem Beispiel rufen Sie einfach den Blockreader und den Blockwriter aus dem Quellframe bzw. Zielframe ab. Der Blockwriter wird dann vom Blockreader initialisiert. Dadurch wird der Blockwriter mit den vorab aufgefüllten Metadaten des Blockreaders initialisiert. Weitere Methoden zum Kopieren von Metadaten finden Sie im Abschnitt Schreiben von Metadaten in [der Übersicht über das Lesen und Schreiben von Bildmetadaten.](-wic-codec-readingwritingmetadata.md)

Auch hier funktioniert dieser Vorgang nur, wenn die Quell- und Zielimages das gleiche Format aufweisen. Dies liegt daran, dass die Metadatenblöcke von verschiedenen Bildformaten an unterschiedlichen Speicherorten gespeichert werden. Jpeg und Tagged Image File Format (TIFF) unterstützen beispielsweise XMP-Metadatenblöcke (Extensible Metadata Platform). In JPEG-Bildern befindet sich der XMP-Block im Stammmetadatenblock, wie in der [Übersicht über WIC-Metadaten](-wic-about-metadata.md)veranschaulicht. In einem TIFF-Image ist der XMP-Block jedoch in den IFD-Stammblock eingebettet.

## <a name="part-5-add-additional-metadata"></a>Teil 5: Hinzufügen zusätzlicher Metadaten

Im folgenden Beispiel wird veranschaulicht, wie Dem Zielimage Metadaten hinzugefügt werden. Dazu wird die **SetMetadataByName-Methode** des Abfragewriters mithilfe eines Abfrageausdrucks und der in einem [PROPVARIANT](/windows/win32/api/propidlbase/ns-propidlbase-propvariant)gespeicherten Daten aufgerufen.


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



Weitere Informationen zum Abfrageausdruck finden Sie in der Übersicht über die [Metadatenabfragesprache.](-wic-codec-metadataquerylanguage.md)

## <a name="part-6-finalize-the-encoded-image"></a>Teil 6: Finalisieren des codierten Bilds

Die letzten Schritte zum Kopieren des Bilds sind das Schreiben der Pixeldaten für den Frame, das Committen des Frames an den Encoder und das Committen des Encoders. Durch committen des Encoders wird der Bilddatenstrom in die Datei geschrieben.


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



Die **WriteSource-Methode** des Frames wird verwendet, um die Pixeldaten für das Bild zu schreiben. Beachten Sie, dass dies erfolgt, nachdem die Metadaten geschrieben wurden. Dies ist erforderlich, um sicherzustellen, dass die Metadaten in der Bilddatei über genügend Speicherplatz verfügt. Nachdem die Pixeldaten geschrieben wurden, wird der Frame mithilfe der **Commit-Methode** des Frames in den Stream geschrieben. Nachdem alle Frames verarbeitet wurden, wird der Encoder (und somit das Bild) mithilfe der **Commit-Methode** des Encoders abgeschlossen.

Nachdem Sie den Frame committen, müssen Sie die in der Schleife erstellten COM-Objekte freigeben.

## <a name="jpeg-re-encode-example-code"></a>Beispielcode für die neu codierte JPEG-Datei

Im Folgenden ist der Code aus den Teilen 1 bis 6 in einem konvektiven Block.


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

**Konzeptionellen**
</dt> <dt>

[Übersicht über WIC-Metadaten](-wic-about-metadata.md)
</dt> <dt>

[Übersicht über die Metadatenabfragesprache](-wic-codec-metadataquerylanguage.md)
</dt> <dt>

[Übersicht über das Lesen und Schreiben von Bildmetadaten](-wic-codec-readingwritingmetadata.md)
</dt> <dt>

[Übersicht über die Metadatenerweiterbarkeit](-wic-codec-metadatahandlers.md)
</dt> </dl>

 

 
