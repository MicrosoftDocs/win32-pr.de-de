---
description: Eine Ausnahme ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablaufs der Kontrolle erfordert.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c07e3bce1c15120f5bba8f4423d96a32495dcdab0262957980f2b829ac0fa68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120059010"
---
# <a name="structured-exception-handling"></a>Strukturierte Ausnahmebehandlung

Eine *Ausnahme* ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablaufs der Kontrolle erfordert. Es gibt zwei Arten von Ausnahmen: Hardwareausnahmen und Softwareausnahmen. *Hardwareausnahmen* werden von der CPU initiiert. Sie können sich aus der Ausführung bestimmter Anweisungssequenzen ergeben, z. B. der Division durch 0 (null) oder dem Versuch, auf eine ungültige Speicheradresse zu zugreifen. *Softwareausnahmen* werden explizit von Anwendungen oder dem Betriebssystem initiiert. Beispielsweise kann das System erkennen, wenn ein ungültiger Parameterwert angegeben wird.

*Die strukturierte Ausnahmebehandlung* ist ein Mechanismus für die Behandlung von Hardware- und Softwareausnahmen. Daher behandelt Ihr Code Hardware- und Softwareausnahmen identisch. Mit der strukturierten Ausnahmebehandlung haben Sie die vollständige Kontrolle über die Behandlung von Ausnahmen, bieten Unterstützung für Debugger und können für alle Programmiersprachen und Computer verwendet werden. *Die Behandlung von Vektorausnahmen* ist eine Erweiterung der strukturierten Ausnahmebehandlung.

Das System unterstützt auch *die* Beendigungsbehandlung, wodurch Sie sicherstellen können, dass bei jeder Ausführung eines gesicherten Codekörpers auch ein angegebener Beendigungscodeblock ausgeführt wird. Der Beendigungscode wird unabhängig davon ausgeführt, wie der Ablauf der Steuerung den wächter Text verlässt. Beispielsweise kann ein Beendigungshandler garantieren, dass Bereinigungsaufgaben auch dann ausgeführt werden, wenn während der Ausführung des gesicherten Codekörpers eine Ausnahme oder ein anderer Fehler auftritt.

-   [Informationen zur strukturierten Ausnahmebehandlung](about-structured-exception-handling.md)
-   [Verwenden der strukturierten Ausnahmebehandlung](using-structured-exception-handling.md)
-   [Referenz zur strukturierten Ausnahmebehandlung](structured-exception-handling-reference.md)

 

 



