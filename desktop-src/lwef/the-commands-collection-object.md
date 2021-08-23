---
title: Das Commands-Auflistungsobjekt
description: Das Commands-Auflistungsobjekt
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d30f7933bd973ae500b75abb51c47899fa60322444d49fe0835f6bfa3efab97f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975660"
---
# <a name="the-commands-collection-object"></a>Das Commands-Auflistungsobjekt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Der Microsoft Agent-Server verwaltet eine Liste von Befehlen, die dem Benutzer derzeit zur Verfügung stehen. Diese Liste enthält Befehle, die der Server für die allgemeine Interaktion definiert (z. B. Hide and Open The Voice Commands Window), die Liste der verfügbaren (aber nicht eingabeaktiven) Clients und die vom aktuellen aktiven Client definierten Befehle. Die ersten beiden Befehlssätze sind globale Befehle. Das heißt, sie sind unabhängig vom eingabeaktiven Client jederzeit verfügbar. Clientdefinierte Befehle sind nur verfügbar, wenn dieser Client eingabeaktiv ist und das Zeichen sichtbar ist.

Jede Clientanwendung kann eine Sammlung von Befehlen definieren, die als [**Commands-Sammlung bezeichnet**](/windows/desktop/lwef/the-commands-collection-object) wird. Um der Auflistung einen Befehl hinzuzufügen, verwenden Sie die [**Add- oder**](add-method.md) [**Insert-Methode.**](insert-method.md) Obwohl Sie die Eigenschaften eines Befehls mit separaten Anweisungen angeben können, geben Sie  für eine optimale Codeleistung alle Eigenschaften eines Befehls in der Add- oder **Insert-Methode** an. Für jeden Befehl in der Sammlung können Sie bestimmen, ob der Benutzerzugriff auf den Befehl im Popupmenü des Zeichens, im Fenster "Sprachbefehle", in beiden oder in keinem der beiden Optionen angezeigt wird. Wenn beispielsweise ein Befehl im Popupmenü für das Zeichen angezeigt werden soll, legen Sie die Eigenschaften [**Caption**](caption-property.md) und Visible des [**Befehls**](visible-property.md) fest. Um den Befehl im Fenster Sprachbefehle anzuzeigen, legen Sie die [**VoiceCaption-**](voicecaption-property.md) und Voice-Eigenschaften des [**Befehls**](voice-property.md) fest.

Ein Benutzer kann nur[](/windows/desktop/lwef/the-commands-collection-object)dann auf die einzelnen Befehle und Befehle in Ihrer Sammlung zugreifen, wenn Ihre Clientanwendung eingabeaktiv ist. Wenn Sie das Zeichen möglicherweise für andere Clientanwendungen freigeben, sollten Sie daher in der Regel die Eigenschaften [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)und [**Voice**](voice-property.md) für das **Sammlungsobjekt Commands** sowie für die Befehle in der Sammlung festlegen. Dadurch wird ein Eintrag für Ihre **Commands-Sammlung** im Popupmenü eines Zeichens und im Fenster "Sprachbefehle" platziert.

Wenn der Benutzer zu Ihrem Client [](/windows/desktop/lwef/the-commands-collection-object) wechselt, indem er seinen Befehlseintrag auswählt, macht der Server den Client automatisch eingabeaktiv, benachrichtigt Ihre Clientanwendung mithilfe des [**ActivateInput-Ereignisses**](activateinput-event.md) und macht die Befehle in seiner Sammlung verfügbar. Der Server benachrichtigt den Client außerdem darüber, dass er mit dem [**DeActivateInput-Ereignis**](deactivateinput-event.md) nicht mehr eingabeaktiv ist. Dadurch kann der Server nur die Befehle präsentieren und akzeptieren, die für den Kontext des aktuellen eingabeaktiven Clients gelten. Es dient auch dazu, Befehlsnamenskollisionen zwischen Clients zu vermeiden.

Ein Client kann mithilfe der Activate-Methode auch explizit anfordern, sich selbst zum eingabeaktiven [**Client zu**](activate-method.md) machen. Diese Methode unterstützt auch das Festlegen der Anwendung, dass sie nicht der eingabeaktive Client ist. Sie können diese Methode verwenden, wenn Sie ein Zeichen für eine andere Anwendung freigeben und die Anwendung so festlegen, dass sie eingabeaktiv ist, wenn das Anwendungsfenster den Fokus erhält, und nicht eingabeaktiv, wenn es den Fokus verliert.

Auf ähnliche Weise können Sie mit der [**Activate-Methode**](activate-method.md) festlegen, dass Ihre Anwendung der aktive Client des Zeichens ist (oder nicht). Der aktive Client ist der Client, der Eingaben empfängt, wenn sein Zeichen das oberste Zeichen ist. Wenn sich dieser Status ändert, benachrichtigt der Server Ihre Anwendung mit dem [**ActiveClientChange-Ereignis.**](activeclientchange-event.md)

Wenn das Popupmenü eines Zeichens angezeigt wird, werden Änderungen an den Eigenschaften einer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) oder an den Befehlen in der Sammlung erst angezeigt, wenn der Benutzer das Menü erneut anzeigt. Im Befehlsfenster werden jedoch Änderungen angezeigt, sobald sie vorgenommen werden.

-   [Commands-Objektmethoden](commands-object-methods.md)
-   [Commands-Objekteigenschaften](commands-object-properties.md)

 

 