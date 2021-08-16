---
title: Direct2D und High-DPI
description: Beschreibt, wie Direct2D die Anzeige mit hohen DPI-Daten aufnehmen kann.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, hoher DPI-Anteil
- hoher DPI-Anteil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec5c48f9a1b3552115ebbec8a54a6878716ef34675e41193ae08fb9cb8e55bc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825982"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D und High-DPI

Das Schreiben einer DPI-fähigen Anwendung ist der Schlüssel dafür, dass eine Benutzeroberfläche in einer Vielzahl von Anzeigeeinstellungen mit hohem DPI konsistent gut aussieht. Eine Anwendung, die nicht DPI-fähige Anwendungen ist, aber auf einer Anzeigeeinstellung mit hohem DPI-Anteil ausgeführt wird, kann unter vielen visuellen Artefakten wie einer falschen Skalierung von Benutzeroberflächenelementen, abgeschnittenem Text und unscharf dargestellten Bildern beeinträchtigt werden. Indem Sie Ihrer Anwendung Unterstützung für DPI-Informationen hinzufügen, machen Sie die Darstellung der Benutzeroberfläche Ihrer Anwendung besser vorhersagbar, sodass sie für Benutzer visuell ansprechender und besser lesbar ist. Glücklicherweise ist es mit Direct2D einfacher denn je, Anwendungen zu schreiben, die mit hohen DPI-Daten gut funktionieren. Dieses Thema enthält folgende Abschnitte:

-   [Unterstützung für hohe DPI-Daten in Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 und hohe DPI-Daten](#windows-8-and-high-dpi)
-   [Was ist eine DIP?](#what-is-a-dip)
-   [Zugehörige Themen](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>Unterstützung für hohe DPI-Daten in Direct2D

Direct2D bietet die folgenden Features für die Arbeit mit Szenarien mit hohem DPI-Anteil:

-   Der System-DPI wird beim Erstellen eines Renderziels mit Fenstern automatisch berücksichtigt, solange das Anwendungsmanifest angibt, dass die Anwendung den DPI ordnungsgemäß verarbeitet. (Informationen dazu, wie Sie deklarieren, dass Ihre Anwendung DPI-fähigen Ist, finden Sie unter [How to Ensure That Your Application Displays Ordnungsgemäß on High-DPI Displays](how-to--size-a-window-properly-for-high-dpi-displays.md).)
-   Er drückt Koordinaten in DIPs (Geräteunabhängige Pixel) aus, wodurch die Anwendung automatisch skaliert werden kann, wenn sich die DPI-Einstellung ändert.
-   Es ermöglicht Bitmaps, über einen DPI zu verfügen, und skaliert sie ordnungsgemäß, indem der DPI berücksichtigt wird. Dieses Feature kann auch verwendet werden, um Symbole in unterschiedlichen Auflösungen zu verwalten.
-   Die meisten Ressourcen werden in DIPs ausgedrückt, wodurch die Ressourcen automatisch unabhängig von der Auflösung werden.
-   Er verwendet einen Gleitkommakoordinatenraum und Antialiasing, sodass jeder Inhalt auf beliebige DPI skaliert werden kann.

Die Direct2D-Grafikpipeline ist für die Skalierung von 96 DPI auf 1200DPI konzipiert.

## <a name="windows-8-and-high-dpi"></a>Windows 8 und hohe DPI-Daten

Ab Windows 8 gibt es zusätzliche Features für die Unterstützung hoher DPI-Daten.

Wenn der DPI des Gerätekontexts hoch genug ist, ändert Direct2D den Schwellenwert, der verwendet wird, um vertikales Antialiasing von Text zu ermöglichen. Dies führt zu einem schnelleren Textrendering auf Hoch-DPI-Anzeigen. Darüber hinaus können Sie den Einheitenmodus mithilfe der [**ID2D1DeviceContext::SetUnitMode-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) in Pixel anstelle von DIPs ändern. Wenn Sie den Einheitenmodus auf Pixel und den Gerätekontext-DPI auf den Bildschirm-DPI festlegen, ist die Optimierung weiterhin aktiviert.

## <a name="what-is-a-dip"></a>Was ist eine DIP?

Ein geräteunabhängiges Pixel (DEVICE Independent Pixel, DIP) ist ein logisches Pixel, das den Pixeln des physischen Geräts über einen Skalar( DPI) zugeordnet wird. DPI steht für Punkte pro Zoll, wobei ein Punkt ein physisches Gerätepixel darstellt. (Die Nomenclature stammt aus dem Drucken, wobei Punkte der kleinste Ink-Punkt sind, den ein Druckvorgang erzeugen kann.) Da ein Standardmonitor bisher 96 Punkte pro Zoll hatte, bedeutete ein DPI von 96, dass ein geräteunabhängiges Pixel (oder DIP) 1:1 mit einem physischen Pixel zugeordnet wurde. Wenn der DPI beispielsweise 96 \* 2 = 192 beträgt, würde eine einzelne DIP zwei physische Pixel umfassen.

Es gibt viele Gründe, warum Anwendungen diese Skalierung nicht unbedingt ordnungsgemäß verarbeiten. Einer der einfachsten Gründe ist, dass zusätzliche Arbeit erforderlich ist, um diesen Skalarwert beim Rendern zu ermitteln und zu verwenden. In Direct2D wird die Skalierung standardmäßig angewendet. Aufgrund dieser Zuordnung können physische Gerätepixel an DIP-Bruchteilkoordinaten enden. Dies ist einer der Gründe, warum Direct2D einen Gleitkommakoordinatenraum verwendet.

<dl> physisches Pixel = (Dip × DPI) / 96  
</dl>

Verwenden Sie diese Formel, um ein physisches Pixel in eine DIP zu konvertieren:

<dl> dip = (physische Pixel × 96) / DPI  
</dl>

> [!Note]
>
> Ab Windows 8 können Sie den Einheitenmodus in Pixel anstelle von DIPs ändern, indem Sie die [**ID2D1DeviceContext::SetUnitMode-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) verwenden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sicherstellen, dass Ihre Anwendung ordnungsgemäß auf Anzeige mit hohem DPI-Anteil angezeigt wird](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 