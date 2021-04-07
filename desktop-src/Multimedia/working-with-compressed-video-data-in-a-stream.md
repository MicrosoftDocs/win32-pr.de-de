---
title: Arbeiten mit komprimierten Video Daten in einem Stream
description: Arbeiten mit komprimierten Video Daten in einem Stream
ms.assetid: b701e072-f162-438f-b607-aea7491a02f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0587ee6c12a93eb014368642ba1605f546129e0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038884"
---
# <a name="working-with-compressed-video-data-in-a-stream"></a>Arbeiten mit komprimierten Video Daten in einem Stream

Avifile bietet mehrere Möglichkeiten für den Zugriff auf komprimierte Videostreams.

Wenn Sie einen oder mehrere Frames eines komprimierten Videodaten Stroms anzeigen möchten, können Sie die Frames mithilfe der [**avistreamread**](/windows/desktop/api/Vfw/nf-vfw-avistreamread) -Funktion abrufen und die komprimierten Frame Daten an drawdib-Funktionen weiterleiten, um Sie anzuzeigen. Die drawdib-Funktionen können Bilder mehrerer Bild tiefen anzeigen und Bilder für Anzeige Dateien, die bestimmte Typen von geräteunabhängigen Bitmaps (DIBs) nicht verarbeiten können, automatisch unterscheiden. Diese Funktionen können mit nicht komprimierten und komprimierten Bildern verwendet werden. Weitere Informationen zu drawdib-Funktionen finden Sie unter [drawdib Functions](drawdib-functions.md).

Avifile bietet Funktionen zum Dekomprimieren eines einzelnen Video Frames. Verwenden Sie zum Zuordnen von Ressourcen die [**AVIStreamGetFrameOpen**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeopen) -Funktion. Mit dieser Funktion wird ein Puffer für die entkomprimierten Daten erstellt.

Sie können einen einzelnen Videoframe mithilfe der [**AVIStreamGetFrame**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframe) -Funktion entkomprimieren. Diese Funktion zerlegt den Frame und Ruft einen kompletten Rahmen der Bilddaten ab, wobei die Adresse des DIB in der [BITMAPINFOHEADER](/previous-versions//ms532290(v=vs.85)) -Struktur zurückgegeben wird. Die Anwendung kann das DIB mithilfe von Standard Zeichnungsfunktionen oder mithilfe der drawdib-Funktionen anzeigen.

Wenn die Anwendung aufeinander folgende Aufrufe an **AVIStreamGetFrame** durchführt, überschreibt die Funktion den Puffer mit jedem abgerufenen Frame.

Wenn Sie die Verwendung von **AVIStreamGetFrame** abgeschlossen haben und sich das entkomprimierte DIB in seinem Puffer befindet, können Sie die zugeordneten Ressourcen mithilfe der [**avistreamgetframeclose**](/windows/desktop/api/Vfw/nf-vfw-avistreamgetframeclose) -Funktion freigeben.

Weitere Informationen zur Dekomprimierung von Bildern finden Sie unter [Video Compression Manager](video-compression-manager.md).

 

 