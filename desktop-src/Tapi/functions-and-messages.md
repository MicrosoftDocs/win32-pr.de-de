---
description: Die phonedevspecific-Funktion und die zugehörige Phone \_ DevSpecific-Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefon Features, die über die gemeinsamen Telefoniedienste für Smartphones nicht verfügbar sind.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funktionen und Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292f85e2ea57ac11da8150d4d0a183c7c4fd2c88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959715"
---
# <a name="functions-and-messages"></a>Funktionen und Nachrichten

Die [**phonedevspecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) -Funktion und die zugehörige [**Phone \_ DevSpecific**](phone-devspecific.md) -Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefon Features, die über die gemeinsamen Telefoniedienste für Smartphones nicht verfügbar sind. Mit anderen Worten: **phonedevspecific** ist die gerätespezifische Escape-Funktion, die Hersteller abhängige Erweiterungen zulässt, und Phone \_ DevSpecific ist die gerätespezifische Nachricht, die an die Anwendung gesendet wird.

Das Parameter Profil der [**phonedevspecific**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) -Funktion ist generisch, da die Parameter von TAPI nicht interpretiert werden. Stattdessen wird die Interpretation der Parameter vom Dienstanbieter definiert und muss von einer Anwendung verstanden werden, die Sie verwendet. Die Parameter werden einfach von TAPI von der Anwendung an den Dienstanbieter übermittelt. Eine Anwendung, die auf gerätespezifischen Erweiterungen basiert, funktioniert in der Regel nicht mit anderen Dienstanbietern, aber Anwendungen, die in die üblichen Telefoniedienste geschrieben werden, funktionieren mit dem erweiterten Dienstanbieter.

 

 



