---
title: Ermitteln von Geräten
description: Sie können auf drei Arten nach Geräten suchen, indem Sie den Typ, den udn und die asynchrone Suche (eine Suche nach Gerätetyp) durchsuchen.
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 055d08db76edd5bcc5591d3254613462c00fc974
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856751"
---
# <a name="discovering-devices"></a>Ermitteln von Geräten

Sie können auf drei Arten nach Geräten suchen: nach Typ, udn und asynchroner Suche (bei der es sich um eine Suche nach Gerätetyp handelt).

![Fenster "Geräte ermitteln"](images/ucp-disc.png)

**So ermitteln Sie Geräte**

1.  Wählen Sie den Typ der Suche aus, den Sie verwenden möchten: Suchen **nach Typ**, **nach udn suchen** oder **Async** suchen.
2.  Wählen Sie in der Liste den Typ des Geräts oder den udn aus, den Sie suchen möchten (für Suchvorgänge nach Typ oder udn). Der Inhalt der Liste basiert auf dem Inhalt der udn.txt-und devtype.txt Dateien, die Sie zuvor bearbeitet haben.
3.  Klicken Sie auf **Ermittlung starten**. Die Suche wird gestartet. Die Ergebnisse werden in der Liste **gefundene Geräte** angezeigt. Wenn keine Geräte gefunden werden, wird eine Meldung mit dem Hinweis angezeigt, dass diese Bedingung angezeigt wird. Der Status des Such Fortschritts wird im Feld **Status** angezeigt.

Wenn Sie die asynchrone Suche verwenden, werden neue gefundene Geräte in der Liste **Geräte gefunden** und in der **Status** Leiste angezeigt. Wenn die asynchrone Suche abgeschlossen ist, wird in der **Status** Leiste eine Meldung mit dem Hinweis angezeigt. Da jedoch eine asynchrone Suche ausgeführt wird, bis Sie manuell beendet wird, werden neue Geräte in der Liste **gefundene Geräte** und in der **Status** Leiste angezeigt, wenn die Geräte im Netzwerk angezeigt werden.

Nachdem Sie Geräte ermittelt haben, können Sie [diese Steuern](controlling-a-device.md).

 

 




