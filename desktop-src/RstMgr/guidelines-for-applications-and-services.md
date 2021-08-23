---
title: Richtlinien für Anwendungen und Dienste
description: Um die Anzahl von Systemneustarts beim Installieren und Warten von Anwendungen unter Windows Vista oder Windows Server 2008 zu reduzieren, sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst sauber heruntergefahren und neu gestartet werden kann.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1d4aa10da60ca5019a723ec996532ac5b60fdbfcdb7c322ff07ecbf8681f37b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010158"
---
# <a name="guidelines-for-applications-and-services"></a>Richtlinien für Anwendungen und Dienste

Um die Anzahl von Systemneustarts beim Installieren und Warten von Anwendungen unter Windows Vista oder Windows Server 2008 zu reduzieren, sollten Sie die folgenden Richtlinien beachten, damit Ihre Anwendung oder Ihr Dienst sauber heruntergefahren und neu gestartet werden kann.

-   Ihre Anwendungen und Dienste sollten darauf vorbereitet sein, vom System heruntergefahren und neu gestartet zu werden, wenn dies zum Installieren eines Updates erforderlich ist. Wenn ein Update installiert wird, muss in der Regel eine Anwendung oder ein Dienst heruntergefahren werden, da derzeit eine betroffene Datei verwendet wird. Alle Anwendungen oder Dienste, die eine Während eines Updates verwendete Datei speichern können, sollten auf ein sauberes Herunterfahren vorbereitet werden.
-   Ihre Anwendungen sollten Benutzerdaten und Zustandsinformationen speichern, die nach einem Neustart benötigt werden, und die Richtlinien einhalten, die im Abschnitt Richtlinien für [Anwendungen beschrieben sind.](guidelines-for-applications.md)
-   Ihre Dienste sollten die Richtlinien einhalten, die im Abschnitt [Richtlinien für Dienste beschrieben werden.](guidelines-for-services.md)
-   Der Neustart-Manager fährt wichtige [Systemdienste nicht herunter.](critical-system-services.md) Daher sollten diese Dienste die Anzahl der DLLs begrenzen, von denen sie abhängen.

 

 




