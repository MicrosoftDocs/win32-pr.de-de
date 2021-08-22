---
description: Festlegen von Deinterlace-Einstellungen
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Festlegen von Deinterlace-Einstellungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33dae356618653f501b56f8b7a7eeb98e24ee92eb196cac78466e8cd26c01610
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072574"
---
# <a name="setting-deinterlace-preferences"></a>Festlegen von Deinterlace-Einstellungen

Der Video Mixing Renderer (VMR) unterstützt hardwarebeschleunigte Deinterlacing, wodurch die Renderingqualität für Interlacingvideo verbessert wird. Welche Features genau verfügbar sind, hängt von der zugrunde liegenden Hardware ab. Die Anwendung kann die Hardwaredeinterlacingfunktionen abfragen und Deinterlacingeinstellungen über die [**IVMRDeinterlaceControl-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) (VMR-7) oder [**die IVMRDeinterlaceControl9-Schnittstelle**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) (VMR-9) festlegen. Deinterlacing wird pro Stream ausgeführt.

Es gibt einen wichtigen Unterschied beim Interlacingverhalten zwischen VMR-7 und VMR-9. Auf Systemen, in denen die Grafikhardware erweitertes Deinterlacing nicht unterstützt, kann VMR-7 auf die Hardwareüberlagerung zurückfallen und sie anweisen, eine Bob-Deinterlace zu verwenden. In diesem Fall wird das Video mit 60 Flips pro Sekunde gerendert, obwohl der VMR 30 Bps meldet.

Außer im Fall von VMR-7 mit Hardwareüberlagerung wird das Deinterlacing vom Mixer des virtuellen Computers durchgeführt. Der Mixer verwendet die DirectX-Videobeschleunigung (DXVA) deinterlacing device driver interface (DDI), um das Deinterlacing durchzuführen. Diese DDI kann von Anwendungen nicht aufrufbar sein, und Anwendungen können die Deinterlacing-Funktionalität des virtuellen Computers nicht ersetzen. Eine Anwendung kann jedoch den gewünschten Deinterlacingmodus auswählen, wie in diesem Abschnitt beschrieben.

> [!Note]  
> In diesem Abschnitt werden die **IVMRDeinterlaceControl9-Methoden** beschrieben, aber die VMR-7-Versionen sind fast identisch.

 

Gehen Sie wie folgt vor, um die Deinterlacingfunktionen für einen Videostream zu erhalten:

1.  Füllen Sie eine [**VMR9VideoDesc-Struktur**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) mit einer Beschreibung des Videostreams aus. Details zum Ausfüllen dieser Struktur finden Sie später.
2.  Übergeben Sie die -Struktur an die [**IVMRDeinterlaceControl9::GetNumberOfDeinterlaceModes-Methode.**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) Rufen Sie die -Methode zweimal auf. Der erste Aufruf gibt die Anzahl der Deinterlace-Modi zurück, die die Hardware für das angegebene Format unterstützt. Ordnen Sie ein Array von GUIDs dieser Größe zu, und rufen Sie die Methode erneut auf, und übergeben Sie dabei die Adresse des Arrays. Der zweite Aufruf füllt das Array mit GUIDs. Jede GUID identifiziert einen Deinterlacingmodus.
3.  Um die Funktionen eines bestimmten Modus zu erhalten, rufen Sie die [**IVMRDeinterlaceControl9::GetDeinterlaceModeCaps-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) auf. Übergeben Sie die gleiche **VMR9VideoDesc-Struktur** zusammen mit einer der GUIDs aus dem Array. Die -Methode füllt eine [**VMR9DeinterlaceCaps-Struktur**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) mit den Modusfunktionen auf.

Diese Schritte sind im folgenden Code dargestellt:


```C++
VMR9VideoDesc VideoDesc; 
DWORD dwNumModes = 0;
// Fill in the VideoDesc structure (not shown).
hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
    &dwNumModes, NULL);
if (SUCCEEDED(hr) && (dwNumModes != 0))
{
    // Allocate an array for the GUIDs that identify the modes.
    GUID *pModes = new GUID[dwNumModes];
    if (pModes)
    {
        // Fill the array.
        hr = pDeinterlace->GetNumberOfDeinterlaceModes(&VideoDesc, 
            &dwNumModes, pModes);
        if (SUCCEEDED(hr))
        {
            // Loop through each item and get the capabilities.
            for (int i = 0; i < dwNumModes; i++)
            {
                VMR9DeinterlaceCaps Caps;
                hr = pDeinterlace->GetDeinterlaceModeCaps(pModes + i, 
                    &VideoDesc, &Caps);
                if (SUCCEEDED(hr))
                {
                    // Examine the Caps structure.
                }
            }
        }
        delete [] pModes;
    }
}
```



Nun kann die Anwendung den Deinterlacingmodus für den Stream mithilfe der folgenden Methoden festlegen:

-   Die [**SetDeinterlaceMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) legt den bevorzugten Modus fest. Verwenden Sie GUID \_ NULL, um das Deinterlacing zu deaktivieren.
-   Die [**SetDeinterlacePrefs-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) gibt das Verhalten an, wenn der angeforderte Modus nicht verfügbar ist.
-   Die [**GetDeinterlaceMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) gibt den bevorzugten Modus zurück, den Sie festlegen.
-   Die [**GetActualDeinterlaceMode-Methode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) gibt den tatsächlichen Modus zurück, der möglicherweise ein Fallbackmodus ist, wenn der bevorzugte Modus nicht verfügbar ist.

Die Methodenverweisseiten enthalten weitere Informationen.

**Verwenden der VMR9VideoDesc-Struktur**

In der zuvor beschriebenen Prozedur besteht der erste Schritt im Ausfüllen einer **VMR9VideoDesc-Struktur** mit einer Beschreibung des Videostreams. Beginnen Sie mit dem Abrufen des Medientyps des Videostreams. Rufen Sie hierzu [**IPin::ConnectionMediaType**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) auf dem Eingabepin des VMR-Filters auf. Vergewissern Sie sich dann, dass der Videodatenstrom als Interlacing angezeigt wird. Nur [**VIDEOINFOHEADER2-Formate**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) können als Interlacing verwendet werden. Wenn der Formattyp FORMAT \_ VideoInfo ist, muss es sich um einen progressiven Frame handelt. Wenn der Formattyp FORMAT VideoInfo2 ist, überprüfen Sie das \_ **Feld dwInterlaceFlags** auf das AMINTERLACE \_ IsInterlaced-Flag. Das Vorhandensein dieses Flags gibt an, dass das Video als Interlacing angezeigt wird.

Angenommen, die **Variable pBMI** ist ein Zeiger auf die [**BITMAPINFOHEADER-Struktur**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) im Formatblock. Legen Sie die folgenden Werte in der **VMR9VideoDesc-Struktur** fest:

-   **dwSize:** Legen Sie dieses Feld auf `sizeof(VMR9VideoDesc)` fest.
-   **dwSampleWidth:** Legen Sie dieses Feld auf `pBMI->biWidth` fest.
-   **dwSampleHeight:** Legen Sie dieses Feld auf `abs(pBMI->biHeight)` fest.
-   **SampleFormat:** Dieses Feld beschreibt die Interlace-Merkmale des Medientyps. Überprüfen Sie **das Feld dwInterlaceFlags** in der **VIDEOINFOHEADER2-Struktur,** und legen Sie **SampleFormat** auf das entsprechende [**VMR9 \_ SampleFormat-Flag**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) fest. Eine Hilfsfunktion hierzu finden Sie unten.
-   **InputSampleFreq:** Dieses Feld gibt die Eingabehäufigkeit an, die aus dem **Feld AvgTimePerFrame** in der **VIDEOINFOHEADER2-Struktur berechnet werden** kann. Legen Sie im Allgemeinen **dwNumerator** auf 10000000 und **dwDenominator** auf **AvgTimePerFrame fest.** Sie können jedoch auch nach einigen bekannten Frameraten überprüfen:

    | Durchschnittliche Zeit pro Frame | Framerate (fps) | Zähler | Nenner |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59.94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29.97 (NTSC)     | 30.000     | 1001        |
    | 417188                 | 23.97 (NTSC)     | 24.000     | 1001        |
    | 200.000                 | 50.00 (PAL)      | 50        | 1           |
    | 400000                 | 25.00 (PAL)      | 25        | 1           |
    | 416667                 | 24.00 (Film)     | 24        | 1           |

    

     

-   **OutputFrameFreq:** Dieses Feld gibt die Ausgabehäufigkeit an, die aus dem **InputSampleFreq-Wert** und den überlappenden Merkmalen des Eingabestreams berechnet werden kann:
    -   Legen **Sie OutputFrameFreq.dwDenominator** auf **InputSampleFreq.dwDenominator fest.**
    -   Wenn das Eingabevideo übereinander liegt, legen Sie **OutputFrameFreq.dwNumerator** auf 2 x **InputSampleFreq.dwNumerator fest.** (Nach dem Deinterlacing wird die Bildfrequenz verdoppelt.) Legen Sie andernfalls den Wert auf **InputSampleFreq.dwNumerator fest.**
-   **dwFourCC:** Legen Sie dieses Feld auf `pBMI->biCompression` fest.

Die folgende Hilfsfunktion konvertiert AMINTERLACE \_ *X-Flags* in [**VMR9 \_ SampleFormat-Werte:**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat)


```C++
#define IsInterlaced(x) ((x) & AMINTERLACE_IsInterlaced)
#define IsSingleField(x) ((x) & AMINTERLACE_1FieldPerSample)
#define IsField1First(x) ((x) & AMINTERLACE_Field1First)

VMR9_SampleFormat ConvertInterlaceFlags(DWORD dwInterlaceFlags)
{
    if (IsInterlaced(dwInterlaceFlags)) {
        if (IsSingleField(dwInterlaceFlags)) {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldSingleEven;
            }
            else {
                return VMR9_SampleFieldSingleOdd;
            }
        }
        else {
            if (IsField1First(dwInterlaceFlags)) {
                return VMR9_SampleFieldInterleavedEvenFirst;
             }
            else {
                return VMR9_SampleFieldInterleavedOddFirst;
            }
        }
    }
    else {
        return VMR9_SampleProgressiveFrame;  // Not interlaced.
    }
}
```



 

 



