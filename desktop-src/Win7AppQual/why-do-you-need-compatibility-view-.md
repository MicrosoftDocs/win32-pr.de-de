---
description: .
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Warum benötigen Sie eine Kompatibilitäts Ansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74fd1902ad77af863e61be36800a8c4f9eabf227
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362967"
---
# <a name="why-do-you-need-compatibility-view"></a>Warum benötigen Sie eine Kompatibilitäts Ansicht?

Die Funktion Kompatibilitäts Ansicht folgt einem Satz von Regeln, um Inhalte ordnungsgemäß anzuzeigen, ohne dass eine Benutzer-(oder eine IT-Administrator Aktion) nach Möglichkeit benötigt wird. Mithilfe der Kompatibilitäts Ansicht können Entwickler den Browser anweisen, welches Renderingmodul verwendet werden soll, und Benutzern das Überschreiben der Auswahl-und switchmodi des Browsers ermöglichen Wenn der Entwickler und IT-Experte nicht angeben, welcher Renderingmodus verwendet werden soll, wird dem Benutzer das Symbol "unterbrochene Seite" am rechten Ende der Adressleiste angezeigt, wie in der folgenden Abbildung dargestellt.

![Abbildung des Symbols für eine beschädigte Seite neben der Adressleiste](images/iecompatview.png)

Wenn ein Benutzer auf das Symbol klickt, schaltet Windows Internet Explorer 8 die Renderingmodi um, und die Seite wird sofort erneut geladen.

Benutzer sehen dieses Symbol nicht immer. Dabei handelt es sich um eine sekundäre Lösung anstelle des primären Anwendungs Kompatibilitäts Mechanismus. Windows Internet Explorer zeigt dieses Symbol nur an, wenn eine Änderung in der Kompatibilitäts Ansicht sinnvoll ist, z. b. Wenn ein Benutzer die Seiten im Standardmodus anweist. In allen anderen Fällen, z. b. Wenn ein Benutzer Seiten im quiranmodus oder Ansichten für Intranetzone anzeigt, wird das Symbol nicht angezeigt. Weitere Informationen zur Kompatibilitäts Ansicht und zum Anzeigen des Symbols finden Sie unter Einführung in die [Kompatibilitäts Ansicht](/archive/blogs/ie/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
