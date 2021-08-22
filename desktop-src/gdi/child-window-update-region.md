---
description: Ein untergeordnetes Fenster ist ein Fenster mit dem \_ WS CHILD- oder WS \_ CHILDWINDOW-Stil.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Updatebereich des untergeordneten Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbf702855e506424a08e5be6c6b0cfe514035f1c54348306475140fb7fc440a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105895"
---
# <a name="child-window-update-region"></a>Updatebereich des untergeordneten Fensters

Ein untergeordnetes Fenster ist ein Fenster mit dem \_ WS CHILD- oder WS \_ CHILDWINDOW-Stil. Wie andere Fensterstile erhalten untergeordnete Fenster [**WM \_ PAINT-Meldungen,**](wm-paint.md) um zur Aktualisierung aufzufordern. Jedes untergeordnete Fenster verfügt über einen Updatebereich, den entweder das System oder die Anwendung festlegen kann, um letztlich **WM \_ PAINT-Meldungen** zu generieren.

Die Aktualisierung eines untergeordneten Fensters und die sichtbaren Bereiche sind vom übergeordneten Fenster des untergeordneten Elements betroffen. Dies gilt nicht für Fenster anderer Stile. Das System legt häufig den Updatebereich des untergeordneten Fensters fest, wenn es den Updatebereich des übergeordneten Fensters festlegt, wodurch das untergeordnete Fenster [**WM \_ PAINT-Meldungen**](wm-paint.md) empfängt, wenn sie vom übergeordneten Fenster empfangen werden. Das System schränkt die Position des sichtbaren Bereichs des untergeordneten Fensters auf innerhalb des Clientbereichs des übergeordneten Fensters ein und schränkt jeden Teil des untergeordneten Fensters ein, der außerhalb des übergeordneten Fensters verschoben wird.

Das System legt den Updatebereich für ein untergeordnetes Fenster fest, wenn ein Teil des Updatebereichs des übergeordneten Fensters einen Teil des untergeordneten Fensters enthält. In solchen Fällen sendet das System zuerst eine [**WM \_ PAINT-Nachricht**](wm-paint.md) an das übergeordnete Fenster und dann eine Nachricht an das untergeordnete Fenster, sodass das untergeordnete Element alle Teile des Fensters wiederherstellen kann, die das übergeordnete Fenster möglicherweise übergezeichnet hat.

Das System legt den Updatebereich des übergeordneten Elements nicht fest, wenn die des untergeordneten Elements festgelegt ist. Eine Anwendung kann keine [**WM \_ PAINT-Nachricht**](wm-paint.md) für das übergeordnete Fenster generieren, indem das untergeordnete Fenster ungültig wird. Ebenso kann eine Anwendung keine **WM \_ PAINT-Nachricht** für das untergeordnete Element generieren, indem ein Teil des Clientbereichs des übergeordneten Elements ungültig wird, der vollständig unter dem untergeordneten Fenster liegt. In solchen Fällen empfängt kein Fenster eine **WM \_ PAINT-Meldung.**

Eine Anwendung kann verhindern, dass der Updatebereich eines untergeordneten Fensters festgelegt wird, wenn das übergeordnete Fenster festgelegt wird, indem beim Erstellen des übergeordneten Fensters der WS \_ CLIPCHILDREN-Stil angegeben wird. Wenn dieser Stil festgelegt ist, schließt das System die untergeordneten Fenster aus dem sichtbaren Bereich des übergeordneten Elements aus und ignoriert daher jeden Teil des Updatebereichs, der die untergeordneten Fenster enthalten kann. Wenn die Anwendung im übergeordneten Fenster zeichnet, wird jede Zeichnung, die das untergeordnete Fenster abdecken würde, abgeschnitten, sodass eine nachfolgende [**WM \_ PAINT-Meldung**](wm-paint.md) an das untergeordnete Fenster nicht erforderlich ist.

Die Updatebereiche und sichtbaren Bereiche eines untergeordneten Fensters sind auch von den gleichgeordneten Fenstern des untergeordneten Fensters betroffen. Gleichgeordnete Fenster sind alle Fenster, die über ein gemeinsames übergeordnetes Fenster verfügen. Wenn sich nebengeordnete Fenster überlappen, wirkt sich das Festlegen des Updatebereichs für einen auf den Updatebereich eines anderen aus, sodass [**WM \_ PAINT-Meldungen**](wm-paint.md) an beide Fenster gesendet werden. Wenn ein Fenster in der übergeordneten Kette zusammengesetzt ist (ein Fenster mit WX \_ EX \_ COMPOSITED), erhalten gleichgeordnete Fenster **WM \_ PAINT-Meldungen** in umgekehrter Reihenfolge ihrer Position in der Z-Reihenfolge. Vor diesem Hintergrund empfängt das Fenster, das in der Z-Reihenfolge (oben) am höchsten ist, zuletzt die **\_ WM-PAINT-Nachricht** und umgekehrt. Wenn ein Fenster in der übergeordneten Kette nicht zusammengesetzt ist, erhalten gleichgeordnete Fenster **WM \_ PAINT-Meldungen** in Z-Reihenfolge.

Nebengeordnete Fenster werden nicht automatisch abgeschnitten. Ein gleichgeordnetes Mitglied kann auch dann über ein anderes überlappende nebengeordnetes Zeichen zeichnen, wenn das gezeichnete Fenster eine niedrigere Position in der Z-Reihenfolge hat. Eine Anwendung kann dies verhindern, indem sie beim Erstellen der Fenster den Stil \_ WS CLIPSIBLINGS angibt. Wenn dieser Stil festgelegt ist, schließt das System alle Teile eines überlappenden nebengeordneten Fensters aus dem sichtbaren Bereich eines Fensters aus, wenn das überlappende nebengeordnete Fenster eine höhere Position in der Z-Reihenfolge hat.

> [!Note]  
> Die Update- und sichtbaren Bereiche für Fenster mit dem \_ WS-POPUP- oder \_ WS-POPUPWINDOW-Stil sind von den übergeordneten Fenstern nicht betroffen.

 

 

 



