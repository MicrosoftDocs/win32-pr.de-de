---
description: Eine Ausnahme ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablauf Steuerungs Codes erfordert.
ms.assetid: 6b6326d8-6875-4146-a4e3-7873f4e400cb
title: Strukturierte Ausnahmebehandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62069b5aed16869a3f56b644d522c368702251c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860675"
---
# <a name="structured-exception-handling"></a>Strukturierte Ausnahmebehandlung

Eine *Ausnahme* ist ein Ereignis, das während der Ausführung eines Programms auftritt und die Ausführung von Code außerhalb des normalen Ablauf Steuerungs Codes erfordert. Es gibt zwei Arten von Ausnahmen: Hardware Ausnahmen und Software Ausnahmen. *Hardware Ausnahmen* werden von der CPU initiiert. Sie können sich aus der Ausführung bestimmter Anweisungs Sequenzen ergeben, z. b. der Division durch 0 (null) oder einem Versuch, auf eine ungültige Speicheradresse zuzugreifen. *Software Ausnahmen* werden explizit von Anwendungen oder dem Betriebssystem initiiert. Beispielsweise kann das System erkennen, wenn ein Ungültiger Parameterwert angegeben wird.

Die *strukturierte Ausnahmebehandlung* ist ein Mechanismus für die Behandlung von Hardware-und Software Ausnahmen. Daher verarbeitet der Code Hardware-und Software Ausnahmen identisch. Die strukturierte Ausnahmebehandlung ermöglicht Ihnen die vollständige Kontrolle über die Behandlung von Ausnahmen, bietet Unterstützung für debuggerund kann für alle Programmiersprachen und Computer verwendet werden. Die *Behandlung von Vektoren Ausnahmen* ist eine Erweiterung der strukturierten Ausnahmebehandlung.

Das System unterstützt auch die *Beendigung der Beendigung*, sodass Sie sicherstellen können, dass bei jeder Ausführung eines geschützten Code Texts auch ein angegebener Block von Beendigungs Code ausgeführt wird. Der Beendigungs Code wird ausgeführt, unabhängig davon, wie die Ablauf Steuerung den überwachten Text verlässt. Ein Beendigungs Handler kann z. b. sicherstellen, dass Bereinigungs Tasks ausgeführt werden, auch wenn eine Ausnahme oder ein anderer Fehler auftritt, während der überwachte Code Körper ausgeführt wird.

-   [Informationen über die strukturierte Ausnahmebehandlung](about-structured-exception-handling.md)
-   [Verwenden der strukturierten Ausnahmebehandlung](using-structured-exception-handling.md)
-   [Referenz für die strukturierte Ausnahmebehandlung](structured-exception-handling-reference.md)

 

 



