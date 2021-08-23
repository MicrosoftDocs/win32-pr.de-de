---
title: Steuerungsereignisse (COM)
description: Zusätzlich zur Bereitstellung von Eigenschaften und Methoden stellt ein Steuerelement auch ausgehende Schnittstellen bereit, um seinen Client über Ereignisse zu benachrichtigen.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82b987202cb4e4e635a947ed60e9f947cc428f0aaaacb3d27c27d60ad536b636
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119243630"
---
# <a name="control-events-com"></a>Steuerungsereignisse (COM)

Zusätzlich zur Bereitstellung von Eigenschaften und Methoden stellt ein Steuerelement auch ausgehende Schnittstellen bereit, um seinen Client über Ereignisse zu benachrichtigen. Der Client muss die Behandlung dieser Ereignisse unterstützen. Weitere Informationen zur Funktionsweise von miteinander verbundenen Objekten finden Sie [unter Ereignisse in COM und Connectable Objects.](events-in-com-and-connectable-objects.md)

Ein Steuerelement kann verschiedene ausgehende Schnittstellen für verschiedene Zwecke unterstützen. Alle ausgehenden Schnittstellen werden in den Typinformationen des Steuerelements als Quellschnittstellen markiert, aber nur eine ist als Standard gekennzeichnet, um anzugeben, dass es sich um die primäre ausgehende Schnittstelle handelt.

Ein Container kann eine oder mehrere ausgehende Schnittstellen unterstützen, die von einem -Steuerelement definiert werden. Das Steuerelement sollte darauf vorbereitet sein, Container zu behandeln, die nur unterstützung für einige ihrer ausgehenden Schnittstellen bereitstellen.

Steuerelemente unterstützen vier Arten von Ereignissen:

-   Anforderungsereignisse. Ein Steuerelement fordert die Berechtigung vom Client an, etwas zu tun, indem eine Methode in der ausgehenden Schnittstelle aufgerufen wird, wodurch ein Anforderungsereignis ausgelöst wird. Der Client signalisiert das Steuerelement über einen booleschen out-Parameter in der Methode, die das Steuerelement aufgerufen hat. Der Client kann daher verhindern, dass das Steuerelement die Aktion ausführt.
-   Vor Ereignissen. Ein Steuerelement benachrichtigt seinen Client darüber, dass es etwas tun wird, indem es eine Methode in der ausgehenden Schnittstelle aufruft, wodurch ein before-Ereignis ausgelöst wird. Der Client hat nicht die Möglichkeit, die Aktion zu verhindern, aber er kann alle erforderlichen Schritte ausführen, wenn die Aktion ausgeführt wird, die gerade ausgeführt wird.
-   Nach Ereignissen. Ein Steuerelement benachrichtigt seinen Client, dass es gerade etwas getan hat, indem es eine Methode in der ausgehenden Schnittstelle aufruft und somit ein After-Ereignis auslöst. Auch hier kann der Client diese Aktion nicht abbrechen, aber unter Berücksichtigung der aufgetretenen Aktion erforderliche Schritte ausführen.
-   Do-Ereignisse. Ein Steuerelement löst ein Do-Ereignis aus, damit der Client die Aktion des Steuerelements überschreiben und einige alternative oder ergänzende Aktionen bereitstellen kann. In der Regel verfügt die Methode, die ein Steuerelement für ein Do-Ereignis aufruft, über eine Reihe von Parametern zum Aushandeln mit dem Client über die aktionen, die ausgeführt werden.

Die folgenden Dispids sind für Standardereignisse definiert, die von Steuerelementen unterstützt werden können: Click, DblClick, KeyDown, KeyPress, KeyUp, MouseMove, MouseUp und Error. Alle diese Standardereignisse weisen negative DISPID-Werte auf, die ihren Standardstatus angeben.

Die [**IOleControl::FreezeEvents-Methode**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) teilt einem Steuerelement beim Aufruf mit **TRUE** mit, ob der Container Ereignisse vom Steuerelement verarbeitet, bis **FreezeEvents** erneut mit **FALSE** aufgerufen wird. Während dieser Zeit kann die Steuerung nicht davon abhängen, dass der Container tatsächlich Ereignisse verarbeitet. Wenn ein Ereignis behandelt werden muss, sollte das Steuerelement das Ereignis in die Warteschlange stellen, um es auszu auslösen, wenn **FreezeEvents** mit **FALSE** aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




