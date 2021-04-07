---
title: Starten einer ausführbaren Datei beim System Start
description: Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn ein System gestartet wird, definieren Sie einen Start-und eine ausführbare Aktion.
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- Taskplaner Beispiele Taskplaner, Start-Auslösers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103712576"
---
# <a name="starting-an-executable-on-system-boot"></a>Starten einer ausführbaren Datei beim System Start

Wenn Sie eine Aufgabe schreiben, die eine ausführbare Datei startet, wenn ein System gestartet wird, definieren Sie einen Start-und eine ausführbare Aktion.

## <a name="boot-trigger"></a>Start-auslöst

Start Trigger werden über die Start Grenze aktiviert, starten die ausführbare Datei jedoch erst, wenn das System gestartet wird. Sie können auch eine Verzögerungszeit im Start-Fehler angeben, die den Zeitraum zwischen dem Start des Systems und dem Start der Aufgabe angibt. Dies wird durch die [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay) -Eigenschaft in der [**iboottrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger) -Schnittstelle ([**boottrigger**](boottrigger.md) -Objekt für die Skripterstellung) definiert.

## <a name="boot-trigger-examples"></a>Beispiele für Start Beispiele

In den folgenden Beispielen wird Notepad gestartet, nachdem das System gestartet wurde:

-   [Beispiel für einen Start-Beispiel (Skripterstellung)](boot-trigger-example--scripting-.md)
-   [Beispiel für einen Start Auslösers (C++)](boot-trigger-example--c---.md)
-   [Beispiel für einen Start Auslösers (XML)](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden des Taskplaner](using-the-task-scheduler.md)
</dt> </dl>

 

 




