---
title: Zugreifen auf Speech-Dienste (Microsoft Agent-Serverschnittstelle)
description: Erfahren Sie mehr über den Zugriff auf Spracherkennungsdienste mit der Microsoft Agent-Serverschnittstelle. Microsoft Agent ist ab Windows 7 veraltet.
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f87bf5cf88141344d5328592c9e823c7365c5d5
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262702"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Zugreifen auf Speech-Dienste (Microsoft Agent-Serverschnittstelle)

\[Microsoft Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Obwohl die Dienste von Microsoft Agent Unterstützung für die Spracheingabe bieten, muss eine kompatible Engine für die Spracherkennung installiert werden, um auf die Spracheingabedienste des Agents zugreifen zu können. Wenn Sie die Sprachdienste von Microsoft Agent verwenden möchten, um die synthetisierte Sprachausgabe für ein Zeichen zu unterstützen, müssen Sie eine kompatible Spracherkennungs-Engine (Text-to-Speech, TTS) für Ihr Zeichen installieren. Da die Sprachdienste von Microsoft Agent auf der Microsoft Speech-API (SAPI) basieren, können Sie alle Engines verwenden, die die erforderlichen Sprachschnittstellen inkompatibel unterstützen.

Definieren Sie zum Aktivieren der Spracheingabeunterstützung in Ihrer Anwendung ein [**Command-Objekt,**](https://www.bing.com/search?q=**Command**) und legen Sie dessen [**Voice-Eigenschaft**](https://www.bing.com/search?q=**Voice**) fest. Microsoft Agent wird automatisch Spracherkennungsdienste laden, sodass die Spracherkennungs-Engine geladen wird, wenn der Benutzer die Taste "Lauschen" drückt oder "Lauschen" aufruft. [](https://www.bing.com/search?q=**Listen**) Standardmäßig bestimmt die Sprach-ID des Zeichens, welche Engine geladen wird. Der Agent versucht, die erste Engine zu laden, die SAPI als mit dieser Sprache übereinstimmend zurückgibt. Verwenden **Sie IAgentCharacterEx::SetSRModeID,** wenn Sie eine bestimmte Engine laden möchten.

Verwenden Sie zum Aktivieren der Sprachtextausgabe die [**Speak-Methode.**](https://www.bing.com/search?q=**Speak**) Microsoft Agent versucht automatisch, eine Engine zu laden, die der Sprach-ID des Zeichens entspricht. Wenn die Definition des Zeichens eine bestimmte TTS-Engine-Modus-ID enthält und diese Engine verfügbar ist und der Sprach-ID des Zeichens entspricht, lädt der -Agent diese Engine für das Zeichen. Falls nicht, lädt der -Agent die erste TTS-Engine, die SAPI als mit der Spracheinstellung des Zeichens übereinstimmend zurückgibt. Sie können auch **IAgentCharacterEx::SetTTSModeID** verwenden, um eine bestimmte Engine zu laden.

In der Regel lädt Microsoft Agent eine Spracherkennungs-Engine, wenn der Lauschenmodus initiiert wird, und lädt eine Text-to-Speech-Engine, wenn [**Speak**](https://www.bing.com/search?q=**Speak**) zum ersten Mal aufgerufen wird. Wenn Sie jedoch die Sprach-Engine vorab laden möchten, können Sie dazu die Eigenschaften abfragen, die sich auf die Sprachschnittstellen bezieht. Wenn Sie beispielsweise **IAgentCharacterEx::GetSRModeID** oder **IAgentCharacterEx::GetTTSModeID** aufrufen, wird versucht, diesen Engine-Typ zu laden.

 

 




