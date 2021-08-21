---
description: Der ELS-Spracherkennungsdienst heißt Microsoft Sprachenerkennung. Dieser Dienst verwendet von Microsoft patentierte Technologie, damit Anwendungen die Sprache erkennen können, in der bestimmter Text geschrieben wird.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft Sprachenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 472c4c4df0484287ef8bebcfdb2f395212b1985b282b7391d6c047dfb98d2ed8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119788380"
---
# <a name="microsoft-language-detection"></a>Microsoft Sprachenerkennung

Der ELS-Spracherkennungsdienst heißt Microsoft Sprachenerkennung. Dieser Dienst verwendet von Microsoft patentierte Technologie, damit Anwendungen die Sprache erkennen können, in der bestimmter Text geschrieben wird.

## <a name="input-to-microsoft-language-detection"></a>Eingabe für Microsoft Sprachenerkennung

Die Eingabe für den Microsoft Sprachenerkennung-Dienst ist UTF-16-Text (normalisierte Form C). Der Dienst muss die Sprache für diesen Text bestimmen.

## <a name="output-of-microsoft-language-detection"></a>Ausgabe von Microsoft Sprachenerkennung

Der Microsoft Sprachenerkennung-Dienst ruft eine mit doppel NULL beendete, registrierungsformatierte UTF-16-Zeichenfolge ab, die Sprachen auflistet, die durch ihre Namen dargestellt und durch NULL-Zeichentrennzeichen getrennt sind. Die Liste wird nach Relevanz sortiert. Für die meisten Sprachen werden neutrale Namen verwendet. Für einige, z. B. sr-Cyrl, sr-Latn, zh-Hant und zh-Hans, werden jedoch vollständige Namen verwendet.

## <a name="microsoft-language-detection-operation"></a>Microsoft Sprachenerkennung Vorgang

Der Microsoft Sprachenerkennung überprüft das Unicode-Skript des von der Anwendung bereitgestellten Texts. Sie segmentiert den Text basierend auf den erkannten Skripts und bestimmt dann die Sprache, in der die einzelnen Segmente geschrieben werden. Wenn ein Skript eine einzelne Sprache angibt, ist die Sprache garantiert in der Ausgabeliste der Sprachen vorhanden. Der Dienst verwendet einen patentierten Algorithmus, um die Relevanz der einzelnen unterstützten Sprachen zu bestimmen.

## <a name="microsoft-language-detection-guid"></a>Microsoft Sprachenerkennung-GUID

Die GUID für den Microsoft Sprachenerkennung-Dienst wird in Elssrvc.h deklariert, wie im folgenden Code gezeigt.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu erweiterten linguistischen Diensten](about-extended-linguistic-services.md)
</dt> </dl>

 

 



