---
title: IAgentCommands
description: IAgentCommands
ms.assetid: a171a2f0-7c1c-440f-9b19-28447cc68b95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a1bcc40f80e9a10301ec305fdc3e8f3e83984ceb0de5d36121e13c3d823b8a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119961890"
---
# <a name="iagentcommands"></a>IAgentCommands

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Der Microsoft Agent-Server verwaltet eine Liste von Befehlen, die dem Benutzer derzeit zur Verfügung stehen. Diese Liste enthält Befehle, die der Server für die allgemeine Interaktion definiert, z. B. Eigenschaften von Ausblenden und Microsoft-Agent, die Liste der verfügbaren Clients (aber nicht eingabeaktiv) und die vom aktuellen aktiven Client definierten Befehle. Die ersten beiden Befehlssätze sind globale Befehle. Das heißt, sie sind unabhängig vom eingabeaktiven Client jederzeit verfügbar. Clientdefinierte Befehle sind nur verfügbar, wenn dieser Client eingabeaktiv ist.

Rufen Sie **eine IAgentCommands-Schnittstelle** ab, indem Sie die [**IAgentCharacter-Schnittstelle**](https://www.bing.com/search?q=**IAgentCharacter**) für **IAgentCommands abfragen.** Jede Microsoft Agent-Clientanwendung kann eine Sammlung von Befehlen definieren, die als [**Commands-Sammlung bezeichnet**](/windows/desktop/lwef/the-commands-collection-object) wird. Um der Auflistung [**einen Befehl**](/windows/desktop/lwef/the-command-object) hinzuzufügen, verwenden Sie die [**Add- oder**](add-method.md) [**Insert-Methode.**](insert-method.md) Obwohl Sie die  Eigenschaften eines Befehls mithilfe von [**IAgentCommand-Methoden**](iagentcommand.md) angeben können, geben Sie für eine optimale Codeleistung alle Eigenschaften eines Befehls in den [**Methoden IAgentCommands::Add**](iagentcommands--add.md) oder [**IAgentCommands::Insert**](iagentcommands--insert.md) an, wenn Sie anfänglich die Eigenschaften für einen neuen **Befehl festlegen.** Sie können die **IAgentCommand-Methoden verwenden,** um die Eigenschafteneinstellungen abfragt oder zu ändern.

Für jeden [**Befehl**](/windows/desktop/lwef/the-command-object) in der [**Sammlung Befehle**](/windows/desktop/lwef/the-commands-collection-object) können Sie bestimmen, ob der Befehl im Popupmenü des Zeichens, im Fenster Sprachbefehle, in beiden oder in keiner der beiden Optionen angezeigt wird. Wenn beispielsweise ein Befehl im Popupmenü für das Zeichen angezeigt werden soll, legen Sie die Eigenschaften [**Caption**](caption-property.md) und Visible des [**Befehls**](visible-property.md) fest. Um den Befehl im Fenster Sprachbefehle **anzuzeigen,** legen Sie die Eigenschaften **Caption und** Voice des [**Befehls**](voice-property.md) fest.

Ein Benutzer kann nur dann auf die einzelnen Befehle in ihrer Commands-Sammlung zugreifen, wenn Ihre Clientanwendung eingabeaktiv ist und das Zeichen sichtbar ist. Daher sollten Sie in der Regel die Eigenschaften [**Caption**](caption-property.md), [**VoiceCaption**](voicecaption-property.md)und [**Voice**](voice-property.md) für das Commands-Sammlungsobjekt sowie für die Befehle in der Sammlung festlegen, da dadurch ein Eintrag für Ihre [](/windows/desktop/lwef/the-commands-collection-object) **Commands-Sammlung** im Popupmenü eines Zeichens und im Fenster für Sprachbefehle platziert wird. Wenn der Benutzer zu Ihrem Client  wechselt, indem er seinen Befehlseintrag auswählt, macht der Server die Clienteingabe automatisch aktiv, benachrichtigt Ihre Clientanwendung mithilfe von [**IAgentNotifySink::ActivateInputState**](https://www.bing.com/search?q=**IAgentNotifySink::ActivateInputState**) und macht die Befehle **in** der Sammlung verfügbar. Der Server benachrichtigt auch den Client, der nicht mehr eingabeaktiv ist, mit dem **IAgentNotifySink::ActivateInputState-Ereignis.** Dadurch kann der Server nur die  Befehle präsentieren und akzeptieren, die für den Kontext des aktuellen eingabeaktiven Clients gelten. Sie dient auch [](/windows/desktop/lwef/the-command-object)dazu, Command -name-Kollisionen zwischen Clients zu vermeiden.

Ein Client kann auch explizit anfordern, sich selbst mithilfe der [**IAgentCharacter::Activate-Methode**](iagentcharacter--activate.md) zum eingabeaktiven Client zu machen. Diese Methode unterstützt auch das Festlegen der Anwendung, dass sie nicht der eingabeaktive Client ist. Sie können diese Methode verwenden, wenn Sie ein Zeichen für eine andere Anwendung freigeben und die Anwendung so festlegen, dass sie eingabeaktiv ist, wenn ihr Anwendungsfenster den Fokus erhält, und nicht eingabeaktiv, wenn es den Fokus verliert.

Auf ähnliche Weise können Sie [**IAgentCharacter::Activate**](iagentcharacter--activate.md) verwenden, um ihre Anwendung auf den aktiven Client des Zeichens (oder nicht) zu setzen. Der aktive Client ist der Client, der Eingaben empfängt, wenn sein Zeichen das oberste Zeichen ist. Wenn sich dieser Status ändert, benachrichtigt der Server Ihre Anwendung mit dem [**IAgentNotifySinkEx::ActiveClientChange-Ereignis.**](iagentnotifysinkex--activeclientchange.md)

Wenn das Popupmenü eines Zeichens angezeigt wird, werden Änderungen an den Eigenschaften einer [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) oder an den Befehlen in der Sammlung erst angezeigt, wenn der Benutzer das Menü erneut einblendet. Wenn sie jedoch geöffnet sind, zeigt das Fenster "Sprachbefehle" Änderungen an, sobald sie vorgenommen werden.

**IAgentCommands definiert eine** Schnittstelle, mit der Anwendungen Eigenschaften für eine Commands-Sammlung hinzufügen, entfernen, festlegen [**und abfragen**](/windows/desktop/lwef/the-commands-collection-object) können. Diese Funktionen sind auch über [**IAgentCommandsEx verfügbar.**](iagentcommandsex.md)

Eine [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) kann sowohl im Popupmenü als auch im Fenster für Sprachbefehle für ein Zeichen als Befehl angezeigt werden. Damit die **Commands-Auflistung** angezeigt wird, müssen Sie deren [**Caption-Eigenschaft**](caption-property.md) festlegen. In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften einer **Commands-Auflistung** auf ihre Darstellung auswirken.



| Caption-Eigenschaft | Voice-Caption-Eigenschaft | Voice-Eigenschaft | Visible-Eigenschaft | Wird im Popupmenü des Zeichens angezeigt             | Wird im Fenster "Sprachbefehle" angezeigt                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Ja              | Ja                    | Ja            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Ja, verwenden [ **von VoiceCaption**](voicecaption-property.md) |
| Ja              | Ja                    | No.            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Nein                                                       |
| Ja              | Ja                    | Ja            | False            | Nein                                             | Ja, verwenden [ **von VoiceCaption**](voicecaption-property.md) |
| Ja              | Ja                    | No.            | False            | Nein                                             | Nein                                                       |
| No.              | Ja                    | Ja            | True             | Nein                                             | Ja, verwenden [ **von VoiceCaption**](voicecaption-property.md) |
| No.              | Ja                    | Ja            | False            | Nein                                             | Ja, verwenden [ **von VoiceCaption**](voicecaption-property.md) |
| No.              | Ja                    | No.            | True             | Nein                                             | Nein                                                       |
| No.              | Ja                    | No.            | False            | Nein                                             | Nein                                                       |
| Ja              | No.                    | Ja            | Richtig             | Ja, mit [ **Beschriftung**](caption-property.md) | Ja, mit [ **Beschriftung**](caption-property.md)           |
| Ja              | No.                    | No.            | True             | Ja                                            | Nein                                                       |
| Ja              | No.                    | Ja            | False            | Nein                                             | Ja, mit [ **Beschriftung**](caption-property.md)           |
| Ja              | No.                    | No.            | False            | Nein                                             | Nein                                                       |
| No.              | No.                    | Ja            | True             | Nein                                             | Nein²                                                      |
| No.              | No.                    | Ja            | False            | Nein                                             | Nein²                                                      |
| No.              | No.                    | No.            | True             | Nein                                             | Nein                                                       |
| No.              | No.                    | No.            | False            | Nein                                             | Nein                                                       |



 

¹Wenn die Eigenschafteneinstellung NULL ist. In einigen Programmiersprachen wird eine leere Zeichenfolge möglicherweise nicht wie eine NULL-Zeichenfolge interpretiert.

4Der Befehl ist weiterhin sprachanzugebar.

**Methoden in Vtable-Reihenfolge**



| IAgentCommands-Methoden                           | Beschreibung                                                                                                                      |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [**GetCommand**](iagentcommands--getcommand.md) | Ruft ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) aus der [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ab.              |
| [**GetCount**](iagentcommands--getcount.md)     | Gibt den Wert der Anzahl [](/windows/desktop/lwef/the-commands-collection-object) von Befehlen in einer [**Commands-Auflistung**](/windows/desktop/lwef/the-command-object) zurück. |
| [**SetCaption**](iagentcommands--setcaption.md) | Legt den Wert der [**Caption-Eigenschaft**](caption-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) fest.    |
| [**GetCaption**](iagentcommands--getcaption.md) | Gibt den Wert der [**Caption-Eigenschaft**](caption-property.md) einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) zurück.  |
| [**SetVoice**](iagentcommands--setvoice.md)     | Legt den Wert der [**Voice-Eigenschaft**](voice-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) fest.        |
| [**GetVoice**](iagentcommands--getvoice.md)     | Gibt den Wert der [**Voice-Eigenschaft**](voice-property.md) einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) zurück.      |
| [**Setvisible**](iagentcommands--setvisible.md) | Legt den Wert der [**Visible-Eigenschaft**](visible-property.md) für eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) fest.    |
| [**Getvisible**](iagentcommands--getvisible.md) | Gibt den Wert der [**Visible-Eigenschaft**](visible-property.md) einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) zurück.  |
| [**Add**](iagentcommands--add.md)               | Fügt einer [**Commands-Auflistung**](/windows/desktop/lwef/the-command-object) ein [**Command-Objekt**](/windows/desktop/lwef/the-commands-collection-object) hinzu.                       |
| [**Einfügen**](iagentcommands--insert.md)         | Fügt ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ein.                    |
| [**Entfernen**](iagentcommands--remove.md)         | Entfernt ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object)                    |
| [**Removeall**](iagentcommands--removeall.md)   | Entfernt alle [**Command-Objekte**](/windows/desktop/lwef/the-command-object) aus einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object)               |



 

 

 