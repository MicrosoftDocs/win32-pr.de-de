---
title: Starten einer ausführbaren Datei, wenn eine Aufgabe registriert ist
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, definieren Sie einen Registrierungs-und eine ausführbare Aktion.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Taskplaner Beispiele Taskplaner, Registrierungs-Auslösung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947829"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Starten einer ausführbaren Datei, wenn eine Aufgabe registriert ist

Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, definieren Sie einen Registrierungs-und eine ausführbare Aktion.

## <a name="registration-trigger"></a>Registrierungs-auslöst

Registrierungs Trigger starten einen Task, sobald er registriert ist. Sie können auch eine Verzögerung für den Registrierungs-Auslösung angeben, die eine Aufgabe nach einem bestimmten Zeitraum (Verzögerung) nach der Registrierung des Tasks startet. Die Verzögerung wird in der [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) -Eigenschaft der [**iregistration-auslöserschnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) angegeben ([**Registration-Auslösers**](registrationtrigger.md) für die Skripterstellung).

> [!Note]  
> Wenn eine Aufgabe mit einem Registrierungs-ausgelöst wird, wird die Aufgabe ausgeführt, nachdem das Update ausgeführt wurde.

 

## <a name="registration-trigger-examples"></a>Beispiele für Registrierungs Beispiele

In den folgenden Beispielen wird Notepad gestartet, wenn ein Task registriert wird:

-   [Beispiel für Registrierungs Beispiel (Skripterstellung)](registration-trigger-example--scripting-.md)
-   [Registrierungs auslöserbeispiel (C++)](registration-trigger-example--c---.md)
-   [Registrierungs auslöserbeispiel (XML)](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




