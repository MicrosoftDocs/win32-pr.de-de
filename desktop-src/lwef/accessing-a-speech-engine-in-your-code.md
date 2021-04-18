---
title: Zugreifen auf eine Sprach-Engine in Ihrem Code
description: Zugreifen auf eine Sprach-Engine in Ihrem Code
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d81841f6f287d36a6ac01fa77294b1754eeb9b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337839"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Zugreifen auf eine Sprach-Engine in Ihrem Code

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Verwenden Sie die Agent-API, um die Engine festzulegen, um ein bestimmtes Sprachmodul in Ihrem Code zu verwenden. Verwenden Sie für Spracheingabe-Engines [**srmodeid**](https://www.bing.com/search?q=**SRModeID**), und geben Sie dabei die Mode-ID für die Engine an. Beachten Sie jedoch, dass die-Engine installiert werden muss. Um zu ermitteln, ob die Engine vorhanden ist, können Sie **srmodeid** Abfragen. Die Engine muss mit der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) -Einstellung des Zeichens identisch sein. Beispielsweise können Sie **srmodeid** nicht für ein Zeichen, dessen **LanguageID** auf Französisch festgelegt ist, auf eine deutsche Spracherkennungs-Engine-Modus-ID festlegen.

**ID des Spracheingabe-Engine-Modus**



| Sprache                                    | Modus-IDs                             |
|------------------------------------------|--------------------------------------|
| Microsoft Speech Recognition Engine v 4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Aktivieren und legen Sie die [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) und [**srmodeid**](https://www.bing.com/search?q=**SRModeID**) des Zeichens in Ihrem Code fest, bevor Sie versuchen, die Grammatik für die sprach Parameter der **Befehls** Objekte Ihrer Anwendung zu definieren. Sie sollten auch die Browser-oder Systemsprache überprüfen, damit Sie sicher sein können, dass Sie der Konfiguration Ihrer Benutzer entsprechen. Die Engine schlägt möglicherweise fehl, wenn Sie versuchen, eine Grammatik für eine Sprache zu definieren, die nicht mit der Engine identisch ist.

Ein Zeichensatz für die Ausgabe von Text-zu-Sprache (TTS) kann mit der Mode-ID-Voreinstellung der Standard Sprachausgabe-Engine kompiliert werden. Wenn das-Zeichen geladen wird und die-Engine installiert ist und mit der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens übereinstimmt, versucht der-Agent, diese Modus-ID für die Sprachausgabe zu laden. Wenn das Modul nicht vorhanden ist oder über eine andere **LanguageID** verfügt, versucht der-Agent, die erste gefundene Modus-ID zu laden, die mit der **LanguageID** des Zeichens übereinstimmt, wobei jedoch weiterhin die kompilierte Geschwindigkeit und die festgelegte Einstellung für das Zeichen festgelegt wird.

Beachten Sie, dass alle vom Microsoft-Agent bereitgestellten Zeichen für die Verwendung der "lerout & Hauspie truvoice-American-Engine als Standard-Sprachausgabe-Engine" kompiliert werden. die Einstellung für Geschwindigkeit und Tonhöhe der Zeichen ist für diese Sprache und Engine optimiert. Wenn Sie also andere TTS-Engines oder Engines anderer Sprachen verwenden, sprechen die Zeichen möglicherweise nicht mit der optimalen Tonhöhe oder Geschwindigkeit aus. Obwohl Ihre Anwendung oder Webseite die Werte für die Eigenschaft " [**Tonhöhe**](/previous-versions/ms809428(v=msdn.10)) " und " [**Geschwindigkeit**](https://www.bing.com/search?q=**Speed**) " nicht schreiben kann, können Sie die Tags " [Pit](pit-tag.md) (Pitch)" und " [SPD](spd-tag.md) " (Geschwindigkeit) in den Ausgabetext einschließen, der die Größe und Geschwindigkeit für eine bestimmte Äußerung vorübergehend ändert. Wenn Sie die Tags "Pit" und "SPD" verwenden, werden **die Eigenschaften für** die Eigenschaft " **Tonhöhe** " und " Ausführliche Informationen finden Sie unter [Programmieren des Microsoft-Agent-Steuer](programming-the-microsoft-agent-control.md) Elements und der [Sprachausgabe Tags von Microsoft Agent](microsoft-agent-speech-output-tags.md) .

Sie müssen auch die SAPI 4.0-Lauf Zeit Binärdateien (SPCHAPI.exe) installieren, wenn Sie andere SAPI-kompatible TTS-Engines verwenden, als die "L&H truvoice-American-Engine", bei der der Microsoft-Agent Zeichen bereitgestellt hat, sodass die Engines ordnungsgemäß aufgelistet werden. Fügen Sie auf Ihrer Webseite das folgende Objekttag ein, um die Komponente automatisch zu installieren:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Verwenden Sie [**ttsmodeid**](https://www.bing.com/search?q=**TTSModeID**), um die Modus-ID einer Engine abzufragen oder festzulegen. Mit **ttsmodeid** können Sie eine Mode-ID festlegen, die sich von der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens unterscheidet. Beispielsweise können Sie ein deutsches Zeichen für die Verwendung einer ID im französischen Modus festlegen. Die IDs des Sprachausgabe-Engine-Modus definieren nicht nur, welches Modul Sie verwenden, sondern auch bestimmten Stimmen, die für eine Engine unterstützt werden. Sie können auch den Zeichen-Editor von Microsoft-Agent oder die in der [Microsoft Speech SDK-Dokumentation](https://msdn.microsoft.com/library/ee705648.aspx) enthaltenen Tools verwenden, um die im System installierten TTS-Engines in den Modus-IDs zu Abfragen.

**Sprachausgabe Modus-IDs**



| Sprache                                       | Modus-IDs                               |
|---------------------------------------------|----------------------------------------|
| Erwachsene weiblich \# 1, US-Englisch, L&H truvoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adult Female \# 2, US-Englisch, L&H truvoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Erwachsener männlich \# 1, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Erwachsener männlich \# 2, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Erwachsener männlich \# 3, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Erwachsener männlich \# 4, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adult männlich \# 5, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Erwachsener männlich \# 6, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adult männlich \# 7, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Erwachsener männlich \# 8, US-Englisch, L&H truvoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, britisches Englisch, L&H TTS3000         | {227a0e40-a92a-11d1-B17B-0020afed142e} |
| Peter, britisches Englisch, L&H TTS3000         | {227a0e41-a92a-11d1-B17B-0020afed142e} |
| Linda, Niederländisch, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Alexander, Niederländisch, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Véronique, Französisch, L&H TTS3000              | {0879a4e0-a92c-11d1-B17B-0020afed142e} |
| Pierre, Französisch, L&H TTS3000                 | {0879a4e1-a92c-11d1-B17B-0020afed142e} |
| Anna, Deutsch, L&H TTS3000                   | {3a1b760-a92b-11d1-B17B-0020afed142e} |
| Stefan, Deutsch, L&H TTS3000                 | {3a1b761-a92b-11d1-B17B-0020afed142e} |
| Barbara, Italienisch, L&H TTS3000               | {7ef71700-a92d-11d1-B17B-0020afed142e} |
| Stefano, Italienisch, L&H TTS3000               | {7ef71701-a92d-11d1-B17B-0020afed142e} |
| Naoko, Japanisch, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, Japanisch, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shin-ah, Koreanisch, L&H TTS3000                | {12e0b720-A936-11d1-B17B-0020afed142e} |
| Jun-Ho, Koreanisch, L&H TTS3000                 | {12e0b721-A936-11d1-B17B-0020afed142e} |
| Juliana, Portugiesisch (Brasilien), L&H TTS3000   | {8aa08ca0-A1ae-11d3-9bc5-00a0c967a2d1} |
| Alexandre, Portugiesisch (Brasilien), L&H TTS3000 | {8aa08ca1-A1ae-11d3-9bc5-00a0c967a2d1} |
| Svetlana, Russisch, L&H TTS3000              | {06377f 80-d48e-11d1-B17B-0020afed142e} |
| Boris, Russisch, L&H TTS3000                 | {06377f 81-d48e-11d1-B17B-0020afed142e} |
| Carmen, Spanisch, L&H TTS3000                | {2ce326e0-A935-11d1-B17B-0020afed142e} |
| Julio, Spanisch, L&H TTS3000                 | {2ce326e1-A935-11d1-B17B-0020afed142e} |



 

> [!Note]  
> Es gibt einen Unterschied zwischen der Installations-CLSID einer Sprach-Engine und ihrer Mode-ID. Ebenso verfügt eine Sprach-Engine auch über eine Engine-ID, aber diese ID ist in der Agent-API nicht anwendbar.

 

 

 