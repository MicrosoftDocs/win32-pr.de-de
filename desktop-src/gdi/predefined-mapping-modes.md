---
description: Die sechs vordefinierten Zustellungs Modi sind Geräte abhängig (mm \_ -Text) und die verbleibenden fünf (mm- \_ hienglish, mm \_ -loenglish, mm \_ HIMETRIC, mm \_ lometrisch und mm \_ Twips) Geräte unabhängig voneinander.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Vordefinierte Karten Modi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104978384"
---
# <a name="predefined-mapping-modes"></a>Vordefinierte Karten Modi

Die sechs vordefinierten Zustellungs Modi sind Geräte abhängig (mm \_ -Text) und die verbleibenden fünf (mm- \_ hienglish, mm \_ -loenglish, mm \_ HIMETRIC, mm \_ lometrisch und mm \_ Twips) Geräte unabhängig voneinander.

Der standardmäßige Kartenmodus ist mm- \_ Text. Eine logische Einheit ist mit einem Pixel. Positives x ist rechts, und das positive y ist niedrig. Dieser Modus wird direkt dem Koordinatensystem des Geräts zugeordnet. Die Zuordnung zwischen logischen und physischen Dateien umfasst nur einen Offset in x und y, der durch das Anwendungs gesteuerte Fenster und die viewportursprünge definiert wird. Die Viewport-und Fensterblöcke werden alle auf 1 festgelegt und erstellen eine eins-zu-Eins-Zuordnung.

Anwendungen, die geometrische Formen (Kreise, Quadrate, Polygone usw.) anzeigen, nutzen einen der geräteunabhängigen Karten Modi. Wenn Sie z. b. eine Anwendung schreiben, um Diagramm Funktionen für ein Tabellen Kalkulations Programm bereitzustellen, und sicherstellen möchten, dass der Durchmesser jedes Kreis Diagramms 2 Zoll beträgt, verwenden Sie den \_ Zuordnungsmodus von mm loenglish, und führen Sie die entsprechenden Funktionen zum Zeichnen und Ausfüllen des Diagramms aus. \_Durch die Angabe von mm-loenglish wird sichergestellt, dass der Durchmesser des Diagramms auf jedem Bildschirm oder Drucker konsistent ist. Wenn \_ der mm-Text anstelle von mm- \_ loenglish verwendet wird, wird ein Diagramm, das in einer VGA-Anzeige zirkulär angezeigt wird, in einem EGA-Display als elliptisch angezeigt und auf einem 300 dpi-Laserdrucker (dpi pro Zoll) sehr klein angezeigt.

 

 



