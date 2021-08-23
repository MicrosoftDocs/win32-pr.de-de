---
title: Implementieren von CEcho DoProcessOutput
description: Implementieren von CEcho DoProcessOutput
ms.assetid: afd91022-4e2d-46a2-a0f4-cd2b558536d6
keywords:
- Windows Media Player-Plug-Ins, DoProcessOutput-Methode im Echo-Beispiel
- Plug-Ins, DoProcessOutput-Methode im Echo-Beispiel
- Digitale Signalverarbeitungs-Plug-Ins, DoProcessOutput-Methode im Echo-Beispiel
- DSP-Plug-Ins, DoProcessOutput-Methode im Echo-Beispiel
- Echo-DSP-Plug-In-Beispiel, DoProcessOutput-Methode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07054950cabadbc835c9904d48cdb4e6ddf5f05c0822c997558381958a9857d1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135643"
---
# <a name="implementing-cechodoprocessoutput"></a>Implementieren von CEcho::D oProcessOutput

Die **DoProcessOutput-Methode** führt die digitale Signalverarbeitung aus. Dies ist die Methode, die die Von Windows Media Player bereitgestellten Daten ändert. Es sind die Ergebnisse dieser Methode, die Sie als Echoeffekt hören, wenn Das Echo-Beispiel-Plug-In abgeschlossen ist.

In diesem Beispiel verarbeitet das Plug-In nur 8-Bit- oder 16-Bit-Audio. Sie müssen einige Änderungen am Beispielcode des Plug-In-Assistenten vornehmen, um die Abschnitte zu entfernen, die Audio mit höherer Bittiefe verarbeiten. Es lohnt sich jedoch, diese Abschnitte zu untersuchen, da Sie sich entscheiden können, ihre eigene Echoimplementierungen für diese Formate hinzuzufügen.

In den folgenden Abschnitten werden die Änderungen beschrieben, die Sie am Code vornehmen müssen:

-   [Entfernen des Codes für die Verarbeitung von mehr als 16 Bits](removing-the-code-to-process-greater-than-16-bits.md)
-   [Verarbeiten der Audiodaten](processing-the-audio-data.md)
-   [Variablen für die Verarbeitung](variables-to-perform-processing.md)
-   [Erstellen des Echoeffekts](creating-the-echo-effect.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Das Echobeispiel**](the-echo-sample.md)
</dt> </dl>

 

 




