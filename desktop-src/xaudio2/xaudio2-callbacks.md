---
description: XAudio2 kann vom Client bereitgestellte Funktionen aufrufen, um ihn asynchron über bestimmte Ereignisse zu benachrichtigen, die im Audioverarbeitungsthread stattfinden.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: XAudio2-Rückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3377bd029cc2e21971748eaca7309dd44390a5bd3420d772c45264dfdbd075c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120054290"
---
# <a name="xaudio2-callbacks"></a>XAudio2-Rückrufe

XAudio2 kann vom Client bereitgestellte Funktionen aufrufen, um ihn asynchron über bestimmte Ereignisse zu benachrichtigen, die im Audioverarbeitungsthread stattfinden. Diese Rückrufe können global oder spezifisch für eine bestimmte Quellstimme sein. Um globale Engine-Rückrufe zu empfangen, muss der Client eine Instanz einer Klasse bereitstellen, die die [**IXAudio2EngineCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) implementiert, wenn XAudio2 initialisiert wird. Um Quellstimmenrückrufe zu empfangen, muss der Client eine Instanz einer Klasse bereitstellen, die beim Erstellen von Quellstimmen die [**IXAudio2VoiceCallback-Schnittstelle**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) implementiert. Weitere Informationen finden Sie unter **IXAudio2EngineCallback** und **IXAudio2VoiceCallback.**

Sie müssen Rückrufe sorgfältig implementieren, um unterbrechungsverursachende Audiodaten zu vermeiden. Wenn ein Rückruf ausgeführt wird, kann XAudio2 keine Audiodaten generieren. Verzögerungen von mehr als einigen Millisekunden können zu einem Audioproblem führen. Verzögerungen dieser Art generieren auch eine Debuggerausgabe. Dies weist auf potenzielle Leistungsprobleme hin. Rückruffunktionen dürfen mindestens folgende Aufgaben nicht ausführen:

-   Zugreifen auf die Festplatte oder anderen permanenten Speicher
-   Durchführen von teuren oder blockierenden API-Aufrufen
-   Synchronisieren mit anderen Teilen des Clientcodes
-   Erhebliche CPU-Auslastung erforderlich

Wenn der Cliententwurf einen Rückruf erfordert, um Aktionen wie die zuvor aufgeführten auszulösen, sollte der Rückruf einen anderen Clientthread signalisieren, um die Arbeit durchzuführen. Dazu können Sie einen einfachen **SetEvent-Mechanismus** oder komplexere Mechanismen wie eine Befehlswarteschlange ohne Blockierung verwenden, die von einem anderen Thread genutzt wird.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

Die [**IXAudio2EngineCallback-Klasse**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) enthält Methoden, die den Client benachrichtigen, wenn bestimmte Ereignisse in der XAudio2-Engine auftreten. Diese Methoden sollten vom XAudio2-Client implementiert werden. XAudio2 ruft diese Methoden mithilfe eines Schnittstellenzeigers auf, der vom Client mit der [**IXAudio2::RegisterForCallbacks-Methode**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) bereitgestellt wird. Alle diese Methoden geben **void** anstelle eines **HRESULT** zurück.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

Die [**IXAudio2VoiceCallback-Klasse**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) enthält Methoden, die den Client benachrichtigen, wenn bestimmte Ereignisse in einer bestimmten XAudio2-Quellstimme auftreten. XAudio2 ruft diese Methoden mithilfe eines Schnittstellenzeigers auf, der vom Client in [**IXAudio2::CreateSourceVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)bereitgestellt wird. Wie bei [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)sollten diese Methoden vom XAudio2-Client implementiert werden und **void** anstelle eines **HRESULT** zurückgeben.

Wie bereits erwähnt, ist es entscheidend, dass die vom Client bereitgestellten Implementierungen dieser Rückrufe so schnell wie möglich zurückgegeben werden, vorzugsweise innerhalb einer Millisekunde. Die Rückrufe werden im Audioverarbeitungsthread ausgeführt, und die gesamte Verarbeitung wird unterbrochen, bis der Rückruf zurückgegeben wird. Eine Verzögerung bei einem Rückruf kann leicht zu einem Audioproblem führen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rückrufe](callbacks.md)
</dt> <dt>

[XAudio2-Programmieranleitung](programming-guide.md)
</dt> <dt>

[So wird's gemacht: Verwenden der Rückrufe für Quellstimmen](how-to--use-source-voice-callbacks.md)
</dt> <dt>

[So wird's gemacht: Verwenden der Modulrückrufe](how-to--use-engine-callbacks.md)
</dt> <dt>

[So wird's gemacht: Streamen von Sound von einem Datenträger](how-to--stream-a-sound-from-disk.md)
</dt> </dl>

 

 
