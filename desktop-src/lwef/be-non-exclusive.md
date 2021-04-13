---
title: Nicht exklusiv
description: Nicht exklusiv
ms.assetid: 7a44840d-6bf9-4c12-ba14-66d7067a984d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b637bcf0860ccc4917b1af344664f9828b0da8d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388139"
---
# <a name="be-non-exclusive"></a>Nicht exklusiv

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Interaktive Zeichen können in der Benutzeroberfläche als Assistenten, Anleitungen, Entertainer, Storyteller, Vertriebs-Agents oder in einer Vielzahl anderer Rollen eingesetzt werden. Ein Zeichen, das automatisch ausführt oder unterstützt, sollte nicht im Gegensatz zum Entwurfs Prinzip entworfen werden, um den Benutzer in die Kontrolle zu behalten. Wenn Sie der-Schnittstelle einer Website oder einer konventionellen Anwendung ein Zeichen hinzufügen, verwenden Sie das Zeichen als Erweiterung und nicht als Ersatz für die primäre Schnittstelle. Vermeiden Sie das Implementieren von Features oder Vorgängen, die ausschließlich ein Zeichen erfordern.

Gleichermaßen können Sie den Benutzer entscheiden, wann er mit Ihrem Zeichen interagieren soll. Ein Benutzer sollte in der Lage sein, das Zeichen zu verwerfen und nur mit der Berechtigung des Benutzers zurückzugeben. Das Erzwingen von Zeichen Interaktionen für Benutzer kann einen schwerwiegenden negativen Effekt haben. Zur Unterstützung der Benutzersteuerung der Zeichen Interaktion schließt der Microsoft-Agent automatisch die Befehle zum Ausblenden und anzeigen ein. Die Microsoft-Agent-API unterstützt auch diese Methoden, sodass Sie die Unterstützung für diese Funktionen in ihrer eigenen Schnittstelle einschließen können. Darüber hinaus enthält die Benutzeroberfläche des Microsoft-Agents globale Eigenschaften, die es dem Benutzer ermöglichen, bestimmte Zeichenausgabe Optionen zu überschreiben. Diese Eigenschaften können nicht über die API überschrieben werden, um sicherzustellen, dass die Benutzereinstellungen beibehalten werden.

 

 




