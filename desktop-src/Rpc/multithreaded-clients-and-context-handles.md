---
title: Multithreadclients und Kontexthandles
description: Wenn Sie über einen Multithreadclient verfügen, bei dem mehrere Threads dieselbe Kontexthandleinstanz verwenden, wird der Zugriff auf die Kontexthandleinstanz standardmäßig auf dem Server serialisiert.
ms.assetid: 192be467-b1e0-422b-878a-738cb7d72b5b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e7fed15deacca47754f51869fa0b18b37135586addb7f80b8aa75b9dde63082
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118928085"
---
# <a name="multithreaded-clients-and-context-handles"></a>Multithreadclients und Kontexthandles

Wenn Sie über einen Multithreadclient verfügen, bei dem mehrere Threads dieselbe Kontexthandleinstanz verwenden, wird der Zugriff auf die Kontexthandleinstanz standardmäßig auf dem Server serialisiert. Dies verhindert, dass der Server-Manager sich vor einem anderen Thread desselben Clients schützen muss, der den Kontext oder den Kontext ändert, der während der Verteilung eines Aufrufs ausgeführt wird. In bestimmten Fällen kann sich die Serialisierung jedoch auf die Leistung auswirken.

Beachten Sie Folgendes: Zwei Clientthreads rufen einen Remoteprozeduraufruf auf, der den Zustand des Kontexts nicht ändert (z. B. ruft der Aufruf einfach einige Werte davon ab). Solche Aufrufe müssen nicht serialisiert werden.

In solchen Situationen bietet Windows XP ein Serialisierungsmodell im gemischten Modus, bei dem jede Methode als exklusiver oder freigegebener Zugriff auf ein Kontexthandle deklariert werden kann. Weitere Informationen finden Sie unter [ \_ \_ Kontexthandleserialisierung](/windows/desktop/Midl/context-handle-serialize) und [ \_ Kontexthandle \_ noserialize.](/windows/desktop/Midl/context-handle-noserialize)

In Versionen von Windows vor Windows XP besteht die einzige Möglichkeit, gleichzeitigen Zugriff auf ein Kontexthandle zuzulassen, darin, die [**RpcSsDontSerializeContext-Funktion**](/previous-versions/aa378473(v=vs.80)) aufzurufen, damit mehrere Aufrufe für ein einzelnes Kontexthandle verteilt werden können. Durch aufrufen der **RpcSsDontSerializeContext-Funktion** wird die Serialisierung nicht vollständig deaktiviert. Wenn ein Kontext run-down auftritt, wird die Kontext-Run-Down-Routine nur ausgeführt, wenn alle ausstehenden Clientanforderungen abgeschlossen wurden. Ein Aufruf von **RpcScDontSerializeContext** wirkt sich auf den gesamten Prozess aus und kann nicht rückgängig gemacht werden. Die Verwendung von **RpcScDontSerializeContext** in Windows XP und höher wird nicht empfohlen. Dies macht Servercode sehr kompliziert, wenn es zuverlässig mit Racebedingungen zu tun hat, die in vollständig nicht serialisierten Umgebungen inhärent sind.

 

 