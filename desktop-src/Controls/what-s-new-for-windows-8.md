---
title: Neuerungen (Windows-Steuerelemente)
description: In diesem Thema werden die Unterschiede bei der Unterstützung von Designs und visuellen Stilen zwischen Windows 8 und früheren Versionen von Windows beschrieben.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d7801eea011aabb05663cc2e29f18e0dd58edc9fddc4f32014fcffb96c559cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957549"
---
# <a name="whats-new-windows-controls"></a>Neuerungen (Windows-Steuerelemente)

In diesem Thema werden die Unterschiede bei der Unterstützung von Designs und visuellen Stilen zwischen Windows 8 und früheren Versionen von Windows beschrieben.

## <a name="through-windows-7"></a>Bis Windows 7

Bis Windows 7 sind visuelle Stile standardmäßig aktiviert, aber der Benutzer kann sie deaktivieren, indem er Windows klassische Design auswählt oder den Dienst Designs deaktiviert. Wenn visuelle Stile deaktiviert sind, erhält die gesamte Benutzeroberfläche das klassische Aussehen, und die meisten visuellen Stil-APIs sind nicht verfügbar. Visuelle Stile außerhalb des Modus wurden bis Windows 7 beibehalten, um die verschiedenen Designs mit hohem Kontrast sowie Windows klassische Design zu unterstützen. Wenn Sie visuelle Stile und Designs mit hohem Kontrast in derselben Anwendung unterstützen möchten, müssen Sie in der Regel zwei separate Codepfade für Renderingsteuerelemente verwalten.

## <a name="windows-8-and-later"></a>Windows 8 und höher

In Windows 8 können visuelle Stile nicht über die **Personalisierungsseite** des **PC-Einstellungen** oder durch Deaktivieren des Designs-Diensts deaktiviert werden. Windows Der klassische Modus ist nicht mehr vorhanden, und der Modus für hohen Kontrast wurde so geändert, dass er mit visuellen Stilen funktioniert. Aufgrund dieser Änderungen benötigen Anwendungen, die nur auf Windows 8 ausgerichtet sind, keine zwei separaten Codepfade mehr, um visuelle Stile und Designs mit hohem Kontrast zu unterstützen.

Visuelle Stile in Windows 8 enthalten Abwärtskompatibilitätsunterstützung für Windows klassischen Themingmodus. Jeglicher Benutzeroberflächenrenderingcode, der in früheren Versionen funktioniert, funktioniert weiterhin ohne Änderungen an Windows 8.

Wenn Ihre Anwendung in Windows 8 die Designs mit hohem Kontrast unterstützen soll, die auf visuellen Stilen basieren, müssen Sie die Windows 8 GUID in den Kompatibilitätsabschnitt Ihres Anwendungsmanifests einschließen. Andernfalls geht das System davon aus, dass die Anwendung für eine frühere Version konzipiert ist und rendert den Clientbereich, indem Windows klassische Designs mit hohem Kontrast simuliert wird. Weitere Informationen finden Sie unter [Supporting hoher Kontrast Themes](supporting-high-contrast-themes.md).

Wie in früheren Versionen unterstützt Windows 8 sowohl Version 5 als auch Version 6 der allgemeinen Steuerelemente, wobei Version 5 die Standardeinstellung ist. Da nur Version 6 visuelle Stile unterstützt, müssen Sie Version 6 in Ihrem Anwendungsmanifest angeben, wenn visuelle Stile auf die allgemeinen Steuerelemente im Clientbereich Ihrer Anwendung angewendet werden sollen. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen.](cookbook-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> <dt>

[Unterstützen hoher Kontrast Designs](supporting-high-contrast-themes.md)
</dt> <dt>

[Visuelle Stile](themes-overview.md)
</dt> <dt>

[Übersicht über visuelle Stile](visual-styles-overview.md)
</dt> </dl>

 

 




