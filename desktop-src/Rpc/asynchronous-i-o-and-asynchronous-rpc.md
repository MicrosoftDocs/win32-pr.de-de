---
title: Asynchrone e/a-und asynchrone RPC
description: Asynchrone e/a ist ein effizientes Mittel für einen einzelnen Thread zur gleichzeitigen Verwaltung mehrerer e/a-Anforderungen.
ms.assetid: a9105518-4130-4119-b8d1-e73064b077e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e932e85283eb67ff6675a646e791bbce5fe15d65
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390895"
---
# <a name="asynchronous-io-and-asynchronous-rpc"></a>Asynchrone e/a-und asynchrone RPC

Asynchrone e/a ist ein effizientes Mittel für einen einzelnen Thread zur gleichzeitigen Verwaltung mehrerer e/a-Anforderungen. Der asynchrone RPC auf dem Server erreicht einen ähnlichen Zweck für RPC-Anforderungen. In Windows-Versionen vor Windows Vista wird von der Veröffentlichung von asynchronen e/a-Anforderungen von Server Prozeduren mithilfe von asynchronem RPC abgeraten. In Windows Vista und höheren Versionen von Windows werden asynchrone e/a-Anforderungen, die einem e/a-Abschlussport zugeordnet sind, jedoch von asynchronem RPC unterstützt.

Vor Windows Vista kann ein asynchroner Remote Prozedur Aufrufvorgang abgeschlossen werden, bevor die asynchrone e/a-Anforderung abgeschlossen ist. Wenn der asynchrone Aufruf abgeschlossen ist, kann der zugehörige Thread beendet werden, wenn die RPC-Laufzeit entscheidet, dass genügend Threads für die erwartete Arbeitsauslastung zur Verfügung stehen. Das System bindet alle e/a-Anforderungen an den Thread, der Sie initiiert. Wenn der Thread beendet wird, werden alle für diesen Thread ausstehenden e/a-Anforderungen abgebrochen. Ausstehende e/a-Anforderungen können nicht in einen anderen Thread verschoben werden.

Daher können Anwendungs-Designer, die auf Windows-Versionen vor Windows Vista abzielen, entweder synchrone e/a-Vorgänge in Server Prozeduren verwenden oder alle Anforderungen, die asynchrone e/a betreffen, an Prozeduren weiterleiten, die in einem von der Anwendung verwalteten Thread Pool ausgeführt werden. Die Windows-API stellt Funktionen für die Thread Pool Verwaltung bereit. Siehe [Prozess-und Thread Funktionen](/windows/desktop/ProcThread/process-and-thread-functions).

 

 