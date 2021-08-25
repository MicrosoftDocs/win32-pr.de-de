---
title: Erfahren Sie mehr über DirectShow in Windows Media Format 11 SDK, einer umfassenden, modularen, erweiterbaren Datenstreamingarchitektur für die Windows-Plattform.
description: Informationen zu DirectShow
ms.assetid: 1a0b68c7-9444-4389-8d81-dc734e95634d
keywords:
- Windows Medienformat-SDK, DirectShow
- Advanced Systems Format (ASF), DirectShow
- ASF (Advanced Systems Format), DirectShow
- DirectShow, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1aeb5dc9ebc613f7820a8ba4c4f5877ce9ac27068f1c4e873f9e8b00ec2f3b64
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119840410"
---
# <a name="about-directshow-windows-media-format-11-sdk"></a>Informationen zu DirectShow (Windows Media Format 11 SDK)

DirectShow ist eine umfassende, modulare, erweiterbare Datenstreamingarchitektur für die Windows-Plattform. Es stellt die zugrunde liegenden Softwarekomponenten und Anwendungsprogrammierschnittstellen (Application Programming Interfaces, APIs) für eine Vielzahl von digitalen Audio- und Videoanwendungen auf dem Markt bereit. DirectShow ist als Teil des Microsoft DirectX Software Development Kit verfügbar. Weitere Informationen zu DirectShow finden Sie im Microsoft Platform SDK.

In DirectShow werden alle Datenstreamingkomponenten als *Filter* bezeichnet. Ein Filter kann ein Hardwaregerät, einen Softwareencoder oder Decoder, einen Audio- oder Videorenderer oder eine beliebige Audiovideoverarbeitungsfunktion darstellen. Um DirectShow-basierten Anwendungen das Lesen und Schreiben Windows Medienformatinhalts zu ermöglichen, einschließlich inhalten, die durch Digital Rights Management (DRM) geschützt sind, stellt Microsoft zwei Filter bereit, die Teile des Windows Media Format SDK kapseln. Dies sind der [WM ASF Reader](wm-asf-reader-filter.md) und der [WM ASF Writer](wm-asf-writer-filter.md). Diese Filter und schnittstellen, die sie verfügbar machen, werden zusammen als QASF-Komponenten bezeichnet, nach der DLL, in der sie gepackt sind. (Das Q steht für "Wird", ein früher Codename für DirectShow.)

> [!Note]  
> Für die Verwendung der Codecs der Windows Media Audio- und Video 9-Serie über die DirectShow QASF-Komponenten ist Microsoft Windows Edition oder höher oder DirectX 8.0 oder höher erforderlich.

 

Das folgende Diagramm zeigt einen DirectShow-Filtergraphen zum Wiedergeben Windows Medienvideodateien.

![Videowiedergabediagramm für Windows-Medien](images/wmv-wmasfreader.png)

Der [WM ASF-Reader](wm-asf-reader-filter.md) ist eine QASF-Komponente, die Decoder sind Windows Media Format SDK-Komponenten, die im DMO Wrapperfilter (eine QASF-Komponente) gehostet werden, und die Renderer sind DirectShow-Komponenten.

 

 




