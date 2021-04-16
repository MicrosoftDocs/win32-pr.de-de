---
title: Treffer Test Optionen
description: In diesem Abschnitt werden die Optionswerte aufgelistet, die mit dem dwOptions-Parameter der hittesttemebackground-Funktion verwendet werden. Eine Liste der Werte, die zurückgegeben werden, wenn Sie eine dieser Optionen angeben, finden Sie unter Treffer Test-Rückgabewerte.
ms.assetid: a0d5c6c8-bb50-46e1-98ae-2374842344c6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 638a7aaca83c658ad852b195cdb9514210a14c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471293"
---
# <a name="hit-test-options"></a>Treffer Test Optionen

In diesem Abschnitt werden die Optionswerte aufgelistet, die mit dem *dwOptions* -Parameter der [**hittesttemebackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) -Funktion verwendet werden. Eine Liste der Werte, die zurückgegeben werden, wenn Sie eine dieser Optionen angeben, finden Sie unter [Treffer Test-Rückgabewerte](theme-hit-test-retval.md).

## <a name="option-values"></a>Optionswerte

In der folgenden Tabelle sind die Treffer Test Optionen aufgeführt.



| Option                       | Wert                                                                                                                    | BESCHREIBUNG                                                                                                                                                                         |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| httb \_ backgroundgg          | 0x00000000                                                                                                               | Treffer Testoption des Design Hintergrund Segments.                                                                                                                                           |
| httb \_ fixedborder            | 0x00000002                                                                                                               | Die Option "fester Rahmen Treffer Test".                                                                                                                                                       |
| httb- \_ Beschriftung                | 0x00000004                                                                                                               | Caption-Treffer Testoption.                                                                                                                                                            |
| httb \_ resizingborder         | (Httb \_ resizingborder \_ left \| httb \_ resizingborder \_ Top \| httb \_ resizingborder \_ right \| httb \_ resizingborder \_ Bottom) | Ändern der Größe von Rahmen Treffer Test Optionen.                                                                                                                                                   |
| httb \_ resizingborder \_ left   | 0x00000010                                                                                                               | Option zum Ändern der Größe des linken Rahmens.                                                                                                                                               |
| httb \_ resizingborder \_ Top    | 0x00000020                                                                                                               | Die Größe der Top-Border-Treffer Testoption wird geändert                                                                                                                                                |
| httb \_ resizingborder \_ right  | 0x00000040                                                                                                               | Option zum Ändern der Größe des rechten Rahmens.                                                                                                                                              |
| httb \_ resizingborder \_ Bottom | 0x00000080                                                                                                               | Größe des Rahmens für den unteren Rahmen der Treffer Änderung.                                                                                                                                             |
| httb \_ SizingTemplate         | 0x00000100                                                                                                               | Die Größe der Rahmengröße wird als Vorlage angegeben, nicht nur als Fensterkanten. Diese Option schließt sich mit httb \_ systemsizingmargin gegenseitig aus. Httb \_ SizingTemplate hat Vorrang.         |
| httb \_ systemsizingmargin    | 0x00000200                                                                                                               | Verwendet die Rahmenbreite für die Größe des Systems für die Größe anstelle visueller Stil Inhalts Ränder. Diese Option schließt sich mit "httb \_ SizingTemplate;" gegenseitig aus. Httb \_ SizingTemplate hat Vorrang. |



 

 

 




