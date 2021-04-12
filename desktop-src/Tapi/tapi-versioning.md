---
description: Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden.
ms.assetid: 35fea8f9-307e-4429-b4ec-ffb5c62c2610
title: TAPI-Versionsverwaltung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8565eb6282fd124c4f43e56d121ba7c053143683
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346788"
---
# <a name="tapi-versioning"></a>TAPI-Versionsverwaltung

Im Laufe der Zeit können verschiedene Versionen von TAPI, Anwendungen und Dienstanbietern erstellt werden. Diese neuen Versionen können neue Definitionen erstellen, z. b. für neue Features, neue Member in Datenstrukturen und neue Bitfelder. Daher sind Versionsnummern erforderlich, um anzugeben, wie verschiedene Datenstrukturen interpretiert werden sollen.

Um eine optimale Interoperabilität verschiedener Versionen von Anwendungen, Versionen von TAPI selbst und Versionen von Dienstanbietern durch verschiedene Lieferanten zu ermöglichen, bietet Microsoft Telefonie einen einfachen Versions Aushandlungs Mechanismus für Anwendungen. Es gibt zwei verschiedene Versionen, die TAPI und der Telefoniedienstanbieter für jedes Zeilen Gerät akzeptieren müssen. Die erste ist die Version, die mit TAPI und dem Telefoniedienstanbieter (TSP) "Basic" und der ergänzenden Telefonieschnittstelle ausgehandelt wird. Die andere gilt für anbieterspezifische Erweiterungen, sofern vorhanden, und wird als Erweiterungs Version bezeichnet. Das Format der Datenstrukturen und Datentypen, die von den grundlegenden und ergänzenden Features von TAPI verwendet werden, wird durch die TAPI-Version definiert, während die Erweiterungs Version das Format der Datenstrukturen bestimmt, die von den herstellerspezifischen Erweiterungen definiert werden.

Die [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) -Funktion aushandiert eine TAPI-Version, und [**linenegotiateextversion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) aushandiert die TSP-Erweiterungs Version. Ein einzelner TSP kann möglicherweise mehr als eine Version verarbeiten, und eine Anwendung muss bei Verwendung eines älteren TSP auf eine ältere Version zurückgreifen. In **lineNegotiateAPIVersion** wird der Parameter " *dwapiversion* " standardmäßig wie folgt auf einen Wert gemäß Version verwendet.



| TAPI-Version | Standardwert |
|--------------|---------------|
| 1.3          | 0x00010003    |
| 1.4          | 0x00010004    |
| 2.0          | 0x00020000    |
| 2.1          | 0x00020001    |
| 2.2          | 0x00020002    |



 

TAPI macht dies jedoch viel einfacher, solange der TSP selbst eine neuere Version als die Anwendung verwendet. Wenn der TSP tatsächlich neuer ist, kann TAPI "Down" in die Version der Anwendung übersetzen. Beispielsweise müssen TAPI 2,0-TSPS nicht speziell in der Lage sein, die TAPI-Version 1,4 zu verarbeiten. Wenn eine TAPI 1,4-Anwendung ausgeführt wird, konvertiert TAPI alle TAPI 2,0-Strukturen und-Nachrichten in TAPI 1,4-Entsprechungen oder so nah wie möglich. Wenn TAPI 1,4 keine genaue Näherung hat, gehen alle TAPI 2,0-spezifischen Informationen verloren.

Die genaue Bedeutung einer Erweiterungs Version ist Anbieter spezifisch. Informationen zur Verwendung eines TSP, der Erweiterungen unterstützt, finden Sie in der Dokumentation des Anbieters.

Es gibt eine Reihe von TAPI-Versionen. Obwohl die meisten dieser Versionen Änderungen an den Dokumentations Sätzen der TAPI-und Telefonie-Dienstanbieter Schnittstelle (TSPI) vorgenommen haben, gibt es für jede Version weitere Implikationen, nämlich Architektur Unterschiede, Betriebssystem Variationen, verteilbare Komponenten und Probleme mit der TSP-Entwicklung.



| TAPI-Version        | Distribution                                                   |
|---------------------|----------------------------------------------------------------|
| 1,0 – 1,2           | Beta Versionen, die nicht länger verwendet werden sollen.              |
| [1.4](tapi-1-4.md) | In Windows 95 enthalten.                                        |
| [1.5](tapi-1-5.md) | In Windows CE 1,0 enthalten.                                    |
| [2.0](tapi-2-0.md) | Enthalten in Windows NT 4,0 mit SP3.                           |
| [2.1](tapi-2-1.md) | In Windows NT 4,0 mit SP4 und Windows 98 enthalten.            |
| [2.2](tapi-2-2.md) | Enthalten in Windows Server 2003, Windows XP und Windows 2000. |



 

 

 



