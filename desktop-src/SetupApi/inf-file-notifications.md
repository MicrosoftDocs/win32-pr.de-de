---
description: Die folgenden Benachrichtigungen werden mit den Funktionen "setupinstallfile", "setupinstallfileex" und "setupinstallfrominlosection" verwendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter Benachrichtigungen.
ms.assetid: 095cf4c9-3cb9-4b95-a8a2-9312c134e721
title: INF-Datei Benachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f58863d48c1af809c0cbbcdc2d625214a6e90a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959859"
---
# <a name="inf-file-notifications"></a>INF-Datei Benachrichtigungen

Die folgenden Benachrichtigungen werden mit den Funktionen " [**setupinstallfile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)", " [**setupinstallfileex**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfileexa)" und " [**setupinstallfrominlosection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) " verwendet. Weitere Informationen zum Format und zur Verwendung von Benachrichtigungen finden Sie unter [Benachrichtigungen](notifications.md).



| Benachrichtigung                                                      | Beschreibung                                                                            |
|-------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**\_spfilenotififileopverzögert**](spfilenotify-fileopdelayed.md) | Die Datei wird verwendet, und der aktuelle Vorgang wird verzögert, bis das System neu gestartet wird. |
| [**spfilenotify nicht übereinstimmende \_**](spfilenotify-langmismatch.md)   | Die Sprache der aktuellen Datei stimmt nicht mit der Systemsprache zusammen.                   |
| [**spfilenotify \_ targetexists**](spfilenotify-targetexists.md)   | Eine Kopie der angegebenen Datei ist bereits auf dem Ziel vorhanden.                             |
| [**spfilenotify \_ targetneuere**](spfilenotify-targetnewer.md)     | Eine neuere Version der angegebenen Datei ist auf dem Ziel vorhanden.                            |



 

> [!Note]  
> Da [**setupinstallfrominlosection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona) eine interne Datei Warteschlange erstellt und committet, verwendet Sie auch die [Benachrichtigungen der Datei Warteschlange](file-queue-notifications.md).

 

 

 



