---
title: Neuigkeiten (Windows-Steuerelemente)
description: In diesem Thema werden die Unterschiede in der Unterstützung für Designs und visuelle Stile zwischen Windows 8 und früheren Windows-Versionen beschrieben.
ms.assetid: 866C2E0B-D3AF-4DA0-8B45-D5FF1335C350
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b203152c8fae5b844eeab334870bf8efb04ac20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104474820"
---
# <a name="whats-new-windows-controls"></a>Neuigkeiten (Windows-Steuerelemente)

In diesem Thema werden die Unterschiede in der Unterstützung für Designs und visuelle Stile zwischen Windows 8 und früheren Windows-Versionen beschrieben.

## <a name="through-windows-7"></a>Über Windows 7

In Windows 7 sind visuelle Stile standardmäßig aktiviert, der Benutzer kann Sie jedoch deaktivieren, indem er das klassische Windows-Design oder den Designs-Dienst deaktiviert. Wenn visuelle Stile deaktiviert sind, erhält die gesamte Benutzeroberfläche das klassische Aussehen, und die meisten Visual Styles-APIs sind nicht verfügbar. Der Modus "visuelle Stile aus" wurde durch Windows 7 beibehalten, um die verschiedenen Designs mit hohem Kontrast und das klassische Windows-Design zu unterstützen. Wenn Sie visuelle Stile und Designs mit hohem Kontrast in der gleichen Anwendung unterstützen möchten, müssen Sie in der Regel zwei separate Codepfade zum Rendern von Steuerelementen beibehalten.

## <a name="windows-8-and-later"></a>Windows 8 und höher

In Windows 8 können visuelle Stile nicht durch die **Personalisierungs** Seite der **PC-Einstellungen** oder durch Ausschalten des Designs-Diensts ausgeschaltet werden. Der klassische Windows-Modus ist nicht mehr vorhanden, und der Modus für hohe Kontraste wurde geändert, um mit visuellen Stilen arbeiten zu können. Aufgrund dieser Änderungen benötigen Anwendungen, die nur auf Windows 8 abzielen, nicht mehr zwei separate Codepfade, um visuelle Stile und Designs mit hohem Kontrast zu unterstützen.

Visuelle Stile in Windows 8 enthalten abwärts Kompatibilitäts Unterstützung für den klassischen Windows-themenmodus. Alle Benutzeroberflächen-Renderingcodes, die auf früheren Versionen funktionieren, funktionieren unter Windows 8 weiterhin ohne Änderungen.

Wenn die Anwendung in Windows 8 die Designs mit hohem Kontrast, die auf visuellen Stilen basieren, unterstützen soll, müssen Sie die Windows 8-GUID in den Kompatibilitäts Abschnitt Ihres Anwendungs Manifests einschließen. Andernfalls geht das System davon aus, dass die Anwendung auf eine frühere Version ausgelegt ist, und rendert den Client Bereich durch Simulieren der klassischen Windows-Designs mit hohem Kontrast. Weitere Informationen finden Sie [unter unterstützen von hoher Kontrast](supporting-high-contrast-themes.md)Designs.

Wie in früheren Versionen unterstützt Windows 8 sowohl Version 5 als auch Version 6 der allgemeinen Steuerelemente, wobei Version 5 die Standardeinstellung ist. Da nur Version 6 visuelle Stile unterstützt, müssen Sie im Anwendungs Manifest Version 6 angeben, wenn visuelle Stile auf die allgemeinen Steuerelemente im Client Bereich Ihrer Anwendung angewendet werden sollen. Weitere Informationen finden Sie unter [Aktivieren von visuellen Stilen](cookbook-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Aktivieren von visuellen Stilen](cookbook-overview.md)
</dt> <dt>

[Unterstützen von hoher Kontrast Designs](supporting-high-contrast-themes.md)
</dt> <dt>

[Visuelle Stile](themes-overview.md)
</dt> <dt>

[Übersicht über visuelle Stile](visual-styles-overview.md)
</dt> </dl>

 

 




