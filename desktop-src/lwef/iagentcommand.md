---
title: Iagentcommand
description: Iagentcommand
ms.assetid: 70873093-df71-4377-9c39-c7528400052f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c4ba90f7d355a0baa088a78aa05b7a91e14112
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106341516"
---
# <a name="iagentcommand"></a>Iagentcommand

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt ist ein Element in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung. Der Server ermöglicht dem Benutzer den Zugriff auf Ihre Befehle, damit Ihre Client Anwendung aktiv wird. Rufen Sie zum Abrufen eines Befehls [**iagentcommands:: GetCommand**](iagentcommands--getcommand.md)auf.

**Iagentcommand** definiert eine Schnittstelle, die es Anwendungen ermöglicht, Eigenschaften für [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte festzulegen und abzufragen, die im Popupmenü eines Zeichens und im Fenster "Sprachbefehle" angezeigt werden können. Diese Funktionen sind auch über [**iagentcommandex**](iagentcommandex.md)verfügbar. Ein **Command** -Objekt ist ein Element in einer [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung. Der Server ermöglicht dem Benutzer den Zugriff auf Ihre Befehle, wenn die Client Anwendung aktiv wird.

Ein [**Befehl**](/windows/desktop/lwef/the-command-object) kann entweder in oder im Popupmenü des Zeichens und im Fenster "Sprachbefehle" angezeigt werden. Um im Popup Menü angezeigt zu werden, muss Sie über eine [**Beschriftung**](caption-property.md) verfügen, und die [**Visible**](visible-property.md) -Eigenschaft muss auf **true** festgelegt sein. Die **Visible** -Eigenschaft für das [**Befehle**](/windows/desktop/lwef/the-commands-collection-object) Collection-Objekt muss auch auf **true** festgelegt werden, damit der Befehl im Popup Menü angezeigt wird, wenn die Client Anwendung aktiv ist. Um im Fenster "Sprachbefehle" angezeigt zu werden, muss für einen **Befehl** die Eigenschaften [**voicecaption**](voicecaption-property.md) und [**Voice**](voice-property.md) festgelegt sein. (Aus Gründen der Abwärtskompatibilität wird die **Beschriftungs** Einstellung verwendet, wenn keine **voicecaption** vorhanden ist.)

Die Popup Menüeinträge eines Zeichens ändern sich nicht, während das Menü angezeigt wird. Wenn Sie Befehle hinzufügen oder entfernen oder deren Eigenschaften ändern, während das Popup Menü des Zeichens angezeigt wird, werden diese Änderungen im Menü angezeigt, wenn Sie erneut angezeigt werden. Das Fenster "Sprachbefehle" zeigt jedoch Änderungen an, während Sie Sie vornehmen.

In der folgenden Tabelle wird zusammengefasst, wie die Eigenschaften eines Befehls seine Darstellung beeinflussen.



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



 

¹, wenn die Eigenschafts Einstellung NULL ist. In manchen Programmiersprachen kann eine leere Zeichenfolge nicht als identisch mit einer NULL-Zeichenfolge interpretiert werden.

² der Befehl ist weiterhin sprach zugänglich.

Wenn Sie einen [**Befehl**](/windows/desktop/lwef/the-command-object) mit einer [**sprach**](voice-property.md) Einstellung definieren, definieren Sie im Allgemeinen auch die [**Beschriftungs**](caption-property.md) -und **sprach** Einstellungen für die zugeordnete [**Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung. Wenn die **Commands** -Auflistung für einen Satz von Befehlen keine **Stimme** oder keine **Beschriftungs** Einstellung hat und zurzeit aktiv ist, aber **die Befehle über** **Schriften-und** **sprach** Einstellungen verfügen, werden die **Befehle** in der Fenster Strukturansicht der Sprachbefehle unter "(nicht definierter Befehl)" angezeigt, wenn die Client Anwendung als Eingabe aktiv wird.

Wenn der Server Eingaben empfängt, die mit einem der [**Befehls**](/windows/desktop/lwef/the-command-object) Objekte übereinstimmen, die Sie für die [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung definiert haben, sendet er ein [**iagentnotifysink:: Command**](https://www.bing.com/search?q=**IAgentNotifySink::Command**) -Ereignis und übergibt die ID des Befehls als Attribut des [**iagentuserinput**](https://www.bing.com/search?q=**IAgentUserInput**) -Objekts zurück. Anschließend können Sie bedingte Anweisungen verwenden, um den Befehl abzugleichen und zu verarbeiten.

**Methoden in Vtable-Reihenfolge**



| Iagentcommand-Methoden                                                   | BESCHREIBUNG                                                                                                                         |
|-------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| [**SetCaption**](https://www.bing.com/search?q=**SetCaption**)                             | Legt den Wert für die [**Beschriftung**](caption-property.md) eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts fest.                         |
| [**Getcaption**](https://www.bing.com/search?q=**GetCaption**)                             | Gibt den Wert der [**Caption**](caption-property.md) -Eigenschaft eines [**Command**](/windows/desktop/lwef/the-command-object) -Objekts zurück.               |
| [**Setvoice**](iagentcommand--setvoice.md)                             | Legt den Wert für den [**sprach**](voice-property.md) Text eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts fest.                        |
| [**Getvoice**](iagentcommand--getvoice.md)                             | Gibt den Wert der [**Voice**](voice-property.md) -Eigenschaft eines [**Command**](/windows/desktop/lwef/the-command-object) -Objekts zurück.                   |
| [**Abgeleitete**](iagentcommand--setenabled.md)                         | Legt den Wert der [**aktivierten**](enabled-property.md) Eigenschaft für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt fest.                 |
| [**GetEnabled**](iagentcommand--getenabled.md)                         | Gibt den Wert der [**aktivierten**](enabled-property.md) Eigenschaft eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zurück.               |
| [**SetVisible**](iagentcommand--setvisible.md)                         | Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt fest.                 |
| [**GetVisible**](iagentcommand--getvisible.md)                         | Gibt den Wert der [**Visible**](visible-property.md) -Eigenschaft eines [**Command**](/windows/desktop/lwef/the-command-object) -Objekts zurück.               |
| [**Setconficethreshold**](iagentcommand--setconfidencethreshold.md) | Legt den Wert der Eigenschaft " [**Vertrauen**](confidence-property.md) " für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt fest.           |
| [**Getconficethreshold**](iagentcommand--getconfidencethreshold.md) | Gibt den Wert der Eigenschaft " [**Vertrauen**](confidence-property.md) " eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zurück.         |
| [**Setconficetext**](iagentcommand--setconfidencetext.md)           | Legt den Wert der [**conficetext**](confidencetext-property.md) -Eigenschaft für ein [**Command**](/windows/desktop/lwef/the-command-object) -Objekt fest.   |
| [**getconficetext**](iagentcommand--getconfidencetext.md)           | Gibt den Wert der [**conficetext**](confidencetext-property.md) -Eigenschaft eines [**Command**](/windows/desktop/lwef/the-command-object) -Objekts zurück. |
| [**GetId**](iagentcommand--getid.md)                                   | Gibt die ID eines [**Befehls**](/windows/desktop/lwef/the-command-object) Objekts zurück.                                                                      |



 

 

 