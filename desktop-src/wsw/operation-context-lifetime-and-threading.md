---
title: Lebensdauer und Threading des Vorgangskontexts
description: Die Lebensdauer des Vorgangskontexts, dargestellt durch ein WS \_ OPERATION \_ CONTEXT-Handle, bestimmt die Lebensdauer der darin enthaltenen Eigenschaften.
ms.assetid: 37caf382-2b33-464d-b6c1-e4bd3271a5aa
keywords:
- Lebensdauer des Vorgangskontexts und Threadingwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd2748f797e43bab750f4e02409e62e6293b39cb44d4cfd3626f86099502fc3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119344830"
---
# <a name="operation-context-lifetime-and-threading"></a>Lebensdauer und Threading des Vorgangskontexts

Die Lebensdauer des Vorgangskontexts, dargestellt durch ein [WS \_ OPERATION \_ CONTEXT-Handle,](ws-operation-context.md) bestimmt die Lebensdauer der darin enthaltenen Eigenschaften. Daher sollte ein Kontext nur innerhalb der Lebensdauer des [Dienstvorgangs](service-operation.md) oder des Rückrufs verwendet werden, für den er bereitgestellt hat. Die Lebensdauer eines synchronen Aufrufs ist die Ausführung der Funktion selbst. Bei einem asynchronen Aufruf endet die Lebensdauer, sobald der asynchrone Aufruf abgeschlossen ist. Das Dienstmodell bietet keine Garantien für den Kontext, sobald der Aufruf abgeschlossen ist. Das Verhalten der Abhängigkeit vom Vorgangskontext oder einer seiner Eigenschaften über die Lebensdauer hinaus ist nicht definiert.


Siehe auch das sitzungsbasierte Rechnerbeispiel [SessionfullCalculatorServiceExample](sessionfullcalculatorserviceexample.md).

## <a name="threading-model"></a>Threading-Modell

Der Vorgangskontext unterstützt das freie Threading. Dies gilt jedoch für den Vorgangskontext selbst und gilt nicht für die darin enthaltenen Eigenschaften.

Wenn Sie einen Abbruchrückruf für einen Dienstvorgang über die [**WsRegisterOperationForCancel-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsregisteroperationforcancel) registrieren, beachten Sie, dass die erste Registrierung erfolgreich ist. Das mehrmalige Festlegen des Abbruchrückrufs schlägt jedoch fehl.

 

 




