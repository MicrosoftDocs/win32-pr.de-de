---
title: Arbeiten mit komprimierten Videodaten in einem Stream
description: Arbeiten mit komprimierten Videodaten in einem Stream
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7c09de239fa28f3d9739dafc953ce10c2a6f1d69c0c607aeb03bc388a0f3003
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118622090"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Arbeiten mit komprimierten Videodaten in einem Stream

AVIFile bietet mehrere Möglichkeiten für den Zugriff auf komprimierte Videostreams.

Wenn Sie einen oder mehrere Frames eines komprimierten Videostreams anzeigen möchten, können Sie die Frames mithilfe der [**AVIStreamRead-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) abrufen und die komprimierten Framedaten an DrawDib-Funktionen weiterleiten, um sie anzuzeigen. DrawDib-Funktionen können Bilder mit mehreren Bildtiefe anzeigen und automatisch Bilder für Anzeigen dithern, die bestimmte Arten von geräteunabhängigen Bitmaps (DIBs) nicht verarbeiten können. Diese Funktionen funktionieren mit unkomprimierten und komprimierten Bildern. Weitere Informationen zu DrawDib-Funktionen finden Sie unter [DrawDib-Funktionen.](drawdib-functions.md)

AVIFile bietet Funktionen zum Dekomprimieren eines einzelnen Videoframes. Verwenden Sie zum Zuordnen von Ressourcen die [**FUNKTION AVIStreamGetFrameOpen.**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) Diese Funktion erstellt einen Puffer für die dekomprimierten Daten.

Sie können einen einzelnen Videoframe mithilfe der [**AVIStreamGetFrame-Funktion**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) dekomprimieren. Diese Funktion dekomprimiert den Frame und ruft einen vollständigen Frame von Bilddaten ab und gibt die Adresse des DIB in der [BITMAPINFOHEADER-Struktur](/previous-versions//ms532290(v=vs.85)) zurück. Ihre Anwendung kann das DIB mithilfe von Standardzeichnungsfunktionen oder mithilfe der DrawDib-Funktionen anzeigen.

Wenn Ihre Anwendung aufeinanderfolgende Aufrufe von **AVIStreamGetFrame** vornimmt, überschreibt die Funktion ihren Puffer mit jedem abgerufenen Frame.

Wenn Sie mit der Verwendung von **AVIStreamGetFrame** fertig sind und sich der dekomprimierte DIB im Puffer befindet, können Sie die zugeordneten Ressourcen mithilfe der [**FUNKTION AVIStreamGetFrameClose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) freigeben.

Weitere Informationen zum Dekomprimieren von Bildern finden Sie unter [Videokomprimierungs-Manager.](video-compression-manager.md)

 

 