---
title: Starten, Anhalten und Fortsetzen der Wiedergabe
description: Starten, Anhalten und Fortsetzen der Wiedergabe
ms.assetid: 4af92781-5461-4195-82f5-a9213a9bdbd7
keywords:
- MCIWndPlay-Makro
- MCIWndPause-Makro
- MCIWndResume-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49977b9bc741c6b32ce0da0c0ae9f63bd875a24268a00bb4782cd71531a4ef31
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119688670"
---
# <a name="starting-pausing-and-resuming-playback"></a>Starten, Anhalten und Fortsetzen der Wiedergabe

[**MCIWndPlay ist**](/windows/desktop/api/Vfw/nf-vfw-mciwndplay) das allgemeinste Wiedergabemakro. Mit diesem Makro können Sie eine Datei oder ein Gerät von der aktuellen Wiedergabeposition wiedergeben. Die Wiedergabe wird bis zum Ende des Inhalts fortgesetzt, es sei denn, sie wird unterbrochen.

Sie können ein Gerät, das abspielt, vorübergehend unterbrechen, indem Sie das [**Makro MCIWndPause**](/windows/desktop/api/Vfw/nf-vfw-mciwndpause) verwenden. Verwenden Sie das [**Makro MCIWndResume,**](/windows/desktop/api/Vfw/nf-vfw-mciwndresume) um die Wiedergabe von der angehaltenen Position aus wieder aufzunehmen. Einige Geräte unterstützen die Befehle zum Anhalten und Fortsetzen nicht. Diese Geräte ordnen in der **Regel MCIWndPause** dem [**MCIWndStop-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndstop) zu, wodurch die Wiedergabe oder Aufzeichnung beendet wird. Sie können ein Gerät neu starten, das anhalten oder fortsetzen nicht unterstützt, indem Sie **MCIWndPlay** verwenden, wodurch die Wiedergabe von der aktuellen Wiedergabeposition aus gestartet wird.

 

 




