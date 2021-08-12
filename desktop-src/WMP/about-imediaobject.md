---
title: Informationen zu IMediaObject
description: Informationen zu IMediaObject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player-Plug-Ins,Schnittstellen
- Plug-Ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-Ins, Schnittstellen
- Schnittstellen,DSP-Plug-Ins
- Windows Media Player-Plug-Ins, IMediaObject-Schnittstelle
- Plug-Ins, IMediaObject-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, IMediaObject-Schnittstelle
- DSP-Plug-Ins, IMediaObject-Schnittstelle
- IMediaObject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2dbf44a527d61d924045a4bcceded5d90bb174fef608e3b7667338e99aa1efe9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118583907"
---
# <a name="about-imediaobject"></a>Informationen zu IMediaObject

Die **IMediaObject-Schnittstelle** ist die erforderliche Schnittstelle für DMOs. **IMediaObject** enthält die Methoden, die ein Windows Media Player DSP-Plug-In verwendet, um Daten aus Windows Media Player zu erhalten, die Daten zu verarbeiten und die verarbeiteten Daten an Windows Media Player. Die vollständige Dokumentation der **IMediaObject-Schnittstelle** finden Sie im Abschnitt DirectShow des Windows SDK.

Die Methoden von **IMediaObject** können wie folgt kategorisiert werden:

## <a name="methods-that-handle-format-negotiation"></a>Methoden zur Behandlung der Formataushandlung

Dies sind die Methoden, Windows Media Player aufrufen, um Informationen über die vom Plug-In unterstützten Datenformate zu erhalten. Diese Methoden umfassen:

-   **GetInputMaxLatency**
-   **GetInputSizeInfo**
-   **GetInputStreamInfo**
-   **GetInputType**
-   **GetOutputSizeInfo**
-   **GetOutputStreamInfo**
-   **GetOutputType**
-   **GetStreamCount**
-   **SetInputMaxLatency**
-   **SetInputType**
-   **SetOutputType**

Einige dieser Methoden, z. B. **GetInputType** und **SetInputType,** verwenden die **DMO MEDIA \_ \_ TYPE-Struktur,** um das Format der von einem Stream verwendeten Daten zu beschreiben. Wenn Windows Media Player diese Methoden aufruft, stellt sie einen Zeiger auf eine DMO **\_ MEDIA \_ TYPE-Struktur.** Wenn eine Methode wie **SetInputType** die Medientypinformationen angibt, sollte das Plug-In die **DMO MEDIA \_ \_ TYPE-Struktur in** eine Membervariable kopieren und deren Datenmitglieder überprüfen, um den Datentyp zu bestimmen, den Windows Media Player im Eingabepuffer bereitstellen wird. Wenn eine Methode wie **GetInputType** die Medientypinformationen abruft, sollte das Plug-In die Adresse der Membervariablen, die die **DMO MEDIA \_ \_ TYPE-Struktur enthält, in** den Zeiger kopieren, der von Windows Media Player in der Parameterliste bereitgestellt wird.

Windows Media Player werden hauptsächlich zwei Member der MEDIA **\_ \_ TYPE DMO struktur** verwendet:

-   **majortype:** Ein GUID (Globally Unique Identifier), der die Gesamtkategorie der Medien angibt, z. B. Audio oder Video.
-   **Untertyp:** Eine GUID, die eine ausführlichere Beschreibung der Medien angibt, z. B. PCM-Audio.

Diese GUIDs finden Sie im Header mit dem Namen uuids.h, der im Windows SDK enthalten ist.

Methoden wie **GetInputSizeInfo** stellen Informationen Windows Media Player, wie viel Arbeitsspeicher zum Zuordnen der Verarbeitungspuffer erforderlich ist. Methoden wie **GetStreamCount und** **GetOutputStreamInfo** stellen Informationen Windows Media Player die Anzahl und das Zeichen der vom DSP-Plug-In unterstützten Streams zur Verfügung.

**GetInputMaxLatency und** **SetInputMaxLatency** werden von DMOs in Sonderfällen implementiert. Windows Media Player DSP-Plug-Ins sollten E \_ NOTIMPL zurückgeben.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Methoden zum Angeben oder Abrufen von Zustandsinformationen

Dies sind die Methoden, Windows Media Player aufrufen, um Werte im Zusammenhang mit dem aktuellen Zustand des Plug-Ins zu erhalten oder zu festlegen. Diese Methoden umfassen:

-   **GetInputCurrentType**
-   **GetInputStatus**
-   **GetOutputCurrentType**

**GetInputCurrentType** und **GetOutputCurrentType** verwenden die **DMO MEDIA \_ \_ TYPE-Struktur,** um Informationen zu den zuvor für die Eingabe- und Ausgabestreams festgelegten Medientypen Windows Media Player an Windows Media Player zurück zu geben. **GetInputStatus gibt** ein Flag zurück, das Windows Media Player ob das DSP-Plug-In Eingabedaten akzeptieren kann.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Methoden zum Verarbeiten von Pufferungs- und Verarbeitungsdaten

Dies sind die Methoden, Windows Media Player aufrufen, um die verschiedenen Prozesse zu initiieren, die das Plug-In für die Verarbeitung digitaler Signale ausführt. Diese Methoden umfassen:

-   **AllocateStreamingResources**
-   **Diskontinuität**
-   **Leerung**
-   **FreeStreamingResources**
-   **Sperre**
-   **ProcessInput**
-   **ProcessOutput**

Windows Media Player aufruft **AllocateStreamingResources** und **FreeStreamingResources,** um dem DSP-Plug-In die Möglichkeit zu geben, zusätzliche Puffer, die das Plug-In möglicherweise für die interne Verarbeitung benötigt, ein- oder frei zu geben.

Windows Media Player DSP-Plug-Ins müssen nicht die DMO **Discontinuity-Methode** verwenden.

Windows Media Player **Wird geleert,** um das DSP-Plug-In an das Leeren aller intern gepufferten Daten zu richten. Das Plug-In sollte alle Verweise auf **IMediaBuffer-Schnittstellen** veröffentlichen, alle Werte löschen, die den Zeitstempel oder die Stichprobenlänge für den Medienpuffer angeben, und alle internen Zustände erneut initialisieren, die vom Inhalt des Medienbeispiels abhängen.

Windows Media Player ProcessInput auf, um einen Zeiger auf eine **IMediaBuffer-Schnittstelle** an das DSP-Plug-In zu übergeben. Diese Schnittstelle bietet Zugriff auf den Eingabepuffer, der von Windows Media Player, um Daten an das Plug-In zu übergeben. Windows Media Player anschließend **ProcessOutput** auf, um einen Zeiger auf eine **IMediaBuffer-Schnittstelle** zu übergeben, die Zugriff auf den von Windows Media Player zugeordneten Ausgabepuffer ermöglicht, um die verarbeiteten Daten vom DSP-Plug-In zu empfangen.

Die **IMediaObject-Schnittstelle** enthält eine Methode namens **Lock**. Diese Methode ist so konzipiert, dass sie eine Sperre für die DMO, um die DMO serialisiert zu lassen, wenn mehrere Vorgänge ausführen. Die Version von **IMediaObject::Lock** im Assistentencode überschreibt die ATL-Implementierung von **Lock.** Da Windows Media Player Aufrufe an die DMO-Schnittstelle eines DSP-Plug-Ins serialisiert, gibt die Implementierung von **Lock** einfach S \_ OK zurück. Weitere Informationen zum Erstellen eines Multithread-DMO finden Sie im Abschnitt DirectShow des Windows SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erforderliche Schnittstellen**](required-interfaces.md)
</dt> </dl>

 

 




