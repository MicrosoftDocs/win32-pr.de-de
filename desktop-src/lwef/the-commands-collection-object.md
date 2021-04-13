---
title: Das Commands-Auflistungs Objekt
description: Das Commands-Auflistungs Objekt
ms.assetid: 8726ce04-77d3-4ae3-bd46-e75f42b36d6f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2367035d86f92d57dc459564943b9e7797ecb04
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390154"
---
# <a name="the-commands-collection-object"></a>Das Commands-Auflistungs Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Microsoft-Agent-Server verwaltet eine Liste der Befehle, die dem Benutzer zurzeit zur Verfügung stehen. Diese Liste enthält Befehle, die der Server für allgemeine Interaktionen definiert (z. b. das Fenster Sprachbefehle ausblenden und öffnen), die Liste der verfügbaren (aber nicht Eingabe aktiven) Clients und die Befehle, die vom aktuellen aktiven Client definiert werden. Die ersten beiden Befehls Sätze sind globale Befehle. Das heißt, Sie sind unabhängig vom eingegebenen aktiven Client jederzeit verfügbar. Client definierte Befehle sind nur verfügbar, wenn der Client für die Eingabe aktiviert ist und das Zeichen sichtbar ist.

Jede Client Anwendung kann eine Auflistung von Befehlen definieren, die als [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung bezeichnet werden. Um der Auflistung einen Befehl hinzuzufügen, verwenden [**Sie die Add**](add-method.md) -oder [**Insert**](insert-method.md) -Methode. Obwohl Sie die Eigenschaften eines Befehls mit separaten Anweisungen angeben können, geben Sie für optimale Code Leistung alle Eigenschaften eines Befehls in der **Add** -oder **Insert** Method-Anweisung an. Sie können für jeden Befehl in der Auflistung ermitteln, ob der Benutzer Zugriff auf den Befehl im Popup Menü des Zeichens, im Fenster "Sprachbefehle", sowohl in als auch in keinem von angezeigt wird. Wenn z. b. ein Befehl im Popup Menü für das Zeichen angezeigt werden soll, legen Sie die [**Beschriftung**](caption-property.md) des Befehls und die [**sichtbaren**](visible-property.md) Eigenschaften fest. Um den Befehl im Fenster "Sprachbefehle" anzuzeigen, legen Sie die [**voicecaption**](voicecaption-property.md) -und die [**Voice**](voice-property.md) -Eigenschaften des Befehls fest.

Ein Benutzer kann nur dann auf die einzelnen comm-[**Befehle**](/windows/desktop/lwef/the-commands-collection-object)in ihrer Auflistung zugreifen, wenn die Client Anwendung aktiv ist. Wenn Sie das Zeichen also möglicherweise für andere Client Anwendungen freigeben, sollten Sie in der Regel die [**Beschriftungs**](caption-property.md)-, [**voicecaption**](voicecaption-property.md)-und [**Voice**](voice-property.md) -Eigenschaften für das **Commands** Collection-Objekt sowie für die Befehle in der Auflistung festlegen. Dadurch wird ein Eintrag für die **Befehls** Auflistung im Popupmenü eines Zeichens und im Fenster "Sprachbefehle" eingefügt.

Wenn der Benutzer durch Auswahl seines [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Eintrags zu Ihrem Client wechselt, wird der Client automatisch von dem Server eingegeben, und die Client Anwendung wird mithilfe des [**activateinput**](activateinput-event.md) -Ereignisses benachrichtigt, sodass die Befehle in der zugehörigen Auflistung verfügbar sind. Der Server benachrichtigt den Client auch darüber, dass er nicht mehr mit dem Ereignis " [**endactivateinput**](deactivateinput-event.md) " aktiv ist. Dies ermöglicht es dem Server, nur die Befehle anzuzeigen und zu akzeptieren, die auf den Kontext des aktuellen Eingabe aktiven Clients angewendet werden. Es dient auch zur Vermeidung von Konflikten mit Befehlsnamen zwischen Clients.

Ein Client kann mit der [**Aktivierungs**](activate-method.md) Methode auch explizit anfordern, dass er sich selbst als Eingabe aktiver Client erweist. Diese Methode unterstützt auch das festlegen, dass die Anwendung nicht der Eingabe aktive Client ist. Sie können diese Methode verwenden, wenn Sie ein Zeichen für eine andere Anwendung freigeben, und die Anwendung als Eingabe aktiv festlegen, wenn das Anwendungsfenster den Fokus erhält und nicht Eingabe aktiv ist, wenn es den Fokus verliert.

Auf ähnliche Weise können Sie die Methode [**aktivieren**](activate-method.md) verwenden, um die Anwendung auf den aktiven Client des Zeichens festzulegen. Der aktive Client ist der Client, der Eingaben empfängt, wenn sein Zeichen das oberste Zeichen ist. Wenn sich dieser Status ändert, benachrichtigt der Server Ihre Anwendung mit dem [**activeclientchange**](activeclientchange-event.md) -Ereignis.

Wenn das Popup Menü eines Zeichens angezeigt wird, werden Änderungen an den Eigenschaften einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung oder die Befehle in der Auflistung erst angezeigt, wenn der Benutzer das Menü erneut anzeigt. Im Fenster Befehle werden jedoch Änderungen angezeigt, sobald sie auftreten.

-   [Commands-Objektmethoden](commands-object-methods.md)
-   [Objekteigenschaften für Befehle](commands-object-properties.md)

 

 