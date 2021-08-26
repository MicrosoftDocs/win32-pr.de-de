---
title: Starten einer ausführbaren Datei beim Registrieren eines Tasks
description: Das Schreiben einer Aufgabe, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, erfolgt durch Definieren eines Registrierungstriggers und einer ausführbaren Aktion.
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- Taskplaner Beispiele Taskplaner , Registrierungstrigger
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6a051c820a1099828ae0ee123e4241ec42d6edbb23ce9e98275057b5903dfbc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120033950"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>Starten einer ausführbaren Datei beim Registrieren eines Tasks

Das Schreiben einer Aufgabe, die eine ausführbare Datei startet, wenn eine Aufgabe registriert wird, erfolgt durch Definieren eines Registrierungstriggers und einer ausführbaren Aktion.

## <a name="registration-trigger"></a>Registrierungstrigger

Registrierungstrigger starten eine Aufgabe, sobald sie registriert ist. Sie können auch eine Verzögerung für den Registrierungstrigger angeben, der eine Aufgabe nach einer bestimmten Zeitspanne (der Verzögerung) startet, nachdem der Task registriert wurde. Die Verzögerung wird in der [**Delay-Eigenschaft**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay) der [**IRegistrationTrigger-Schnittstelle**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger) [**(RegistrationTrigger**](registrationtrigger.md) für Skripterstellung) angegeben.

> [!Note]  
> Wenn eine Aufgabe mit einem Registrierungstrigger aktualisiert wird, wird der Task nach dem Update ausgeführt.

 

## <a name="registration-trigger-examples"></a>Beispiele für Registrierungstrigger

Die folgenden Beispiele beginnen Editor, wenn eine Aufgabe registriert wird:

-   [Beispiel für Registrierungstrigger (Skripterstellung)](registration-trigger-example--scripting-.md)
-   [Beispiel für registrierungstrigger (C++)](registration-trigger-example--c---.md)
-   [Registration Trigger Example (XML) (Beispiel für Registrierungstrigger (XML))](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden der Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




