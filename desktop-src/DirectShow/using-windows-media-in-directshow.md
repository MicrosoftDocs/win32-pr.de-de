---
description: Verwenden von Windows Medien in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Verwenden von Windows Medien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fea308943d4be732c75e774d3e0c3cb09ac7c6609a8399d2e6eca4666d99e6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651086"
---
# <a name="using-windows-media-in-directshow"></a>Verwenden von Windows Medien in DirectShow

In diesem Abschnitt wird beschrieben, wie DirectShow zum Wiedergeben und Schreiben von ASF-Dateien (Advanced Systems Format) verwendet wird. ASF-Dateien enthalten in der Regel Audio- und Videoinhalte, die mit dem Windows Medienaudio- und Videocodecs codiert wurden. ASF kann jedoch einen beliebigen Datentyp enthalten.

Die folgenden DirectShow-Filter unterstützen das Lesen und Schreiben von ASF-Dateien:

-   [WM ASF-Leserfilter](wm-asf-reader-filter.md). Liest ASF-Dateien.
-   [WM ASF Writer Filter](wm-asf-writer-filter.md). Wrties ASF-Dateien.
-   [DMO Wrapperfilter .](dmo-wrapper-filter.md) Umschließt die Windows Media Encoder- und Decoder-DMOs.

### <a name="versions"></a>Versionen

Die WM ASF-Reader- und WM ASF Writer-Filter werden in der DLL mit dem Namen qasf.dll gepackt, und die Filter werden zusammen als "QASF-Komponenten" bezeichnet. Diese Filter sind Wrapper für das Windows Media Format SDK. Die DLL (qasf.dll) wurde zuerst im DirectX SDK veröffentlicht, aber später im Windows Media Format SDK aktualisiert. Hier ist der Versionsverlauf der QASF-Filter:

-   DirectShow 8.1 unterstützt Windows Media Format SDK Version 7.0.
-   DirectShow 9.0 unterstützt Windows Media Format SDK Version 7.1.
-   Windows XP Service Pack 2 unterstützt Windows Media Format 9 SDK.
-   Windows Vista unterstützt Windows Media Format 11 SDK.
-   Windows Media Format 9 SDK und höher enthalten entsprechende Versionen von QASF.

Um die neueste Version von QASF zu erhalten, laden Sie immer das neueste Windows Media Format SDK herunter.

### <a name="legacy-windows-media-source-filter"></a>Legacy-Windows Medienquellenfilter

In Windows XP Service Pack 1 und früher ist der Standardquellfilter für ASF-Dateien (ASF-, WMV- und WMA-Dateierweiterungen) der veraltete [Windows Medienquellenfilter.](windows-media-source-filter.md) Dieses Verhalten wurde beibehalten, um Abwärtskompatibilität mit Anwendungen sicherzustellen, die die Windows Media Player 6.4 verwendet haben. Neue Anwendungen sollten die neueren Versionen von QASF verwenden, wodurch der WM-ASF-Reader als Standardfilter für die Wiedergabe von ASF-Dateien festgelegt wird.

Weitere Informationen zur Windows Media Suite von Software Development Kits finden Sie im Abschnitt [Audio und Video](../audio-and-video.md) der MDSN-Bibliothek.

Dieser Artikel enthält folgende Themen:

-   [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
-   [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 
