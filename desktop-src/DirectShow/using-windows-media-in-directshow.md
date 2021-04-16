---
description: Verwenden von Windows-Medien in DirectShow
ms.assetid: 2fae0504-d1da-413a-80dd-de7818f506ef
title: Verwenden von Windows-Medien in DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e73726f0d7251f1c19beee05cfd8f335d3fdd7a
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "104393858"
---
# <a name="using-windows-media-in-directshow"></a>Verwenden von Windows-Medien in DirectShow

In diesem Abschnitt wird beschrieben, wie Sie mit DirectShow-Dateien (Advanced Systems Format) wiedergeben und schreiben. ASF-Dateien enthalten häufig Audioinhalte und Videoinhalte, die mit den Windows Media Audio-und Video Codecs codiert sind. Allerdings kann ASF beliebige Datentypen enthalten.

Die folgenden DirectShow-Filter unterstützen das Lesen und Schreiben von ASF-Dateien:

-   [WM-ASF-Lesefilter](wm-asf-reader-filter.md). Liest ASF-Dateien.
-   [WM-ASF-Writer-Filter](wm-asf-writer-filter.md). Wrties von ASF-Dateien.
-   [DMO-Wrapper Filter](dmo-wrapper-filter.md). Umschließt den Windows Media Encoder und Decoder-DMOS.

### <a name="versions"></a>Versionen

Die Filter "WM ASF Reader" und "WM ASF Writer" sind in der DLL mit dem Namen "qasf.dll" verpackt, und die Filter werden zusammen mit dem Namen "qasf Components Diese Filter sind Wrapper für das Windows Media-Format-SDK. Die dll (qasf.dll) wurde zuerst im DirectX SDK veröffentlicht, aber später im Windows Media-Format SDK aktualisiert. Im folgenden finden Sie den Versionsverlauf der qasf-Filter:

-   DirectShow 8,1 unterstützt das Windows Media-Format SDK Version 7,0.
-   DirectShow 9,0 unterstützt das Windows Media-Format SDK Version 7,1.
-   Windows XP Service Pack 2 unterstützt das SDK für Windows Media-Format 9.
-   Windows Vista unterstützt das SDK für Windows Media-Format 11.
-   Das Windows Media-Format 9 SDK und höher enthalten entsprechende Versionen von qasf.

Um die neueste Version von qasf zu erhalten, laden Sie immer das neueste SDK für den Windows Media-Format herunter.

### <a name="legacy-windows-media-source-filter"></a>Windows Media-Quell Filter (Legacy)

In Windows XP Service Pack 1 und früher ist der Standard Quell Filter für ASF-Dateien (. ASF-, WMV-und. WMA-Dateierweiterungen) der veraltete [Windows Media-Quell Filter](windows-media-source-filter.md). Dieses Verhalten wurde beibehalten, um die Abwärtskompatibilität mit Anwendungen sicherzustellen, die Windows Media Player 6,4 verwendet haben. Neue Anwendungen sollten die neueren Versionen von qasf verwenden, sodass der WM-ASF-Reader den Standardfilter für die Wiedergabe von ASF-Dateien filtert.

Weitere Informationen zur Windows Media Suite von Software Development Kits finden Sie im Abschnitt " [Audiodateien und Video](../audio-and-video.md) " der MDSN-Bibliothek.

Dieser Artikel enthält folgende Themen:

-   [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)
-   [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von DirectShow](using-directshow.md)
</dt> </dl>

 

 
