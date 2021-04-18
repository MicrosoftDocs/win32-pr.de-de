---
description: .
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43f4ff54a919058127a5f72ba60f3683c6583e1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/03/2021
ms.locfileid: "106371828"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Beheben von Kompatibilitätsproblemen in Webanwendungen mithilfe der Kompatibilitäts Ansicht

In diesem Abschnitt werden die grundlegenden Schritte zur Entschärfung beschrieben und erläutert, wie Sie zukünftige Anwendungs Kompatibilität planen, während Sie Probleme beheben.

Windows Internet Explorer unterstützt die älteren Internet Explorer-Modelle, wenn dies möglich ist, sodass Websites, die Sie für diese entwickeln, sich in neueren Versionen von Internet Explorer weiterhin erwartungsgemäß verhalten. Ab Windows Internet Explorer 8 können Sie das Legacy Verhalten unterstützen, indem Sie den Renderingmodus Seite für Seite auswählen.

Internet Explorer 8 umfasst die folgenden Renderingmodi, die Sie mit dem X-UA-kompatiblen Header festlegen können.



| Wert für „content“ | BESCHREIBUNG                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Verwenden Sie den quirsmodus.                                                                      |
| IE = 7          | Verwenden Sie immer den Windows Internet Explorer 7-Modus.                                          |
| IE=EmulateIE7 | Anzeige im Internet Explorer 7-Modus, es sei denn, die Website verfügt über den quiringdoctype.           |
| IE = 8          | Verwenden Sie immer den Internet Explorer 8-Modus.                                                  |
| IE=EmulateIE8 | Überschreiben Sie die Kompatibilitäts Ansicht auf Client Computern und den Internet Explorer 8-Modus.      |
| IE=Edge       | Wird im aktuellen Modus angezeigt. In Internet Explorer 8 entspricht dieser Wert IE = 8. |



 

In den folgenden Themen wird beschrieben, wie Webanwendungen mithilfe der Kompatibilitäts Ansicht aktualisiert werden.



| Thema                                                                                                  | BESCHREIBUNG                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Was ist die Kompatibilitäts Ansicht?](what-is-compatibility-view-.md)                                          | Beschreibt die Kompatibilitäts Ansicht.                                                  |
| [Warum benötigen Sie eine Kompatibilitäts Ansicht?](why-do-you-need-compatibility-view-.md)                         | Beschreibt, warum Sie die Kompatibilitäts Ansicht verwenden sollten.                               |
| [Verwenden des Meta-Tags zum Sicherstellen der zukünftigen Kompatibilität](use-the-meta-tag-to-ensure-future-compatibility.md) | Beschreibt, wie Sie mit dem **Meta** -Element zukünftige Kompatibilität gewährleisten können. |



 

 

 



