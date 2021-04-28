---
description: Zeichenfolge des Benutzer-Agents
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Zeichenfolge des Benutzer-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d227eead5c02f50b689779bd0a8f0ba4b031d06
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084178"
---
# <a name="user-agent-string"></a>Zeichenfolge des Benutzer-Agents

Die *Benutzer-Agent-Zeichenfolge* enthält Informationen zur Identität eines Browsers. Die Zeichenfolge des Benutzer-Agents wird dem Webserver jedes Mal als HTTP-Header gemeldet, wenn ein Browser eine Anforderung an einen Webserver stellt. Sie können auch über ein clientseitiges Skript darauf zugreifen. Beispielsweise können Sie die Zeichenfolge des Benutzer-Agents anzeigen, indem Sie die folgende URL in die Adressleiste von Windows Internet Explorer 8 eingeben: "javascript:alert(navigator.userAgent)". Die folgende Abbildung zeigt das typische resultierende Dialogfeld aus Internet Explorer 8 unter Windows 7.

![Screenshot des Internet Explorer-Diaogfelds mit der Zeichenfolge des Benutzer-Agents](images/useragent-alert.png)

In der Regel wird die Zeichenfolge des Benutzer-Agents speziell für die MSIE-Teilzeichenfolge analysiert. Basierend auf der gemeldeten Version des Browsers führt die clientseitige oder serverseitige Programmierlogik eine andere Aktion aus. Weitere Informationen zur Zeichenfolge des Benutzer-Agents finden Sie unter [Was wird Windows Internet Explorer Bericht als User-Agent Zeichenfolge?](/previous-versions/cc817582(v=msdn.10)) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



