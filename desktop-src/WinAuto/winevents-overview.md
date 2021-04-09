---
title: Übersicht über WinEvents und Active Accessibility
description: Microsoft Active Accessibility-Server rufen WinEvents auf, um Clients zu benachrichtigen, wenn sich ein Barrierefreies Objekt ändert.
ms.assetid: a2d486ee-84ef-4c44-a832-dbc0dae81542
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b351b1ce7b6337c4ca0ac0827daff2978c6611af
ms.sourcegitcommit: 85688bbfbe5b121bc05ddf112d54c23a469dfbc0
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "103948385"
---
# <a name="winevents-and-active-accessibility"></a>WinEvents und Active Accessibility

Microsoft Active Accessibility-Server rufen *WinEvents* auf, um Clients zu benachrichtigen, wenn sich ein Barrierefreies Objekt ändert. Es gibt zahlreiche Bedingungen, bei denen ein Server einen Client über eine Änderung benachrichtigt. Jede von Active Accessibility Microsoft definierte [Ereignis Konstante](event-constants.md) beschreibt eine Bedingung, über die ein Client benachrichtigt wird. WinEvents kann beispielsweise Folgendes signalisieren:

- Wenn ein Objekt erstellt oder zerstört wird.
- Wenn ein Objekt den Fokus erhält oder verliert.
- Wenn sich der Zustand oder der Speicherort eines Objekts ändert.
- Wenn eine Eigenschaft eines Objekts geändert wird.

Client Anwendungen empfangen Ereignis Benachrichtigungen nicht automatisch. Sie müssen angeben, welche Ereignisse Sie empfangen möchten, indem Sie die [**setwineventhook**](/windows/desktop/api/Winuser/nf-winuser-setwineventhook) -Funktion aufrufen. Mit **setwineventhook** registriert ein Client, dass ein oder mehrere Ereignisse empfangen werden, und legt eine Hook-Funktion fest, um die angegebenen Ereignisse zu behandeln. Clients können die gleiche Hook-Funktion verwenden, um mehrere Arten von Ereignissen zu verarbeiten, oder Sie können mehrere-Hook-Funktionen verwenden. Clients wird **setwineventhook** einmal für jede Hook-Funktion aufgerufen, die Sie registrieren müssen.

Hook-Funktionen befinden sich im Code Körper des Clients, in einer DLL, die dem Client Prozess zugeordnet ist, oder in einer DLL, die dem Server Prozess zugeordnet ist. Jede dieser Methoden hat vor-und Nachteile. Weitere Informationen finden Sie unter [Kontext übergreifende und Out-of-Context-Hook-Funktionen](in-context-and-out-of-context-hook-functions.md).

Zum Benachrichtigen von Clients über ein Ereignis auftreten, wird " [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)" aufgerufen. Das System überprüft, ob Client Anwendungen Hook-Funktionen für das Ereignis festgelegt haben, und ruft bei Bedarf die entsprechenden Hook-Funktionen auf.

Wenn die Hook-Funktion des Clients aufgerufen wird, empfängt Sie eine Reihe von Parametern, die das Ereignis und das Objekt beschreiben, das das Ereignis generiert hat. Um Zugriff auf das Objekt zu erhalten, das das Ereignis generiert hat, ruft die Client-Hook-Funktion [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent)auf.

> [!NOTE]
> Wenn keine Clients für den Empfang von WinEvents registriert sind, ist die Auswirkungen auf die Leistung eines Servers zum Aufrufen von [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) unerheblich.
>
> Server wenden [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent) für Änderungen nur in ihren eigenen zugänglichen Objekten an. Sie werden für Änderungen an vom System bereitgestellten Benutzeroberflächen Elementen nicht als **NotifyWinEvent** bezeichnet.

## <a name="event-driven-communication"></a>Event-Driven Kommunikation

Clients müssen einen WinEvent-Hook registrieren, bevor Sie WinEvent-Benachrichtigungen empfangen können. Um unnötige Rückrufe zu vermeiden und die Leistung zu verbessern, wird empfohlen, nur für die Ereignisse zu registrieren, die Sie empfangen müssen.

Innerhalb der Hook-Prozedur kann der Client [**accessibleobjectfromevent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) aufrufen, um ein [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) -Objekt für das Element abzurufen, auf das das Ereignis angewendet wird. Mit diesem Objekt kann der Client mit dem Aufrufen von **IAccessible** -Methoden beginnen, um Informationen abzurufen oder mit dem UI-Element zu interagieren.

## <a name="related-topics"></a>Zugehörige Themen

[WinEvents](winevents-infrastructure.md)
