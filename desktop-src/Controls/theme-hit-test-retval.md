---
title: Treffer Test-Rückgabewerte
description: In diesem Abschnitt werden die Treffer Test-Codewerte aufgelistet, die im pwhittestcode-Parameter der hittesttemebackground-Funktion zurückgegeben werden.
ms.assetid: 95b4fc1a-2f9b-4464-b672-552d36b60c42
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 219cb59115bae56ac6cc3ba7f05384c331969b34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036802"
---
# <a name="hit-test-return-values"></a>Treffer Test-Rückgabewerte

In diesem Abschnitt werden die Treffer Test-Codewerte aufgelistet, die im *pwhittestcode* -Parameter der [**hittesttemebackground**](/windows/desktop/api/Uxtheme/nf-uxtheme-hittestthemebackground) -Funktion zurückgegeben werden. Welche Codewerte zurückgegeben werden, hängt von den Treffer Test Optionen ab, die im *dwOptions* -Parameter der Funktion " **hittestpoinmebackground** " angegeben sind. Eine Liste der Optionen finden Sie unter [Treffer Test Optionen](theme-hit-test-options.md).

## <a name="return-values"></a>Rückgabewerte

In der folgenden Tabelle sind die Treffer Test Optionen und die entsprechenden Rückgabecodes aufgeführt.



| Option                       | Rückgabecodes  | BESCHREIBUNG                                                                                                        |
|------------------------------|---------------|--------------------------------------------------------------------------------------------------------------------|
| httb \_ backgroundgg          | Htbottom      | Der Treffer Test war erfolgreich im unteren Rahmen Segment.                                                                   |
|                              | Htbottomleft  | Der Treffer Test war im unteren und linken Rahmen Bereich erfolgreich.                                                     |
|                              | Htbottomright | Der Treffer Test war im unteren und rechten Rahmen Bereich erfolgreich.                                                    |
|                              | Htclient      | Der Treffer Test war erfolgreich im mittleren Hintergrund Segment.                                                               |
|                              | Htleft        | Der Treffer Test war im linken Rahmen Segment erfolgreich.                                                                     |
|                              | Htnirgendwo     | Der Treffer Test war außerhalb des Steuer Elements oder eines transparenten Bereichs erfolgreich.                                                   |
|                              | Htright       | Der Treffer Test war erfolgreich im rechten Rahmen Segment.                                                                    |
|                              | Httop         | Der Treffer Test war erfolgreich im oberen Rahmen Segment.                                                                      |
|                              | Httopleft     | Der Treffer Test war erfolgreich in der oberen und linken Rahmen Schnittmenge.                                                            |
|                              | Httopright    | Der Treffer Test war am oberen und rechten Randbereich erfolgreich.                                                       |
| httb- \_ Beschriftung                | Htcaption     | Der Treffer Test war erfolgreich in den ersten, oberen linken oder oberen rechten Hintergrund Segmenten.                                         |
|                              | Htnirgendwo     | Der Treffer Test war außerhalb des Steuer Elements oder eines transparenten Bereichs erfolgreich.                                                   |
| httb \_ fixedborder            | "Htborder"      | Der Treffer Test war in einem beliebigen Hintergrund Segment außer dem mittleren Hintergrund Segment erfolgreich.                                 |
|                              | Htclient      | Der Treffer Test war erfolgreich im mittleren Hintergrund Segment.                                                               |
| httb \_ resizingborder         | "Htborder"      | Fehler beim Treffer Test im mittleren Hintergrund Segment und in der Größe der Zonen Größe, jedoch in einem Hintergrund Rahmen Segment. |
| httb \_ resizingborder \_ Bottom | Htbottom      | Der Treffer Test war erfolgreich im unteren Rahmen Segment.                                                                   |
| httb \_ resizingborder \_ left   | Htleft        | Der Treffer Test war im linken Rahmen Segment erfolgreich.                                                                     |
| httb \_ resizingborder \_ right  | Htright       | Der Treffer Test war erfolgreich im rechten Rahmen Segment.                                                                    |
| httb \_ resizingborder \_ Top    | Httop         | Der Treffer Test war erfolgreich im oberen Rahmen Segment.                                                                      |



 

 

 




