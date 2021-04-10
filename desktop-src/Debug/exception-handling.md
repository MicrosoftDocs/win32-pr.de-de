---
description: Ausnahmen können von Hardware oder Software initiiert werden und können sowohl im Kernel Modus als auch im Benutzermoduscode auftreten. Die strukturierte Ausnahmebehandlung bietet einen einzigen Mechanismus für die Behandlung von Ausnahmen im Kernel Modus und im Benutzermodus.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Ausnahmebehandlung (Fehlerbehandlung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb44cd294d89be81862c5330dda5b14811add1f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125707"
---
# <a name="exception-handling-error-handling"></a>Ausnahmebehandlung (Fehlerbehandlung)

Ausnahmen können von Hardware oder Software initiiert werden und können sowohl im Kernel Modus als auch im Benutzermoduscode auftreten. Die strukturierte Ausnahmebehandlung bietet einen einzigen Mechanismus für die Behandlung von Ausnahmen im Kernel Modus und im Benutzermodus.

Die Ausführung bestimmter Anweisungs Sequenzen kann zu Ausnahmen führen, die von der Hardware initiiert werden. Beispielsweise wird von der Hardware eine Zugriffsverletzung generiert, wenn ein Prozess versucht, aus einer virtuellen Adresse zu lesen oder in diese zu schreiben, für die er nicht über die erforderlichen Zugriffsrechte verfügt.

Ereignisse, die eine Ausnahmebehandlung erfordern, können auch während der Ausführung einer Software Routine auftreten (z. b. Wenn ein Ungültiger Parameterwert angegeben wird). In diesem Fall kann ein Thread eine Ausnahme explizit auslösen, indem er die [**RaiseException**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) -Funktion aufrufen. Diese Funktion ermöglicht es dem aufrufenden Thread, Informationen anzugeben, die die Ausnahme beschreiben.

Eine Ausnahme kann fort setzbar oder nicht fort setzbar sein. Eine nicht fort Setz Bare Ausnahme tritt auf, wenn das Ereignis in der Hardware nicht fortgesetzt werden kann oder wenn die Fortsetzung keinen Sinn macht. Eine nicht fort Setz Bare Ausnahme beendet die Anwendung nicht. Daher ist es möglich, dass eine Anwendung die Ausnahme abfängt und ausgeführt wird. Allerdings entsteht eine nicht fort Setz Bare Ausnahme in der Regel aufgrund eines beschädigten Stapels oder eines anderen ernsten Problems, was die Wiederherstellung nach der Ausnahme erschwert.

 

 
