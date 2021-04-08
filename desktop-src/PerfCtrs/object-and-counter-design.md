---
description: Ein Leistungs Objekt ist eine Entität, für die Leistungsdaten verfügbar sind.
ms.assetid: 97b9c9ec-e758-4928-b3fa-90d220bca5fb
title: Objekt-und Gegenentwurf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9556882f5dd6c323697d9d41fa80727895550a5d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959762"
---
# <a name="object-and-counter-design"></a>Objekt-und Gegenentwurf

Ein Leistungs Objekt ist eine Entität, für die Leistungsdaten verfügbar sind. Leistungsindikatoren definieren den Datentyp, der für ein Leistungs Objekt verfügbar ist. Eine Anwendung kann Informationen für mehrere Leistungs Objekte bereitstellen. Leistungs Objekte können entweder Einzelinstanzzähler oder Zähler für mehrere Instanzen enthalten. Ein einzelnes Instanzobjekt gibt einen einzelnen Satz von Zählers zurück.

Ein Objekt mit mehreren Instanzen gibt eine Instanz des-Objekts für jedes Vorkommen des-Objekts zurück, das die Anwendung steuert. Eine SCSI-Anwendung könnte z. b. ein Laufwerks Objekt mit zwei Indikatoren definieren, z. b. gelesene Bytes und geschriebene Bytes. Wenn der Consumer das Objekt abfragt, gibt die Leistungs-DLL eine Instanz des-Objekts für jedes Laufwerk zurück, das die Anwendung steuert.

Nachdem Sie entschieden haben, ob das Objekt eine einzelne Instanz oder mehrere Instanzen unterstützt, müssen Sie den Typ der Indikatoren festlegen, die das Objekt bereitstellen soll. Beispielsweise können Sie Leistungswerte angeben, die als Rohwerte, als Raten oder als Prozentsätze angezeigt werden.

Eine Liste der vordefinierten gegen Typen, aus denen Sie auswählen sollten, finden Sie im Abschnitt Counter Types des [Windows Server 2003 Deployment Kits](/previous-versions/windows/it-pro/windows-server-2003/cc776490(v=ws.10)). Abhängig vom zähtertyp können Sie einfach die Rohdaten bereitstellen, oder Sie müssen Zeit-und Häufigkeits Informationen sowie zusätzliche Leistungsdaten angeben, die vom Consumer zum Berechnen eines anzeigbaren Werts verwendet werden.

Die Methode, die Sie verwenden, um die Daten zu erfassen, kann so einfach sein wie das erhöhen eines Zählers, wenn eine bestimmte Routine in der Anwendung aufgerufen wird, oder es kann zeitaufwändige Berechnungen einschließen. Zähler und Timer sollten Inkrement und nie gelöscht werden. Leistungsindikatoren können eingebunden werden, solange Sie nicht zweimal zwischen den Stichproben durch den Consumer gebunden werden. Die Anwendung kann Daten während ihrer normalen Ausführung erfassen und speichern, solange Sie sich nicht auf Ihre Leistung auswirkt.

Bei einigen Datentypen kann es effizienter oder geeigneter sein, die Daten bei Bedarf zu erfassen. In diesem Fall muss die Leistungs-DLL mit der Anwendung kommunizieren, dass die Daten angefordert wurden. Für Daten, die teuer zu erfassen sind (im Hinblick auf die Prozessorzeit oder die Arbeitsspeicher Auslastung), sollten Sie Daten nur sammeln, wenn der Consumer **teure** Daten anfordert. Dadurch kann ein Consumer routinemäßig Daten für alle Leistungsindikatoren anfordern, die nicht kostspielig sind. Die Daten können nur bei Bedarf angefordert werden. Das Leistungs Tool sammelt keine **teuren** Daten.

 

 
