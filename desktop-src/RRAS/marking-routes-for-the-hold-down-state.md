---
title: Markieren von Routen für den Hold-Down Zustand
description: Einige Clients, z. B. Entfernungsvektorprotokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 833f41da08c45d8f9bbe9419360f4d1857b2a52fb92ee0be341b56bc8362536e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790488"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Markieren von Routen für den Hold-Down Zustand

Einige Clients, z. B. Entfernungsvektorprotokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde. Die letzte gelöschte Route muss auch dann als nicht erreichbar angekündigt werden, wenn neuere Routen in der Zwischenzeit eintreffen. Die letzte gelöschte Route wird als *zurückhaltend markiert.* Der zurückhaltende Prozess verhindert die Bildung von Routingschleifen. Routingschleifen werden verursacht, wenn ein Routingprotokoll veraltete Routinginformationen angekündigt. Wenn das Zurückhalten abläuft, setzen diese Protokolle ihre Ankündigung mit der neuen besten Route wieder ein.

Ein Protokoll, das Zurückhaltungszustände implementiert, gibt an, dass sich ein Ziel mithilfe der [**RtmHoldDestination-Funktion**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) in einem Zurückhaltungszustand befindet. Der Client ruft diese Funktion auf, wenn er die beste Route zu diesem Ziel anklädt. Wenn alle Routen zu diesem Ziel später gelöscht werden, wird die letzte gelöschte Route für den zeitraum, der im früheren Aufruf von **RtmHoldDestination** angegeben wurde, in einem zurückgehaltenen Zustand gehalten.

Wenn ein Protokoll ein Ziel ank angekündigt, hängen die verwendeten Routeninformationen davon ab, ob das Protokoll zurückhaltende Zustände verwendet und ob eine Route im Zurückhalten-Zustand für das Ziel vorhanden ist.

Protokolle, die keine Zurückhalten-Zustände verwenden, können Routeninformationen ignorieren, die sich auf zurückhaltende Zustände für ein Ziel beziehen, und immer die beste Route ankn geben.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [Use the Route Hold-Down State](use-the-route-hold-down-state.md).

 

 




