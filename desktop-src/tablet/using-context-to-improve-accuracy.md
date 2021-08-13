---
description: Eine Handschrifterkennungs-Engine oder -Erkennung ist eine Software, die Ink verarbeitet und diese Ink in Text konvertiert.
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Verwenden von Kontext zur Verbesserung der Genauigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7564c18ace39c17e8877c3e5edee6464caea0c36d148cffbfcfb3b5ac09f666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118715274"
---
# <a name="using-context-to-improve-accuracy"></a>Verwenden von Kontext zur Verbesserung der Genauigkeit

Eine Handschrifterkennungs-Engine oder -Erkennung ist eine Software, die Ink verarbeitet und diese Ink in Text konvertiert. Ein Kontext ist relevant, anwendungsspezifische Informationen, die Sie für eine Erkennung bereitstellen, um die Erkennungsgenauigkeit zu verbessern. Mit anderen Worten: Kontext ist eine beliebige Information über Eingaben, die die Erkennende bei der genauen Verarbeitung der Ink in einem Feld unterstützt.

In diesem Abschnitt werden die verschiedenen Möglichkeiten beschrieben, wie Sie den Kontext in Ihrer Tablet PC-Anwendung nutzen können. Dabei liegt der Schwerpunkt auf der bevorzugten programmgesteuerten Technik für Anwendungen, die nicht ink aktiviert sind.

> [!Note]  
> In den Abschnitten zur Tablet PC-Technologie des Windows Vista Software Development Kit (SDK) wird der Begriff "Context" in Bezug auf das [**RecognizerContext-Objekt**](inkrecognizercontext-class.md) und dessen [**Eigenschaften PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) und [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) verwendet. Verwechseln Sie diese anderen Verwendungen von "context" nicht mit der Definition in diesem Abschnitt.

 

 

 



