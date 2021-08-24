---
description: Die phoneDevSpecific-Funktion und die zugehörige PHONE DEVSPECIFIC-Nachricht ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefonfunktionen, die über die allgemeinen Telefoniedienste für Telefone nicht verfügbar \_ sind.
ms.assetid: b4c8d721-26e4-4895-9f09-0f67fe4d346b
title: Funktionen und Meldungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cabdc271548e42b20de695296321f5f5ab0fdbe45a246be2b7ccb1993ee5d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660734"
---
# <a name="functions-and-messages"></a>Funktionen und Meldungen

Die [**phoneDevSpecific-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) und die zugehörige [**PHONE \_ DEVSPECIFIC-Nachricht**](phone-devspecific.md) ermöglichen einer Anwendung den Zugriff auf gerätespezifische Telefonfunktionen, die über die allgemeinen Telefoniedienste für Telefone nicht verfügbar sind. Anders ausgedrückt: **phoneDevSpecific** ist die gerätespezifische Escapefunktion, die anbieterabhängige Erweiterungen zulässt, und PHONE DEVSPECIFIC ist die gerätespezifische Nachricht, die an die Anwendung gesendet \_ wird.

Das Parameterprofil der [**phoneDevSpecific-Funktion**](/windows/desktop/api/Tapi/nf-tapi-phonedevspecific) ist generisch, da tapI nur eine geringe Interpretation der Parameter vorgibt. Stattdessen wird die Interpretation der Parameter vom Dienstanbieter definiert und muss von einer Anwendung verstanden werden, die sie verwendet. Die Parameter werden einfach von TAPI von der Anwendung an den Dienstanbieter übergeben. Eine Anwendung, die auf gerätespezifischen Erweiterungen basiert, funktioniert in der Regel nicht mit anderen Dienstanbietern, aber Anwendungen, die in die allgemeinen Telefonietelefondienste geschrieben werden, funktionieren mit dem erweiterten Dienstanbieter.

 

 



