---
description: XAudio2 kann vom Client bereitgestellte Funktionen aufzurufen, um Sie asynchron über bestimmte Ereignisse zu benachrichtigen, die im Audioverarbeitungs Thread stattfinden.
ms.assetid: 4fbd4229-f7ac-33b3-b4b7-f09150a60598
title: XAudio2-Rückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ee191ad8c15d238a065c837c6fb192befbe7a51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349809"
---
# <a name="xaudio2-callbacks"></a>XAudio2-Rückrufe

XAudio2 kann vom Client bereitgestellte Funktionen aufzurufen, um Sie asynchron über bestimmte Ereignisse zu benachrichtigen, die im Audioverarbeitungs Thread stattfinden. Diese Rückrufe können global oder spezifisch für eine bestimmte Quell Stimme sein. Um globale Engine-Rückrufe zu erhalten, muss der Client eine Instanz einer Klasse bereitstellen, die die [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Schnittstelle implementiert, wenn XAudio2 initialisiert wird. Um Quellcode-Rückrufe zu erhalten, muss der Client eine Instanz einer Klasse bereitstellen, die die [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Schnittstelle implementiert, wenn Quell Stimmen erstellt werden. Weitere Informationen finden Sie unter **IXAudio2EngineCallback** und **IXAudio2VoiceCallback**.

Sie müssen Rückrufe sorgfältig implementieren, um zu vermeiden, dass die Audiodaten beeinträchtigt werden. Wenn ein Rückruf ausgeführt wird, kann XAudio2 keine Audiodaten generieren. Verzögerungen mit mehr als wenigen Millisekunden können zu einem Audioproblem führen. Bei Verzögerungen dieser Art wird auch eine Debugger-Ausgabe generiert. Dies deutet auf potenzielle Leistungsprobleme hin. Rückruf Funktionen dürfen mindestens nicht folgende Aktionen ausführen:

-   Zugreifen auf die Festplatte oder einen anderen permanenten Speicher
-   Tätigen Sie teure oder blockierende API-Aufrufe
-   Mit anderen Teilen des Client Codes synchronisieren
-   Beträchtliche CPU-Auslastung erforderlich

Wenn der Client Entwurf einen Rückruf zum Auslassen von Aktionen erfordert, wie z. b. die zuvor aufgeführten, sollte der Rückruf einem anderen Client Thread signalisieren, dass die Arbeit ausgeführt werden soll. Hierfür können Sie einen einfachen **SetEvent** -Mechanismus oder anspruchsvollere Mechanismen wie eine nicht blockierende Befehls Warteschlange verwenden, die von einem anderen Thread verwendet wird.

## <a name="ixaudio2enginecallback"></a>IXAudio2EngineCallback

Die [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback) -Klasse enthält Methoden, die den Client Benachrichtigen, wenn bestimmte Ereignisse in der XAudio2-Engine auftreten. Diese Methoden sollten vom XAudio2-Client implementiert werden. XAudio2 ruft diese Methoden mithilfe eines Schnittstellen Zeigers auf, der vom Client mithilfe der [**IXAudio2:: registerforcallbacks**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-registerforcallbacks) -Methode bereitgestellt wird. Alle diese Methoden geben **void** anstelle eines **HRESULT** zurück.

## <a name="ixaudio2voicecallback"></a>IXAudio2VoiceCallback

Die [**IXAudio2VoiceCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2voicecallback) -Klasse enthält Methoden, die den Client Benachrichtigen, wenn bestimmte Ereignisse in einer bestimmten XAudio2-Quellsprache auftreten. XAudio2 ruft diese Methoden mithilfe eines Schnittstellen Zeigers auf, der vom Client in [**IXAudio2:: kreatesourcevoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createsourcevoice)bereitgestellt wird. Wie bei [**IXAudio2EngineCallback**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2enginecallback)sollten diese Methoden vom XAudio2-Client implementiert werden und anstelle eines **HRESULT**" **void** " zurückgeben.

Wie bereits erwähnt, ist es von entscheidender Bedeutung, dass die vom Client bereitgestellten Implementierungen dieser Rückrufe so schnell wie möglich zurückgegeben werden, vorzugsweise innerhalb einer Millisekunde. Die Rückrufe werden im Audioverarbeitungs Thread ausgeführt, und die gesamte Verarbeitung wird unterbrochen, bis der Rückruf zurückgegeben wird. Eine Verzögerung in einem Rückruf kann problemlos zu einem Audioproblem führen.

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

 

 
