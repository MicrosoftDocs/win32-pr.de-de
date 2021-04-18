---
title: Zugreifen auf Sprachdienste (Microsoft Agent-Server Schnittstelle)
description: Zugreifen auf Sprachdienste
ms.assetid: 99cf630d-3bd1-403a-833a-9173a84fe3c0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fda1369fa83c5e8ffaf7f08317f69a2a569620f3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341348"
---
# <a name="accessing-speech-services-microsoft-agent-server-interface"></a>Zugreifen auf Sprachdienste (Microsoft Agent-Server Schnittstelle)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Obwohl die Dienste von Microsoft Agent Unterstützung für Spracheingaben enthalten, muss ein kompatibles Befehls-und Steuerelement-Spracherkennungs-Engine installiert sein, um auf die Spracheingabe Dienste des Agents zugreifen zu können. Wenn Sie die Sprachausgabe von Microsoft-Agent verwenden möchten, um die Sprachausgabe für ein Zeichen in synthetischer Sprache zu unterstützen, müssen Sie auch eine kompatible Text-zu-Sprache-sprach-Engine (TTS) für Ihr Zeichen installieren. Da die Sprachdienste von Microsoft-Agent auf der Microsoft Speech-API (SAPI) basieren, können Sie alle Engines verwenden, die die erforderlichen Sprachschnittstellen unterstützen.

Um die Spracheingabe Unterstützung in der Anwendung zu aktivieren, definieren Sie ein [**Command**](https://www.bing.com/search?q=**Command**) -Objekt, und legen Sie die [**Voice**](https://www.bing.com/search?q=**Voice**) -Eigenschaft fest. Der Microsoft-Agent lädt Sprachdienste automatisch, sodass die Spracherkennungs-Engine geladen wird, wenn der Benutzer die Abhör Taste drückt oder [**lauschen**](https://www.bing.com/search?q=**Listen**)aufruft. Standardmäßig bestimmt die Sprach-ID des Zeichens, welches Modul geladen wird. Der-Agent versucht, die erste Engine zu laden, die SAPI als Übereinstimmung mit dieser Sprache zurückgibt. Wenn Sie ein bestimmtes Modul laden möchten, verwenden Sie [**iagentcharakteriex:: absrmodeid**](IAgentCharacterEx::SetSRModeID) .

Um die Text-zu-Sprache-Ausgabe zu aktivieren, verwenden Sie die [**Sprech**](https://www.bing.com/search?q=**Speak**) Methode. Der Microsoft-Agent wird automatisch versuchen, ein Modul zu laden, das mit der Sprach-ID des Zeichens übereinstimmt. Wenn die Definition des Zeichens eine bestimmte ID des TTS-Engine-Modus enthält und diese Engine verfügbar ist und mit der Sprach-ID des Zeichens übereinstimmt, lädt der-Agent diese Engine für das Zeichen. Andernfalls lädt der-Agent die erste von SAPI zurückgegebene TTS-Engine als Übereinstimmung mit der Spracheinstellung des Zeichens. Sie können auch [**iagentcharakteriex:: setttmodeid**](IAgentCharacterEx::SetTTSModeID) verwenden, um eine bestimmte Engine zu laden.

In der Regel lädt der Microsoft-Agent eine Spracherkennungs-Engine, wenn der Empfangsmodus initiiert wird, und lädt eine Text-zu-Sprache-Engine, wenn zum ersten Mal [**gesprochen**](https://www.bing.com/search?q=**Speak**) wird. Wenn Sie jedoch die Sprach-Engine vorab laden möchten, können Sie dazu die Eigenschaften Abfragen, die mit den Sprachschnittstellen verknüpft sind. Beispielsweise wird durch den Aufruf von [**iagentcharakteriex:: gezrmodeid**](IAgentCharacterEx::GetSRModeID) oder [**iagentcharakteriex:: getttionmodeid**](IAgentCharacterEx::GetTTSModeID) versucht, diese Art von Engine zu laden.

 

 




