---
title: Steuerelement Ereignisse (com)
description: Zusätzlich zur Bereitstellung von Eigenschaften und Methoden stellt ein Steuerelement auch ausgehende Schnittstellen bereit, um den Client über Ereignisse zu benachrichtigen.
ms.assetid: e7085bc0-c087-4cc8-9c69-ba05b0923b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1833e1396847e09366d1e06193196cfcf981d330
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104039959"
---
# <a name="control-events-com"></a>Steuerelement Ereignisse (com)

Zusätzlich zur Bereitstellung von Eigenschaften und Methoden stellt ein Steuerelement auch ausgehende Schnittstellen bereit, um den Client über Ereignisse zu benachrichtigen. Der Client muss die Behandlung dieser Ereignisse unterstützen. Weitere Informationen zur Funktionsweise von Verbindungs fähigen Objekten finden Sie unter [Ereignisse in com und Verbindungs fähigen Objekten](events-in-com-and-connectable-objects.md) .

Ein Steuerelement kann verschiedene ausgehende Schnittstellen für verschiedene Zwecke unterstützen. Alle ausgehenden Schnittstellen werden in den Typinformationen des Steuer Elements als Quell Schnittstellen gekennzeichnet, aber nur eine ist als Standard gekennzeichnet, um anzugeben, dass es sich um die primäre ausgehende Schnittstelle handelt.

Ein Container kann eine oder mehrere der ausgehenden Schnittstellen unterstützen, die von einem-Steuerelement definiert werden. Das-Steuerelement sollte auf den Umgang mit Containern vorbereitet sein, die nur einige der ausgehenden Schnittstellen unterstützen.

Steuerelemente unterstützen vier Arten von Ereignissen:

-   Anforderungs Ereignisse. Ein-Steuerelement fordert von seinem Client eine Berechtigung zum Durchführen einer Methode in der ausgehenden Schnittstelle an, wodurch ein Anforderungs Ereignis ausgelöst wird. Der Client signalisiert dem Steuerelement über einen booleschen out-Parameter in der Methode, die vom-Steuerelement aufgerufen wurde. Der Client kann somit verhindern, dass das Steuerelement die Aktion ausführt.
-   Vor Ereignissen. Ein-Steuerelement benachrichtigt seinen Client hat, dass es etwas durch Aufrufen einer Methode in der ausgehenden Schnittstelle macht, wodurch ein before-Ereignis ausgelöst wird. Der Client hat nicht die Möglichkeit, die Aktion zu verhindern, er kann jedoch alle notwendigen Schritte ausführen, wenn die Aktion ausgeführt wird.
-   Nach Ereignissen. Ein-Steuerelement benachrichtigt seinen Client, dass es gerade einen Vorgang durch Aufrufen einer Methode in der ausgehenden Schnittstelle durchgeführt hat, wodurch ein After-Ereignis ausgelöst wird. Auch hier kann dieser Vorgang vom Client nicht abgebrochen werden, es können jedoch erforderliche Schritte ausgeführt werden, wenn die aufgetretene Aktion erfolgt ist.
-   Do-Ereignisse. Ein-Steuerelement löst ein do-Ereignis aus, damit der Client die Aktion des Steuer Elements überschreiben und Alternative oder ergänzende Aktionen bereitstellen kann. Normalerweise verfügt die-Methode, die ein Steuerelement für ein do-Ereignis aufruft, über eine Reihe von Parametern für die Aushandlung mit dem Client zu den Aktionen, die ausgeführt werden.

Die folgenden DISPIDs sind für Standard Ereignisse definiert, die von Steuerelementen unterstützt werden können: Click, DblClick, KeyDown, KeyPress, KeyUp, mougmove, mousetup und Error. Alle diese Standard Ereignisse weisen negative DISPID-Werte auf, die ihren Standardstatus angeben.

Mit der [**IOleControl:: frezeevents**](/windows/desktop/api/OCIdl/nf-ocidl-iolecontrol-freezeevents) -Methode, bei Aufruf mit **true**, wird ein Steuerelement darüber informiert, ob der Container sich mit der Behandlung von Ereignissen aus dem Steuerelement beschäftigt, bis " **frezeevents** " erneut mit **false** aufgerufen wird. Während dieses Zeitraums kann das Steuerelement nicht davon abhängen, dass der Container tatsächlich Ereignisse verarbeitet. Wenn ein Ereignis behandelt werden muss, sollte das Steuerelement das Ereignis in die Warteschlange stellen, um es auszulösen, wenn " **frezeevents** " mit " **false**" aufgerufen wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ActiveX-Steuerelemente](activex-controls.md)
</dt> </dl>

 

 




