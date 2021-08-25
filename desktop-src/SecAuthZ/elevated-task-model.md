---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Aufgabenmodell mit erhöhten Rechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08aa485c47983760cc260a97cb52b58316a0d87bd4083d3ed09e72032f8fc7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119672320"
---
# <a name="elevated-task-model"></a>Aufgabenmodell mit erhöhten Rechten

Im Modell mit erhöhten Aufgaben führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge aus, für die Administratorrechte erforderlich sind, indem eine geplante Aufgabe gestartet wird.

**Windows Server 2003 und Windows XP:** Das Aufgabenmodell mit erhöhten Rechten wird nicht unterstützt.

Tasks verbrauchen nicht so viele Systemressourcen wie Dienste, und Tasks werden automatisch geschlossen, wenn sie abgeschlossen sind. Erwägen Sie die Verwendung dieses Modells anstelle des [Betriebssystemdienstmodells,](operating-system-service-model.md) sofern keine Abwärtskompatibilität mit früheren Betriebssystemen erforderlich ist.

Um eine Aufgabe zum Ausführen privilegierter Vorgänge für eine Standardbenutzeranwendung zu verwenden, müssen die folgenden Bedingungen erfüllt sein:

-   Der Task muss so festgelegt werden, dass er als **SYSTEM** ausgeführt wird.
-   Die dem Task zugeordnete [*Sicherheitsbeschreibung*](/windows/desktop/SecGloss/s-gly) muss so konfiguriert werden, dass Standardbenutzer die Aufgabe starten können.
-   Der Taskplanerdienst muss ausgeführt werden.

Informationen zum Erstellen und Starten von Aufgaben finden Sie unter [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, die Administratorrechte erfordern](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administrator Broker-Modell](administrator-broker-model.md)
</dt> <dt>

[COM-Objektmodell des Administrators](administrator-com-object-model.md)
</dt> <dt>

[Betriebssystemdienstmodell](operating-system-service-model.md)
</dt> </dl>

 

 
