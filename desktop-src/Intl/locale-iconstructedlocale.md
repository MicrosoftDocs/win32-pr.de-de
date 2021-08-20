---
description: LOCALE \_ ICONSTRUCTEDLOCALE constant description
ms.assetid: 5557ee1e-09bf-0d0b-8e73-df32d9a406dd
title: LOCALE_ICONSTRUCTEDLOCALE
ms.topic: article
ms.date: 09/01/2020
ms.openlocfilehash: 26d54ce55393f54d56f521231e257a8b0692758f8e6c830a890d81c8f82e8422
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809638"
---
# <a name="locale_iconstructedlocale"></a>LOCALE \_ ICONSTRUCTEDLOCALE

Bezeichner, der anfordern soll, wenn das Locale ein "konstruiertes" Locale ist. Von der Verwendung dieses LCTYPE wird abgeraten.

Dadurch wird ein Locale identifiziert, Windows viele nicht über vollständige Informationen verfügen und informationen zur Laufzeit "erstellen" müssen. In der Regel sind die von LOCALE_ICONSTRUCTEDLOCALE bereitgestellten Informationen eingeschränkt, da Windows so viele Daten wie für jedes Einzelne verfügbar sind. Daher wird davon abgeraten, diesen LCTYPE zu verwenden.


| Wert | Bedeutung                 |
|-------|-------------------------|
| 0     | Nicht erstellt         |
| 1     | Ein konstruiertes Locale |


Ein Beispiel wäre eine Anforderung für "de-US" oder Deutsch in der USA. NLS verwendet die daten der deutschen Sprache, die es finden kann, und die USA Region, die es finden kann. 

Dies ist möglicherweise nicht perfekt, da das System z. B. wahrscheinlich keine Informationen über den Namen des USA auf Deutsch hat. Wenn die Anwendung oder der Benutzer jedoch einen "de-US"-Kontext wünschen, sind die zurückgegebenen Daten die besten verfügbaren. 

Apps, die LOCALE_ICONSTRUCTEDLOCALE verwenden, um Lokale abzulehnen und auf ein anderes Locale zurückfallen, haben in der Regel eine schlechtere Erfahrung, z. B. das Landen auf de-DE oder en-US in diesem Beispiel. Keiner dieser Sprachen liegt in der Nähe der ursprünglichen Anforderung für die deutsche Sprache mit einer USA Region.

