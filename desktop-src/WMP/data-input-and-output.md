---
title: Dateneingabe und -ausgabe
description: Dateneingabe und -ausgabe
ms.assetid: a03b5327-65df-4cb9-a639-1e943ac28bfc
keywords:
- Windows Media Player-Plug-ins, Dateneingabe und-Ausgabe
- Plug-ins, Dateneingabe und-Ausgabe
- Plug-Ins für digitale Signalverarbeitung, Dateneingabe und-Ausgabe
- DSP-Plug-ins, Dateneingabe und-Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39f66946dc796337d1f1e638cfe3828b3cbfbb6e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100722"
---
# <a name="data-input-and-output"></a>Dateneingabe und -ausgabe

Windows Media Player stellt den DSP-Plug-ins über einen von Windows Media Player zugeordneten Eingabepuffer Audiodaten oder Videodaten bereit. DSP-Plug-ins geben verarbeitete Daten an Windows Media Player über einen Ausgabepuffer zurück, der auch von Windows Media Player zugeordnet ist. Windows Media Player verwaltet den Prozess der Übergabe von Daten zwischen sich selbst und dem DSP-Plug-in durch Aufrufen von Methoden, die vom Plug-in implementiert werden. Für ein Plug-in, das als DirectX-Medienobjekt (DMO) fungiert, funktioniert der Prozess wie folgt:

1.  Windows Media Player ruft **imediaobject::P rocessinput** auf und übergibt einen Zeiger auf ein **imediabuffer** -Objekt an das DSP-Plug-in.
2.  Das DSP-Plug-in speichert einen Verweis Zähler für das Eingabepuffer Objekt. Das DSP-Plug-in gibt einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.
3.  Windows Media Player ruft **imediaobject::P rocess Output** auf und übergibt einen Zeiger auf ein Array von **DMO- \_ Ausgabe \_ Daten \_ Puffer** Strukturen (die Ausgabepuffer enthalten) an das DSP-Plug-in.
4.  Das DSP-Plug-in verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer. Das DSP-Plug-in gibt den Verweis Zähler für das Eingabepuffer Objekt frei, wenn alle Daten im Puffer verarbeitet wurden. Das DSP-Plug-in gibt dann einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.
5.  Windows Media Player rendert den Inhalt im Ausgabepuffer.

Für ein Plug-in, das als Media Foundation Transformation (MFT) fungiert, funktioniert der Prozess wie folgt:

-   Windows Media Player ruft **imftransform::P rocessinput** auf und übergibt einen Zeiger auf ein **imfsample** -Schnittstellen Objekt an das DSP-Plug-in.
    1.  Das DSP-Plug-in speichert einen Verweis Zähler für die **IMF Sample** -Schnittstelle. Das DSP-Plug-in gibt einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.
    2.  Windows Media Player ruft **imftransform::P rocess Output** auf und übergibt einen Zeiger auf ein Array von **MFT- \_ Ausgabe \_ Daten \_ Puffer** Strukturen (die Ausgabepuffer enthalten) an das DSP-Plug-in.
    3.  Das DSP-Plug-in verarbeitet die Daten im Eingabepuffer und kopiert die Daten dann in den entsprechenden Ausgabepuffer. Das DSP-Plug-in gibt den Verweis Zähler für das Eingabepuffer Objekt frei, wenn alle Daten im Puffer verarbeitet wurden. Das DSP-Plug-in gibt dann einen entsprechenden Erfolg oder Fehler- **HRESULT** zurück.
    4.  Windows Media Player rendert den Inhalt im Ausgabepuffer.

Dieser Prozess wird fortlaufend wiederholt, während das Plug-in aktiviert ist und Windows Media Player über Inhalte zum Rendering verfügt.

> [!Note]  
> Schreiben Sie keinen Code, der Daten in den Eingabepuffer schreibt oder Daten aus dem Ausgabepuffer liest. Falscher Zugriff auf Datenpuffer kann zu unerwarteten Ergebnissen führen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




