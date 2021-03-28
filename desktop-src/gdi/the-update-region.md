---
description: Der Aktualisierungs Bereich identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gezeichnet werden muss.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Der Aktualisierungs Bereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e670bac065782a1e09c4d142f964aaea97d4b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104995094"
---
# <a name="the-update-region"></a>Der Aktualisierungs Bereich

Der *Aktualisierungs Bereich* identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gezeichnet werden muss. Das System verwendet die Update Region, um [**WM \_ Paint**](wm-paint.md) -Meldungen für Anwendungen zu generieren und die Zeit zu minimieren, in der Anwendungen die Inhalte ihrer Fenster auf den neuesten Stand bringen. Das System fügt dem Aktualisierungs Bereich nur den ungültigen Teil des Fensters hinzu. Dies erfordert, dass nur dieser Teil gezeichnet wird.

Wenn das System ermittelt, dass ein Fenster aktualisiert werden muss, legt es die Abmessungen des Aktualisierungs Bereichs auf den ungültigen Teil des Fensters fest. Wenn Sie den Update Bereich festlegen, wird die Anwendung nicht sofort gezeichnet. Stattdessen ruft die Anwendung weiterhin Nachrichten aus der Nachrichten Warteschlange der Anwendung ab, bis keine Nachrichten mehr vorhanden sind. Das System überprüft dann den Update Bereich. wenn die Region nicht leer (nicht null) ist, sendet Sie eine [**WM \_ Paint**](wm-paint.md) -Meldung an die Fenster Prozedur.

Eine Anwendung kann den Update Bereich verwenden, um Ihre [**WM \_ Paint**](wm-paint.md) -Meldungen zu generieren. Beispielsweise legt eine Anwendung, die Daten aus geöffneten Dateien lädt, in der Regel den Update Bereich beim Laden fest, sodass neue Daten während der Verarbeitung der nächsten WM-Zeichnungs Nachricht gezeichnet werden. **\_** Im Allgemeinen sollte eine Anwendung nicht zu dem Zeitpunkt gezeichnet werden, an dem sich die Daten ändern, sondern alle Zeichnungsvorgänge durch die WM-Zeichnungs Nachricht weiterleiten. **\_**

 

 



