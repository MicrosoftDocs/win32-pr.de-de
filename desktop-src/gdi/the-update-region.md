---
description: Der Updatebereich identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gedrammt werden muss.
ms.assetid: 21228620-9491-4e1b-8658-15e9605951f2
title: Der Updatebereich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d9a8f847a1e2d479200cfe6ea4e60a1b3a8ebf4c02aaf7c89fc719f62d91e91
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119717970"
---
# <a name="the-update-region"></a>Der Updatebereich

Der *Updatebereich* identifiziert den Teil eines Fensters, der veraltet oder ungültig ist und neu gedrammt werden muss. Das System verwendet den Updatebereich, um [**WM \_ PAINT-Nachrichten**](wm-paint.md) für Anwendungen zu generieren und die Zeit zu minimieren, die Anwendungen damit verbringen, den Inhalt ihrer Fenster auf den neuesten Stand zu bringen. Das System fügt dem Updatebereich nur den ungültigen Teil des Fensters hinzu, was erfordert, dass nur dieser Teil gezeichnet wird.

Wenn das System feststellt, dass ein Fenster aktualisiert werden muss, legt es die Dimensionen des Updatebereichs auf den ungültigen Teil des Fensters fest. Das Festlegen des Updatebereichs führt nicht sofort zum Zeichnen der Anwendung. Stattdessen ruft die Anwendung weiterhin Nachrichten aus der Anwendungsnachrichtenwarteschlange ab, bis keine Nachrichten mehr verbleiben. Das System überprüft dann den Updatebereich. Wenn der Bereich nicht leer ist (nicht NULL), sendet es eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an die Fensterprozedur.

Eine Anwendung kann den Updatebereich verwenden, um seine [**WM \_ PAINT-Meldungen**](wm-paint.md) zu generieren. Beispielsweise legt eine Anwendung, die Daten aus geöffneten Dateien lädt, in der Regel den Updatebereich beim Laden so fest, dass während der Verarbeitung der nächsten WM PAINT-Nachricht neue **\_ Daten gezeichnet** werden. Im Allgemeinen sollte eine Anwendung nicht zeichnen, wenn sich ihre Daten ändern, sondern alle Zeichnungsvorgänge über die **WM \_ PAINT-Nachricht** routen.

 

 



