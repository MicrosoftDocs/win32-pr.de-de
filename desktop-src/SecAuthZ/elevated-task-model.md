---
description: Eine Anwendung, die als Standardbenutzer ausgeführt wird, führt Vorgänge aus, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.
ms.assetid: cd7485b3-6be5-4163-9a86-7892dbc59181
title: Modell mit erhöhten Rechten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27006e32210cfea05de5c2b3b9adf36613dc4f5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104348929"
---
# <a name="elevated-task-model"></a>Modell mit erhöhten Rechten

Im Modell mit erhöhten Rechten führt eine Anwendung, die als Standardbenutzer ausgeführt wird, Vorgänge durch, die Administratorrechte erfordern, indem eine geplante Aufgabe gestartet wird.

**Windows Server 2003 und Windows XP:** Das Modell mit erhöhten Rechten wird nicht unterstützt.

Tasks verbrauchen nicht so viele Systemressourcen wie Dienste, und Aufgaben werden nach Abschluss des Vorgangs automatisch geschlossen. Sie sollten dieses Modell anstelle des [Betriebs System-Dienst Modells](operating-system-service-model.md) verwenden, es sei denn, es ist Abwärtskompatibilität mit früheren Betriebssystemen erforderlich.

Die folgenden Bedingungen müssen erfüllt sein, um eine Aufgabe zum Ausführen privilegierter Vorgänge für eine Standardbenutzer Anwendung zu verwenden:

-   Der Task muss auf " **System** ausführen" festgelegt werden.
-   Die [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly) , die dem Task zugeordnet ist, muss so konfiguriert werden, dass Standardbenutzer die Aufgabe starten können.
-   Der Taskplaner-Dienst muss ausgeführt werden.

Weitere Informationen zum Erstellen und starten von Aufgaben finden Sie unter [Taskplaner](/windows/desktop/TaskSchd/task-scheduler-start-page).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Anwendungen, für die Administrator Rechte erforderlich sind](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[Administrator Broker Modell](administrator-broker-model.md)
</dt> <dt>

[COM-Objektmodell für Administratoren](administrator-com-object-model.md)
</dt> <dt>

[Betriebs System-Dienstmodell](operating-system-service-model.md)
</dt> </dl>

 

 
