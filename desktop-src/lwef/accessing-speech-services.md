---
title: Zugreifen auf Speech-Dienste (Microsoft-Agent-Serverschnittstelle)
description: Zugreifen auf Speech-Dienste
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9eeb4afb2b05ca13c52d49508c3c25b7e02da676
ms.sourcegitcommit: 59ec383331366f8a62c94bb88468ca03e95c43f8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "107380804"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Zugreifen auf Speech-Dienste (Microsoft-Agent-Serverschnittstelle)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Obwohl die Dienste des Microsoft-Agents Unterstützung für die Spracheingabe enthalten, muss eine kompatible Spracherkennungs-Engine für Befehle und Steuerungen installiert werden, um auf die Spracheingabedienste des -Agents zuzugreifen. Wenn Sie die Sprachdienste des Microsoft-Agents verwenden möchten, um die synthetisierte Sprachausgabe für ein Zeichen zu unterstützen, müssen Sie eine kompatible Sprachsynthese-Engine (Text-to-Speech, TTS) für Ihr Zeichen installieren. Da die Sprachdienste des Microsoft-Agents auf der Microsoft Speech API (SAPI) basieren, können Sie beliebige Engines verwenden, die die erforderlichen Sprachschnittstellen problemlos unterstützen.

Um die Spracheingabeunterstützung in Ihrer Anwendung zu aktivieren, definieren Sie ein [**Command-Objekt,**](https://www.bing.com/search?q=**Command**) und legen Sie dessen [**Voice-Eigenschaft**](https://www.bing.com/search?q=**Voice**) fest. Der Microsoft-Agent lädt spracherkennungsdienste automatisch, sodass die Spracherkennungs-Engine geladen wird, wenn der Benutzer die Hörtaste drückt oder [**Sie Lauschen**](https://www.bing.com/search?q=**Listen**)aufrufen. Standardmäßig bestimmt die Sprach-ID des Zeichens, welche Engine geladen wird. Der Agent versucht, die erste Engine zu laden, die SAPI als Übereinstimmung mit dieser Sprache zurückgibt. Verwenden Sie **IAgentCharacterEx::SetSRModeID,** wenn Sie eine bestimmte Engine laden möchten.

Verwenden Sie die Speak-Methode, [](https://www.bing.com/search?q=**Speak**) um die Sprachtextausgabe zu aktivieren. Der Microsoft-Agent versucht automatisch, eine Engine zu laden, die der Sprach-ID des Zeichens entspricht. Wenn die Definition des Zeichens eine bestimmte ID des TTS-Engine-Modus enthält und diese Engine verfügbar ist und mit der Sprach-ID des Zeichens übereinstimmt, lädt der -Agent diese Engine für das Zeichen. Falls nicht, lädt der -Agent die erste TTS-Engine, die SAPI als Übereinstimmung mit der Spracheinstellung des Zeichens zurückgibt. Sie können auch **IAgentCharacterEx::SetTTSModeID** verwenden, um eine bestimmte Engine zu laden.

In der Regel lädt Microsoft Agent eine Spracherkennungs-Engine, wenn der Überwachungsmodus initiiert wird, und lädt eine Text-zu-Sprache-Engine, wenn [**Speak**](https://www.bing.com/search?q=**Speak**) zum ersten Mal aufgerufen wird. Wenn Sie jedoch die Sprach-Engine vorab laden möchten, können Sie dazu die Eigenschaften abfragen, die sich auf die Sprachschnittstellen beziehen. Wenn Sie beispielsweise **IAgentCharacterEx::GetSRModeID** oder **IAgentCharacterEx::GetTTSModeID** aufrufen, wird versucht, diesen Engine-Typ zu laden.

 

 




