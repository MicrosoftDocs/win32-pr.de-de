---
title: DirectShow und Windows Medien
description: DirectShow und Windows Medien
ms.assetid: e2ddc781-9f56-4f77-a191-015018755eff
keywords:
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b975347d26414dda0c1f54c0b71ac852541bd58c314e3724725c3768ddfc7bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119027908"
---
# <a name="directshow-and-windows-media"></a>DirectShow und Windows Medien

Als Alternative zur ausschließlichen Verwendung des Windows Media Format SDK können Anwendungen auch medienbasierte Inhalte Windows mithilfe der Streamingarchitektur Microsoft® DirectShow® lesen und schreiben, wie in den folgenden Abschnitten beschrieben.



| `Section`                                                                                   | BESCHREIBUNG                                                                                                                                 |
|-------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu DirectShow](about-directshow.md)                                                  | Beschreibt DirectShow allgemein und informiert darüber, wo Weitere Informationen dazu zu erhalten sind.                                                     |
| [Gründe für die Verwendung von DirectShow](why-use-directshow.md)                                             | Beschreibt, wie DirectShow bestimmte Aufgaben bei der Erstellung und Wiedergabe Windows medienbasierten Inhalten vereinfacht.                              |
| [Lesen von ASF-Dateien in DirectShow](reading-asf-files-in-directshow.md)                    | Beschreibt die Wiedergabe von ASF-Dateien mit DirectShow.                                                                                           |
| [Erstellen von ASF-Dateien in DirectShow](creating-asf-files-in-directshow.md)                  | Beschreibt, wie ASF-Dateien mit DirectShow erstellt werden.                                                                                         |
| [WMT \_ STATUS-Ereignisbenachrichtigung in DirectShow](wmt-status-notification-in-directshow.md) | Beschreibt, **welche WMT \_ STATUS-Ereignisse** von den FILTERN ASF-Reader und ASF Writer verarbeitet werden und wie Anwendungen diese Ereignisse empfangen können. |
| [DRM-Unterstützung in DirectShow](drm-support-in-directshow.md)                                | Beschreibt, wie DRM-geschützte Dateien über DirectShow gelesen und geschrieben werden.                                                                     |
| [DirectShow QASF-Referenz](directshow-qasf-reference.md)                                | Enthält die Referenzdokumentation für die DirectShow-Komponenten, die Windows unterstützen.                                              |



 

Drei Beispielanwendungen im SDK veranschaulichen die Verwendung von DirectShow: DSCopy, DSPlay und DSSeekFM. Weitere Informationen finden Sie unter [Beispielanwendungen](sample-applications.md).

> [!Note]  
> Für Anwendungen, die die in diesem SDK enthaltenen QASF-Komponenten verwenden, muss die Microsoft DirectX® 8.1- oder höher SDK-Runtime auf den Systemen Windows® 2000, Windows 98 und Windows 95 installiert werden. Diese Laufzeit ist insbesondere für den DMO Wrapper-Filter erforderlich, der die Windows Mediencodecs in einem DirectShow-Filterdiagramm hostet.

 

 

 




