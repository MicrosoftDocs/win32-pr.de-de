---
title: XAudio2-Schnittstellen
description: Dieser Abschnitt enthält Informationen zu Schnittstellen, die von der Microsoft XAudio2-API bereitgestellt werden.
ms.assetid: 96691e00-9ed0-b31c-fbe9-4daaba0daf98
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d9f2c777a7b98c5cbc78a130c0a1431be5971d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218559"
---
# <a name="xaudio2-interfaces"></a>XAudio2-Schnittstellen

Dieser Abschnitt enthält Informationen zu Schnittstellen, die von der Microsoft XAudio2-API bereitgestellt werden.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2)<br/>                             | IXAudio2 ist die Schnittstelle für das [XAudio2](xaudio2-apis-portal.md) -Objekt, das alle audiomodulzustände, den Audioverarbeitungs Thread, das sprach Diagramm usw. verwaltet. <br/>                                                                                                                                                |
| [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice)<br/>                   | [**IXAudio2Voice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voice) stellt die Basisschnittstelle dar, von der [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice), [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice) und [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) abgeleitet werden. Die unten aufgeführten Methoden gelten für alle sprach Unterklassen.<br/> |
| [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)<br/>       | Verwenden Sie eine Quell Stimme, um Audiodaten an die XAudio2-Verarbeitungs Pipeline zu senden.<br/>                                                                                                                                                                                                                                                   |
| [**IXAudio2SubmixVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2submixvoice)<br/>       | Eine teilmix-Stimme wird hauptsächlich für Leistungsverbesserungen und Auswirkungen der Verarbeitung verwendet. <br/>                                                                                                                                                                                                                                        |
| [**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice)<br/> | Eine "Mastering Voice" wird verwendet, um das Audioausgabegerät darzustellen.<br/>                                                                                                                                                                                                                                                               |
| [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)<br/> | Die IXAudio2EngineCallback-Schnittstelle enthält Methoden, die den Client Benachrichtigen, wenn bestimmte Ereignisse in der [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) -Engine auftreten.<br/>                                                                                                                                                                           |
| [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback)<br/>   | Die [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle enthält Methoden, die den Client Benachrichtigen, wenn bestimmte Ereignisse in einem bestimmten [**IXAudio2SourceVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2sourcevoice)auftreten. <br/>                                                                                                                       |
| [**Ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)<br/>                                   | Die Schnittstelle für ein audioverarbeitungsobjekt, das in einer XAudio2 Effect-Kette verwendet wird.<br/>                                                                                                                                                                                                                                        |
| [**Ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)<br/>               | Eine optionale Schnittstelle, die es xapo ermöglicht, Effekt spezifische Parameter zu verwenden.<br/>                                                                                                                                                                                                                                                  |
| [**Ixapohrtfparameters**](/windows/win32/api/hrtfapoapi/nn-hrtfapoapi-ixapohrtfparameters)<br/>       | Die-Schnittstelle, die verwendet wird, um Parameter festzulegen, die Steuern, wie die Head-Related Transfer Function (HRTF) auf einen Sound angewendet wird<br/>                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programmierverzeichnis](programming-reference.md)
</dt> <dt>

[Programmierverzeichnis](./programming-reference.md)
</dt> </dl>

 

 
