---
description: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5acb7249854d9ac89b5601fdf83efa397c11c17
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116358"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe von Kompatibilitätsansicht

In diesem Abschnitt werden die grundlegenden Schritte zur Risikominderung und die Planung der zukünftigen Anwendungskompatibilität beschrieben, während Sie probleme beheben.

Windows Internet Explorer unterstützt nach Möglichkeit die älteren Internet Explorer-Modelle, sodass sich Standorte, die Sie für sie entwickeln, in neueren Versionen von Internet Explorer weiterhin wie erwartet verhalten. Ab Windows Internet Explorer 8 können Sie Legacyverhalten unterstützen, indem Sie den Renderingmodus seiteweise auswählen.

Internet Explorer 8 enthält die folgenden Renderingmodi, die Sie mit dem X-UA-kompatiblen Header festlegen können.



| Wert für „content“ | BESCHREIBUNG                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Verwenden Sie den quirks-Modus.                                                                      |
| IE=7          | Verwenden Sie immer den Windows Internet Explorer 7-Modus.                                          |
| IE=EmulateIE7 | Wird im Modus Internet Explorer 7 angezeigt, es sei denn, die Website verfügt über den DOCTYPE-Typ derQuirks.           |
| IE=8          | Verwenden Sie immer Internet Explorer 8 Modus.                                                  |
| IE=EmulateIE8 | Überschreiben Sie Kompatibilitätsansicht auf Clientcomputern, und verwenden Sie Internet Explorer 8-Modus.      |
| IE=Edge       | Anzeige im aktuellen Modus. In Internet Explorer 8 entspricht dieser Wert IE=8. |



 

In den folgenden Themen wird beschrieben, wie Webanwendungen mithilfe von Kompatibilitätsansicht aktualisiert werden.



| Thema                                                                                                  | BESCHREIBUNG                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Was ist Kompatibilitätsansicht](what-is-compatibility-view-.md)                                          | Beschreibt Kompatibilitätsansicht.                                                  |
| [Warum benötigen Sie Kompatibilitätsansicht?](why-do-you-need-compatibility-view-.md)                         | Beschreibt die Gründe für die Verwendung Kompatibilitätsansicht.                               |
| [Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität](use-the-meta-tag-to-ensure-future-compatibility.md) | Beschreibt, wie Sie das Metaelement **verwenden** können, um zukünftige Kompatibilität sicherzustellen. |



 

 

 



