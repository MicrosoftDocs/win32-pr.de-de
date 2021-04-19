---
description: Verwenden der WDDM-Erfassung in DirectShow
ms.assetid: 57ee86b0-50bc-4992-94d4-f290f83d2afc
title: Verwenden der WDDM-Erfassung in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7926af70a3b7f1c4ba67c791d98c9928c3809b89
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360655"
---
# <a name="using-wddm-capture-in-directshow"></a>Verwenden der WDDM-Erfassung in DirectShow

Dieses Thema gilt für Windows Vista und höher.

Einige Videokarten verfügen über integrierte Funktionen für die Videoaufzeichnung. Auf diesen Karten werden erfasste Videorahmen in den Videospeicher (VRAM) eingefügt. Vor Windows Vista gab es keinen Standardmechanismus für die Verarbeitung der Frames, während Sie im VRAM verbleibt. Stattdessen mussten die Daten in den Systemspeicher kopiert, verarbeitet und dann zur Anzeige wieder in den VRAM kopiert werden. In Windows Vista unterstützt DirectShow nun einen Mechanismus, um die Video Frames im VRAM in der gesamten Verarbeitungs Pipeline zu halten, von der Erfassung bis zum anzeigen.

Der ksproxy-Filter bestimmt, ob der Treiber die VRAM-Oberflächen Erfassung unterstützt, indem er den Treiber für die bevorzugte ksproperty- \_ \_ Erfassungs \_ Oberflächen Eigenschaft abfragt. (Diese Eigenschaft ist in der Dokumentation zum Windows-Treiberkit dokumentiert.) Wenn der Treiber die VRAM-Oberflächen Erfassung unterstützt, ordnet ksproxy eine spezielle Art von Medien Beispiel zu, das einen Zeiger auf eine Direct3D-Oberfläche enthält.

Anschließend bestimmt ksproxy, ob der Downstream-Filter die DirectX-Video Beschleunigung (DXVA) 2,0 unterstützt, wie folgt:

1.  Ksproxy fragt die downstreameingabepin für die **IMF GetService** -Schnittstelle ab.
2.  Wenn die PIN " **IMF**" verfügbar macht, ruft "ksproxy" **IMF GetService:: GetService** für die **IDirect3DDeviceManager** -Schnittstelle auf. Der Dienst Bezeichner ist der Mr- \_ Video \_ Acceleration \_ Service.

Beide Schnittstellen sind in der Media Foundation SDK-Dokumentation dokumentiert.

Wenn der Downstream-Filter DXVA 2,0 nicht unterstützt, ordnet ksproxy einen zusätzlichen Systemspeicher Puffer zu. Dieser Puffer wird verwendet, um die Video Frames aus VRAM in den Systemspeicher zu kopieren. Die [**imediasample:: getpointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) -Methode des Medien Beispiels gibt einen Zeiger auf diesen Systemspeicher Puffer zurück.

Wenn der Downstream-Filter jedoch DXVA 2,0 unterstützt, weist ksproxy keinen Systemspeicher Puffer zu. In diesem Fall gibt die **getpointer** -Methode E \_ notimpl zurück. Stattdessen wird erwartet, dass der Downstream-Filter direkt auf die Direct3D-Oberfläche des Beispiels zugreift. Es gibt zwei Möglichkeiten für den downstreamfilter, einen Zeiger auf die-Oberfläche zu erhalten. beide sind gleichwertig:

-   Fragen Sie das Beispiel nach der **imfgetservice** -Schnittstelle ab, und nennen Sie **GetService** für die **IDirect3DSurface9** -Schnittstelle. Der Dienst Bezeichner ist der Mr- \_ Puffer \_ Dienst.
-   Fragen Sie das Beispiel nach der [**IMediaSample2Config**](/windows/desktop/api/Strmif/nn-strmif-imediasample2config) -Schnittstelle ab, und nennen Sie [**IMediaSample2Config:: getSurface**](/windows/desktop/api/Strmif/nf-strmif-imediasample2config-getsurface).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erweiterte Erfassungs Themen](advanced-capture-topics.md)
</dt> </dl>

 

 



