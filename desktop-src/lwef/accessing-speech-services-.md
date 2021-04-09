---
title: Zugreifen auf Sprachdienste (Microsoft-Agent-Steuerelement)
description: Zugreifen auf Sprachdienste
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83459cfd7ee478fca7d2cf2d25c4c1d590d8ed54
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103739657"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Zugreifen auf Sprachdienste (Microsoft-Agent-Steuerelement)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Obwohl die Dienste von Microsoft Agent Unterstützung für Spracheingaben enthalten, muss ein kompatibles Befehls-und Steuerelement-Spracherkennungs-Engine installiert sein, um auf die Spracheingabe Dienste des Agents zugreifen zu können. Wenn Sie die Sprachausgabe von Microsoft-Agent verwenden möchten, um die Sprachausgabe für ein Zeichen in synthetischer Sprache zu unterstützen, müssen Sie auch eine kompatible Text-zu-Sprache-sprach-Engine (TTS) für Ihr Zeichen installieren.

Um die Spracheingabe Unterstützung in der Anwendung zu aktivieren, definieren Sie ein [**Command**](https://www.bing.com/search?q=**Command**) -Objekt, und legen Sie die [**Voice**](https://www.bing.com/search?q=**Voice**) -Eigenschaft fest. Der-Agent lädt Sprachdienste automatisch, sodass die Spracherkennungs-Engine geladen wird, wenn der Benutzer die Abhör Taste drückt oder [**lauschen**](https://www.bing.com/search?q=**Listen**)aufruft. Standardmäßig bestimmt die [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) des Zeichens, welche Engine geladen wird. Der-Agent versucht, das erste Modul zu laden, das die Microsoft Speech-API (SAPI) als Übereinstimmung mit dieser Sprache zurückgibt. Verwenden Sie [**srmodeid**](https://www.bing.com/search?q=**SRModeID**) , wenn Sie eine bestimmte Engine laden möchten.

Um die Text-zu-Sprache-Ausgabe zu aktivieren, verwenden Sie die [**Sprech**](https://www.bing.com/search?q=**Speak**) Methode. Der-Agent versucht automatisch, ein Modul zu laden, das mit der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens übereinstimmt. Wenn die Definition des Zeichens eine bestimmte ID des TTS-Engine-Modus enthält und diese Engine verfügbar ist und mit der **LanguageID** des Zeichens übereinstimmt, lädt der Agent diese Engine für das Zeichen. Wenn dies nicht der Fall ist, wird die erste von SAPI zurückgegebene TTS-Engine geladen, die mit der Spracheinstellung des Zeichens übereinstimmt. Sie können auch " [**ttsmodeid**](https://www.bing.com/search?q=**TTSModeID**) " verwenden, um eine bestimmte Engine zu laden.

In der Regel lädt der-Agent die Spracherkennung, wenn der Empfangsmodus initiiert wird, und eine Text-zu-Sprache-Engine [**, wenn Speech**](https://www.bing.com/search?q=**Speak**) zuerst aufgerufen wird. Wenn Sie die Sprach-Engine jedoch vorab laden möchten, Fragen Sie die Eigenschaften ab, die mit den Sprachschnittstellen verknüpft sind. Wenn Sie z. b. [**srmodeid**](https://www.bing.com/search?q=**SRModeID**) oder [**ttsmodeid**](https://www.bing.com/search?q=**TTSModeID**) Abfragen, wird versucht, diese Art von Engine zu laden.

Da die Sprachdienste von Microsoft-Agent auf der Microsoft Speech-API basieren, können Sie alle Engines verwenden, die die erforderlichen Sprachschnittstellen unterstützen.

 

 




