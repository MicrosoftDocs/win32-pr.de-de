---
title: Direct2D und High-dpi
description: Beschreibt, wie Direct2D eine hohe dpi-Anzeige bietet.
ms.assetid: 1809ab0e-853f-4dac-be97-563c92b9caee
keywords:
- Direct2D, High-dpi
- High-dpi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6548849416268f31b8b0c4a4261347c818ffa24c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949060"
---
# <a name="direct2d-and-high-dpi"></a>Direct2D und High-dpi

Das Schreiben einer dpi-fähigen Anwendung ist der Schlüssel, mit dem eine Benutzeroberfläche (UI) über eine Vielzahl von Anzeigeeinstellungen mit hoher dpi hinweg konsistent aussehen kann. Eine Anwendung, die nicht dpi-fähig ist, aber in einer Einstellung mit hoher dpi-Anzeige ausgeführt wird, kann von vielen visuellen Elementen leiden, einschließlich falscher Skalierung von Benutzeroberflächen Elementen, ausgeschnittenen Text und unscharfe Bilder. Durch Hinzufügen von Unterstützung in Ihrer Anwendung für dpi-Bewusstsein machen Sie die Darstellung der Benutzeroberfläche Ihrer Anwendung besser vorhersagbar, sodass Sie für Benutzer visuell ansprechend und leichter lesbar ist. Glücklicherweise erleichtert Direct2D das Schreiben von Anwendungen, die gut in High-dpi funktionieren. Dieses Thema enthält folgende Abschnitte:

-   [High-dpi-Unterstützung in Direct2D](#high-dpi-support-in-direct2d)
-   [Windows 8 und High-dpi](#windows-8-and-high-dpi)
-   [Was ist eine DIP?](#what-is-a-dip)
-   [Zugehörige Themen](#related-topics)

## <a name="high-dpi-support-in-direct2d"></a>High-dpi-Unterstützung in Direct2D

Direct2D bietet die folgenden Features für die Arbeit mit Szenarien mit hoher dpi-Verwendung:

-   Der System-dpi wird beim Erstellen eines Renderziels automatisch berücksichtigt, solange das Anwendungs Manifest angibt, dass dpi korrekt von der Anwendung verarbeitet wird. (Informationen dazu, wie Sie deklarieren, dass Ihre Anwendung dpi-fähig ist, finden [Sie unter sicherstellen, dass Ihre Anwendung ordnungsgemäß auf hoch-dpi-anzeigen angezeigt](how-to--size-a-window-properly-for-high-dpi-displays.md)wird.)
-   Er drückt Koordinaten in Dips (geräteunabhängige Pixel) aus, sodass die Anwendung automatisch skaliert werden kann, wenn die dpi-Einstellung geändert wird.
-   Bitmaps können einen dpi-Wert aufweisen und diese ordnungsgemäß skalieren, indem Sie den dpi-Wert berücksichtigen. Diese Funktion kann auch verwendet werden, um Symbole in unterschiedlichen Auflösungen beizubehalten.
-   Die meisten Ressourcen werden in Dips ausgedrückt, wodurch die Ressourcen automatisch unabhängig von der Auflösung werden.
-   Es verwendet einen Gleit Komma Koordinaten Bereich und Antialiasing, sodass jeder Inhalt auf beliebige dpi-Werte skaliert werden kann.

Die Direct2D-Grafik Pipeline ist so konzipiert, dass Sie zwischen 96 dpi und 1200dpi skaliert.

## <a name="windows-8-and-high-dpi"></a>Windows 8 und High-dpi

Ab Windows 8 gibt es zusätzliche Features für die Unterstützung von hoch dpi.

Wenn der Gerätekontext dpi hoch genug ist, ändert Direct2D den Schwellenwert, der zum Aktivieren des vertikalen Antialiasing von Text verwendet wird. Dies führt zu schnellerem Text Rendering in hoch dpi-anzeigen. Darüber hinaus können Sie den Einheits Modus mithilfe der [**ID2D1DeviceContext::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) *-Methode auf Pixel anstelle von Dips umstellen. Wenn Sie den Einheiten Modus auf Pixel und den Gerätekontext dpi auf den Bildschirm dpi festlegen, ist die Optimierung weiterhin aktiviert.

## <a name="what-is-a-dip"></a>Was ist eine DIP?

Bei einem geräteunabhängigen Pixel (DIP) handelt es sich um ein logisches Pixel, das den Pixeln des physischen Geräts über einen skalaren, den dpi-Wert zugeordnet wird. DPI steht für Punkte pro Zoll, wobei ein Punkt ein physisches Geräte Pixel darstellt. (Die Nomenklatur stammt aus dem Druck, wobei Punkte der kleinste frei Hand Punkt sind, den ein Druckprozess verursachen kann). Da ein Standard Monitor, der 96 Punkte pro Zoll hat, den dpi-Wert 96 bedeutete, dass ein Geräte unabhängiges Pixel (oder DIP) 1:1 mit einem physischen Pixel zugeordnet hat. Wenn z. b. der dpi-Code 96 \* 2 = 192 ist, würde eine einzelne DIP zwei physische Pixel umfassen.

Es gibt zahlreiche Gründe, warum Anwendungen diese Skalierung nicht unbedingt ordnungsgemäß verarbeiten müssen. einer der einfachsten Gründe hierfür ist, dass zusätzliche Arbeit erforderlich ist, um diesen Skalarwert beim Rendern zu ermitteln und zu verwenden. In Direct2D wird die Skalierung standardmäßig angewendet. Aufgrund dieser Zuordnung kann es vorkommen, dass physische Geräte Pixel an Bruch Koordinaten in Bruchteilen stehen. Dies ist einer der Gründe, warum Direct2D einen Gleit Komma Koordinaten Bereich verwendet.

<dl> physisches Pixel = (DIP × dpi)/96  
</dl>

Um ein physisches Pixel in eine DIP zu konvertieren, verwenden Sie die folgende Formel:

<dl> DIP = (physisches Pixel × 96)/dpi  
</dl>

> [!Note]
>
> Ab Windows 8 können Sie den Einheits Modus mithilfe der [**ID2D1DeviceContext::**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-setunitmode) *-Methode auf Pixel anstelle von Dips umstellen.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[So stellen Sie sicher, dass Ihre Anwendung auf hoch-dpi-anzeigen ordnungsgemäß angezeigt wird](how-to--size-a-window-properly-for-high-dpi-displays.md)
</dt> </dl>

 

 