---
description: .
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: Was ist die Kompatibilitäts Ansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eac72fc5afa0e2946a4f904cbcea3c7b0af723c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760783"
---
# <a name="what-is-compatibility-view"></a>Was ist die Kompatibilitäts Ansicht?

Die *Kompatibilitäts Ansicht* ist ein Feature von Windows Internet Explorer 8, das es dem Browser ermöglicht, eine Webseite nahezu identisch mit der Art und Weise zu gestalten, in der Windows Internet Explorer 7 Sie Rendering.

In Internet Explorer 8 ändert die Kompatibilitäts Ansicht, wie der Browser Code interpretiert, der in CSS, HTML und Dokumentobjektmodell (DOM) geschrieben ist, um eine Entsprechung für Internet Explorer 7 zu versuchen. Ein-Standort, der in der Internet Explorer 8-Kompatibilitäts Ansicht von Benutzern angezeigt wird, ist nahezu identisch mit einer Website, die der Benutzer in Internet Explorer 7 anzeigt. Die Kompatibilitäts Ansicht ändert jedoch nicht, wie der Browser den gesamten Code interpretiert. Beispielsweise können die Änderungen in Internet Explorer 8, wie der Browser ActiveX, den Parser, AJAX, JavaScript, das Netzwerk und die Sicherheit verarbeitet, weiterhin Kompatibilitätsprobleme verursachen. In der Kompatibilitäts Ansicht werden diese Verhaltensweisen nicht geändert.

In einer Unternehmensumgebung besteht in einigen Bereichen ein geringeres Risiko von Kompatibilitätsproblemen. Websites der Intranetzone verwenden die Kompatibilitätsansicht beispielsweise standardmäßig. Client Webanwendungen, die mit dem Webbrowser-Steuerelement oder WebOC (Internet Explorer-Rendering-Engine) gerendert werden, haben auch ein niedriges Risiko für Kompatibilitätsprobleme, da Internet Explorer 8 standardmäßig einen Kompatibilitätsmodus für den WebOC verwendet. Die Standard Konfigurationseinstellungen für die Kompatibilitäts Ansicht gewährleisten jedoch möglicherweise nicht die gesamte Kompatibilität. Um zu ermitteln, ob eine Website oder Webanwendung mit Internet Explorer 8 kompatibel ist, sollten Sie die Website oder die Webanwendung testen.

Weitere Informationen zu den Unterschieden zwischen der Internet Explorer 8-Kompatibilitäts Ansicht und Internet Explorer 7 finden Sie im [Blog Website Kompatibilität und Internet Explorer 8](/archive/blogs/ie/site-compatibility-and-ie8). Eine Liste der Überprüfungen beim Upgrade auf Internet Explorer 8 finden Sie unter [Internet Explorer 8 Readiness Toolkit](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).

Weitere Informationen zur Kompatibilitäts Ansicht finden Sie im [Internet Explorer-Teamblog](/archive/blogs/ie/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
