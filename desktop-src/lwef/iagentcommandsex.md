---
title: IAgentCommandsEx
description: IAgentCommandsEx
ms.assetid: 6c354677-4cdb-4a74-9c41-2d0bf6f8dd55
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4ff8e6dc87eb1a5fa5c3e79fe26b00d8bd3c8eb18a5fc6ca7cac22d3dfd07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118976260"
---
# <a name="iagentcommandsex"></a>IAgentCommandsEx

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

[**IAgentCommandsEx**](iagentcommandex.md) definiert eine Schnittstelle, die die [**IAgentCommands-Schnittstelle**](iagentcommands.md) erweitert.

**Methoden in Vtable-Reihenfolge**



| IAgentCommandsEx-Methoden                                                             | Beschreibung                                                                                                   |
|--------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [SetDefaultID](iagentcommandsex--setdefaultid.md)                                   | Legt den Standardbefehl für das Popupmenü des Zeichens fest.                                                     |
| [GetDefaultID](iagentcommandsex--getdefaultid.md)                                   | Gibt den Standardbefehl für das Popupmenü des Zeichens zurück.                                                  |
| [**SetHelpContextID**](iagentcommandex--sethelpcontextid.md)                        | Legt die kontextbezogene Hilfethema-ID für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) fest.                     |
| [**GetHelpContextID**](iagentcommandex--gethelpcontextid.md)                        | Gibt die kontextbezogene Hilfethema-ID für ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) zurück.                  |
| [SetFontName](iagentcommandsex--setfontname.md)                                     | Legt die Schriftart fest, die im Popupmenü des Zeichens verwendet werden soll.                                                          |
| [GetFontName](iagentcommandsex--getfontname.md)                                     | Gibt die Schriftart zurück, die im Popupmenü des Zeichens verwendet wird.                                                         |
| [Formattedtext.setfontsize](iagentcommandsex--setfontsize.md)                                     | Legt den Schriftgrad fest, der im Popupmenü des Zeichens verwendet werden soll.                                                     |
| [GetFontSize](iagentcommandsex--getfontsize.md)                                     | Gibt den Schriftgrad zurück, der im Popupmenü des Zeichens verwendet wird.                                                    |
| [**SetVoiceCaption**](iagentcommandex--setvoicecaption.md)                          | Legt die Sprachbeschriftung für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) des Zeichens fest.                         |
| [**GetVoiceCaption**](iagentcommandex--getvoicecaption.md)                          | Gibt die Sprachbeschriftung für das [**Command-Objekt**](/windows/desktop/lwef/the-command-object) des Zeichens zurück.                      |
| [AddEx](iagentcommandsex--addex.md)                                                 | Fügt einer [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) hinzu.    |
| [InsertEx](iagentcommandsex--insertex.md)                                           | Fügt ein [**Command-Objekt**](/windows/desktop/lwef/the-command-object) in eine [**Commands-Auflistung**](/windows/desktop/lwef/the-commands-collection-object) ein. |
| [SetGlobalVoiceCommandsEnabled](iagentcommandsex--setglobalvoicecommandsenabled.md) | Aktiviert die Sprachgrammatik für globale Befehle des -Agents.                                                        |
| [GetGlobalVoiceCommandsEnabled](iagentcommandsex--getglobalvoicecommandsenabled.md) | Gibt zurück, ob die Sprachgrammatik für die globalen Befehle des -Agents aktiviert ist.                                     |



 

 

 