---
title: IAgentCommand
description: IAgentCommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e2288a7b913becc54e2c0baa43eb14903e65fb7eddf6620d5cefbd78968026
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665480"
---
# <a name="iagentcommand"></a>IAgentCommand

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) ist ein Element in einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object) Der Server bietet dem Benutzer Zugriff auf Ihre Befehle, wenn Ihre Clientanwendung eingabeaktiv wird. Um einen **Befehl** abzurufen, rufen [**Sie IAgentCommands::GetCommand auf.**](iagentcommands--getcommand.md)

**IAgentCommand** definiert eine Schnittstelle, mit der Anwendungen Eigenschaften für [**Command-Objekte**](/windows/desktop/lwef/the-command-object) festlegen und abfragen können, die im Popupmenü eines Zeichens und im Fenster "Sprachbefehle" angezeigt werden können. Diese Funktionen sind auch über [**IAgentCommandEx**](iagentcommandex.md)verfügbar. Ein **Command-Objekt** ist ein Element in einer [**Commands-Auflistung.**](/windows/desktop/lwef/the-commands-collection-object) Der Server bietet dem Benutzer Zugriff auf Ihre Befehle, wenn Ihre Clientanwendung eingabeaktiv wird.

Ein [**Befehl**](/windows/desktop/lwef/the-command-object) kann entweder im Popupmenü des Zeichens oder im Fenster "Sprachbefehle" angezeigt werden. Um im Popupmenü angezeigt zu werden, muss eine [**Beschriftung**](caption-property.md) vorhanden sein, und die [**Visible-Eigenschaft**](visible-property.md) muss auf **True** festgelegt sein. Die **Visible-Eigenschaft** für das [**Commands-Auflistungsobjekt**](/windows/desktop/lwef/the-commands-collection-object) muss auch auf **True** festgelegt werden, damit der Befehl im Popupmenü angezeigt wird, wenn ihre Clientanwendung eingabeaktiv ist. Um im Fenster "Sprachbefehle" angezeigt zu werden, müssen für einen **Befehl** die Eigenschaften [**VoiceCaption**](voicecaption-property.md) und [**Voice**](voice-property.md) festgelegt sein. (Aus Gründen der Abwärtskompatibilität wird die **Einstellung Caption** verwendet, wenn keine **VoiceCaption** vorhanden ist.)

Die Popupmenüeinträge eines Zeichens ändern sich nicht, während das Menü angezeigt wird. Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, während das Popupmenü des Zeichens angezeigt wird, werden diese Änderungen im Menü angezeigt, wenn sie erneut angezeigt werden. Im Fenster "Sprachbefehle" werden jedoch Änderungen angezeigt, während Sie sie vornehmen.

In der folgenden Tabelle wird zusammengefasst, wie sich die Eigenschaften eines Befehls auf seine Darstellung auswirken.



| Caption-Eigenschaft | Voice-Caption-Eigenschaft | Voice-Eigenschaft | Visible-Eigenschaft | Wird im Popupmenü des Zeichens angezeigt.             | Wird im Fenster "Sprachbefehle" angezeigt                         |
|------------------|------------------------|----------------|------------------|------------------------------------------------|----------------------------------------------------------|
| Ja              | Ja                    | Ja            | True             | Ja, [ **beschriftungsbeschriftung**](caption-property.md) | Ja, mit [ **VoiceCaption**](voicecaption-property.md) |
| Ja              | Ja                    | Nein::            | True             | Ja, [ **beschriftungsbeschriftung**](caption-property.md) | Nein                                                       |
| Ja              | Ja                    | Ja            | False            | Nein                                             | Ja, mit [ **VoiceCaption**](voicecaption-property.md) |
| Ja              | Ja                    | Nein::            | False            | Nein                                             | Nein                                                       |
| Nein::              | Ja                    | Ja            | True             | Nein                                             | Ja, mit [ **VoiceCaption**](voicecaption-property.md) |
| Nein::              | Ja                    | Ja            | False            | Nein                                             | Ja, mit [ **VoiceCaption**](voicecaption-property.md) |
| Nein::              | Ja                    | Nein::            | True             | Nein                                             | Nein                                                       |
| Nein::              | Ja                    | Nein::            | False            | Nein                                             | Nein                                                       |
| Ja              | Nein::                    | Ja            | True             | Ja, [ **beschriftungsbeschriftung**](caption-property.md) | Ja, [ **beschriftungsbeschriftung**](caption-property.md)           |
| Ja              | Nein::                    | Nein::            | True             | Ja                                            | Nein                                                       |
| Ja              | Nein::                    | Ja            | False            | Nein                                             | Ja, [ **beschriftungsbeschriftung**](caption-property.md)           |
| Ja              | Nein::                    | Nein::            | False            | Nein                                             | Nein                                                       |
| Nein::              | Nein::                    | Ja            | True             | Nein                                             | Nein²                                                      |
| No.              | No.                    | Ja            | False            | Nein                                             | Nein²                                                      |
| No.              | No.                    | No.            | True             | Nein                                             | Nein                                                       |
| No.              | No.                    | No.            | False            | Nein                                             | Nein                                                       |



 

¹Wenn die Eigenschafteneinstellung NULL ist. In einigen Programmiersprachen kann eine leere Zeichenfolge nicht als identisch mit einer NULL-Zeichenfolge interpretiert werden.

4Der Befehl ist weiterhin sprachanzugebar.

Wenn Sie einen Befehl mit [](voice-property.md) [**einer**](/windows/desktop/lwef/the-command-object) Spracheinstellung [](caption-property.md) definieren,  definieren Sie im Allgemeinen auch Die Beschriftungs- und Spracheinstellungen für die zugehörige [**Commands-Sammlung.**](/windows/desktop/lwef/the-commands-collection-object) Wenn die Commands-Sammlung für eine  Gruppe von Befehlen keine Einstellung Voice oder  no **Caption** auf  hat und derzeit eingabeaktiv ist, die Befehle jedoch über Caption- und **Voice-Einstellungen** verfügen, werden die Befehle in der Strukturansicht des Sprachbefehlsfensters unter "(nicht definierter Befehl)" angezeigt, wenn Ihre Clientanwendung eingabeaktiv wird.  

Wenn der Server Eingaben empfängt, die einem der [**Command-Objekte**](/windows/desktop/lwef/the-command-object) entspricht, die Sie für Ihre [**Commands-Sammlung**](/windows/desktop/lwef/the-commands-collection-object) definiert haben, sendet er ein [**IAgentNotifySink::Command-Ereignis**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) und übergibt die ID des Befehls als Attribut des [**IAgentUserInput-Objekts**](https://www.bing.com/search?q=**IAgentUserInput**) zurück. Anschließend können Sie bedingte Anweisungen verwenden, um den Befehl zu finden und zu verarbeiten.

**Methoden in Vtable-Reihenfolge**



| IAgentCommand-Methoden                                                   | Beschreibung                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Legt den Wert für die [**Beschriftung für**](caption-property.md) ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.                         |
| [**GetCaption**](https://www.bing.com/search?q=**GetCaption**)                             | Gibt den Wert der [**Caption-Eigenschaft**](caption-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.               |
| [**SetVoice**](iagentcommand--setvoice.md)                             | Legt den Wert für den [**Sprachtext**](voice-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.                        |
| [**GetVoice**](iagentcommand--getvoice.md)                             | Gibt den Wert der [**Voice-Eigenschaft**](voice-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.                   |
| [**SetEnabled**](iagentcommand--setenabled.md)                         | Legt den Wert der [**Enabled-Eigenschaft**](enabled-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.                 |
| [**Getenabled**](iagentcommand--getenabled.md)                         | Gibt den Wert der [**Enabled-Eigenschaft**](enabled-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.               |
| [**Setvisible**](iagentcommand--setvisible.md)                         | Legt den Wert der [**Visible-Eigenschaft**](visible-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.                 |
| [**Getvisible**](iagentcommand--getvisible.md)                         | Gibt den Wert der [**Visible-Eigenschaft**](visible-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.               |
| [**SetConfidenceThreshold**](iagentcommand--setconfidencethreshold.md) | Legt den Wert der [**Confidence-Eigenschaft**](confidence-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.           |
| [**GetConfidenceThreshold**](iagentcommand--getconfidencethreshold.md) | Gibt den Wert der [**Confidence-Eigenschaft**](confidence-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.         |
| [**SetConfidenceText**](iagentcommand--setconfidencetext.md)           | Legt den Wert der [**ConfidenceText-Eigenschaft**](confidencetext-property.md) für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.   |
| [**getConfidenceText**](iagentcommand--getconfidencetext.md)           | Gibt den Wert der [**ConfidenceText-Eigenschaft**](confidencetext-property.md) eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück. |
| [**Getid**](iagentcommand--getid.md)                                   | Gibt die ID eines [**Command-Objekts**](/windows/desktop/lwef/the-command-object) zurück.                                                                      |



 

 

 