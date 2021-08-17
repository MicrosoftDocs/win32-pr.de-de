---
title: DRM-Unterstützung in DirectShow
description: DRM-Unterstützung in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Medienformat-SDK, DRM-Unterstützung in DirectShow
- Windows Medienformat-SDK, DirectShow
- Windows Medienformat-SDK, Digital Rights Management (DRM)
- Advanced Systems Format (ASF), DRM-Unterstützung in DirectShow
- ASF (Advanced Systems Format), DRM-Unterstützung in DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- DirectShow,DRM-Unterstützung
- Digital Rights Management (DRM), DirectShow
- DRM (Verwaltung digitaler Rechte),DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4b3de3ca80d1b3b2fe27c9af590fe0cba0202b1fdd9b6fc322d8ed1c1871536
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930880"
---
# <a name="drm-support-in-directshow"></a>DRM-Unterstützung in DirectShow

Das Lesen und Schreiben von DRM-geschützten Dateien in DirectShow erfolgt im Grunde auf die gleiche Weise wie bei der direkten Verwendung des Windows Media Format SDK. Zunächst benötigen Sie die statische wmstubdrm-Bibliothek, die separat von Microsoft abgerufen wird. Darüber hinaus müssen Sie die **IKeyProvider-Schnittstelle** implementieren, damit Ihre Anwendung auf die Laufzeitobjekte Windows Media Format SDK zugreifen kann, wenn DRM aktiviert ist.

Verwenden Sie beim Anwenden des DRM-Schutzes der Version 1 die [**IWMHeaderInfo-Schnittstelle,**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) die wie unter [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)beschrieben abgerufen wird. Rufen Sie beim Anwenden des DRM-7-Schutzes die [**IWMDRMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) ab, indem Sie **QueryService** für den [WM ASF Writer-Filter](wm-asf-writer-filter.md) aufrufen, wie im Codeausschnitt weiter unten in diesem Thema gezeigt.

Alle anderen DRM-spezifischen Konfigurationen sind identisch mit der Beschreibung unter [Aktivieren der DRM-Unterstützung.](enabling-drm-support.md) Verwenden Sie **QueryService,** um die [**IWMDRMReader-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) aus dem [WM ASF-Readerfilter](wm-asf-reader-filter.md) abzurufen.

DirectX 9.0 enthält ein Beispiel, PlayWndASF, eine DRM-fähige DirectShow-Playeranwendung, die den Erwerb von DRM-Lizenzen der Version 1 und Version 7 veranschaulicht. Dieses Beispiel enthält auch eine Implementierung der **CKeyProvider-Klasse,** die die **IKeyProvider-Schnittstelle** unterstützt.

 

 




