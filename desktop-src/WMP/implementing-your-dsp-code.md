---
title: Implementieren Ihres DSP-Codes
description: Implementieren Ihres DSP-Codes
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Windows Media Player Plug-Ins, digitale Signalverarbeitung (DSP)
- Plug-Ins, digitale Signalverarbeitung (DSP)
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-Ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern des Beispielcodes
- DSP-Plug-Ins, Ändern von Beispielcode
- Audio-DSP-Plug-Ins,Implementieren von Code
- Video-DSP-Plug-Ins, Implementieren von Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8504a44b9f3e980be612569e9b7cbe06081d0bfe704a5932e44eef789127687f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135563"
---
# <a name="implementing-your-dsp-code"></a>Implementieren Ihres DSP-Codes

Nachdem Sie das DSP-Beispiel-Plug-In erstellt haben, können Sie den Code ändern, um Ihr eigenes Windows Media Player DSP-Plug-In zu erstellen. Welche Methoden Sie ändern und welche sie verlassen können, hängt von den folgenden Faktoren ab:

-   Die Anzahl der Eigenschaften, die der Benutzer ändern kann. Sie sollten die Standardimplementierung der Eigenschaftenseite auf jeden Fall ihren Anforderungen entsprechend ändern und möglicherweise zusätzliche Eigenschaften hinzufügen.
-   Gibt an, ob Ihr DSP-Plug-In Streamingressourcen zuordnen muss. Ihr Plug-In erfordert möglicherweise zusätzliche Puffer.
-   Gibt an, ob Ihr Audio-DSP-Plug-In weiterhin Daten ausliefern muss, Windows Media Player die Bereitstellung von Daten im Eingabepuffer beendet wurde.

In den folgenden Abschnitten wird der DSP-Plug-In-Beispielcode verwendet, der vom Windows Media Player-Plug-In-Assistenten generiert wurde, um wichtige Konzepte zu veranschaulichen. Möglicherweise ist es hilfreich, Microsoft Visual Studio zu öffnen und den Beispielcode zuerst zu generieren, damit Sie beim Lesen dieses Abschnitts darauf verweisen können. Weitere Informationen zur Verwendung des Windows Media Player Plug-In-Assistenten finden Sie unter [Erstellen eines DSP-Plug-Ins.](building-a-dsp-plug-in.md)



| `Section`                                                                    | BESCHREIBUNG                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementieren eines Audio-DSP-Plug-Ins](implementing-an-audio-dsp-plug-in.md) | Erläutert, was Sie wissen müssen, um Ihr eigenes Audio-DSP-Plug-In basierend auf dem vom Assistenten generierten Beispiel zu erstellen. |
| [Implementieren eines Video-DSP-Plug-Ins](implementing-a-video-dsp-plug-in.md)   | Erläutert, was Sie wissen müssen, um Ihr eigenes Video-DSP-Plug-In basierend auf dem vom Assistenten generierten Beispiel zu erstellen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu DSP-Plug-Ins**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




