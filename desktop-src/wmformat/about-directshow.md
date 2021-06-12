---
title: Erfahren Sie mehr über DirectShow im Windows Media Format 11 SDK, einer modularen, erweiterbaren Datenstreamingarchitektur auf hoher Ebene für die Windows-Plattform.
description: Informationen zu DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media Format SDK, DirectShow
- Advanced Systems Format (ASF),DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow,About
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a76d7c8971c452f01176be7472e313181eb2831
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011293"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informationen zu DirectShow (Windows Media Format 11 SDK)

DirectShow ist eine umfassende, modulare, erweiterbare Datenstreamingarchitektur für die Windows-Plattform. Es stellt die zugrunde liegenden Softwarekomponenten und Anwendungsprogrammierschnittstellen (APPLICATION Programming Interfaces, APIs) für eine Vielzahl von digitalen Audio- und Videoanwendungen bereit, die heute auf dem Markt verfügbar sind. DirectShow ist als Teil des Microsoft DirectX Software Development Kit verfügbar. Weitere Informationen zu DirectShow finden Sie im Microsoft Platform SDK.

In DirectShow werden alle Datenstreamingkomponenten als Filter *bezeichnet.* Ein Filter kann ein Hardwaregerät, einen Softwareencoder oder -decoder, einen Audio- oder Videorenderer oder eine beliebige Audiovideoverarbeitungsfunktion darstellen. Damit DirectShow-basierte Anwendungen Inhalte im Windows Media Format lesen und schreiben können, einschließlich von Digital Rights Management (DRM) geschützter Inhalte, stellt Microsoft zwei Filter bereit, die Teile des Windows Media Format SDK kapseln. Dies sind [der WM ASF-Reader](wm-asf-reader-filter.md) und der [WM ASF Writer.](wm-asf-writer-filter.md) Diese Filter und die schnittstellen, die sie verfügbar machen, werden zusammen als QASF-Komponenten nach der DLL bezeichnet, in der sie gepackt sind. (Das Q steht für "Party", ein früher Codename für DirectShow.)

> [!Note]  
> Die Verwendung der Codecs der Windows Media Audio- und Video 9-Serie über die DirectShow QASF-Komponenten erfordert Microsoft Windows Edition Edition oder höher oder DirectX 8.0 oder höher.

 

Das folgende Diagramm zeigt ein DirectShow-Filterdiagramm für die Wiedergabe Windows Media Video Dateien.

![Wiedergabediagramm für Windows-Medienvideos](images/wmv-wmasfreader.png)

Der [WM ASF-Reader](wm-asf-reader-filter.md) ist eine QASF-Komponente, die Decoder sind Windows Media Format SDK-Komponenten, die im DMO-Wrapperfilter (eine QASF-Komponente) gehostet werden, und die Renderer sind DirectShow-Komponenten.

 

 




