---
title: Informationen zum Videokomprimierungs-Manager
description: Informationen zum Videokomprimierungs-Manager
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows Multimedia, Videokomprimierungs-Manager (VCM)
- Multimedia, Videokomprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 122114666713b3bf5d1e706db2206a3d4894f8a40dea94d33d3b12829fb02bfd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808720"
---
# <a name="about-the-video-compression-manager"></a>Informationen zum Videokomprimierungs-Manager

In der Regel arbeiten installierbare Komprimierungen mit Videobilddaten, die in A3D-Dateien (Audio Video Interleaved) gespeichert sind. In dieser Übersicht werden die Programmiertechniken erläutert, die für den Zugriff auf installierbare Installationsmethoden über VCM verwendet werden, und es werden die folgenden Themen behandelt:

-   VCM und das Video für Windows Architektur
-   Komprimieren und Dekomprimieren von Bilddaten aus Ihrer Anwendung
-   Verwenden von VCM-Renderern zum Zeichnen von Daten aus Ihrer Anwendung
-   VCM-Funktionen und -Strukturen

Bevor Sie diese Übersicht lesen, sollten Sie mit den Microsoft Win32-Grafikdiensten vertraut sein. Insbesondere Bitmaps und bitmapbezogene Strukturen wie [**BITMAPINFO**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) und [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)werden von VCM umfassend verwendet. Weitere Informationen zu den **BitmapINFO-** und **BITMAPINFOHEADER-Strukturen** finden Sie unter [Bitmaps](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> Der Audiokomprimierungs-Manager (ACM) bietet Unterstützung auf Systemebene für Audiokomprimierungs- und Dekomprimierungstreiber. Eine Beschreibung der Audiokomprimierungsdienste finden Sie unter [Audiokomprimierungs-Manager](audio-compression-manager.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> </dl>

 

 