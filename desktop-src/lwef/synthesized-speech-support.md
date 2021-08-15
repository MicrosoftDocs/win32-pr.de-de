---
title: Unterstützung von synthetisierter Sprache
description: Unterstützung von synthetisierter Sprache
ms.assetid: 38172e04-a5b6-41e4-9d7c-539d9d4117be
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c31fcb655ccb5a8fbb2ffbbb8d01d1da317209fbfa3e270a76d92208c06777df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118475322"
---
# <a name="synthesized-speech-support"></a>Unterstützung von synthetisierter Sprache

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Wenn Sie synthetisierte Sprache verwenden, kann Ihr Zeichen fast alles sagen, was die größte Flexibilität bietet. Mit aufgezeichneten Audiodaten können Sie dem Zeichen eine bestimmte oder eindeutige Stimme geben. Um die Ausgabe anzugeben, geben Sie den gesprochenen Text als Parameter der [**Speak-Methode**](speak-method.md) an.

Da die Architektur des Microsoft-Agents Microsoft SAPI für die synthetisierte Sprachausgabe verwendet, können Sie eine beliebige Engine verwenden, die dieser Spezifikation entspricht, und die IPA-Ausgabe (International Phonetic Alphabet) mithilfe der [**Visual-Methode**](https://www.bing.com/search?q=**Visual**) der [**ITTSNotifySinkW-Schnittstelle**](ittsnotifysinkw.md) unterstützt. Weitere Informationen zu den Engine-Anforderungen finden Sie unter Supportanforderungen für die [Sprach-Engine.](requirements-for-text-to-speech-engines.md)

Die Sprach-ID-Einstellung eines Zeichens bestimmt die TTS-Ausgabe. Wenn ein Client keine Sprach-ID für das Zeichen angibt, wird die Sprach-ID des Zeichens auf die Standardsprach-ID des Benutzers festgelegt. Wenn die Definition des Zeichens eine bestimmte Engine enthält und diese Engine geladen werden kann und der Spracheinstellung des Zeichens entspricht, wird diese Engine verwendet. Andernfalls listet der Microsoft-Agent die anderen verfügbaren Engines auf und fordert eine SAPI-Beste Übereinstimmung basierend auf Sprache, Geschlecht und Alter (in dieser Reihenfolge) an. Wenn keine übereinstimmende Engine verfügbar ist, gibt es keine TTS-Ausgabe für die Verwendung des Zeichens durch diesen Client. Der Agent versucht, die TTS-Engine beim ersten [**Speak-Aufruf**](speak-method.md) oder beim Abfragen oder erfolgreichen Festlegen der Modus-ID zu laden.

Eine Clientanwendung kann auch eine TTS-Engine für ihr Zeichen angeben (mithilfe der [**TTSModeID-Eigenschaft).**](ttsmodeid-property.md) Dadurch wird der Versuch des Servers überschrieben, basierend auf der bevorzugten TTS-Modus-ID des Zeichens oder der aktuellen Sprach-ID-Einstellung des Zeichens automatisch eine übereinstimmende Engine zu finden. Wenn diese Engine jedoch nicht installiert ist (oder anderweitig nicht geladen werden kann), schlägt der Aufruf fehl (und gibt einen Fehler im Steuerelement aus). Der Server versucht dann, basierend auf der Sprach-ID, der TTS-Einstellung für kompilierte Zeichen und den verfügbaren TTS-Engines eine andere Engine zu laden. Wenn immer noch keine Übereinstimmung vorhanden ist, ist TTS für diesen Client nicht verfügbar, aber das Zeichen kann trotzdem in seinen Wortsprechblasen sprechen.

Nur die TTS-Engines, die von einem beliebigen Client verwendet werden, bleiben geladen. Wenn z. B. ein Zeichen eine definierte Einstellung für eine bestimmte Engine hat und diese Engine verfügbar ist, ihre Clientanwendung jedoch eine andere Engine angegeben hat (indem die Sprach-ID eines Zeichens anders als die Engine festgelegt oder eine andere Modus-ID angegeben wurde), bleibt nur die von der Anwendung angegebene Engine geladen. Die Engine, die der definierten Einstellung des Zeichens für eine TTS-Einstellung entspricht, wird entladen (es sei denn, ein anderer Client verwendet die kompilierte Engine-Einstellung des Zeichens).

 

 




