---
title: Unterstützung für synthetisierte Sprache
description: Unterstützung für synthetisierte Sprache
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
# <a name="synthesized-speech-support"></a>Unterstützung für synthetisierte Sprache

\[Microsoft Agent ist ab Version Windows 7 veraltet und möglicherweise in nachfolgenden Versionen von Windows.\]

Wenn Sie synthetisierte Sprache verwenden, kann Ihr Zeichen fast alles sagen, was die größte Flexibilität bietet. Mit aufgezeichneten Audiodaten können Sie dem Zeichen eine bestimmte oder eindeutige Stimme geben. Um die Ausgabe anzugeben, geben Sie den gesprochenen Text als Parameter der [**Speak-Methode**](speak-method.md) an.

Da die Microsoft Agent-Architektur Microsoft SAPI für die synthetisierte Sprachausgabe verwendet, können Sie jede Engine verwenden, die dieser Spezifikation entspricht, und die IPA-Ausgabe (International Phonetic Alphabet) mithilfe der [**Visual-Methode**](https://www.bing.com/search?q=**Visual**) der [**ITTSNotifySinkW-Schnittstelle**](ittsnotifysinkw.md) unterstützen. Weitere Informationen zu den Engine-Anforderungen finden Sie unter [Supportanforderungen für die Spracherkennungs-Engine.](requirements-for-text-to-speech-engines.md)

Die Sprach-ID-Einstellung eines Zeichens bestimmt seine TTS-Ausgabe. Wenn ein Client keine Sprach-ID für das Zeichen an gibt, wird die Sprach-ID des Zeichens auf die Standardsprach-ID des Benutzers festgelegt. Wenn die Definition des Zeichens eine bestimmte Engine enthält und diese Engine geladen werden kann und der Spracheinstellung des Zeichens entspricht, wird diese Engine verwendet. Andernfalls werden von Microsoft Agent die anderen verfügbaren Engines aufzählt und eine optimale SAPI-Übereinstimmung basierend auf Sprache, Geschlecht und Alter (in dieser Reihenfolge) anfordern. Wenn keine übereinstimmende Engine verfügbar ist, gibt es keine TTS-Ausgabe für die Verwendung des Zeichens durch diesen Client. Der -Agent versucht, die TTS-Engine beim ersten [**Speak-Aufruf**](speak-method.md) oder beim Abfragen oder erfolgreichen Festlegen der Modus-ID zu laden.

Eine Clientanwendung kann auch eine TTS-Engine für das Zeichen angeben (mithilfe der [**TTSModeID-Eigenschaft).**](ttsmodeid-property.md) Dadurch wird der Versuch des Servers überschrieben, automatisch eine übereinstimmende Engine basierend auf der bevorzugten TTS-Modus-ID des Zeichens oder der aktuellen Sprach-ID-Einstellung des Zeichens zu finden. Wenn diese Engine jedoch nicht installiert ist (oder anderweitig nicht geladen werden kann), tritt beim Aufruf ein Fehler auf (und es wird ein Fehler im Steuerelement ausgegeben). Der Server versucht dann, basierend auf der Sprach-ID, der TTS-Einstellung für kompilierte Zeichen und den verfügbaren TTS-Engines eine weitere Engine zu laden. Wenn immer noch keine Übereinstimmung vorhanden ist, ist TTS für diesen Client nicht verfügbar, aber das Zeichen kann weiterhin in seinen Wortsprechblasen sprechen.

Nur die TTS-Engines, die von jedem Client verwendet werden, bleiben geladen. Wenn beispielsweise ein Zeichen eine definierte Einstellung für eine bestimmte Engine hat und diese Engine verfügbar ist, ihre Clientanwendung jedoch eine andere Engine angegeben hat (indem die Sprach-ID eines Zeichens anders als die Engine festgelegt oder eine andere Modus-ID angegeben wird), bleibt nur die von Ihrer Anwendung angegebene Engine geladen. Die Engine, die mit der definierten Einstellung des Zeichens für eine TTS-Einstellung übereinstimmen, wird entladen (es sei denn, ein anderer Client verwendet die kompilierte Engine-Einstellung des Zeichens).

 

 




