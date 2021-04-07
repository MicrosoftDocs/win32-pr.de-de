---
description: Einstellungen für deinterlace werden festgelegt
ms.assetid: 31d59f17-552b-46d1-89e4-751216f54280
title: Einstellungen für deinterlace werden festgelegt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be52ae3023c8e4bc83c3305a104c389f423cffd6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103745408"
---
# <a name="setting-deinterlace-preferences"></a>Einstellungen für deinterlace werden festgelegt

Der Video Mischungs-Renderer (VMR) unterstützt die hardwarebeschleunigte Deinterlacing, wodurch die renderingqualität für Zeilen Sprung Video verbessert wird. Welche Features genau verfügbar sind, hängt von der zugrunde liegenden Hardware ab. Die Anwendung kann die Deinterlacing-Hardwarefunktionen Abfragen und deinterlacingeinstellungen über die [**ivmrdeinterlacecontrol**](/windows/desktop/api/Strmif/nn-strmif-ivmrdeinterlacecontrol) -Schnittstelle (VMR-7) oder die [**IVMRDeinterlaceControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrdeinterlacecontrol9) -Schnittstelle (VMR-9) festlegen. Deinterlacing wird pro Stream ausgeführt.

Es gibt einen wichtigen Unterschied beim interlacingverhalten zwischen VMR-7 und VMR-9. Auf Systemen, auf denen die Grafikhardware erweiterte Deinterlacing nicht unterstützt, kann VMR-7 auf die Hardware Überlagerung zurückgreifen und Sie anweisen, eine Bob-Formatvorlage zu verwenden. In diesem Fall wird das Video tatsächlich bei 60 kippt pro Sekunde gerendert, obwohl der VMR 30 fps meldet.

Außer im Fall von VMR-7 mit Hardware Überlagerung wird Deinterlacing vom Mixer von VMR ausgeführt. Der Mixer verwendet die DXVA (DirectX Video Acceleration) Deinterlacing-Gerätetreiber Schnittstelle (DDI), um die Deinterlacing-Datei auszuführen. Dieser DDI kann von Anwendungen nicht aufgerufen werden, und Anwendungen können die Deinterlacing-Funktionalität von VMR nicht ersetzen. Allerdings kann eine Anwendung den gewünschten Deinterlacing-Modus auswählen, wie in diesem Abschnitt beschrieben.

> [!Note]  
> In diesem Abschnitt werden die **IVMRDeinterlaceControl9** -Methoden beschrieben, die Versionen von VMR-7 sind jedoch nahezu identisch.

 

Gehen Sie folgendermaßen vor, um die Deinterlacing-Funktionen für einen Videostream zu erhalten:

1.  Füllen Sie eine [**VMR9VideoDesc**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9videodesc) -Struktur mit einer Beschreibung des Videodaten Stroms aus. Details zum Ausfüllen dieser Struktur werden später angegeben.
2.  Übergeben Sie die Struktur an die [**IVMRDeinterlaceControl9:: getnumofdeinterlacemodes**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getnumberofdeinterlacemodes) -Methode. Ruft die-Methode zweimal auf. Der erste-Befehl gibt die Anzahl der Deinterlacing-Modi zurück, die von der Hardware für das angegebene Format unterstützt werden. Weisen Sie ein Array von GUIDs dieser Größe zu, und wenden Sie die-Methode erneut an, und übergeben Sie dabei die Adresse des-Arrays. Der zweite-Befehl füllt das Array mit GUIDs. Jeder GUID identifiziert einen deinterlacingmodus.
3.  Um die Untertitel eines bestimmten Modus abzurufen, müssen Sie die [**IVMRDeinterlaceControl9:: getdeinterlacemodecaps**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemodecaps) -Methode aufrufen. Übergeben Sie dieselbe **VMR9VideoDesc** -Struktur zusammen mit einer der GUIDs aus dem Array. Die-Methode füllt eine [**VMR9DeinterlaceCaps**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9deinterlacecaps) -Struktur mit den Funktionen des-Modus.

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



Nun kann die Anwendung den Deinterlacing-Modus für den Stream mit den folgenden Methoden festlegen:

-   Die [**setdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlacemode) -Methode legt den bevorzugten Modus fest. Verwenden \_ Sie die GUID NULL, um Deinterlacing zu deaktivieren.
-   Die [**setdeinterlaceprefs**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-setdeinterlaceprefs) -Methode gibt das Verhalten an, wenn der angeforderte Modus nicht verfügbar ist.
-   Die [**getdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getdeinterlacemode) -Methode gibt den von Ihnen festgelegten bevorzugten Modus zurück.
-   Die [**getactualdeinterlacemode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrdeinterlacecontrol9-getactualdeinterlacemode) -Methode gibt den tatsächlich verwendeten Modus zurück, bei dem es sich um einen Fall Back Modus handeln kann, wenn der bevorzugte Modus nicht verfügbar ist.

Weitere Informationen finden Sie auf den Referenzseiten der Methode.

**Verwenden der VMR9VideoDesc-Struktur**

Im zuvor beschriebenen Verfahren besteht der erste Schritt darin, eine **VMR9VideoDesc** -Struktur mit einer Beschreibung des Videodaten Stroms auszufüllen. Beginnen Sie, indem Sie den Medientyp des Videodaten Stroms erhalten. Hierzu können Sie [**IPin:: connectionmediatype**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectionmediatype) in der Eingabe-PIN des VMR-Filters aufrufen. Überprüfen Sie dann, ob der Videostream Zeilen Sprung ist. Nur [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate können mit Zeilen Sprung verknüpft werden. Wenn der Formatierungstyp Format \_ videoinfo ist, muss es sich um einen progressiven Frame handeln. Wenn der Formattyp Format \_ VideoInfo2 ist, überprüfen Sie das Feld **dwinterlaceflags** für das aminterlace- \_ Flag isinterlacing. Das vorhanden sein dieses Flags gibt an, dass das Video mit Zeilen Sprung versehen ist.

Angenommen, die Variable **pbmi** ist ein Zeiger auf die [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) -Struktur im Format Block. Legen Sie die folgenden Werte in der **VMR9VideoDesc** -Struktur fest:

-   **dwSize**: Legen Sie dieses Feld auf fest `sizeof(VMR9VideoDesc)` .
-   **dwsamplewidth**: Legen Sie dieses Feld auf fest `pBMI->biWidth` .
-   **dwsampleheight**: Legen Sie dieses Feld auf fest `abs(pBMI->biHeight)` .
-   **Sample Format**: Dieses Feld beschreibt die damit-Eigenschaften des Medientyps. Überprüfen Sie das Feld **dwinterlaceflags** in der **VIDEOINFOHEADER2** -Struktur, und legen Sie **Sampleformat** auf das entsprechende [**VMR9 \_ Sampleformat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) -Flag fest. Eine Hilfsfunktion hierfür finden Sie unten.
-   **Inputsamplefreq**: Dieses Feld gibt die Eingabe Häufigkeit an, die aus dem **avgtimeperframe** -Feld in der **VIDEOINFOHEADER2** -Struktur berechnet werden kann. Legen Sie im allgemeinen Fall **dwzähler** auf 10 Millionen fest, und legen Sie für **dwnenner** den Wert **avgtimeperframe** fest. Sie können jedoch auch nach einigen bekannten Frameraten suchen:

    | Durchschnittliche Zeit pro Frame | Frame Rate (fps) | Zähler | Vorzuschlagen |
    |------------------------|------------------|-----------|-------------|
    | 166833                 | 59,94 (NTSC)     | 60000     | 1001        |
    | 333667                 | 29,97 (NTSC)     | 30.000     | 1001        |
    | 417188                 | 23,97 (NTSC)     | 24.000     | 1001        |
    | 200.000                 | 50,00 (PAL)      | 50        | 1           |
    | 400000                 | 25,00 (PAL)      | 25        | 1           |
    | 416667                 | 24,00 (Film)     | 24        | 1           |

    

     

-   **Outputframefreq**: Dieses Feld gibt die Ausgabe Häufigkeit an, die anhand des **inputsamplefreq** -Werts und der überlappenden Merkmale des Eingabedaten Stroms berechnet werden kann:
    -   Legen Sie **outputframefreq. dwnenner** auf **inputsamplefreq. dwnenner** fest.
    -   Wenn das Eingabe Video verschachtelt ist, legen Sie **outputframefreq. dwnumerator** auf 2 x **inputsamplefreq. dwnumerator** fest. (Nach Deinterlacing wird die Framerate verdoppelt.) Legen Sie andernfalls den Wert auf **inputsamplefreq. dwnumerator** fest.
-   **dwfourcc**: Legen Sie dieses Feld auf fest `pBMI->biCompression` .

Die folgende Hilfsfunktion konvertiert aminterlace \_ *X* -Flags in [**VMR9 \_ Sampleformat**](/previous-versions/windows/desktop/api/Vmr9/ne-vmr9-vmr9_sampleformat) -Werte:


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



 

 



