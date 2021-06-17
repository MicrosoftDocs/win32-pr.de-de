---
title: Zugreifen auf Speech-Dienste (Microsoft-Agent-Steuerung)
description: Erfahren Sie mehr über den Zugriff auf Sprachdienste mit Microsoft Agent Control. Der Microsoft-Agent ist ab Windows 7 veraltet.
ms.assetid: c6c10f2a-a433-4a8e-a069-48e3c2032fb8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 035bde03d18b77ce43c47375f2075bba02416c39
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262712"
---
# <a name="accessing-speech-services-microsoft-agent-control"></a>Zugreifen auf Speech-Dienste (Microsoft-Agent-Steuerung)

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

Obwohl die Dienste des Microsoft-Agents Unterstützung für die Spracheingabe enthalten, muss eine kompatible Spracherkennungs-Engine für Befehle und Steuerungen installiert werden, um auf die Spracheingabedienste des -Agents zuzugreifen. Wenn Sie die Sprachdienste des Microsoft-Agents verwenden möchten, um die synthetisierte Sprachausgabe für ein Zeichen zu unterstützen, müssen Sie eine kompatible Sprachsynthese-Engine (Text-to-Speech, TTS) für Ihr Zeichen installieren.

Um die Spracheingabeunterstützung in Ihrer Anwendung zu aktivieren, definieren Sie ein [**Command-Objekt,**](https://www.bing.com/search?q=**Command**) und legen Sie dessen [**Voice-Eigenschaft**](https://www.bing.com/search?q=**Voice**) fest. Der -Agent lädt automatisch Sprachdienste, sodass die Spracherkennungs-Engine geladen wird, wenn der Benutzer die Überwachungsschlüssel drückt oder [**Sie Lauschen**](https://www.bing.com/search?q=**Listen**)aufrufen. Standardmäßig bestimmt die [**LanguageID**](https://www.bing.com/search?q=**LanguageID**) des Zeichens, welche Engine geladen wird. Der Agent versucht, die erste Engine zu laden, die von der Microsoft Speech API (SAPI) als übereinstimmung mit dieser Sprache zurückgegeben wird. Verwenden Sie [**SRModeID,**](https://www.bing.com/search?q=**SRModeID**) wenn Sie eine bestimmte Engine laden möchten.

Verwenden Sie die Speak-Methode, [](https://www.bing.com/search?q=**Speak**) um die Sprachtextausgabe zu aktivieren. Der Agent versucht automatisch, eine Engine zu laden, die der [**LanguageID**](https://www.bing.com/search?q=**LanguageID**)des Zeichens entspricht. Wenn die Definition des Zeichens eine bestimmte ID des TTS-Engine-Modus enthält und diese Engine verfügbar ist und mit der **LanguageID** des Zeichens übereinstimmt, lädt der -Agent diese Engine für das Zeichen. Wenn nicht, lädt es die erste TTS-Engine, die SAPI zurückgibt, entsprechend der Spracheinstellung des Zeichens. Sie können auch [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) verwenden, um eine bestimmte Engine zu laden.

In der Regel lädt der -Agent die Spracherkennung, wenn der Überwachungsmodus initiiert wird, und eine Text-to-Speech-Engine, wenn [**Speak**](https://www.bing.com/search?q=**Speak**) zum ersten Mal aufgerufen wird. Wenn Sie jedoch die Sprach-Engine vorab laden möchten, fragen Sie die Eigenschaften ab, die sich auf die Sprachschnittstellen beziehen. Beim Abfragen von [**SRModeID**](https://www.bing.com/search?q=**SRModeID**) oder [**TTSModeID**](https://www.bing.com/search?q=**TTSModeID**) wird beispielsweise versucht, diesen Engine-Typ zu laden.

Da die Sprachdienste des Microsoft-Agents auf der Microsoft Speech-API basieren, können Sie beliebige Engines verwenden, die die erforderlichen Sprachschnittstellen unterstützen.

 

 




