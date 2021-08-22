---
title: Bestimmen und Ändern der aktuellen Position
description: Bestimmen und Ändern der aktuellen Position
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- MCIWndGetStart-Makro
- MCIWndGetEnd-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 594aa63b4b620327cd8b9ae41c263c197e1a981405c2148545ae7b8d4df86c5c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119497340"
---
# <a name="determining-and-changing-the-current-position"></a>Bestimmen und Ändern der aktuellen Position

Wenn eine Datei oder ein Gerät einem MCIWnd-Fenster zugeordnet ist, wird die Wiedergabeposition unabhängig vom Medientyp zunächst am Anfang des Inhalts festgelegt. Während der Wiedergabe bewegt sich die Wiedergabeposition linear durch den Inhalt und erreicht, wenn die Wiedergabe unterbrechungsfrei ist, schließlich das Ende des Inhalts. Wenn eine Unterbrechung auftritt, ist die aktuelle Wiedergabeposition die Position, an der die Wiedergabe beendet oder angehalten wurde.

Sie können die Speicherorte für den Anfang und das Ende des Inhalts mithilfe der Makros [**MCIWndGetStart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) und [**MCIWndGetEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) abrufen. Sie können die Länge des Inhalts bestimmen, indem Sie den von **MCIWndGetStart** zurückgegebenen Wert von dem wert subtrahieren, der von **MCIWndGetEnd** zurückgegeben wird, oder indem Sie das [**MCIWndGetLength-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) verwenden. Sie können die aktuelle Wiedergabeposition mithilfe des [**MCIWndGetPosition-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) oder die Wiedergabeposition als auf NULL endende Zeichenfolge abrufen, indem Sie das [**MCIWndGetPositionString-Makro**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) verwenden.

Um die aktuelle Wiedergabeposition zu ändern, verwenden Sie die Makros [**MCIWndHome,**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome) [**MCIWndEnd**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)und [**MCIWndSeek.**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) Sie können die Wiedergabeposition mit **MCIWndHome** oder mit **MCIWndEnd** an den Anfang des Inhalts verschieben. Verwenden Sie **MCIWndSeek,** um die Wiedergabeposition an eine beliebige Position im Inhalt zu verschieben.

Sie können den Inhalt auch mithilfe des [**MCIWndStep-Makros**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) schrittweise durchlaufen. Ab der aktuellen Wiedergabeposition verschiebt dieses Makro die Wiedergabeposition um ein angegebenes Inkrement vorwärts oder rückwärts.

> [!Note]  
> Die Einheiten, die zum Angeben der Position verwendet werden, variieren zwischen den verschiedenen Medientypen und Geräten. Beispielsweise wird die Wiedergabeposition für AVI-Dateien, die vom MCIAVI-Gerät verwendet werden, in Frames gemessen. Die Wiedergabeposition für CD-Audio-, Waveform-Audio- und CSV-Dateien wird in Millisekunden gemessen.

 

Geräte für andere Medientypen und Geräte von Drittanbietern können andere Einheiten verwenden. Informationen zum Bestimmen dieser Einheiten finden Sie unter [Playback Enhancements](playback-enhancements.md).

 

 




