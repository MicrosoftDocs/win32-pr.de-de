---
title: Schreiben von Streams mit nicht quadratischen Pixeln
description: Schreiben von Streams mit nicht quadratischen Pixeln
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Media-Format-SDK, Schreiben von Videostreams
- Windows Media-Format-SDK, Videostreams
- Windows Media-Format-SDK, nicht eckige Pixel
- Windows Media-Format-SDK, Pixel (ohne Quadrat)
- Advanced Systems Format (ASF), Schreiben von Videostreams
- ASF (Advanced Systems Format), Schreiben von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht eckige Pixel
- Advanced Systems Format (ASF), Pixel (ohne Quadrat)
- ASF (Advanced Systems Format), Pixel (ohne Quadrat)
- Schreiben von Videostreams
- Videostreams, schreiben
- Videostreams, nicht quadratische Pixel
- nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1349840f151ab787ba0e0512cfab8fea08aacf1
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038549"
---
# <a name="writing-streams-with-non-square-pixels"></a>Schreiben von Streams mit nicht quadratischen Pixeln

Es gibt zwei Möglichkeiten, Videostreams mit nicht quadratischen Pixeln zu erstellen, die in Windows-Media Player ordnungsgemäß angezeigt werden. Das erste Verfahren umfasst das Festlegen von Attributen auf Streamebene im Dateiheader. Das zweite Verfahren umfasst das Hinzufügen einer Dateneinheiten Erweiterung zu einem Stream im Profil und das anschließende Festlegen eines Werts für die Erweiterung in jedem geschriebenen Beispiel.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>So verwenden Sie Header Attribute auf Streamebene zum Festlegen des Pixel Seitenverhältnisses

1.  Richten Sie das Writer-Objekt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).
2.  Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams. Weitere Informationen finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
3.  Nennen Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile). (Diese Methode wird immer aufgerufen, bevor Header Attribute festgelegt werden.)
4.  Rufen Sie **QueryInterface** auf, um die [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle zu erhalten, und rufen Sie [**AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) zweimal auf, um [**aspectratiox**](aspectratiox.md) und [**aspectratioy**](aspectratioy.md) als Attribute auf Streamebene des Videodaten Stroms hinzuzufügen. Diese Attribute sind **DWORD** -Werte.
5.  Schreiben Sie die Datei.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>So verwenden Sie Dateneinheiten Erweiterungen zum Festlegen des Pixel Seitenverhältnisses

**Vor dem Schreiben:**

1.  Richten Sie das Writer-Objekt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien](writing-asf-files.md).
2.  Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams. Weitere Informationen finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
3.  Nennen Sie für jeden Stream (eines beliebigen Medientyps) im Profil [**iwmstreamconfig:: setstreamname**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) , um einen eindeutigen Namen Ihrer Wahl anzugeben. Weisen Sie zwei Streams nicht denselben Namen zu.
4.  Verwenden Sie [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) im Videostream, um eine dateneinheits Erweiterung für das Pixel Seitenverhältnis hinzuzufügen.
5.  Nennen Sie [**iwmwriter:: setprofile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile).
6.  Schreiben Sie die Datei.

**Beim Schreiben:**

-   Geben Sie für jedes Beispiel [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) an, und geben Sie die WM \_ sampleextensionguid \_ pixelaspectratio-Eigenschaft zusammen mit dem korrekten Wert an. Seitenverhältnis Werte werden als zwei verketteten zweistelligen Wert geschrieben. Beispielsweise wird 16:9 als 1609 oder 0x0649 geschrieben. Dabei handelt es sich immer um einen 2-Byte-Wert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**So lesen und schreiben Sie Videostreams mit nicht quadratischen Pixeln**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




