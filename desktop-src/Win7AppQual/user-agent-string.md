---
description: Zeichenfolge des Benutzer-Agents
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Zeichenfolge des Benutzer-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a4d918845fe317ef64569cde7ef79c7bb1461bcd0205a5ef74daf55b2c0186
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328695"
---
# <a name="user-agent-string"></a>Zeichenfolge des Benutzer-Agents

Die *Benutzer-Agent-Zeichenfolge* enthält Informationen zur Identität eines Browsers. Die Zeichenfolge des Benutzer-Agents wird dem Webserver jedes Mal als HTTP-Header gemeldet, wenn ein Browser eine Anforderung an einen Webserver stellt. Sie können auch über ein clientseitiges Skript darauf zugreifen. Beispielsweise können Sie die Zeichenfolge des Benutzer-Agents anzeigen, indem Sie die folgende URL in die Adressleiste Windows Internet Explorer 8 eingeben: "javascript:alert(navigator.userAgent)". Die folgende Abbildung zeigt das typische resultierende Dialogfeld aus Internet Explorer 8, das auf Windows 7 ausgeführt wird.

![Screenshot des Internet Explorer-Diaogfelds mit der Zeichenfolge des Benutzer-Agents](images/useragent-alert.png)

In der Regel wird die Benutzer-Agent-Zeichenfolge speziell für die MSIE-Teilzeichenfolge analysiert. Basierend auf der gemeldeten Version des Browsers führt die client- oder serverseitige Programmierlogik eine andere Aktion aus. Weitere Informationen zur Zeichenfolge des Benutzer-Agents finden Sie unter [What Will Windows Internet Explorer Report as the User-Agent String?](/previous-versions/cc817582(v=msdn.10)) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



