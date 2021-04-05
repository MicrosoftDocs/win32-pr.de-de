---
title: Speichern von aufgezeichneten Inhalten
description: Speichern von aufgezeichneten Inhalten
ms.assetid: 0c159c44-f96c-4c08-bd3f-9e65b413026c
keywords:
- Mciwndsave-Makro
- Mciwndsavedialog-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55bb2cd89a72af4412b2555dd9b7c88f2d277ac8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710446"
---
# <a name="saving-recorded-content"></a>Speichern von aufgezeichneten Inhalten

Nachdem Sie die Aufzeichnung abgeschlossen haben, können Sie den Inhalt mithilfe des Makros [**mciwndsave**](/windows/desktop/api/Vfw/nf-vfw-mciwndsave) oder [**mciwndsavedialog**](/windows/desktop/api/Vfw/nf-vfw-mciwndsavedialog) oder mithilfe der [**getsavefile Name Preview**](/windows/desktop/api/Vfw/nf-vfw-getsavefilenamepreviewa) -Funktion mit **mciwndsave** speichern. Das **mciwndsave** -Makro speichert Daten in der Datei, die dem mciwnd-Fenster zugeordnet ist. Das **mciwndsavedialog** -Makro ermöglicht dem Benutzer das Angeben eines Datei namens und das Speichern der aufgezeichneten Daten in der angegebenen Datei. Die Funktion " **getsavefileamepreview** " zeigt das Dialogfeld " **SaveAs** " zum Auswählen einer Datei an und ermöglicht dem Benutzer die Vorschau der Datei. Wenn der Name einer vorhandenen Datei im Dialogfeld " **SaveAs** " angegeben wird, stellt **getsavefileamepreview** ein kleines Steuerelement im Dialogfeld bereit, damit der Benutzer den Inhalt der Datei in der Vorschau anzeigen kann. Sie können die aufgezeichneten Daten in einer Datei speichern, die mit " **getsavefileamepreview** " mithilfe von " **mciwndsave**" ausgewählt wurde.

 

 




