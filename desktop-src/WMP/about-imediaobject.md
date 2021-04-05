---
title: Informationen über imediaobject
description: Informationen über imediaobject
ms.assetid: c483f74a-efd8-4a9f-a719-686099755e63
keywords:
- Windows Media Player-Plug-ins, Schnittstellen
- Plug-ins, Schnittstellen
- Plug-Ins für die digitale Signalverarbeitung, Schnittstellen
- DSP-Plug-ins, Schnittstellen
- Schnittstellen, DSP-Plug-ins
- Windows Media Player-Plug-ins, imediaobject-Schnittstelle
- Plug-ins, imediaobject-Schnittstelle
- Plug-Ins für die digitale Signalverarbeitung, imediaobject-Schnittstelle
- DSP-Plug-ins, imediaobject-Schnittstelle
- Imediaobject-Schnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbbecd749242b67bc5c8f36b3c7a2c0a5fbe461
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708046"
---
# <a name="about-imediaobject"></a>Informationen über imediaobject

Die **imediaobject** -Schnittstelle ist die erforderliche Schnittstelle für DMOS. **Imediaobject** enthält die Methoden, die ein Windows Media Player DSP-Plug-in verwendet, um Daten aus Windows Media Player zu erhalten, die Daten zu verarbeiten und die verarbeiteten Daten an Windows Media Player zurückzugeben. Eine umfassende Dokumentation der **imediaobject** -Schnittstelle finden Sie im Abschnitt DirectShow des Windows SDK.

Die Methoden von **imediaobject** können wie folgt kategorisiert werden:

## <a name="methods-that-handle-format-negotiation"></a>Methoden, die die Format Aushandlung behandeln

Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um Informationen zu den vom Plug-in unterstützten Datenformaten zu erhalten. Diese Methoden umfassen:

-   **Getinputmaxlatency**
-   **Getinputsizone FO**
-   **Getinputstreaminfo**
-   **Getinputtype**
-   **Getoutputsizone FO**
-   **Getoutputstreaminfo**
-   **Getoutputtype**
-   **Getstreamcount**
-   **"* Tinputmaxlatency"**
-   **"Ttinputtype"**
-   **Setoutputtype**

Einige dieser Methoden, wie z. b. **getinputtype** und " **abtinputtype**", verwenden die **DMO- \_ \_ Medientyp** Struktur, um das Format der Daten zu beschreiben, die von einem Stream verwendet werden. Wenn diese Methoden von Windows Media Player aufgerufen werden, wird ein Zeiger auf eine **DMO- \_ \_ Medientyp** Struktur bereitstellt. Wenn eine Methode wie z. b. " **stinputtype** " die Medientyp Informationen angibt, muss das Plug-in die **DMO- \_ \_ Medientyp** Struktur in eine Member-Variable kopieren und deren Datenmember überprüfen, um den Datentyp zu bestimmen, den Windows Media Player im Eingabepuffer bereitstellt. Wenn eine Methode, wie z. b. **getinputtype** , die Medientyp Informationen abruft, muss das Plug-in die Adresse der Element Variablen mit der Struktur des **DMO- \_ Medien \_ Typs** in den von Windows Media Player in der Parameterliste bereitgestellten Zeiger kopieren.

Windows Media Player verwendet hauptsächlich zwei Member der **DMO \_ - \_ Medientyp** Struktur:

-   **majortype**: eine Globally Unique Identifier (GUID), die die Gesamtkategorie der Medien angibt, z. b. Audiodaten oder Videos.
-   **Untertyp**: eine GUID, die eine ausführlichere Beschreibung der Medien angibt, z. b. PCM-Audiodaten.

Diese GUIDs befinden sich im Header "UUIDs. h", der in der Windows SDK enthalten ist.

Methoden wie z. b. **getinputsizeinfo** stellen Informationen für Windows Media Player bereit, wie viel Arbeitsspeicher zum Zuordnen der Verarbeitungs Puffer erforderlich ist. Methoden wie **getstreamcount** und **getoutputstreaminfo** stellen Windows-Media Player Informationen über die Anzahl und das Zeichen der Streams bereit, die vom DSP-Plug-in unterstützt werden.

" **Getinputmaxlatency** " und "* **tinputmaxlatency** " werden in besonderen Fällen von dmos implementiert. Windows Media Player DSP-Plug-Ins müssen E \_ notimpl zurückgeben.

## <a name="methods-that-specify-or-retrieve-state-information"></a>Methoden zum angeben oder Abrufen von Zustandsinformationen

Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um Werte im Zusammenhang mit dem aktuellen Status des Plug-ins zu erhalten oder festzulegen. Diese Methoden umfassen:

-   **Getinputcurrenttype**
-   **Getinputstatus**
-   **Getoutputcurrenttype**

**Getinputcurrenttype** und **getoutputcurrenttype** verwenden die **DMO \_ - \_ Medientyp** Struktur zum Zurückgeben von Informationen an Windows Media Player zu den zuvor festgelegten Medientypen für die Eingabe-und Ausgabestreams. **Getinputstatus** gibt ein Flag zurück, das Windows Media Player angibt, ob das DSP-Plug-in Eingabedaten akzeptieren kann.

## <a name="methods-that-handle-buffering-and-processing-data"></a>Methoden, die die Pufferung und Verarbeitung von Daten verarbeiten

Dies sind die Methoden, die von Windows Media Player aufgerufen werden, um die verschiedenen Prozesse zu initiieren, die das Plug-in für die digitale Signalverarbeitung durchführt. Diese Methoden umfassen:

-   **"" Zugeordnet**
-   **Diskontinuität**
-   **Leerung**
-   **Freestreamingresources**
-   **Sperre**
-   **ProcessInput**
-   **ProcessOutput**

In Windows Media Player werden **zuordungsoramingresources** und **freestreamingresources** aufgerufen, um dem DSP-Plug-in die Möglichkeit zu geben, zusätzliche Puffer einzurichten oder freizugeben, die das Plug-in möglicherweise für die interne Verarbeitung benötigt.

Windows Media Player DSP-Plug-Ins müssen die DMO- **Diskontinuitäts** Methode nicht verwenden.

Windows Media Player ruft **Flush** auf, um das DSP-Plug-in anzuweisen, alle intern gepufferten Daten zu leeren. Das Plug-in sollte alle Verweise auf **imediabuffer** -Schnittstellen freigeben, alle Werte, die den Zeitstempel oder die Stichproben Länge für den Medien Puffer angeben, löschen und alle internen Zustände erneut initialisieren, die vom Inhalt des Mediums "Sample" abhängen.

Windows Media Player ruft ProcessInput auf, um einen Zeiger auf eine **imediabuffer** -Schnittstelle an das DSP-Plug-in zu übergeben. Diese Schnittstelle ermöglicht den Zugriff auf den von Windows Media Player zugeordneten Eingabepuffer zum Bereitstellen von Daten für das Plug-in. Windows Media Player anschließend **ProcessOutput** aufrufen, um einen Zeiger auf eine **imediabuffer** -Schnittstelle zu übergeben, die Zugriff auf den von Windows Media Player zugeordneten Ausgabepuffer ermöglicht, um die verarbeiteten Daten aus dem DSP-Plug-in zu empfangen.

Die **imediaobject** -Schnittstelle enthält eine Methode mit dem Namen **Lock**. Diese Methode ist dafür konzipiert, eine Sperre für den DMO abzurufen oder freizugeben, damit DMO beim Ausführen mehrerer Vorgänge serialisiert wird. Die Version von **imediaobject:: Lock** im Assistenten Code überschreibt die ATL-Implementierung von **Lock**. Da Windows Media Player Aufrufe an die DMO-Schnittstelle eines DSP-Plug-ins serialisiert, gibt die Implementierung von **Lock** einfach S \_ OK zurück. Ausführliche Informationen zum Erstellen eines Multithread-DMO finden Sie im Abschnitt DirectShow des Windows SDK.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erforderliche Schnittstellen**](required-interfaces.md)
</dt> </dl>

 

 




