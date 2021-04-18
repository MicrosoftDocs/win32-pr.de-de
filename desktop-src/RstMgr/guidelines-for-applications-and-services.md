---
title: Richtlinien für Anwendungen und Dienste
description: Zum Reduzieren der Anzahl der Systemneustarts bei der Installation und Wartung von Anwendungen unter Windows Vista oder Windows Server 2008 sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst ordnungsgemäß heruntergefahren und neu gestartet werden kann.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106341642"
---
# <a name="guidelines-for-applications-and-services"></a>Richtlinien für Anwendungen und Dienste

Zum Reduzieren der Anzahl der Systemneustarts bei der Installation und Wartung von Anwendungen unter Windows Vista oder Windows Server 2008 sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst ordnungsgemäß heruntergefahren und neu gestartet werden kann.

-   Ihre Anwendungen und Dienste sollten so vorbereitet werden, dass Sie vom System heruntergefahren und neu gestartet werden, wenn dies für die Installation eines Updates erforderlich ist. Wenn ein Update installiert wird, muss in der Regel eine Anwendung oder ein Dienst heruntergefahren werden, da zurzeit eine betroffene Datei verwendet wird. Alle Anwendungen oder Dienste, die eine Datei enthalten können, die während eines Updates verwendet wird, sollten ordnungsgemäß heruntergefahren werden.
-   Ihre Anwendungen sollten Benutzerdaten und Zustandsinformationen speichern, die nach einem Neustart benötigt werden, und die Richtlinien befolgen, die im Abschnitt [Richtlinien für Anwendungen](guidelines-for-applications.md)beschrieben werden.
-   Ihre Dienste sollten den Richtlinien entsprechen, die im Abschnitt [Richtlinien für Dienste](guidelines-for-services.md)beschrieben werden.
-   Mit dem Neustart-Manager werden [wichtige Systemdienste](critical-system-services.md)nicht heruntergefahren. Daher sollten diese Dienste die Anzahl der DLLs begrenzen, von denen Sie abhängen.

 

 




