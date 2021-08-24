---
title: Schreiben von Streams mit nicht quadratischen Pixeln
description: Schreiben von Streams mit nicht quadratischen Pixeln
ms.assetid: 4af7dedc-e2b8-4dc2-add4-84424e93c297
keywords:
- Windows Medienformat-SDK, Schreiben von Videostreams
- Windows Medienformat-SDK, Videostreams
- Windows Medienformat-SDK, nicht quadratische Pixel
- Windows Medienformat-SDK, Pixel (nicht quadratisch)
- Advanced Systems Format (ASF), Schreiben von Videostreams
- ASF (Advanced Systems Format), Schreiben von Videostreams
- Advanced Systems Format (ASF), Videostreams
- ASF (Advanced Systems Format), Videostreams
- Advanced Systems Format (ASF), nicht quadratische Pixel
- ASF (Advanced Systems Format), nicht quadratische Pixel
- Advanced Systems Format (ASF), Pixel (nicht quadratisch)
- ASF (Advanced Systems Format), Pixel (nicht quadratisch)
- Schreiben von Videostreams
- Videostreams, Schreiben
- Videostreams, nicht quadratische Pixel
- Nicht quadratische Pixel
- Pixel (nicht quadratisch)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b44df1e4b4ce3f2bf2cb0e1d795b4caf396b6396e3e70b68b9040ad9a5456f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657950"
---
# <a name="writing-streams-with-non-square-pixels"></a>Schreiben von Streams mit nicht quadratischen Pixeln

Es gibt zwei Möglichkeiten, Videostreams mit nicht quadratischen Pixeln zu erstellen, die in Windows Media Player korrekt angezeigt werden. Die erste Technik umfasst das Festlegen von Attributen auf Streamebene im Dateiheader. Das zweite Verfahren umfasst das Hinzufügen einer Dateneinheitenerweiterung zu einem Datenstrom im Profil und das anschließende Festlegen eines Werts dafür in jedem geschriebenen Beispiel.

## <a name="to-use-stream-level-header-attributes-to-set-pixel-aspect-ratio"></a>So verwenden Sie Headerattribute auf Streamebene zum Festlegen des Pixel-Seitenverhältnisses

1.  Richten Sie das Writer-Objekt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)
2.  Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams. Weitere Informationen finden Sie unter [So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
3.  Rufen Sie [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)auf. (Rufen Sie diese Methode immer auf, bevor Sie Headerattribute festlegen.)
4.  Rufen Sie **QueryInterface** auf, um die [**IWMHeaderInfo3-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) abzurufen, und rufen [**Sie AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) zweimal auf, um [**AspectRatioX**](aspectratiox.md) und [**AspectRatioY**](aspectratioy.md) als Attribute auf Streamebene des Videostreams hinzuzufügen. Diese Attribute sind **DWORD-Werte.**
5.  Schreiben Sie die Datei.

## <a name="to-use-data-unit-extensions-to-set-pixel-aspect-ratio"></a>So verwenden Sie Dateneinheiterweiterungen zum Festlegen des Pixel-Seitenverhältnisses

**Vor dem Schreiben:**

1.  Richten Sie das Writer-Objekt ein. Weitere Informationen finden Sie unter [Schreiben von ASF-Dateien.](writing-asf-files.md)
2.  Erstellen oder laden Sie ein Profil mit einem oder mehreren Videostreams. Weitere Informationen finden Sie unter [So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md).
3.  Rufen Sie für jeden Stream (eines beliebigen Medientyps) im Profil [**IWMStreamConfig::SetStreamName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-setstreamname) auf, um einen eindeutigen Namen Ihrer Wahl anzugeben. Geben Sie nicht zwei Streams den gleichen Namen.
4.  Verwenden Sie [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) im Videostream, um eine Dateneinheiterweiterung für das Pixel-Seitenverhältnis hinzuzufügen.
5.  Rufen Sie [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile)auf.
6.  Schreiben Sie die Datei.

**Beim Schreiben:**

-   Rufen Sie für jedes Beispiel [**INSSBuffer3::SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) auf, und geben Sie die WM \_ SampleExtensionGUID \_ PixelAspectRatio-Eigenschaft zusammen mit dem richtigen Wert an. Seitenverhältniswerte werden als zwei verkettete zweistellige Werte geschrieben. Beispielsweise wird 16:9 als 1609 oder 0x0649 geschrieben. Dies ist immer ein 2-Byte-Wert.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**So lesen und schreiben Sie Video Streams mit nicht quadratischen Pixeln**](to-read-and-write-video-streams-with-non-square-pixels.md)
</dt> </dl>

 

 




