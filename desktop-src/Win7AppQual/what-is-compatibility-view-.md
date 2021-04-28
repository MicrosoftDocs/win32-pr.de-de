---
description: Was ist Kompatibilitätsansicht?
ms.assetid: 1EAC5799-7943-40AB-A67E-F6D6888C4B7D
title: Was ist Kompatibilitätsansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2be51f94d560d206c579d74d9407d53541205201
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113398"
---
# <a name="what-is-compatibility-view"></a>Was ist Kompatibilitätsansicht?

*Kompatibilitätsansicht* ist ein Feature von Windows Internet Explorer 8, mit dem der Browser eine Webseite nahezu genauso rendern kann wie Windows Internet Explorer 7.

In Internet Explorer 8 ändert Kompatibilitätsansicht, wie der Browser Code interpretiert, der in CSS, HTML und der Dokumentobjektmodell (DOM) geschrieben ist, um zu versuchen, Internet Explorer 7 zu entsprechen. Eine Website, die ein Benutzer in Internet Explorer 8 Kompatibilitätsansicht anzeigt, ist fast identisch mit einer Website, die der Benutzer in Internet Explorer 7 anzeigt. Kompatibilitätsansicht ändert jedoch nicht, wie der Browser den gesamten Code interpretiert. Beispielsweise können die Änderungen in Internet Explorer 8 für die Verarbeitung von ActiveX, dem Parser, AJAX, JavaScript, Netzwerk und Sicherheit durch den Browser weiterhin Kompatibilitätsprobleme verursachen. Kompatibilitätsansicht ändert diese Verhaltensweisen nicht.

In einer Unternehmensumgebung besteht in einigen Bereichen ein geringeres Risiko von Kompatibilitätsproblemen. Websites der Intranetzone verwenden die Kompatibilitätsansicht beispielsweise standardmäßig. Clientwebanwendungen, die mithilfe des Webbrowsersteuerelements oder der WebOC (Internet Explorer Rendering-Engine) gerendert werden, weisen ebenfalls ein geringes Risiko für Kompatibilitätsprobleme auf, da Internet Explorer 8 standardmäßig einen Kompatibilitätsmodus für webOC verwendet. Die Standardkonfigurationseinstellungen für Kompatibilitätsansicht stellen jedoch möglicherweise keine vollständige Kompatibilität sicher. Um festzustellen, ob eine Website oder Webanwendung mit Internet Explorer 8 kompatibel ist, sollten Sie die Website oder Webanwendung testen.

Weitere Informationen zu den Unterschieden zwischen Internet Explorer 8 Kompatibilitätsansicht und Internet Explorer 7 finden Sie im [Blog Site Compatibility and Internet Explorer 8 (Websitekompatibilität und Internet Explorer 8).](/archive/blogs/ie/site-compatibility-and-ie8) Eine Liste der zu überprüfende Informationen zum Upgrade auf Internet Explorer 8 finden Sie im [Internet Explorer 8 Readiness Toolkit.](https://www.microsoft.com/windows/internet-explorer/readiness/developers.aspx)

Weitere Informationen zu Kompatibilitätsansicht finden Sie im [Internet Explorer-Teamblog.](/archive/blogs/ie/)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
