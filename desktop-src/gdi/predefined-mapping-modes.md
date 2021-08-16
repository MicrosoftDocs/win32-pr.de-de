---
description: Von den sechs vordefinierten Zuordnungsmodi ist einer geräteabhängig (MM \_ TEXT), und die restlichen fünf (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM \_ LOMETRIC und MM \_ TWIPS) sind geräteunabhängig.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Vordefinierte Zuordnungsmodi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c0eecce6196672db11d61326c82364c1fde1d1b494e48ff77e214e79df91e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037678"
---
# <a name="predefined-mapping-modes"></a>Vordefinierte Zuordnungsmodi

Von den sechs vordefinierten Zuordnungsmodi ist einer geräteabhängig (MM \_ TEXT), und die restlichen fünf (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM \_ LOMETRIC und MM \_ TWIPS) sind geräteunabhängig.

Der Standardzuordnungsmodus ist MM \_ TEXT. Eine logische Einheit entspricht einem Pixel. Positives x befindet sich auf der rechten Seite, und positives y ist ausgefallen. Dieser Modus wird direkt dem Koordinatensystem des Geräts zugeordnet. Die logische zu physische Zuordnung umfasst nur einen Offset in x und y, der durch die anwendungsgesteuerten Fenster- und Viewportursprungs definiert wird. Die Viewport- und Fenster-Erweiterungen sind alle auf 1 festgelegt, wodurch eine 1:1-Zuordnung erstellt wird.

Anwendungen, die geometrische Formen (Kreise, Quadrate, Polygone usw.) anzeigen, verwenden einen der geräteunabhängigen Zuordnungsmodi. Wenn Sie z. B. eine Anwendung schreiben, um Diagrammfunktionen für ein Tabellenkalkulationsprogramm bereitzustellen, und sicherstellen möchten, dass der Stärke jedes Kreisdiagramms 2 Zoll beträgt, verwenden Sie den MM \_ LOENGLISH-Zuordnungsmodus, und rufen Sie die entsprechenden Funktionen auf, um das Diagramm zu zeichnen und zu füllen. Durch die Angabe von MM \_ LOENGLISH wird sichergestellt, dass der Stärke des Diagramms auf allen Anzeigen oder Druckern konsistent ist. Wenn MM \_ TEXT anstelle von MM \_ LOENGLISH verwendet wird, erscheint ein Diagramm, das auf einer VGA-Anzeige kreisförmig erscheint, elliptisch auf einem EGA-Display und sehr klein auf einem 300 dpi-Drucker (Punkte pro Zoll).

 

 



