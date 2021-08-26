---
description: Verwenden von WDDM Capture in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Verwenden von WDDM Capture in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e0a442c6929ef2435b05268035bb0b39b196a958440cd7ce5cfe44ea4b4c55
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903590"
---
# <a name="using-wddm-capture-in-directshow"></a>Verwenden von WDDM Capture in DirectShow

Dieses Thema gilt für Windows Vista und höher.

Einige Grafikkarten verfügen über integrierte Videoaufnahmefunktionen. Auf diesen Karten werden erfasste Videoframes im Videospeicher (VRAM) platziert. Vor der Windows Vista gab es keinen Standardmechanismus für die Verarbeitung der Frames, während sie in VRAM waren. Stattdessen mussten die Daten in den Systemspeicher kopiert, verarbeitet und dann zur Anzeige wieder in VRAM kopiert werden. In Windows Vista unterstützt DirectShow jetzt einen Mechanismus, um die Videoframes in VRAM in der gesamten Verarbeitungspipeline von der Erfassung bis zur Anzeige zu halten.

Der KsProxy-Filter bestimmt, ob der Treiber die VRAM-Oberflächenerfassung unterstützt, indem er den Treiber nach der KSPROPERTY \_ PREFERRED \_ CAPTURE \_ SURFACE-Eigenschaft abfragt. (Diese Eigenschaft ist in der Dokumentation zum Windows Driver Kit dokumentiert.) Wenn der Treiber die VRAM-Oberflächenerfassung unterstützt, ordnet KsProxy eine besondere Art von Medienbeispiel zu, das einen Zeiger auf eine Direct3D-Oberfläche enthält.

Als Nächstes bestimmt KsProxy wie folgt, ob der Downstreamfilter DirectX Video Acceleration (DXVA) 2.0 unterstützt:

1.  KsProxy fragt den Downstream-Eingabepin für die **BERGETService-Schnittstelle** ab.
2.  Wenn die **Stecknadel DENTGETService** verfügbar macht, ruft KsProxy FÜR die **IDirect3DDeviceManager-Schnittstelle** **DENKGetService::GetService** auf. Der Dienstidentifizierte ist MR \_ VIDEO \_ ACCELERATION \_ SERVICE.

Beide Schnittstellen sind in der Dokumentation zum Media Foundation SDK dokumentiert.

Wenn der Downstreamfilter DXVA 2.0 nicht unterstützt, weist KsProxy einen zusätzlichen Systemspeicherpuffer zu. Dieser Puffer wird verwendet, um die Videoframes aus VRAM in den Systemspeicher zu kopieren. Die [**IMediaSample::GetPointer-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) des Medienbeispiels gibt einen Zeiger auf diesen Systemspeicherpuffer zurück.

Wenn der Downstreamfilter jedoch DXVA 2.0 unterstützt, weist KsProxy keinen Systemspeicherpuffer zu. In diesem Fall gibt die **GetPointer-Methode** E \_ NOTIMPL zurück. Stattdessen wird erwartet, dass der Downstreamfilter direkt auf die Direct3D-Oberfläche des Beispiels zutritt. Es gibt zwei Möglichkeiten für den Downstreamfilter, einen Zeiger auf die Oberfläche zu erhalten, die beide gleichwertig sind:

-   Fragen Sie das Beispiel für die **BENUTZEROBERFLÄCHEGetService-Schnittstelle** ab, und rufen **Sie GetService für** die **IDirect3DSurface9-Schnittstelle** auf. Der Dienstbezeichner ist MR \_ BUFFER \_ SERVICE.
-   Fragen Sie das Beispiel für die [**IMediaSample2Config-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) ab, und rufen [**Sie IMediaSample2Config::GetSurface auf.**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungsthemen](advanced-capture-topics.md)
</dt> </dl>

 

 



