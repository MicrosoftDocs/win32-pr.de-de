---
title: Ittsbusnotifysinkw
description: Ittsbusnotifysinkw
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678a1ce3013ba1d8acf01f79b4f71d2d5088f4d3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103948018"
---
# <a name="ittsbufnotifysinkw"></a>Ittsbusnotifysinkw

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Engine muss **Lesezeichen** durchlesen. Während der Vorverarbeitung der Sprachausgabe fügt der Microsoft-Agent-Code Lesezeichen zwischen "Wörtern" ein und verwendet die Ankunft dieser Lesezeichen, um das Tempo des Texts in der Wort Sprechblase zu steuern. Obwohl SAPI nicht mehr als die Ankunft dieser Lesezeichen vor dem Ende der Äußerung benötigt, müssen die Lesezeichen relativ rechtzeitig zurückgegeben werden, um den Microsoft-Agent zu unterstützen.

Beachten Sie, dass es in manchen Sprachen (z. b. Japanisch) kein Strict-Konzept für "Word" gibt. Die [**sprach**](speak-method.md) Methode von Microsoft-Agent definiert ein Wort als eine verbundene Zeichenfolge von Symbolen, die eine Bedeutung und eine Aussprache isoliert hat. Der Microsoft-Agent verwendet relativ einfachen Code, um zu bestimmen, was ein Wort ist: Es sucht nach Symbolen, die durch Leerzeichen getrennt sind. Folglich gibt es drei "Wörter" in der englischen Zeichenfolge "The 101 dalmatane": "The", "101" und "Dalmatier". Text, der im Microsoft Agent Map-Tag enthalten ist, wird als einzelnes "Wort" zu Anzeige Zwecken behandelt.

 

 




