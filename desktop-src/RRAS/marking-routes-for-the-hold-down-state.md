---
title: Markieren von Routen für den Hold-Down Status
description: Einige Clients, wie z. b. Entfernungs Vektor Protokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde.
ms.assetid: 2a86c092-d8a6-4fd4-8b2e-451c160f743f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af10832452a3a0b9ca851c209d240c97998ef519
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947809"
---
# <a name="marking-routes-for-the-hold-down-state"></a>Markieren von Routen für den Hold-Down Status

Einige Clients, wie z. b. Entfernungs Vektor Protokolle wie RIP und DVMRP, erfordern, dass Ziele für einen bestimmten Zeitraum als nicht erreichbar angekündigt werden, nachdem die letzte Route zum Ziel gelöscht wurde. Die letzte gelöschte Route muss als nicht erreichbar angekündigt werden, auch wenn in der Zwischenzeit neuere Routen eintreffen. Die letzte gelöschte Route ist als " *Hold-Down*" markiert. Der Hold-Down-Prozess verhindert die Bildung von Routing Schleifen. Routing Schleifen werden ausgelöst, wenn ein Routing Protokoll veraltete Routing Informationen auslöst. Wenn die Aufbewahrung abgelaufen ist, setzen diese Protokolle ihre Ankündigung mit der neuen optimalen Route fort.

Ein Protokoll, das Hold-Down-Zustände implementiert, gibt an, dass sich ein Ziel mithilfe der [**rtmholddestination**](/windows/desktop/api/Rtmv2/nf-rtmv2-rtmholddestination) -Funktion in einem Hold-Down-Zustand befindet. Der Client ruft diese Funktion auf, wenn die beste Route zu diesem Ziel angekündigt wird. Wenn alle Routen zu diesem Ziel später gelöscht werden, wird die letzte Route, die gelöscht wird, für den Zeitraum, der im vorherigen Aufruf von **rtmholddestination** angegeben ist, in einem Hold-Down-Zustand aufbewahrt.

Wenn ein Protokoll ein Ziel angekündigt hat, sind die verwendeten Routeninformationen davon abhängig, ob das Protokoll Hold-Down-Zustände verwendet und ob eine Route im Hold-Down-Zustand für das Ziel vorhanden ist.

Protokolle, die keine Hold-Down-Zustände verwenden, können Routeninformationen ignorieren, die sich auf den Hold-Down-Status für ein Ziel beziehen, und immer die beste Route ankündigen.

Beispielcode, der die Verwendung dieser Funktionen veranschaulicht, finden Sie unter [use the Route Hold-Down State](use-the-route-hold-down-state.md).

 

 




