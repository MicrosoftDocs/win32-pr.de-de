---
title: Informationen zum Video Komprimierungs-Manager
description: Informationen zum Video Komprimierungs-Manager
ms.assetid: 2a5ebc95-3ee8-4145-b2c5-512d82e49c6d
keywords:
- Windows-Multimedia, Video Komprimierungs-Manager (VCM)
- Multimedia, Video Komprimierungs-Manager (VCM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6841446a5a0f22b8c05c2419448e65b035f90703
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472948"
---
# <a name="about-the-video-compression-manager"></a>Informationen zum Video Komprimierungs-Manager

Normalerweise arbeiten installierbare Kompressoren mit Video Bilddaten, die in überlappenden Audiodateien (AVI) gespeichert sind. In dieser Übersicht werden die Programmiertechniken erläutert, die für den Zugriff auf installierbare Kompressoren über VCM verwendet werden, und die folgenden Themen behandelt

-   VCM und das Video für die Windows-Architektur
-   Komprimieren und abkomprimieren von Bilddaten aus Ihrer Anwendung
-   Verwenden von VCM-renderatoren zum Zeichnen von Daten aus Ihrer Anwendung
-   VCM-Funktionen und-Strukturen

Bevor Sie diese Übersicht lesen, sollten Sie mit den Microsoft Win32-Grafik Diensten vertraut sein. Insbesondere Bitmaps-und [**bitmapbezogene**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) Strukturen, wie z. b. BitmapInfo und [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader), werden ausgiebig von VCM verwendet. Weitere Informationen zu den **BitmapInfo** -und **BITMAPINFOHEADER** -Strukturen finden Sie unter [Bitmaps](/previous-versions//ms532349(v=vs.85)).

> [!Note]  
> Der Audiokomprimierungs-Manager (ACM) bietet Unterstützung für Audiokomprimierungs-und dekomprimierungstreiber auf Systemebene. Eine Beschreibung der Audiokomprimierungs Dienste finden Sie unter [Audiokomprimierungs-Manager](audio-compression-manager.md).

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Videokomprimierungs-Manager](video-compression-manager.md)
</dt> </dl>

 

 