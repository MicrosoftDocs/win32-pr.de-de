---
title: Sprachunterstützung in synthetischer Sprache
description: Sprachunterstützung in synthetischer Sprache
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8a89610a912cf601724bc9a2153cba8343e6feb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104036937"
---
# <a name="synthesized-speech-support"></a>Sprachunterstützung in synthetischer Sprache

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Wenn Sie die Sprachausgabe verwenden, können Sie mit dem Zeichen fast alles sagen, was die größte Flexibilität bietet. Mit der aufgezeichneten Audiodatei können Sie dem Zeichen eine bestimmte oder eindeutige Stimme übergeben. Um die Ausgabe anzugeben, geben Sie den gesprochenen Text als Parameter der [**Sprech**](speak-method.md) Methode an.

Da in der Microsoft-Agent-Architektur Microsoft SAPI für die Sprachausgabe in synthetischer Sprache verwendet wird, können Sie jedes Modul verwenden, das dieser Spezifikation entspricht, und mithilfe der [**visuellen**](https://www.bing.com/search?q=**Visual**) Methode der [**ittsnotifysinkw**](ittsnotifysinkw.md) -Schnittstelle die Verwendung von International Phonetic Alphabet (IPA) unterstützen. Weitere Informationen zur-Engine, die von benötigt werden, finden Sie [unter Support Anforderungen für sprach](requirements-for-text-to-speech-engines.md)Modul.

Die Sprach-ID-Einstellung eines Zeichens bestimmt seine TTS-Ausgabe. Wenn ein Client keine Sprachen-ID für das Zeichen angibt, wird die Sprach-ID des Zeichens auf die Benutzer-Standardsprachen-ID festgelegt. Wenn die Definition des Zeichens eine bestimmte Engine enthält und diese Engine geladen werden kann, und Sie mit der Spracheinstellung des Zeichens übereinstimmt, wird diese Engine verwendet. Andernfalls listet der Microsoft-Agent die anderen verfügbaren Engines auf und fordert basierend auf Sprache, Geschlecht und Alter (in dieser Reihenfolge) eine am besten geeignete SAPI-Entsprechung auf. Wenn keine übereinstimmende Engine verfügbar ist, gibt es keine TTS-Ausgabe für die Verwendung des Zeichens durch den Client. Der-Agent versucht, die TTS-Engine beim ersten [**Sprech**](speak-method.md) Vorgang oder bei der Abfrage oder erfolgreichen Festlegung der Mode-ID zu laden.

Eine Client Anwendung kann auch eine TTS-Engine für das Zeichen angeben (mithilfe der [**ttsmodeid**](ttsmodeid-property.md) -Eigenschaft). Dadurch wird der Versuch des Servers überschrieben, automatisch eine passende Engine basierend auf der bevorzugten TTS-Modus-ID des Zeichens oder der aktuellen Sprach-ID des Zeichens zu finden. Wenn diese Engine jedoch nicht installiert ist (oder nicht anderweitig geladen werden kann), schlägt der-Befehl fehl (und verursacht einen Fehler im-Steuerelement). Der Server versucht dann, ein anderes Modul basierend auf der Sprach-ID, der Einstellung der kompilierten Zeichen und der verfügbaren TTS-Engines zu laden. Wenn es immer noch keine Entsprechung gibt, ist "TTS" für diesen Client nicht verfügbar, aber das Zeichen kann weiterhin in der Wort Sprechblase sprechen.

Nur die von einem Client verwendeten TTS-Engines bleiben geladen. Wenn ein Zeichen z. b. eine definierte Einstellung für eine bestimmte Engine besitzt und diese Engine verfügbar ist, aber die Client Anwendung ein anderes Modul angegeben hat (indem Sie die Sprach-ID eines Zeichens anders als die Engine festgelegt oder eine andere Modus-ID angegeben hat), bleibt nur die von der Anwendung angegebene Engine geladen. Die Engine, die der definierten Einstellung des Zeichens für eine TTS-Einstellung entspricht, wird entladen (es sei denn, ein anderer Client verwendet die kompilierte Engine-Einstellung des Zeichens).

 

 




