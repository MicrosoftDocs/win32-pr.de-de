---
title: Implementieren von Cecho DoProcess Output
description: Implementieren von Cecho DoProcess Output
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player-Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-ins, Echo Sample DoProcess Output-Methode
- Plug-Ins für die digitale Signalverarbeitung, Echo Sample DoProcess Output-Methode
- DSP-Plug-ins, Echo Sample DoProcess Output-Methode
- Echo DSP-Plug-in-Beispiel, DoProcess Output-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff40246a6a0ccda2b3f17b12924c44cb79fa4d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037596"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementieren von Cecho::D oprocess Output

Die Methode " **DoProcess Output** " führt die digitale Signalverarbeitung aus. Dies ist die Methode, die die Änderungen an den Daten vornimmt, die von Windows Media Player bereitgestellt werden. Dies sind die Ergebnisse dieser Methode, die Sie als Echo Effekt hören, wenn Ihr Echo Sample-Plug-in fertig ist.

In diesem Beispiel verarbeitet das Plug-in nur 8-Bit-oder 16-Bit-Audiodaten. Sie müssen einige Änderungen am Beispielcode des Plug-in-Assistenten vornehmen, um die Abschnitte zu entfernen, in denen ein höheres bidirektionalton verarbeitet wird. Es lohnt sich jedoch, diese Abschnitte zu untersuchen, da Sie sich entscheiden können, eine eigene Echo Implementierung für diese Formate hinzuzufügen.

In den folgenden Abschnitten werden die Änderungen beschrieben, die Sie am Code vornehmen müssen:

-   [Entfernen des Codes für die Verarbeitung von mehr als 16 Bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Verarbeiten der Audiodaten](processing-the-audio-data.md)
-   [Variablen zum Durchführen der Verarbeitung](variables-to-perform-processing.md)
-   [Erstellen des Echo Effekts](creating-the-echo-effect.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Echo-Beispiel**](the-echo-sample.md)
</dt> </dl>

 

 




