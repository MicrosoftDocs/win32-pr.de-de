---
title: Übersicht über WinEvents und Active Accessibility
description: Microsoft Active Accessibility Server winEvents auslösen, um Clients zu benachrichtigen, wenn sich ein barrierefreies Objekt ändert.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95507ff1b6cd56451dd7f9acc04014c6013a7179d536565b3518bccb9137e689
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052178"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents und Active Accessibility

Microsoft Active Accessibility Server auslösen *WinEvents,* um Clients zu benachrichtigen, wenn sich ein barrierefreies Objekt ändert. Es gibt zahlreiche Bedingungen, unter denen ein Server einen Client über eine Änderung benachrichtigt. Jede durch Microsoft Active Accessibility definierte [Ereigniskonstante](event-constants.md) beschreibt eine Bedingung, über die ein Client benachrichtigt wird. WinEvents kann beispielsweise Folgendes signalisieren:

- Wenn ein Objekt erstellt oder zerstört wird.
- Wenn ein Objekt den Fokus empfängt oder verliert.
- Wenn sich der Zustand oder speicherort eines Objekts ändert.
- Wenn sich eine Eigenschaft eines Objekts ändert.

Clientanwendungen empfangen ereignisbenachrichtigungen nicht automatisch. Sie müssen angeben, welche Ereignisse sie empfangen möchten, indem sie die [**SetWinEventHook-Funktion**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) aufrufen. Mit **SetWinEventHook** registriert sich ein Client für den Empfang mindestens eines Ereignisses und legt eine Hookfunktion zur Behandlung der angegebenen Ereignisse fest. Clients können dieselbe Hookfunktion verwenden, um mehrere Ereignistypen zu verarbeiten, oder sie können Hookfunktionen mit mehreren Funktionen verwenden. Clients rufen **den SetWinEventHook** einmal für jede Hookfunktion auf, die registriert werden muss.

Hookfunktionen befinden sich im Codetext des Clients, in einer DLL, die dem Clientprozess zugeordnet ist, oder in einer DLL, die dem Serverprozess zugeordnet ist. Jede dieser Methoden hat Vor- und Nachteile. Weitere Informationen finden Sie unter [In-Context- und Out-of-Context Hook Functions](in-context-and-out-of-context-hook-functions.md).

Um Clients über ein Ereignis zu benachrichtigen, rufen Server [**NotifyWinEvent auf.**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) Das System überprüft, ob Clientanwendungen Hookfunktionen für das Ereignis festgelegt haben, und ruft bei Bedarf die entsprechenden Hookfunktionen auf.

Wenn die Hookfunktion des Clients aufgerufen wird, empfängt sie eine Reihe von Parametern, die das Ereignis und das Objekt beschreiben, das das Ereignis generiert hat. Um Zugriff auf das Objekt zu erhalten, das das Ereignis generiert hat, ruft die Hookfunktion des Clients [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)auf.

> [!NOTE]
> Wenn sich keine Clients für den Empfang von WinEvents registriert haben, sind die Auswirkungen auf die Leistung eines Servers für den Aufruf von [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) vernachlässigbar.
>
> Server rufen [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) nur für Änderungen in ihren eigenen barrierefreien Objekten auf. Sie rufen **notifyWinEvent** nicht für Änderungen an vom System bereitgestellten Benutzeroberflächenelementen auf.

## <a name="event-driven-communication"></a>Event-Driven Kommunikation

Clients müssen einen WinEvent-Hook registrieren, bevor sie WinEvent-Benachrichtigungen empfangen können. Um unnötige Rückrufe zu vermeiden und die Leistung zu verbessern, wird Clients empfohlen, sich nur für die Ereignisse zu registrieren, die sie empfangen müssen.

Innerhalb der Hookprozedur kann der Client [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) aufrufen, um ein [**IAccessible-Objekt**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) für das Element abzurufen, für das das Ereignis gilt. Mit diesem Objekt kann der Client **IAccessible-Methoden** aufrufen, um Informationen abzurufen oder mit dem Benutzeroberflächenelement zu interagieren.

## <a name="related-topics"></a>Zugehörige Themen

[WinEvents](winevents-infrastructure.md)
