---
description: Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht
ms.assetid: ACAC2375-EA6C-4AA1-90B7-0BF237A51C02
title: Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7dd876dcf8d25ebe7e6cca15ea88bfeba52aa29e3e5d83680815c15f8bda46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329509"
---
# <a name="fixing-compatibility-issues-in-web-applications-by-using-compatibility-view"></a>Beheben von Kompatibilitätsproblemen in Webanwendungen mit Kompatibilitätsansicht

In diesem Abschnitt werden grundlegende Schritte zur Entschärfung beschrieben, und es wird beschrieben, wie Sie die zukünftige Anwendungskompatibilität planen, während Sie probleme jetzt beheben.

Windows Internet Explorer unterstützt die Legacy-Internet Explorer, wenn dies möglich ist, sodass sich die Von Ihnen entwickelten Standorte in neueren Versionen von Internet Explorer. Ab Windows Internet Explorer 8 können Sie legacy-Verhalten unterstützen, indem Sie den Renderingmodus seite für Seite auswählen.

Internet Explorer 8 enthält die folgenden Renderingmodi, die Sie mithilfe des X-UA-kompatiblen Headers festlegen können.



| Wert für „content“ | BESCHREIBUNG                                                                           |
|---------------|---------------------------------------------------------------------------------------|
| IE=5          | Verwenden Sie den Quirks-Modus.                                                                      |
| IE=7          | Verwenden Sie immer Windows Internet Explorer 7-Modus.                                          |
| IE=EmulateIE7 | Wird im Internet Explorer 7 angezeigt, es sei denn, die Website verfügt über die EigenheitEN DOCTYPE.           |
| IE=8          | Verwenden Sie immer Internet Explorer 8-Modus.                                                  |
| IE=EmulateIE8 | Überschreiben Kompatibilitätsansicht auf Clientcomputern und Verwenden Internet Explorer 8-Modus.      |
| IE=Edge       | Wird im neuesten Modus angezeigt. In Internet Explorer 8 entspricht dieser Wert IE=8. |



 

In den folgenden Themen wird beschrieben, wie Webanwendungen mithilfe von Kompatibilitätsansicht.



| Thema                                                                                                  | Beschreibung                                                                    |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Was ist Kompatibilitätsansicht](what-is-compatibility-view-.md)                                          | Beschreibt Kompatibilitätsansicht.                                                  |
| [Warum benötigen Sie Kompatibilitätsansicht?](why-do-you-need-compatibility-view-.md)                         | Beschreibt die Gründe für die Verwendung Kompatibilitätsansicht.                               |
| [Verwenden des Metatags zum Sicherstellen der zukünftigen Kompatibilität](use-the-meta-tag-to-ensure-future-compatibility.md) | Beschreibt, wie Sie das Metaelement **verwenden** können, um zukünftige Kompatibilität sicherzustellen. |



 

 

 



