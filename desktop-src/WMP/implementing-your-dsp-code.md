---
title: Implementieren des DSP-Codes
description: Implementieren des DSP-Codes
ms.assetid: e1feaaee-1127-4a3a-9a4c-a30584a7e8ff
keywords:
- Windows Media Player-Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-ins, digitale Signalverarbeitung (DSP)
- Plug-Ins für die digitale Signalverarbeitung, Implementieren von Code
- DSP-Plug-ins, Implementieren von Code
- Plug-Ins für die digitale Signalverarbeitung, Ändern von Beispielcode
- DSP-Plug-ins, Ändern von Beispielcode
- audiodsp-Plug-ins, Implementieren von Code
- Video DSP-Plug-ins, Implementieren von Code
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c9e17dad39a4ba0ebe79e31d9f3eead843d7f81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337171"
---
# <a name="implementing-your-dsp-code"></a>Implementieren des DSP-Codes

Nachdem Sie das Beispiel-DSP-Plug-in erstellt haben, können Sie den Code ändern, um ein eigenes Windows Media Player DSP-Plug-in zu erstellen. Welche Methoden Sie ändern und welche Sie unverändert lassen können, hängt von den folgenden Faktoren ab:

-   Die Anzahl der Eigenschaften, die der Benutzer ändern kann. Sie möchten die Standard Implementierung der Eigenschaften Seite entsprechend Ihren Anforderungen ändern, und Sie müssen möglicherweise zusätzliche Eigenschaften hinzufügen.
-   Gibt an, ob Ihr DSP-Plug-in Streamingressourcen zuordnen muss. Das Plug-in erfordert möglicherweise zusätzliche Puffer.
-   Ob das audiodsp-Plug-in weiterhin Daten ausgeben muss, nachdem Windows Media Player die Bereitstellung von Daten im Eingabepuffer beendet hat.

In den folgenden Abschnitten wird der vom Windows Media Player-Plug-in-Assistenten generierte DSP-Plug-in-Beispielcode verwendet, um wichtige Konzepte zu veranschaulichen. Möglicherweise ist es hilfreich, Microsoft Visual Studio zu öffnen und den Beispielcode zuerst zu generieren, damit Sie beim Lesen dieses Abschnitts darauf verweisen können. Ausführliche Informationen zur Verwendung des Assistenten für Windows Media Player-Plug-in finden Sie unter [Building a DSP Plug-in](building-a-dsp-plug-in.md).



| `Section`                                                                    | BESCHREIBUNG                                                                                                       |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [Implementieren eines audiodsp-Plug-ins](implementing-an-audio-dsp-plug-in.md) | Erläutert, was Sie wissen müssen, um basierend auf dem vom Assistenten generierten Beispiel ein eigenes audiodsp-Plug-in zu erstellen. |
| [Implementieren eines Video DSP-Plug-ins](implementing-a-video-dsp-plug-in.md)   | Erläutert, was Sie wissen müssen, um basierend auf dem vom Assistenten generierten Beispiel ein eigenes Video DSP-Plug-in zu erstellen. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zu DSP-Plug-ins**](about-dsp-plug-ins.md)
</dt> </dl>

 

 




