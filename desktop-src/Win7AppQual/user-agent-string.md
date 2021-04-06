---
description: .
ms.assetid: bcf0a534-c123-40c4-91b4-645c4912f31a
title: Zeichenfolge des Benutzer-Agents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2d9b25863fbc89ee88e24e3f98b8facad6a59f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960989"
---
# <a name="user-agent-string"></a>Zeichenfolge des Benutzer-Agents

Die *Zeichenfolge des Benutzer-Agents* enthält Informationen zur Identität eines Browsers. Die Zeichenfolge des Benutzer-Agents wird bei jeder Anforderung eines Webservers als HTTP-Header an den Webserver gemeldet. Sie können auch über ein Client seitiges Skript darauf zugreifen. Beispielsweise können Sie die Zeichenfolge des Benutzer-Agents anzeigen, indem Sie die folgende URL in die Adressleiste von Windows Internet Explorer 8 eingeben: "JavaScript: Alert (Navigator. UserAgent)". Die folgende Abbildung zeigt das typische resultierende Dialogfeld aus Internet Explorer 8 unter Windows 7.

![Screenshot des Fensters "Internet Explorer diaog" mit der Zeichenfolge "User Agent"](images/useragent-alert.png)

In der Regel wird die Zeichenfolge des Benutzer-Agents speziell für die MSIE-Teil Zeichenfolge analysiert. Basierend auf der gemeldeten Version des Browsers führt die Client seitige oder serverseitige Programmierlogik eine andere Aktion aus. Weitere Informationen zur Benutzer-Agent-Zeichenfolge finden Sie unter [Was wird Windows Internet Explorer als User-Agent Zeichenfolge melden?](/previous-versions/cc817582(v=msdn.10)) in der MSDN Library.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



