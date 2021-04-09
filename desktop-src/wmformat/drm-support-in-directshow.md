---
title: DRM-Unterstützung in DirectShow
description: DRM-Unterstützung in DirectShow
ms.assetid: f464d4a4-3478-489a-b9ce-8ab1acabc3c8
keywords:
- Windows Media-Format-SDK, DRM-Unterstützung in DirectShow
- Windows Media-Format-SDK, DirectShow
- Windows Media-Format-SDK, Digital Rights Management (DRM)
- Advanced Systems Format (ASF), DRM-Unterstützung in DirectShow
- ASF (Advanced Systems Format), DRM-Unterstützung in DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- Advanced Systems Format (ASF), Digital Rights Management (DRM)
- ASF (Advanced Systems Format), Digital Rights Management (DRM)
- DirectShow, DRM-Unterstützung
- Digital Rights Management (DRM), DirectShow
- DRM (Digital Rights Management), DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85a211a3d3b438bac246c0bd90759f648818ac2e
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "103948421"
---
# <a name="drm-support-in-directshow"></a>DRM-Unterstützung in DirectShow

Das Lesen und Schreiben von DRM-geschützten Dateien in DirectShow erfolgt im Grunde auf die gleiche Weise wie bei der direkten Verwendung des Windows Media SDK-SDKs. Zunächst benötigen Sie die statische wmstubdrm-Bibliothek, die separat von Microsoft abgerufen wird. Außerdem müssen Sie die **ikeyprovider** -Schnittstelle implementieren, damit Ihre Anwendung auf die Lauf Zeit Objekte des Windows Media-Formats zugreifen kann, wenn DRM aktiviert ist.

Verwenden Sie beim Anwenden von DRM-Version 1-Schutz die [**iwmheaderinfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) -Schnittstelle, die wie unter [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)beschrieben abgerufen wird. Wenn Sie den DRM-Schutz der Version 7 anwenden, rufen Sie die [**iwmdrmwriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) -Schnittstelle ab, indem Sie **QueryService** für den [WM-ASF-Writer](wm-asf-writer-filter.md) -Filter aufrufen, wie im Code Ausschnitt weiter unten in diesem Thema gezeigt.

Alle anderen DRM-spezifischen Konfigurationen sind exakt identisch mit der Beschreibung [unter Aktivieren der DRM-Unterstützung](enabling-drm-support.md). Verwenden Sie **QueryService** , um die [**iwmdrmreader**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader) -Schnittstelle aus dem [WM-ASF-Reader](wm-asf-reader-filter.md) -Filter abzurufen.

DirectX 9,0 enthält ein Beispiel: playwndasf, eine DRM-fähige DirectShow Player-Anwendung, die DRM-Version 1 und den Lizenzerwerb von Version 7 veranschaulicht. Dieses Beispiel enthält auch eine Implementierung der **ckeyprovider** -Klasse, die die **ikeyprovider** -Schnittstelle unterstützt.

 

 




