---
description: Warum benötigen Sie Kompatibilitätsansicht?
ms.assetid: 5B8D3A76-F30B-4F17-9257-0B6ED7F2D753
title: Warum benötigen Sie Kompatibilitätsansicht?
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5653ae72b3cbf3c21bd2458c1561c1d8823f2b883711e2c3890c16f792254b1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118328658"
---
# <a name="why-do-you-need-compatibility-view"></a>Warum benötigen Sie Kompatibilitätsansicht?

Das Kompatibilitätsansicht-Feature folgt einer Reihe von Regeln, um Inhalte ordnungsgemäß anzuzeigen, ohne dass nach Möglichkeit Benutzeraktionen (oder IT-Administratoren) erforderlich sind. Kompatibilitätsansicht ermöglicht Entwicklern, den Browser anzuweisen, welche Rendering-Engine verwendet werden soll, und ermöglicht benutzern, die Auswahl- und Switchmodi des Browsers außer Kraft zu setzen. Wenn Entwickler und IT-Experten nicht angeben, welcher Renderingmodus verwendet werden soll, wird dem Benutzer das Symbol "Fehlerhafte Seite" am rechten Ende der Adressleiste angezeigt, wie in der folgenden Abbildung dargestellt.

![Abbildung des Symbols "Fehlerhafte Seite" neben der Adressleiste](images/iecompatview.png)

Wenn ein Benutzer auf das Symbol klickt, wechselt Windows Internet Explorer 8 die Renderingmodi, und die Seite wird sofort neu geladen.

Benutzer sehen dieses Symbol nicht immer. Es handelt sich um eine sekundäre Lösung anstelle des primären Anwendungskompatibilitätsmechanismus. Windows Internet Explorer zeigt dieses Symbol nur an, wenn eine Änderung in Kompatibilitätsansicht sinnvoll ist, z. B. wenn ein Benutzer Seiten im Standardmodus anzeigt. In allen anderen Fällen, z. B. wenn ein Benutzer Seiten im quirks-Modus anzeigt oder Intranetzonensites anzeigt, wird das Symbol nicht angezeigt. Weitere Informationen zu Kompatibilitätsansicht und zu dem Zeitpunkt, zu dem das Symbol angezeigt wird, finden Sie unter [Einführung in Kompatibilitätsansicht](/archive/blogs/ie/).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 
