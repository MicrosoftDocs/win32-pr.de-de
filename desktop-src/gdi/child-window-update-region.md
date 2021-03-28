---
description: Ein untergeordnetes Fenster ist ein Fenster mit dem WS-untergeordneten Format \_ oder dem WS \_ ChildWindow-Stil.
ms.assetid: d8110492-c1b9-4b49-9b34-587adb7c65c9
title: Aktualisierungs Bereich des untergeordneten Fensters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b92e6cba93c3be253b8ed8616bdcf9301e92494
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959317"
---
# <a name="child-window-update-region"></a>Aktualisierungs Bereich des untergeordneten Fensters

Ein untergeordnetes Fenster ist ein Fenster mit dem WS-untergeordneten Format \_ oder dem WS \_ ChildWindow-Stil. Wie andere Fenster Stile empfangen untergeordnete Fenster [**WM \_**](wm-paint.md) -Zeichnungs Meldungen, um die Aktualisierung Aufforderungs zu aktualisieren. Jedes untergeordnete Fenster verfügt über einen Update Bereich, der entweder vom System oder von der Anwendung festgelegt werden kann, um endgültige **WM \_ Paint** -Meldungen zu generieren.

Das übergeordnete Fenster eines untergeordneten Fensters wirkt sich auf das übergeordnete Fenster des untergeordneten Fensters aus. Dies gilt nicht für Windows anderer Stile. Das System legt den Update Bereich des untergeordneten Fensters häufig fest, wenn der Aktualisierungs Bereich des übergeordneten Fensters festgelegt wird, sodass das untergeordnete Fenster [**WM- \_ Paint**](wm-paint.md) -Meldungen empfängt, wenn das übergeordnete Fenster Sie empfängt. Das System schränkt den Speicherort des sichtbaren Bereichs des untergeordneten Fensters auf den Client Bereich des übergeordneten Fensters ein und schneidet einen Teil des untergeordneten Fensters ab, das außerhalb des übergeordneten Fensters verschoben wurde.

Das System legt den Update Bereich für ein untergeordnetes Fenster fest, wenn ein Teil des Aktualisierungs Bereichs des übergeordneten Fensters einen Teil des untergeordneten Fensters enthält. In solchen Fällen sendet das System zuerst eine [**WM \_ Paint**](wm-paint.md) -Meldung an das übergeordnete Fenster und sendet dann eine Nachricht an das untergeordnete Fenster, sodass das untergeordnete Element Teile des Fensters wiederherstellen kann, die das übergeordnete Element möglicherweise gezeichnet hat.

Der Aktualisierungs Bereich des übergeordneten Elements wird vom System nicht festgelegt, wenn das untergeordnete Element festgelegt ist. Eine Anwendung kann eine [**WM- \_**](wm-paint.md) Zeichnungs Nachricht für das übergeordnete Fenster nicht generieren, indem das untergeordnete Fenster ungültig wird. Auf ähnliche Weise kann eine Anwendung eine **WM \_** -Zeichnungs Nachricht für das untergeordnete Element nicht generieren, indem ein Teil des Client Bereichs des übergeordneten Elements, der vollständig unterhalb des untergeordneten Fensters liegt, ungültig wird. In solchen Fällen empfängt keines der Fenster eine **WM \_** -Zeichnungs Nachricht.

Eine Anwendung kann verhindern, dass der Aktualisierungs Bereich eines untergeordneten Fensters festgelegt wird, wenn das übergeordnete Fenster festgelegt wird, indem der WS \_ clipchildren-Stil beim Erstellen des übergeordneten Fensters angegeben wird. Wenn dieses Format festgelegt ist, schließt das System die untergeordneten Fenster aus dem sichtbaren Bereich des übergeordneten Elements aus und ignoriert daher jeden Teil des Aktualisierungs Bereichs, der möglicherweise die untergeordneten Fenster enthält. Wenn die Anwendung in das übergeordnete Fenster zeichnet, wird jede Zeichnung, die das untergeordnete Fenster abdecken würde, abgeschnitten, sodass eine nachfolgende WM-Zeichnungs Nachricht für das untergeordnete Fenster unnötig ist. [**\_**](wm-paint.md)

Die Update-und sichtbaren Bereiche eines untergeordneten Fensters werden auch von den neben geordneten Fenstern des untergeordneten Fensters beeinflusst. Gleich geordnete Fenster sind alle Fenster, die über ein gemeinsames übergeordnetes Fenster verfügen. Wenn sich gleich geordnete Fenster überlappen, wirkt sich das Festlegen des Aktualisierungs Bereichs für einen auf den Aktualisierungs Bereich einer anderen aus, sodass [**WM- \_ Paint**](wm-paint.md) -Meldungen an beide Fenster gesendet werden. Wenn ein Fenster in der übergeordneten Kette zusammengesetzt wird (ein Fenster mit einer zusammengesetzten WX-Datei \_ \_ ), empfangen gleich geordnete Fenster **\_ WM** -Zeichnungs Nachrichten in umgekehrter Reihenfolge ihrer Position in der Z-Reihenfolge. Wenn dies der Grund ist, empfängt das Fenster, das in der Z-Reihenfolge (oben) am höchsten ist, zuletzt die WM-Zeichnungs Nachricht und umgekehrt. **\_** Wenn ein Fenster in der übergeordneten Kette nicht zusammengesetzt ist, empfangen gleich geordnete **Fenster \_ WM** -Zeichnungs Nachrichten in der Z-Reihenfolge.

Gleich geordnete Fenster werden nicht automatisch abgeschnitten. Ein gleich geordnetes Element kann über ein anderes überlappendes gleich geordnetes Element zeichnen, auch wenn das Fenster, das zeichnet, eine niedrigere Position in der Z-Reihenfolge aufweist. Eine Anwendung kann dies verhindern, indem Sie \_ beim Erstellen der Fenster den Stil der WS-clipneben geordneten Elemente angibt. Wenn dieses Format festgelegt ist, schließt das System alle Teile eines überlappenden neben geordneten Fensters aus dem sichtbaren Bereich eines Fensters aus, wenn das überlappende neben geordnete Fenster eine höhere Position in der Z-Reihenfolge aufweist.

> [!Note]  
> Das Update und sichtbare Bereiche für Windows mit dem WS- \_ Popup oder dem WS \_ PopupWindow-Stil sind von den übergeordneten Fenstern nicht betroffen.

 

 

 



