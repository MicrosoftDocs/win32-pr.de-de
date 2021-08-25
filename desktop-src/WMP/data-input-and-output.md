---
title: Dateneingabe und -ausgabe
description: Dateneingabe und -ausgabe
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player Plug-Ins, Dateneingabe und -ausgabe
- Plug-Ins, Dateneingabe und -ausgabe
- Plug-Ins für die digitale Signalverarbeitung, Dateneingabe und -ausgabe
- DSP-Plug-Ins, Dateneingabe und -ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d31e7c6fba24451d65e59c3fb9f56ec6b1413be3d595530414c25c52964b9b15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863670"
---
# <a name="data-input-and-output"></a>Dateneingabe und -ausgabe

Windows Media Player stellt Audio- oder Videodaten für DSP-Plug-Ins über einen Eingabepuffer zur Windows Media Player. DSP-Plug-Ins geben verarbeitete Daten an Windows Media Player Ausgabepuffer zurück, der auch von einem Windows Media Player. Windows Media Player verwaltet den Prozess der Übergabe von Daten zwischen sich selbst und dem DSP-Plug-In durch Aufrufen von Methoden, die vom Plug-In implementiert werden. Für ein Plug-In, das als DirectX Media Object (DMO) verwendet wird, funktioniert der Prozess wie folgt:

1.  Windows Media Player **IMediaObject::P rocessInput** auf, und über gibt einen Zeiger auf ein **IMediaBuffer-Objekt** an das DSP-Plug-In weiter.
2.  Das DSP-Plug-In behält eine Verweisanzahl für das Eingabepufferobjekt bei. Das DSP-Plug-In gibt ein entsprechendes Erfolgreiches oder **Fehler-HRESULT zurück.**
3.  Windows Media Player ruft **IMediaObject::P rocessOutput** auf und über gibt einen Zeiger auf ein Array von **DMO OUTPUT DATA \_ \_ \_ BUFFER-Strukturen** (die Ausgabepuffer enthalten) an das DSP-Plug-In weiter.
4.  Das DSP-Plug-In verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer. Das DSP-Plug-In gibt die Verweisanzahl für das Eingabepufferobjekt frei, wenn alle Daten im Puffer verarbeitet wurden. Das DSP-Plug-In gibt dann ein entsprechendes Erfolgreiches oder **Fehler-HRESULT zurück.**
5.  Windows Media Player rendert den Inhalt im Ausgabepuffer.

Für ein Plug-In, das als Media Foundation Transform (MFT) agiert, funktioniert der Prozess wie folgt:

-   Windows Media Player **ruft DIETTRANSFORM::P rocessInput** auf und überträgt einen Zeiger auf ein **NSSAMPLE-Schnittstellenobjekt** an das DSP-Plug-In.
    1.  Das DSP-Plug-In behält eine Verweisanzahl für die **NSBSample-Schnittstelle** bei. Das DSP-Plug-In gibt ein entsprechendes Erfolgreiches oder **Fehler-HRESULT zurück.**
    2.  Windows Media Player ruft **DIEBTRANSFORM::P rocessOutput** auf und überträgt einen Zeiger auf ein Array von **MFT \_ OUTPUT DATA \_ \_ BUFFER-Strukturen** (die Ausgabepuffer enthalten) an das DSP-Plug-In.
    3.  Das DSP-Plug-In verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer. Das DSP-Plug-In gibt die Verweisanzahl für das Eingabepufferobjekt frei, wenn alle Daten im Puffer verarbeitet wurden. Das DSP-Plug-In gibt dann ein entsprechendes Erfolgreiches oder **Fehler-HRESULT zurück.**
    4.  Windows Media Player rendert den Inhalt im Ausgabepuffer.

Dieser Prozess wird kontinuierlich wiederholt, während das Plug-In aktiviert ist und Windows Media Player Inhalt zu rendern hat.

> [!Note]  
> Schreiben Sie keinen Code, der Daten in den Eingabepuffer schreibt oder Daten aus dem Ausgabepuffer liest. Falscher Zugriff auf Datenpuffer kann zu unerwarteten Ergebnissen führen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




