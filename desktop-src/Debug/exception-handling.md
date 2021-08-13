---
description: Ausnahmen können von Hardware oder Software initiiert werden und im Kernelmodus sowie im Benutzermoduscode auftreten. Die strukturierte Ausnahmebehandlung stellt einen einzelnen Mechanismus für die Behandlung von Kernelmodus- und Benutzermodusausnahmen dar.
ms.assetid: 760ddcaa-a18c-4fdf-836c-9028a2e4b62e
title: Ausnahmebehandlung (Fehlerbehandlung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 253776619100095ae1ba9c92fa2caa373bc950bdf6725c6ef5d0239520320bd9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260870"
---
# <a name="exception-handling-error-handling"></a>Ausnahmebehandlung (Fehlerbehandlung)

Ausnahmen können von Hardware oder Software initiiert werden und im Kernelmodus sowie im Benutzermoduscode auftreten. Die strukturierte Ausnahmebehandlung stellt einen einzelnen Mechanismus für die Behandlung von Kernelmodus- und Benutzermodusausnahmen dar.

Die Ausführung bestimmter Anweisungssequenzen kann zu Ausnahmen führen, die von der Hardware initiiert werden. Beispielsweise wird eine Zugriffsverletzung von der Hardware generiert, wenn ein Prozess versucht, aus einer virtuellen Adresse zu lesen oder in diese zu schreiben, auf die er nicht über den entsprechenden Zugriff verfügt.

Ereignisse, die eine Ausnahmebehandlung erfordern, können auch während der Ausführung einer Softwareroutine auftreten (z. B. wenn ein ungültiger Parameterwert angegeben wird). In diesem Fall kann ein Thread eine Ausnahme explizit initiieren, indem er die [**RaiseException-Funktion**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-raiseexception) aufruft. Mit dieser Funktion kann der aufrufende Thread Informationen angeben, die die Ausnahme beschreiben.

Eine Ausnahme kann kontinuierbar oder nicht kontinuierbar sein. Eine nicht fortsetzbare Ausnahme tritt auf, wenn das Ereignis in der Hardware nicht zusammenhängend ist oder wenn eine Fortsetzung keinen Sinn ergibt. Eine nicht übertragbare Ausnahme beendet die Anwendung nicht. Daher kann eine Anwendung die Ausnahme abfangen und ausführen. Eine nicht kontinuierbare Ausnahme tritt jedoch in der Regel aufgrund eines beschädigten Stapels oder eines anderen schwerwiegenden Problems auf, was die Wiederherstellung nach der Ausnahme erschwert.

 

 
