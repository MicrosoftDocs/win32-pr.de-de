---
title: Multithread-Clients und Kontext Handles
description: Wenn Sie über einen Multithreadclient verfügen, bei dem mehrere Threads dieselbe Kontext Handle-Instanz verwenden, wird der Zugriff auf die Instanz des Kontext Handles standardmäßig auf dem Server serialisiert.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67c621d75d8cc48ca1f71719066f455e0efce39f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039303"
---
# <a name="multithreaded-clients-and-context-handles"></a>Multithread-Clients und Kontext Handles

Wenn Sie über einen Multithreadclient verfügen, bei dem mehrere Threads dieselbe Kontext Handle-Instanz verwenden, wird der Zugriff auf die Instanz des Kontext Handles standardmäßig auf dem Server serialisiert. Dadurch ist es nicht mehr erforderlich, dass der Server-Manager vor einem anderen Thread des gleichen Clients schützt und den Kontext ändert In bestimmten Fällen kann sich die Serialisierung jedoch auf die Leistung auswirken.

Beachten Sie Folgendes: zwei Clientthreads rufen einen Remote Prozedur Aufruf auf, der den Zustand des Kontexts nicht ändert (z. b. ruft der Aufruf einfach einige Werte aus). Solche Aufrufe müssen nicht serialisiert werden.

In solchen Fällen bietet Windows XP ein Serialisierungsmodell mit gemischtem Modus, in dem jede Methode so deklariert werden kann, dass Sie exklusiven oder gemeinsamen Zugriff auf ein Kontext Handle hat. Weitere Informationen finden Sie unter [Kontext \_ handle- \_ Serialisierung](/windows/desktop/Midl/context-handle-serialize) und [Kontext \_ handle \_ noserialize](/windows/desktop/Midl/context-handle-noserialize) .

In Windows-Versionen vor Windows XP besteht die einzige Möglichkeit, den gleichzeitigen Zugriff auf ein Kontext Handle zuzulassen, darin, die [**rpcssdontserializecontext**](/previous-versions/aa378473(v=vs.80)) -Funktion aufzurufen, damit mehrere Aufrufe an ein einzelnes Kontext Handle gesendet werden können. Durch Aufrufen der **rpcssdontserializecontext** -Funktion wird die Serialisierung nicht vollständig deaktiviert. Wenn eine Kontext Ausführung auftritt, wird die Kontext-Lauf Zeit Routine nur ausgeführt, wenn alle ausstehenden Client Anforderungen abgeschlossen wurden. Ein **rpcscdontserializecontext** -Aufrufe wirkt sich auf den gesamten Prozess aus und ist nicht revertierbar. Die Verwendung von **rpcscdontserializecontext** in Windows XP und höheren Versionen ist nicht empfehlenswert. der Servercode ist sehr kompliziert, wenn er mit Racebedingungen, die in vollständig nicht serialisierten Umgebungen verankert sind, zuverlässig verarbeitet wird.

 

 