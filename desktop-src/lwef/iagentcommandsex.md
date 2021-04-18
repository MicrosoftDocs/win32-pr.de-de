---
title: Iagentcommandsex
description: Iagentcommandsex
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d16616ccb86bf109dad85a8ee2ac5d2bd009827
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106338059"
---
# <a name="iagentcommandsex"></a>Iagentcommandsex

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

[**Iagentcommandsex**](iagentcommandex.md) definiert eine Schnittstelle, die die [**iagentcommands**](iagentcommands.md) -Schnittstelle erweitert.

**Methoden in Vtable-Reihenfolge**



| Iagentcommandsex-Methoden                                                             | BESCHREIBUNG                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [Setdefaultid](iagentcommandsex--setdefaultid.md)                                   | Legt den Standardbefehl für das Popup Menü des Zeichens fest.                                                     |
| [Getdefaultid](iagentcommandsex--getdefaultid.md)                                   | Gibt den Standardbefehl für das Popup Menü des Zeichens zurück.                                                  |
| [**"Setup"**](iagentcommandex--sethelpcontextid.md)                        | Legt die kontextabhängige Hilfe Themen-ID für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt fest.                     |
| [**Gethelpcontextid**](iagentcommandex--gethelpcontextid.md)                        | Gibt die kontextbezogene Hilfe Themen-ID für ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt zurück.                  |
| [Setfontname](iagentcommandsex--setfontname.md)                                     | Legt die Schriftart fest, die im Popupmenü des Zeichens verwendet werden soll.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Gibt die Schriftart zurück, die im Popupmenü des Zeichens verwendet wird.                                                         |
| [SetFontSize](iagentcommandsex--setfontsize.md)                                     | Legt den Schrift Grad fest, der im Popupmenü des Zeichens verwendet werden soll.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Gibt den im Popupmenü des Zeichens verwendeten Schrift Grad zurück.                                                    |
| [**Setvoicecaption**](iagentcommandex--setvoicecaption.md)                          | Legt die sprach Beschriftung für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt des Zeichens fest.                         |
| [**Getvoicecaption**](iagentcommandex--getvoicecaption.md)                          | Gibt die sprach Beschriftung für das [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt des Zeichens zurück.                      |
| [Addex](iagentcommandsex--addex.md)                                                 | Fügt [**einer Befehls**](/windows/desktop/lwef/the-commands-collection-object) Auflistung ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt hinzu.    |
| [Insertex](iagentcommandsex--insertex.md)                                           | Fügt ein [**Befehls**](/windows/desktop/lwef/the-command-object) Objekt in eine [**Commands**](/windows/desktop/lwef/the-commands-collection-object) -Auflistung ein. |
| [Setglobalvoicecommandsenabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Aktiviert die Sprachgrammatik für die globalen Befehle des Agents.                                                        |
| [Getglobalvoicecommandsenabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Gibt zurück, ob die Sprachgrammatik für die globalen Befehle des Agents aktiviert ist.                                     |



 

 

 