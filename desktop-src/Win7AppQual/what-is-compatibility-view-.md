---
description: Was ist Kompatibilitätsansicht?
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: Was ist Kompatibilitätsansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6974ad32c7f09ee22dafc315cb2122976e84860e62434157f5a3ff46564a9e2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994530"
---
# <a name="what-is-compatibility-view"></a>Was ist Kompatibilitätsansicht?

*Kompatibilitätsansicht* ist ein Feature von Windows Internet Explorer 8, das es dem Browser ermöglicht, eine Webseite nahezu identisch mit der Art und Weise zu rendern, wie Windows Internet Explorer 7 sie rendern würde.

In Internet Explorer 8 ändert Kompatibilitätsansicht, wie der Browser code interpretiert, der in CSS, HTML und dem Dokumentobjektmodell (DOM) geschrieben ist, um zu versuchen, mit Internet Explorer 7 zu übereinstimmen. Eine Website, die ein Benutzer in Internet Explorer 8 Kompatibilitätsansicht, ist fast identisch mit einer Website, die der Benutzer in Internet Explorer 7. Die Kompatibilitätsansicht ändert jedoch nicht, wie der Browser den ganzen Code interpretiert. Beispielsweise können die Änderungen in Internet Explorer 8 für die Art und Weise, wie der Browser ActiveX behandelt, weiterhin Kompatibilitätsprobleme verursachen. Kompatibilitätsansicht ändert diese Verhaltensweisen nicht.

In einer Unternehmensumgebung besteht in einigen Bereichen ein geringeres Risiko von Kompatibilitätsproblemen. Websites der Intranetzone verwenden die Kompatibilitätsansicht beispielsweise standardmäßig. Clientwebanwendungen, die mit dem Webbrowser-Steuerelement oder der WebOC (Internet Explorer-Rendering-Engine) gerendert werden, haben ebenfalls ein geringes Risiko für Kompatibilitätsprobleme, da Internet Explorer 8 standardmäßig einen Kompatibilitätsmodus für das WebOC verwendet. Die Standardkonfigurationseinstellungen für die Kompatibilitätsansicht stellen jedoch möglicherweise nicht die vollständige Kompatibilität sicher. Um festzustellen, ob eine Website oder Webanwendung mit Internet Explorer 8 kompatibel ist, sollten Sie die Website oder Webanwendung testen.

Weitere Informationen zu den Unterschieden zwischen Internet Explorer 8 Kompatibilitätsansicht und Internet Explorer 7 finden Sie im Blog site compatibility and Internet Explorer 8 (Standortkompatibilität und [Internet Explorer 8).](/archive/blogs/ie/site-compatibility-and-ie8) Eine Liste der Zu überprüfenden Punkte beim Upgrade auf Internet Explorer 8 finden Sie im Internet Explorer [8 Readiness Toolkit](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx).

Weitere Informationen zu Kompatibilitätsansicht finden Sie im Internet Explorer [TeamBlog](/archive/blogs/ie/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
