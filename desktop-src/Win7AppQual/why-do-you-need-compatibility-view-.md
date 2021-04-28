---
description: Warum benötigen Sie Kompatibilitätsansicht?
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Warum benötigen Sie Kompatibilitätsansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9991e9dc0c2edcd66ae6655c094f17b240be985a
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108113378"
---
# <a name="why-do-you-need-compatibility-view"></a>Warum benötigen Sie Kompatibilitätsansicht?

Das Kompatibilitätsansicht-Feature folgt einer Reihe von Regeln, um Inhalte ordnungsgemäß anzuzeigen, ohne dass nach Möglichkeit Benutzer- (oder IT-Administrator)-Aktionen erforderlich sind. Kompatibilitätsansicht können Entwickler den Browser anweisen, welche Rendering-Engine verwendet werden soll, und ermöglicht es Benutzern, die Auswahl- und Wechselmodi des Browsers außer Kraft zu setzen. Wenn entwickler und IT-Fachkraft nicht angeben, welcher Renderingmodus verwendet werden soll, wird dem Benutzer das Symbol "Fehlerhafte Seite" am rechten Ende der Adressleiste angezeigt, wie in der folgenden Abbildung dargestellt.

![Abbildung des fehlerhaften Seitensymbols neben der Adressleiste](images/iecompatview.png)

Wenn ein Benutzer auf das Symbol klickt, wechselt Windows Internet Explorer 8 den Renderingmodus, und die Seite wird sofort neu geladen.

Benutzern wird dieses Symbol nicht immer angezeigt. Es handelt sich um eine sekundäre Lösung anstelle des primären Anwendungskompatibilitätsmechanismus. Windows Internet Explorer zeigt dieses Symbol nur an, wenn eine Änderung in Kompatibilitätsansicht sinnvoll ist, z. B. wenn ein Benutzer Standardmodusseiten anzeigt. In allen anderen Fällen, z. B. wenn ein Benutzer Seiten im quirks-Modus oder Intranetzonensites betrachtet, wird das Symbol nicht angezeigt. Weitere Informationen zum Kompatibilitätsansicht und zum Anzeigen des Symbols finden Sie unter [Introducing Kompatibilitätsansicht](/archive/blogs/ie/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
