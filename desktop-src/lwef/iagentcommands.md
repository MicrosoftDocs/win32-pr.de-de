---
title: Iagentcommands
description: Iagentcommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1fc57b7e2e5f628708f46ace98700605f1eb5d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516763"
---
# <a name="iagentcommands"></a>Iagentcommands

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Der Microsoft-Agent-Server verwaltet eine Liste der Befehle, die dem Benutzer zurzeit zur Verfügung stehen. Diese Liste enthält Befehle, die der Server für allgemeine Interaktionen definiert, wie z. b. die Eigenschaften Hide und Microsoft Agent, die Liste der verfügbaren (aber nicht Eingabe aktiven) Clients und die Befehle, die vom aktuellen aktiven Client definiert werden. Die ersten beiden Befehls Sätze sind globale Befehle. Das heißt, Sie sind unabhängig vom eingegebenen aktiven Client jederzeit verfügbar. Client definierte Befehle sind nur verfügbar, wenn der Client aktiv ist.

Rufen Sie eine **iagentcommands** -Schnittstelle ab, indem Sie die [**iagentcharacter**](https://www.bing.com/search?q=**IAgentCharacter**) -Schnittstelle für **iagentcommands** Abfragen. Jede Microsoft-Agent-Client Anwendung kann eine Auflistung von Befehlen definieren, die als [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung bezeichnet werden. Um der Auflistung einen [**Befehl**](/windows/desktop/lwef/the-command-object) hinzuzufügen, verwenden [**Sie die Add**](add-method.md) -oder [**Insert**](insert-method.md) -Methode. Obwohl Sie die Eigenschaften eines **Befehls** mithilfe von [**iagentcommand**](iagentcommand.md) -Methoden angeben können, geben Sie für optimale Code Leistung alle Eigenschaften eines **Befehls** in der [**iagentcommands:: Add**](iagentcommands--add.md) -Methode oder der [**iagentcommands:: Insert**](iagentcommands--insert.md) -Methode an, wenn Sie die Eigenschaften für einen neuen **Befehl** anfänglich festlegen. Sie können die **iagentcommand** -Methoden verwenden, um die Eigenschaften Einstellungen abzufragen oder zu ändern.

Sie können für jeden [**Befehl**](/windows/desktop/lwef/the-command-object) in der [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung bestimmen, ob der Befehl im Popup Menü des Zeichens, im Fenster "Sprachbefehle", in beiden oder in keinem von angezeigt wird. Wenn z. b. ein Befehl im Popup Menü für das Zeichen angezeigt werden soll, legen Sie die [**Beschriftung**](caption-property.md) des Befehls und die [**sichtbaren**](visible-property.md) Eigenschaften fest. Um den Befehl im Fenster " **Sprachbefehle**" anzuzeigen, legen Sie die **Beschriftungs** -und [**sprach**](voice-property.md) Eigenschaften des Befehls fest.

Ein Benutzer kann nur auf die einzelnen Befehle in der Commands-Auflistung zugreifen, wenn die Client Anwendung aktiv ist und das Zeichen sichtbar ist. Daher sollten Sie in der Regel die [**Beschriftungs**](caption-property.md)-, [**voicecaption**](voicecaption-property.md)-und [**Voice**](voice-property.md) -Eigenschaften für das [**Commands**](/windows/desktop/lwef/the-commands-collection-object) Collection-Objekt sowie für die Befehle in der Auflistung festlegen, da dadurch ein Eintrag für die **Commands** -Auflistung im Popupmenü eines Zeichens und im Fenster "Sprachbefehle" eingefügt wird. Wenn der Benutzer durch Klicken auf den zugehörigen **Befehls** Eintrag zu Ihrem Client wechselt, wird der Client automatisch von dem Server in den Client eingegeben, und die Client Anwendung wird mithilfe von [**iagentnotifysink:: activateinputstate**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) benachrichtigt, sodass die **Befehle** in der zugehörigen Auflistung verfügbar sind. Der Server benachrichtigt auch den Client, dass er nicht mehr mit dem **iagentnotifysink:: activateinputstate** -Ereignis aktiv ist. Dies ermöglicht es dem Server, nur die **Befehle** anzuzeigen und zu akzeptieren, die auf den Kontext des aktuellen Eingabe aktiven Clients angewendet werden. Es dient auch zur Vermeidung von Konflikten mit [**Befehls**](/windows/desktop/lwef/the-command-object)Namen zwischen Clients.

Ein Client kann mit der [**iagentcharacter:: Aktivierungs**](iagentcharacter--activate.md) -Methode auch explizit die Eingabe des aktiven Clients anfordern. Diese Methode unterstützt auch das festlegen, dass die Anwendung nicht der Eingabe aktive Client ist. Möglicherweise möchten Sie diese Methode verwenden, wenn Sie ein Zeichen mit einer anderen Anwendung freigeben und die Anwendung als Eingabe aktiv festlegen, wenn das Anwendungsfenster den Fokus erhält und nicht Eingabe aktiv ist, wenn es den Fokus verliert.

Auf ähnliche Weise können Sie [**iagentcharacter:: Aktivierung**](iagentcharacter--activate.md) verwenden, um die Anwendung auf den aktiven Client des Zeichens festzulegen (oder nicht). Der aktive Client ist der Client, der Eingaben empfängt, wenn sein Zeichen das oberste Zeichen ist. Wenn sich dieser Status ändert, benachrichtigt der Server Ihre Anwendung mit dem [**iagentnotifysinkex:: activeclientchange**](iagentnotifysinkex--activeclientchange.md) -Ereignis.

Wenn das Popup Menü eines Zeichens angezeigt wird, werden Änderungen an den Eigenschaften einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung oder die Befehle in der Auflistung erst angezeigt, wenn der Benutzer das Menü erneut anzeigt. Wenn Sie jedoch geöffnet ist, zeigt das Fenster "Sprachbefehle" Änderungen an, sobald sie auftreten.

**Iagentcommands** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Eigenschaften für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung hinzuzufügen, zu entfernen, festzulegen und abzufragen. Diese Funktionen sind auch über [**iagentcommandsex**](iagentcommandsex.md)verfügbar.

Eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung kann als Befehl im Popup Menü und im Fenster "Sprachbefehle" für ein Zeichen angezeigt werden. Damit die **Befehls** Auflistung angezeigt wird, müssen Sie die [**Beschriftung**](caption-property.md) -Eigenschaft festlegen. In der folgenden Tabelle wird zusammengefasst, wie die Eigenschaften einer **Befehls** Auflistung die Darstellung beeinflussen.



| Caption-Eigenschaft | Voice-Caption-Eigenschaft | Voice-Eigenschaft | Visible-Eigenschaft | Wird im Popupmenü des Zeichens angezeigt.             | Wird im Fenster "Sprachbefehle" angezeigt                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Ja              | Ja                    | Ja            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Ja, mit [ **voicecaption**](voicecaption-property.md) |
| Ja              | Ja                    | Nein ¹            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Nein                                                       |
| Ja              | Ja                    | Ja            | False            | Nein                                             | Ja, mit [ **voicecaption**](voicecaption-property.md) |
| Ja              | Ja                    | Nein ¹            | False            | Nein                                             | Nein                                                       |
| Nein ¹              | Ja                    | Ja            | True             | Nein                                             | Ja, mit [ **voicecaption**](voicecaption-property.md) |
| Nein ¹              | Ja                    | Ja            | False            | Nein                                             | Ja, mit [ **voicecaption**](voicecaption-property.md) |
| Nein ¹              | Ja                    | Nein ¹            | True             | Nein                                             | Nein                                                       |
| Nein ¹              | Ja                    | Nein ¹            | False            | Nein                                             | Nein                                                       |
| Ja              | Nein ¹                    | Ja            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Ja, mit [ **Beschriftung**](caption-property.md)           |
| Ja              | Nein ¹                    | Nein ¹            | True             | Ja                                            | Nein                                                       |
| Ja              | Nein ¹                    | Ja            | False            | Nein                                             | Ja, mit [ **Beschriftung**](caption-property.md)           |
| Ja              | Nein ¹                    | Nein ¹            | False            | Nein                                             | Nein                                                       |
| Nein ¹              | Nein ¹                    | Ja            | True             | Nein                                             | Nein²                                                      |
| Nein ¹              | Nein ¹                    | Ja            | False            | Nein                                             | Nein²                                                      |
| Nein ¹              | Nein ¹                    | Nein ¹            | True             | Nein                                             | Nein                                                       |
| Nein ¹              | Nein ¹                    | Nein ¹            | False            | Nein                                             | Nein                                                       |



 

¹, wenn die Eigenschafts Einstellung NULL ist. In manchen Programmiersprachen kann eine leere Zeichenfolge nicht wie eine NULL-Zeichenfolge interpretiert werden.

² der Befehl ist weiterhin sprach zugänglich.

**Methoden in Vtable-Reihenfolge**



| Iagentcommands-Methoden                           | BESCHREIBUNG                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Ruft ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt aus der [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ab.              |
| [**GetCount**](iagentcommands--getcount.md)     | Gibt den Wert der Anzahl von [**Befehlen**](/windows/desktop/lwef/the-command-object) in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück. |
| [**SetCaption**](iagentcommands--setcaption.md) | Legt den Wert der [**Caption**](caption-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.    |
| [**Getcaption**](iagentcommands--getcaption.md) | Gibt den Wert der [**Caption**](caption-property.md) -Eigenschaft einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück.  |
| [**Setvoice**](iagentcommands--setvoice.md)     | Legt den Wert der [**Voice**](voice-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.        |
| [**Getvoice**](iagentcommands--getvoice.md)     | Gibt den Wert der [**Voice**](voice-property.md) -Eigenschaft einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück.      |
| [**SetVisible**](iagentcommands--setvisible.md) | Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung fest.    |
| [**GetVisible**](iagentcommands--getvisible.md) | Gibt den Wert der [**Visible**](visible-property.md) -Eigenschaft einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung zurück.  |
| [**Hinzufügen**](iagentcommands--add.md)               | Fügt [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt hinzu.                       |
| [**Setze**](iagentcommands--insert.md)         | Fügt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ein.                    |
| [**Aufgeh**](iagentcommands--remove.md)         | Entfernt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt [**in einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.                    |
| [**RemoveAll**](iagentcommands--removeall.md)   | Entfernt alle [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte aus einer [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung.               |



 

 

 