---
description: Ein Handschrifterkennungs-Engine oder eine Erkennungsfunktion ist Software, die frei Hand Eingaben verarbeitet und diese frei Hand Eingaben in Text umwandelt
ms.assetid: b64f6856-453c-4080-84e0-0a9e69e79de7
title: Verwenden des Kontexts zur Verbesserung der Genauigkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddd5c807804c1855e0be56b09f08448e3dc2967d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346303"
---
# <a name="using-context-to-improve-accuracy"></a>Verwenden des Kontexts zur Verbesserung der Genauigkeit

Ein Handschrifterkennungs-Engine oder eine Erkennungsfunktion ist Software, die frei Hand Eingaben verarbeitet und diese frei Hand Eingaben in Text umwandelt Ein Kontext ist relevant, anwendungsspezifische Informationen, die Sie für eine Erkennung bereitstellen, um die Erkennungsgenauigkeit zu verbessern. Mit anderen Worten: der Kontext ist ein beliebiger Informationselement, mit dem die Erkennung bei der exakten Verarbeitung der frei Hand Eingaben in einem Feld unterstützt wird.

In diesem Abschnitt werden die verschiedenen Methoden beschrieben, mit denen Sie den Kontext in ihrer Tablet PC-Anwendung nutzen können, um den Schwerpunkt auf das bevorzugte programmgesteuerte Verfahren für Anwendungen zu setzen, die nicht frei Hand Eingaben sind

> [!Note]  
> In den Bereichen der Tablet PC-Technologie des Windows Vista Software Development Kit (SDK) gibt es den Begriff "Kontext", der in Bezug auf das [**erkennnulcontext**](inkrecognizercontext-class.md) -Objekt und seine [**PrefixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_prefixtext) -und [**SuffixText**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_suffixtext) -Eigenschaften verwendet wird. Verwechseln Sie diese anderen Verwendungen von "Context" nicht mit der Definition in diesem Abschnitt.

 

 

 



