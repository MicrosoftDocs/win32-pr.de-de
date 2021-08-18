---
title: ITTSBufNotifySinkW
description: ITTSBufNotifySinkW
ms.assetid: 00f4a529-2db1-4cad-9340-ed95999448f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de27451826a232092bc74e630a54621a004cc15e44ad4a9a7d3377509ff00ca5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118476717"
---
# <a name="ittsbufnotifysinkw"></a>ITTSBufNotifySinkW

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Die Engine muss über **BookMark** aufrufen. Während der Vorverarbeitung der Sprachausgabe fügt der Microsoft-Agent-Code Lesezeichen zwischen "Wörtern" ein und verwendet die Ankunft dieser Lesezeichen, um die Geschwindigkeit des Texts im Wortsprechblasen zu steuern. SapI erfordert zwar nicht mehr als das Eintreffen dieser Lesezeichen zu einem bestimmten Zeitpunkt vor dem Ende der Äußerung, aber die Lesezeichen müssen relativ rechtzeitig zurückgegeben werden, um den Microsoft-Agent zu unterstützen.

Beachten Sie, dass es in einigen Sprachen, z. B. Japanisch, kein striktes Konzept von "Wort" gibt. Die [**Speak-Methode**](speak-method.md) des Microsoft-Agents definiert ein "Wort" als verbundene Zeichenfolge von Symbolen, die isoliert eine Bedeutung und Aussprache hat. Der Microsoft-Agent verwendet relativ einfachen Analysecode, um zu bestimmen, was ein "Wort" ist: Er sucht nach Durch Leerzeichen getrennten Symbolen. Daher gibt es drei "Wörter" in der englischen Zeichenfolge "The 101 Dalmatians": "the", "one hundred and one" und "Dalmatians". Der im Microsoft-Agent-Zuordnungstag enthaltene Text wird zu Anzeigezwecken als einzelnes "Wort" behandelt.

 

 




