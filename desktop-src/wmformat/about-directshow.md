---
title: Informationen zu DirectShow (Windows Media-Format 11 SDK)
description: Informationen zu DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Media-Format-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd77507643edb220bc71a029779c88fe56760eae
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039989"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informationen zu DirectShow (Windows Media-Format 11 SDK)

DirectShow ist eine hochstufige, modulare, erweiterbare datenstreamingarchitektur für die Windows-Plattform. Es bietet die zugrunde liegenden Softwarekomponenten und APIs (Application Programming Interfaces) für eine Vielzahl digitaler Audio-und Videoanwendungen auf dem Markt heute. DirectShow ist als Teil des Microsoft DirectX Software Development Kit verfügbar. Weitere Informationen zu DirectShow finden Sie im Microsoft Platform SDK.

In DirectShow werden alle datenstreamingkomponenten als *Filter* bezeichnet. Ein Filter kann ein Hardware Gerät, einen Software Encoder oder-Decoder, einen Audio-oder Videorenderer oder eine beliebige Audiovideo-Verarbeitungs Funktion darstellen. Zum Aktivieren von DirectShow – basierten Anwendungen zum Lesen und Schreiben von Inhalten im Windows Media-Format, einschließlich von Digital Rights Management (DRM) geschütztes Inhalt, stellt Microsoft zwei Filter bereit, die Teile des SDK des Windows Media-Formats Kapseln. Dies sind der [WM-ASF-Reader](wm-asf-reader-filter.md) und der [WM-ASF-Writer](wm-asf-writer-filter.md). Diese Filter und die Schnittstellen, die Sie verfügbar machen, werden zusammen mit der dll, in der Sie verpackt sind, als qasf-Komponenten bezeichnet. (Q steht für Quartz, einen frühen Codenamen für DirectShow.)

> [!Note]  
> Die Verwendung der Codecs für die Windows Media Audio-und Video 9-Serie über die DirectShow-qasf-Komponenten erfordert Microsoft Windows Millennium Edition oder höher oder DirectX 8,0 oder höher.

 

Das folgende Diagramm zeigt ein DirectShow-Filter Diagramm für die Wiedergabe Windows Media Video Dateien.

![Grafik zur Windows Media-Videowiedergabe](images/wmv-wmasfreader.png)

Der [WM-ASF-Reader](wm-asf-reader-filter.md) ist eine qasf-Komponente, bei den Decodern handelt es sich um Windows Media-SDK-Komponenten, die im DMO-Wrapper Filter (einer qasf-Komponente) gehostet werden, und die Renderer sind DirectShow-Komponenten.

 

 




