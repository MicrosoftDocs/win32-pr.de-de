---
title: DirectShow-und Windows-Medien
description: DirectShow-und Windows-Medien
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd4ca8eb4b1051d6685efa0bf73052ad9e7b31fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714214"
---
# <a name="directshow-and-windows-media"></a>DirectShow-und Windows-Medien

Anstatt das Windows Media SDK exklusiv zu verwenden, können Anwendungen auch Windows Media-basierte Inhalte mithilfe der Microsoft® DirectShow® Streaming-Architektur lesen und schreiben, wie in den folgenden Abschnitten beschrieben.



| `Section`                                                                                   | BESCHREIBUNG                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu DirectShow](about-directshow.md)                                                  | Beschreibt DirectShow in allgemeinen Begriffen und gibt Aufschluss darüber, wo Sie weitere Informationen erhalten.                                                     |
| [Gründe für die Verwendung von DirectShow](why-use-directshow.md)                                             | Beschreibt, wie DirectShow bestimmte Aufgaben beim Erstellen und Wiedergeben von Windows Media – basierten Inhalten vereinfacht.                              |
| [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)                    | Beschreibt die Wiedergabe von ASF-Dateien mithilfe von DirectShow.                                                                                           |
| [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)                  | Beschreibt das Erstellen von ASF-Dateien mithilfe von DirectShow.                                                                                         |
| [WMT- \_ Status Ereignis Benachrichtigung in DirectShow](wmt-status-notification-in-directshow.md) | Beschreibt, welche **WMT- \_ Status** Ereignisse von den "ASF Reader"-und "ASF Writer"-Filtern behandelt werden und wie Anwendungen diese Ereignisse empfangen können. |
| [DRM-Unterstützung in DirectShow](drm-support-in-directshow.md)                                | Beschreibt das Lesen und Schreiben von DRM-geschützten Dateien über DirectShow.                                                                     |
| [DirectShow-qasf-Referenz](directshow-qasf-reference.md)                                | Enthält die Referenz Dokumentation für die DirectShow-Komponenten, die Windows-Medien unterstützen.                                              |



 

Drei Beispielanwendungen im SDK veranschaulichen die Verwendung von DirectShow: dscopy, dsplay und dsseekfm. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

> [!Note]  
> Anwendungen, die die in diesem SDK enthaltenen qasf-Komponenten verwenden, erfordern, dass die SDK-Laufzeit von Microsoft DirectX® 8,1 oder höher unter Windows® 2000, Windows 98 und Windows 95 Systems installiert wird. Diese Laufzeit ist insbesondere für den DMO-Wrapper Filter erforderlich, der die Windows Media-Codecs in einem DirectShow-Filter Diagramm hostet.

 

 

 




