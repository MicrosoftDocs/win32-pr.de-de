---
description: Vorverarbeitungstransformationen für MPEG-Decoder
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: Vorverarbeitungstransformationen für MPEG-Decoder
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82d7bcf8eeda8062606ce0046a55e34d3c2d90fe
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908898"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>Vorverarbeitungstransformationen für MPEG-Decoder

**Letterbox und PanScan**

Das 4x3-Bild kann entweder durch Aufhängen des oberen und unteren Rands des Bilds (als Letterbox-Bild bezeichnet) oder durch Extrahieren eines 4x3-Teils des Bilds (als PanScan-Bild bezeichnet) gebildet werden. Die Menüs und Unterbildstreams werden über dem endgültigen Videobild überlagert. Die Bilder mit einem Verhältnis von 16 x 9 werden in einem anamorphen 4x3-Format gespeichert. Das ursprüngliche 16x9-Seitenbild bildet das anamorphe 4x3-Seitenverhältnis von 720 x 480 Quellvideo auf ein Seitenverhältnis von 16 x 9.

Im Folgenden finden Sie eine Beschreibung der korrekten Anzeige der einzelnen Modi und ihrer Highlights:

-   **Widescreen:** Das Quellvideo wurde in den größten 16x9-Bereich des Ausgabefensters gestreckt. Die Highlights sind relativ zum Inneren des Bereichs 16x9. Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 16x9-Bereich zu erhalten.
-   **Schwenkscan:** Verwenden Sie aus dem 16x9-Video den horizontalen Offset, der im MPEG2-Stream bereitgestellt wird, um ein 4x3-Unterfenster zu extrahieren. Platzieren Sie das 4x3-Unterfenster im größten 4x3-Bereich des Ausgabeclientfensters. Die Koordinaten der Hervorhebung sind relativ zum 4x3-Ausgabefenster und haben keine Beziehung zum 16x9-Quellvideo. Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich zu erhalten.
-   **Letterbox:** Berechnen Sie den größten 4x3-Bereich des Ausgabefensters. Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich zu erhalten. Das anamorphe 4x3-Quellvideo (das ein 16x9-Bild darstellt) wird im größten 16x9-Unterfenster innerhalb des Bereichs 4x3 platziert. Am oberen und unteren Rand des Unterfensters sollten schwarze Balken hinzugefügt werden, um einen 16x9-Bereich zu erhalten. Die Koordinaten der Hervorhebung sind relativ zum 4x3-Bereich und haben keine Beziehung zum 16x9-Quellvideo. Es ist möglich, dass ein Datenträger eine Hervorhebung angibt, die sich außerhalb des Bereichs 16 x 9 befindet (aber immer noch im 4x3-Fenster). Bei 4x3-Videos wird das Video im größten 4x3-Ausgabebereich des Ausgabeclientfensters platziert. Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 4x3-Bereich beizubehalten.

**MPEG-Vorverarbeitung mit dvd navigator und VMR**

Derzeit wird dem Decoder ein FORMAT \_ MPEG2 \_ VIDEO-Medientyp übergeben (dessen Formatblock auf eine [**MPEG2VIDEOINFO-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) zeigt). An den Ausgabepins erzeugt der Decoder einen \_ Format VideoInfo2-Medientyp, dessen Formatblock auf eine [**VIDEOINFOHEADER2-Struktur**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) zeigt. Das **dwReserved-Feld** der Struktur wurde in **dwControls-Flags** umbenannt.

Der **dwControlFlags-Member** enthält jetzt die neuen Bits.



| Bezeichnung | Wert |
|--------------------------|------------|
| AMCONTROL \_ VERWENDET          | 0x00000001 |
| AMCONTROL \_ PAD \_ TO \_ 4x3  | 0x00000002 |
| AMCONTROL \_ PAD \_ TO \_ 16x9 | 0x00000004 |



 

AMCONTROL \_ USED wird verwendet, um zu testen, ob diese neuen Flags unterstützt werden. Ein Quellfilter sollte das AMCONTROL \_ USED-Flag festlegen und prüfen, ob QueryAccept(MediaType) auf dem Downstreampin erfolgreich ausgeführt wird. Wenn sie abgelehnt wird, können die AMCONTROL-Flags nicht verwendet werden, und dwReserved1 muss auf 0 festgelegt werden.

AMCONTROL \_ PAD \_ TO \_ 4x3 gibt an, dass das Bild aufgefüllt und in einem 4x3-Bereich angezeigt werden soll.

AMCONTROL \_ PAD \_ TO \_ 16x9 gibt an, dass das Bild aufgefüllt und in einem 16x9-Bereich angezeigt werden soll.

Der Decoder sollte die Bits entweder blind kopieren oder verarbeiten. Wenn der Decoder das Letterboxing selbst ausführt, muss er das Pixelseitenverhältnis ändern, das Bild aufpadieren und die entsprechenden \_ \* AMCONTROL-Bits entfernen.

MPEG2VIDEOINFO.dwFlags enthält jetzt drei Flags zum Steuern der Anzeige des Inhalts:

-   `AMMPEG2_DoPanScan (0x00000001)`: Wenn dieses Flag festgelegt ist, sollte der MPEG-2-Videodecoder das Ausgabebild basierend auf Schwenkscanvektoren in der Bildanzeigeerweiterung zuschneiden und das Seitenverhältnis des Bilds in \_ \_ 4x3 ändern. Die VMR sollte kein 16x9-Beispiel mit diesem Flag erhalten. Eine einfache Implementierung kann das Quellrechteck ändern, um einen 540-breiten Quellbereich mit einem linken Rand anzugeben, der dem Anzeigeoffset in der \_ Bildanzeigeerweiterung \_ entspricht.
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Wenn ein Hardwaredecoder diesen Stream in einer Videoausgabe anzeigt (in der Regel ein SVIDEO-Connector auf der Karte), sollte er die Regeln zum Anzeigen eines 16x9-Beispiels auf einem 4x3-Display anwenden.

    Ein Softwaredecoder (oder ein Hardwaredecoder, der die Ausgabe erzeugt, die an die VMR gesendet wird) verfügt über zwei Optionen bei der Verarbeitung von Images:

    1.  Ignorieren Sie dieses Flag, und übergeben Sie den VideoInfoHeader2-Inhalt an die VMR (das AMCONTROL \_ PAD \_ TO 4x3-Flag wird bereits vom \_ [DVD-Navigator](dvd-navigator-filter.md) im Beispiel festgelegt). VmR findet ein 16x9-Videobeispiel mit dem Flag AMCONTROL PAD TO 4x3 und einem \_ \_ \_ 4x3-Unterbildstream. Die Anwendung muss festlegen, dass die ausgabenormierten Zielrechtecke der beiden Datenströme die gleiche Breite haben.
    2.  Konvertieren Sie den anamorphen Stream in ein 4x3-Bild, indem Sie den oberen und unteren Rand des Bilds aufpaddieren und das Seitenverhältnis des Bilds auf 4x3 festlegen (siehe Letterbox oben) und das AMCONTROL \_ PAD \_ TO \_ 4x3 Bit aus VIDEOINFOHEADER2 entfernen.

    DirectXVA-Decoder, die video- und subpicture-Streams mischen, müssen dieses Flag verarbeiten. Wenn die Hardware das gemischten Unterbild nicht skalieren kann, sollte der Decoder einen separaten Unterbilddatenstrom erzeugen, damit die VMR mit dem Video kombiniert wird.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Wenn ein Hardwaredecoder diesen Datenstrom in einer Videoausgabe anzeigt (in der Regel ein SVIDEO-Connector auf der Karte), sollte ein 16x9-Display (anamorph) angenommen werden.

    Ein Softwaredecoder (oder ein Hardwaredecoder, der die Ausgabe erzeugt, die an die VMR gesendet wird) verfügt über zwei Optionen bei der Verarbeitung eines anamorphen Bilds:

    1.  Ignorieren Sie dieses Flag, und kopieren Sie den VideoInfoHeader2-Inhalt auf die VMR. Die VMR padt 4x3-Images auf 16 x 9, wenn das \_ AMCONTROL-PAD \_ auf \_ 16 x 9 festgelegt ist.
    2.  Auflisten des Ausgabebilds auf ein 16x9-Bild und Entfernen des \_ AMCONTROL-PAD \_ auf \_ 16 x 9 Bit.

Die meisten Decoder sollten **GetMediaType** verwenden, um eine Medienänderung am Eingabepin zu erkennen und den Inhalt von **VIDEOINFOHEADER2** (in **MPEG2INFOHEADER** enthalten) an den Ausgabepin zu kopieren. Sie verarbeiten wahrscheinlich nur das PanScan-Bit.

Der folgende Beispielcode zeigt, wie der **VIDEOINFOHEADER2-Inhalt** von einem Eingabepin in einen Ausgabepin kopiert wird.


```C++
#include <dvdmedia.h>
HRESULT CopyMPeg2ToVideoInfoHeader2(CMediaSample* pInSample, CMediaSample* pOutSample)
{
    HRESULT hr = S_OK;
    // Check for a media type on the input sample.
    AM_MEDIA_TYPE* pInType;
    if (pInSample->GetMediaType(&pInType) == S_OK) 
    {
        // Make sure it's an MPEG2 Video format.
        if ((pInType->formattype == FORMAT_MPEG2_VIDEO) &&
            (pInType->cbFormat >= sizeof(MPEG2VIDEOINFO)))
        {
            hr = S_OK; // Initialize hr for the CMediaType constructor.
            CMediaType outType(*pInType, &hr);
            if (FAILED(hr))
            {
                DeleteMediaType( pInType );
                return hr;
            }

            // Set the format type GUID.
            outType.SetFormatType(&FORMAT_VideoInfo2);
                
            // Truncate the format block to include just the VIDEOINFOHEADER part.
            MPEG2VIDEOINFO *pMPeg2Header = (MPEG2VIDEOINFO*)pInType->pbFormat;
            BYTE *pVIH = (BYTE*)&pMPeg2Header->hdr;
            hr = (outType.SetFormat(pVIH, sizeof(VIDEOINFOHEADER2)) ? S_OK : E_OUTOFMEMORY);
            if (SUCCEEDED(hr))
            {
                hr = pOutSample->SetMediaType(&outType);
            }
        } 
        else 
        {
            ASSERT(FALSE); // Not a MPEG2 header.
            hr = VFW_E_INVALIDMEDIATYPE;
        }
        DeleteMediaType( pInType );
    } 

    return hr;
}
```



 

 



