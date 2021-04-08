---
description: MPEG-decodervorverarbeitungs Transformationen
ms.assetid: c7ae0137-0d02-46da-9532-738d805e327d
title: MPEG-decodervorverarbeitungs Transformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b70df51b26ec3fa25d67a03a4e494869a2f25760
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747056"
---
# <a name="mpeg-decoder-preprocessing-transformations"></a>MPEG-decodervorverarbeitungs Transformationen

**Letterbox und Panscan**

Das 4X3-Bild kann gebildet werden, indem der obere und untere Rand des Bilds (als Briefkasten Bild bezeichnet) oder ein 4X3-Teil des Bilds (als Panscan-Bild bezeichnet) gebildet wird. Die Menüs und subbildstreams werden oberhalb des letzten Video Bilds überlagert. Die Bilder mit dem Buch "16x9" werden in einem 4X3-anamorphen Format gespeichert. Die Streckung des anamorphen 4X3-Seitenverhältnisses 720x480-Quellvideos auf ein 16x9-Seitenverhältnis bildet das ursprüngliche 16x9-aspektbild.

Im folgenden finden Sie eine Beschreibung der ordnungsgemäßen Anzeige der einzelnen Modi und ihrer Highlights:

-   **Breitbild:** Das Quellvideo wurde in den größten 16x9-Bereich des Ausgabe Fensters gestreckt. Die Highlights sind relativ zum Inneren des Bereichs 16x9. Schwarze Balken sollten entweder am oberen und unteren Rand oder an den Seiten hinzugefügt werden, um einen 16x9-Bereich beizubehalten.
-   **Pan-Scan:** Verwenden Sie aus dem 16x9-Video den horizontalen Offset, der im MPEG2-Stream bereitgestellt wird, um ein 4X3-Unterfenster zu extrahieren. Platzieren Sie das 4X3-Unterfenster in den größten 4X3-Bereich des Ausgabe Client Fensters. Die Koordinaten der Hervorhebung sind relativ zum 4X3-Ausgabefenster und verfügen nicht über eine Beziehung zum 16x9-Quellvideo. Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten.
-   **Letterbox:** Berechnen Sie den größten 4X3-Bereich des Ausgabe Fensters. Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten. Das Video mit der Quelle "anamorph 4X3" (das ein 16x9-Bild darstellt) wird in dem größten 16x9-Unterfenster innerhalb des 4X3-Bereichs platziert. Schwarze Balken sollten am oberen und unteren Rand des unter Fensters eingefügt werden, um einen Bereich von 16x9 beizubehalten. Die Koordinaten der Hervorhebung sind relativ zum 4X3-Bereich und verfügen nicht über eine Beziehung zu dem 16x9-Quellvideo. Ein Datenträger kann eine Hervorhebung angeben, die sich außerhalb des Bereichs 16x9 befindet (aber noch im Fenster 4X3). Bei 4X3-Videos wird das Video in den größten 4X3-Ausgabebereich des Ausgabe Client Fensters eingefügt. Schwarze Balken sollten entweder am oberen und unteren Rand oder auf der Seite hinzugefügt werden, um einen Bereich von 4 x 3 zu erhalten.

**MPEG-Vorverarbeitung mit dem DVD-Navigator und VMR**

Derzeit wird dem Decoder ein Format- \_ \_ Video Medientyp vom Typ "MPEG2" (dessen Format Block auf eine [**MPEG2VIDEOINFO**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo) -Struktur zeigt) übermittelt. Auf den Ausgabe Pins erzeugt der Decoder den \_ Medientyp Format VideoInfo2, dessen Format Block auf eine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Struktur zeigt. Das **dwReserved** -Feld der Struktur wurde in **dwcontrols** -Flags umbenannt.

Der **dwcontrolflags** -Member enthält jetzt die neuen Bits.



|                          |            |
|--------------------------|------------|
| verwendete amcontrol \_          | 0x00000001 |
| Amcontrol- \_ Pad \_ bis \_ 4X3  | 0x00000002 |
| Amcontrol- \_ Pad \_ bis \_ 16x9 | 0x00000004 |



 

Mithilfe von amcontrol \_ wird getestet, ob diese neuen Flags unterstützt werden. Ein Quell Filter sollte das verwendete amcontrol \_ -Flag festlegen und prüfen, ob queryaccept (MediaType) auf dem Downstream-Pin erfolgreich ist. Wenn Sie abgelehnt wird, können die amcontrol-Flags nicht verwendet werden, und dwReserved1 muss auf 0 festgelegt werden.

Amcontrol \_ Pad \_ zu \_ 4X3 gibt an, dass das Bild in einem Bereich von 4 x 3 aufgefüllt und angezeigt werden soll.

\_Der amcontrol \_ -Pad bis \_ 16x9 gibt an, dass das Bild in einem 16x9-Bereich aufgefüllt und angezeigt werden soll.

Der Decoder sollte die Bits entweder Blind kopieren oder verarbeiten. Wenn der Decoder das Letterbox selbst ausführt, muss er das Pixel Seitenverhältnis ändern, das Bild auffüllen und die entsprechenden amcontrol- \_ \* Bits entfernen.

MPEG2VIDEOINFO. dwFlags enthält jetzt drei Flags, mit denen gesteuert werden kann, wie der Inhalt angezeigt werden soll:

-   `AMMPEG2_DoPanScan (0x00000001)`: Wenn dieses Flag festgelegt ist, sollte der MPEG-2-Video Decoder das Ausgabe Bild auf der Grundlage von Pan-Scan-Vektoren in der Bild \_ Anzeige Erweiterung Zuschneiden \_ und das Bildseiten Verhältnis in 4 x 3 ändern. Der VMR sollte kein 16x9-Beispiel mit diesem Flag erhalten. Eine einfache Implementierung kann das Quell Rechteck ändern, um einen 540-weiten Quellbereich mit einem linken Rand anzugeben, der gleich dem Anzeige Offset in der Bild \_ Anzeige \_ Erweiterung ist.
-   `AMMPEG2_LetterboxAnalogOut (0x00000020)`: Wenn ein Hardware Decoder diesen Stream einer Videoausgabe anzeigt (in der Regel ein SVideo-Connector auf der Karte), sollte er die Regeln zum Anzeigen eines 16x9-Beispiels in einer 4X3-Anzeige anwenden.

    Ein Software Decoder (oder ein Hardware Decoder, der die an die VMR gesendete Ausgabe erzeugt) verfügt bei der Verarbeitung von Images über zwei Optionen:

    1.  Ignorieren Sie dieses Flag, und übergeben Sie den VideoInfoHeader2-Inhalt an die VMR (das Flag "amcontrol \_ Pad \_ to \_ 4X3" wird bereits vom [DVD-Navigator](dvd-navigator-filter.md) im Beispiel festgelegt). Die VMR findet ein 16x9-Video Beispiel, bei dem der amcontrol \_ \_ -Pad für das \_ 4X3-Flag und ein 4X3-teilbildstream festgelegt ist. Die Anwendung muss die normalisierten Ausgabeziel Rechtecke der beiden Streams auf die gleiche Breite festlegen.
    2.  Konvertieren Sie den anamorphen Datenstrom in ein 4X3-Bild, indem Sie den oberen und unteren Rand des Bilds auffüllen und das Bildseiten Verhältnis auf 4X3 festlegen (siehe Letterbox oben), und entfernen Sie das amcontrol- \_ Pad \_ \_ aus VIDEOINFOHEADER2.

    Directxva-decoderer, die die Video-und subbildstreams mischen, müssen dieses Flag verarbeiten. Wenn das gemischte subbild von der Hardware nicht skaliert werden kann, sollte der Decoder einen separaten teilbildstream für VMR für die Mischung mit dem Video entwickeln.

-   `AMMPEG2_WidescreenAnalogOut (0x00000200)`: Wenn ein Hardware Decoder diesen Stream einer Videoausgabe anzeigt (in der Regel ein SVideo-Connector auf der Karte), sollte er eine 16x9-Anzeige (anamorph) annehmen.

    Ein Software Decoder (oder ein Hardware Decoder, der die an die VMR gesendete Ausgabe erzeugt) verfügt bei der Verarbeitung eines anamorphen Bilds über zwei Optionen:

    1.  Ignorieren Sie dieses Flag, und kopieren Sie den Inhalt von VideoInfoHeader2 in den VMR. VMR füllt 4X3-Images auf 16x9 aus, wenn der amcontrol- \_ Pad \_ auf \_ 16x9 festgelegt ist.
    2.  Auffüllen Sie das Ausgabe Bild in ein 16x9-Bild, und entfernen Sie das amcontrol- \_ Pad \_ auf \_ 16x9-Bit.

Die meisten Decoder sollten **getmediatype** verwenden, um eine Medien Änderung an der Eingabe-PIN zu erkennen und den **VIDEOINFOHEADER2** -Inhalt (enthalten im **MPEG2INFOHEADER**) in die Ausgabepin zu kopieren. Sie verarbeiten wahrscheinlich nur das Panscan-Bit.

Der folgende Beispielcode zeigt, wie der **VIDEOINFOHEADER2** -Inhalt aus einer Eingabe-PIN in eine Ausgabepin kopiert wird.


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



 

 



