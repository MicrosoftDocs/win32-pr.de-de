---
title: Bestimmen und Ändern der aktuellen Position
description: Bestimmen und Ändern der aktuellen Position
ms.assetid: 20f78dcd-3259-43c2-8da3-8cfc299252e6
keywords:
- Mciwndgetstart-Makro
- Mciwndgetend-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84a8e7022bdfcede526a730014a07deaf22fe66d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471397"
---
# <a name="determining-and-changing-the-current-position"></a>Bestimmen und Ändern der aktuellen Position

Wenn eine Datei oder ein Gerät einem mciwnd-Fenster zugeordnet ist, wird die Wiedergabe Position anfangs unabhängig vom Medientyp am Anfang des Inhalts festgelegt. Während der Wiedergabe wird die Wiedergabe Position linear durch den Inhalt verschoben, und wenn die Wiedergabe ununterbrochen erfolgt, erreicht schließlich das Ende des Inhalts. Wenn eine Unterbrechung auftritt, ist die aktuelle Wiedergabe Position der Speicherort, an dem die Wiedergabe beendet oder angehalten wurde.

Sie können die Speicherorte für den Anfang und das Ende des Inhalts abrufen, indem Sie die Makros [**mciwndgetstart**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetstart) und [**mciwndgetend**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetend) verwenden. Sie können die Länge des Inhalts ermitteln, indem Sie den von **mciwndgetstart** zurückgegebenen Wert von dem Wert subtrahieren, der von **mciwndgetend** zurückgegeben wurde, oder indem Sie das [**mciwndgetlength**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetlength) -Makro verwenden. Sie können die aktuelle Wiedergabe Position abrufen, indem Sie das [**mciwndgetposition**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetposition) -Makro verwenden, oder Sie können die Wiedergabe Position als NULL-terminierte Zeichenfolge abrufen, indem Sie das [**mciwndgetpositionstring**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetpositionstring) -Makro verwenden.

Verwenden Sie zum Ändern der aktuellen Wiedergabe Position die Makros [**mciwndhome**](/windows/desktop/api/Vfw/nf-vfw-mciwndhome), [**mciwndend**](/windows/desktop/api/Vfw/nf-vfw-mciwndend)und [**mciwndseek**](/windows/desktop/api/Vfw/nf-vfw-mciwndseek) . Sie können die Wiedergabe Position an den Anfang des Inhalts verschieben, indem Sie **mciwndhome** oder das Ende des Inhalts mit **mciwndend** verwenden. Verwenden Sie **mciwndseek** , um die Wiedergabe Position an eine beliebige Position im Inhalt zu verschieben.

Sie können den Inhalt auch durchlaufen, indem Sie das [**mciwndstep**](/windows/desktop/api/Vfw/nf-vfw-mciwndstep) -Makro verwenden. Beginnend mit der aktuellen Wiedergabe Position verschiebt dieses Makro die Wiedergabe Position um ein angegebenes Inkrement vorwärts oder rückwärts.

> [!Note]  
> Die Einheiten, die zum Angeben der Position verwendet werden, variieren je nach Medientypen und-Geräten. Die Wiedergabe Position für vom MCIAVI-Gerät verwendete AVI-Dateien wird z. b. in Frames gemessen. die Wiedergabe Position für CD-Audiodateien, Wellenform-Audiodateien und MIDI-Dateien wird in Millisekunden gemessen.

 

Geräte für andere Medientypen und Geräte von Drittanbietern können andere Einheiten verwenden. Informationen zum Ermitteln dieser Einheiten finden Sie unter [Wiedergabe Erweiterungen](playback-enhancements.md).

 

 




