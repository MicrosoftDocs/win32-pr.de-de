---
title: Zugreifen auf eine Sprach-Engine in Ihrem Code
description: Zugreifen auf eine Sprach-Engine in Ihrem Code
ms.assetid: ddfe0552-a29e-4ce4-b608-c131efbe300b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b9769e88437366b72fdff50dc0ab27918d1b21e4c0c317f230049a965629a03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118753119"
---
# <a name="accessing-a-speech-engine-in-your-code"></a>Zugreifen auf eine Sprach-Engine in Ihrem Code

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Um eine bestimmte Sprach-Engine in Ihrem Code zu verwenden, verwenden Sie die -Agent-API, um die Engine festzulegen. Verwenden Sie für Spracheingabe-Engines [**SRModeID,**](https://www.bing.com/search?q=**SRModeID**)und geben Sie die Modus-ID für die Engine an. Beachten Sie jedoch, dass die Engine installiert sein muss. Um festzustellen, ob die Engine vorhanden ist, können Sie **SRModeID** abfragen. Die Engine muss mit der [**LanguageID-Einstellung**](https://www.bing.com/search?q=**LanguageID**) des Zeichens übereinstimmen. Beispielsweise können Sie **SRModeID** für ein Zeichen, dessen **LanguageID** französisch ist, nicht auf eine Id des Deutschen Spracherkennungs-Engine-Modus festlegen.

**IDs im Spracheingabe-Engine-Modus**



| Sprache                                    | Modus-IDs                             |
|------------------------------------------|--------------------------------------|
| Microsoft Speech Recognition Engine v4.0 | {D8905400-B5C8-11D0-B968020AFDB1B9C} |



 

Überprüfen Sie die [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) und [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) des Zeichens in Ihrem Code, und legen Sie sie fest, bevor Sie versuchen, grammatik für die Sprachparameter der **Command-Objekte** Ihrer Anwendung zu definieren. Überprüfen Sie auch den Browser oder die Systemsprache, damit Sie sicher sein können, dass sie mit der Konfiguration Ihrer Benutzer übereinstimmen. Die Engine schlägt möglicherweise fehl, wenn Sie versuchen, eine Grammatik für eine Sprache zu definieren, mit der die Engine nicht übereinstimmt.

Ein Zeichensatz für die TTS-Ausgabe (Text-to-Speech) kann mit der Mode-ID-Einstellung einer Standard-Sprachausgabe-Engine kompiliert werden. Wenn das Zeichen geladen wird und die Engine installiert ist und mit der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens übereinstimmt, versucht der -Agent, diese Modus-ID für die Sprachausgabe zu laden. Wenn die Engine nicht vorhanden ist oder über eine andere **LanguageID** verfügt, versucht der -Agent, die erste Gefundene Modus-ID zu laden, die der **LanguageID** des Zeichens entspricht, legt aber dennoch die kompilierte Geschwindigkeit und Die Tonhöhe des Zeichens fest.

Da alle vom Microsoft-Agent bereitgestellten Zeichen so kompiliert werden, dass die Lernout-& Hauspie TruVoice-Engine für amerikanisches Englisch als Standard-Sprachausgabe-Engine verwendet wird, sind die Geschwindigkeits- und Tonhöheneinstellung der Zeichen für diese Sprache und Engine optimiert. Wenn Sie andere TTS-Engines oder Engines anderer Sprachen verwenden, sprechen die Zeichen daher möglicherweise nicht mit der optimalen Tonhöhe oder Geschwindigkeit. Obwohl Ihre Anwendung oder Webseite die Eigenschaftswerte [**"Pitch"**](/previous-versions/ms809428(v=msdn.10)) und [**"Speed"**](https://www.bing.com/search?q=**Speed**) nicht schreiben kann, können Sie [Pit-Tags](pit-tag.md) (Tonhöhe) und [Markierungen](spd-tag.md) (Geschwindigkeit) in Ihren Ausgabetext einschließen, die vorübergehend die Tonhöhe und Geschwindigkeit für eine bestimmte Äußerung ändern. Die Verwendung der Tags Pit und Tags ändert jedoch nicht die Eigenschaften **Pitch** und **Speed.** Weitere Informationen finden Sie unter [Programmieren des Microsoft-Agent-Steuerelements](programming-the-microsoft-agent-control.md) und der [Sprachausgabetags des Microsoft-Agents.](microsoft-agent-speech-output-tags.md)

Sie müssen auch die SAPI 4.0a-Laufzeitbinärdateien (SPCHAPI.exe) installieren, wenn Sie andere SAPI-kompatible TTS-Engines als die L&H TruVoice-Engine für amerikanisches Englisch mit den von Microsoft Agent bereitgestellten Zeichen verwenden, damit die Engines ordnungsgemäß aufzählt werden. Fügen Sie auf Ihrer Webseite das folgende Objekttag ein, um die Komponente automatisch zu installieren:

``` syntax
<OBJECT width=0 height=0
CLASSID="CLSID:0C7F3F20-8BAB-11d2-9432-00C04F8EF48F"
CODEBASE="#VERSION=4,0,0,0">
</OBJECT>
```

Verwenden Sie [**TTSModeID,**](https://www.bing.com/search?q=**TTSModeID**)um die Modus-ID einer Engine abzufragen oder festzulegen. Mit **TTSModeID** können Sie eine Modus-ID festlegen, die sich von der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens unterscheidet. Beispielsweise können Sie ein deutsches Zeichen festlegen, um mithilfe einer FRANZÖSISCH-Modus-ID zu sprechen. IDs des Sprachausgabe-Engine-Modus definieren nicht nur, welche Engine Sie verwenden, sondern entsprechen auch bestimmten Stimmen, die für eine Engine unterstützt werden. Sie können auch den Zeichen-Editor des Microsoft-Agents oder die in der Dokumentation zum [Microsoft Speech SDK](https://msdn.microsoft.com/library/ee705648.aspx) enthaltenen Tools verwenden, um die Modus-IDs der auf Ihrem System installierten TTS-Engines abzufragen.

**IDs im Sprachausgabemodus**



| Sprache                                       | Modus-IDs                               |
|---------------------------------------------|----------------------------------------|
| Adult Female \# 1, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273008} |
| Adult Female \# 2, US English, L&H TruVoice  | {CA141FD0-AC7F-11D1-97A3-006008273009} |
| Adult Male \# 1, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273000} |
| Adult Male \# 2, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273001} |
| Adult Male \# 3, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273002} |
| Adult Male \# 4, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273003} |
| Adult Male \# 5, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273004} |
| Adult Male \# 6, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273005} |
| Adult Male \# 7, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273006} |
| Adult Male \# 8, US English, L&H TruVoice    | {CA141FD0-AC7F-11D1-97A3-006008273007} |
| Carol, Britisch, L&H TTS3000         | {227A0E40-A92A-11d1-B17B-0020AFED142E} |
| Peter, Britisch Englisch, L&H TTS3000         | {227A0E41-A92A-11d1-B17B-0020AFED142E} |
| Linda, Niederländisch, L&H TTS3000                   | {A0DDCA40-A92C-11d1-B17B-0020AFED142E} |
| Soll, Niederländisch, L&H TTS3000               | {A0DDCA41-A92C-11d1-B17B-0020AFED142E} |
| Zweigronique, Französisch, L&H TTS3000              | {0879A4E0-A92C-11d1-B17B-0020AFED142E} |
| Soll, Französisch, L&H TTS3000                 | {0879A4E1-A92C-11d1-B17B-0020AFED142E} |
| Anna, Deutsch, L&H TTS3000                   | {3A1FB760-A92B-11d1-B17B-0020AFED142E} |
| Sender, Deutsch, L&H TTS3000                 | {3A1FB761-A92B-11d1-B17B-0020AFED142E} |
| Soll, Italienisch, L&H TTS3000               | {7EF71700-A92D-11d1-B17B-0020AFED142E} |
| Sollo, Italienisch, L&H TTS3000               | {7EF71701-A92D-11d1-B17B-0020AFED142E} |
| Naasso, Japanisch, L&H TTS3000                | {A778E060-A936-11d1-B17B-0020AFED142E} |
| Kenji, Japanisch, L&H TTS3000                | {A778E061-A936-11d1-B17B-0020AFED142E} |
| Shirt-Ah, Koreanisch, L&H TTS3000                | {12E0B720-A936-11d1-B17B-0020AFED142E} |
| Jun-Ho, Koreanisch, L&H TTS3000                 | {12E0B721-A936-11d1-B17B-0020AFED142E} |
| Solla, Portugiesisch (Brasilien), L&H TTS3000   | {8AA08CA0-A1AE-11d3-9BC5-00A0C967A2D1} |
| Soll, Portugiesisch (Brasilien), L&H TTS3000 | {8AA08CA1-A1AE-11d3-9BC5-00A0C967A2D1} |
| Svetlana, Russisch, L&H TTS3000              | {06377F80-D48E-11d1-B17B-0020AFED142E} |
| Ole, Russisch, L&H TTS3000                 | {06377F81-D48E-11d1-B17B-0020AFED142E} |
| Fernseher, Spanisch, L&H TTS3000                | {2CE326E0-A935-11d1-B17B-0020AFED142E} |
| Julio, Spanisch, L&H TTS3000                 | {2CE326E1-A935-11d1-B17B-0020AFED142E} |



 

> [!Note]  
> Es gibt einen Unterschied zwischen der INSTALLATIONS-CLSID einer Sprach-Engine und ihrer Modus-ID. Ebenso verfügt eine Sprach-Engine auch über eine Engine-ID, diese ID gilt jedoch nicht für die Agent-API.

 

 

 