---
title: Anforderungen für Text-zu-Sprache-Engines
description: Anforderungen für Text-zu-Sprache-Engines
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa6d1bc9f4340327c5fbfb71b900e10f60738fdf
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471341"
---
# <a name="requirements-for-text-to-speech-engines"></a>Anforderungen für Text-zu-Sprache-Engines

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Die Engine muss vollständig SAPI 4,0-kompatibel sein. Außerdem muss die Engine die folgenden SAPI-Schnittstellen für markierte Text-und Lesezeichen Benachrichtigungen unterstützen. Diese Schnittstellen ermöglichen es dem Microsoft-Agent, die Ausgabe von Text an die Wort Sprechblase eines Zeichens zu beschleunigen und den Mund (oder die Entsprechung) des Zeichens mit den gesprochenen Wörtern zu synchronisieren.

-   [Ittscentralw](ittscentralw.md)
-   [Ittsnotifysinkw](ittsnotifysinkw.md)
-   [Ittsbusnotifysinkw](ittsbufnotifysinkw.md)
-   [Ittsattributesw](ittsattributesw.md)

 

 




