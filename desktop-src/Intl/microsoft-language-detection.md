---
description: Der Dienst für die Spracherkennung von Els heißt Microsoft Sprachenerkennung. Dieser Dienst verwendet von Microsoft patentierte Technologie, um Anwendungen zu ermöglichen, die Sprache zu erkennen, in der bestimmter Text geschrieben wurde.
ms.assetid: 11438e0b-d841-44d0-b68f-77868be4c92f
title: Microsoft-Sprachenerkennung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b395f6a1a320b66f00d996510b7cafc28b8e64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349069"
---
# <a name="microsoft-language-detection"></a>Microsoft-Sprachenerkennung

Der Dienst für die Spracherkennung von Els heißt Microsoft Sprachenerkennung. Dieser Dienst verwendet von Microsoft patentierte Technologie, um Anwendungen zu ermöglichen, die Sprache zu erkennen, in der bestimmter Text geschrieben wurde.

## <a name="input-to-microsoft-language-detection"></a>Eingabe an Microsoft Sprachenerkennung

Die Eingabe für den Microsoft Sprachenerkennung-Dienst ist UTF-16-Text (Normalized Form C). Der Dienst muss die Sprache für diesen Text ermitteln.

## <a name="output-of-microsoft-language-detection"></a>Ausgabe von Microsoft Sprachenerkennung

Der Microsoft Sprachenerkennung-Dienst ruft eine mit zwei NULL endenden, Registrierungs formatierte UTF-16-Zeichen folgen Auflistungs Sprachen ab, die durch ihre Namen dargestellt werden, getrennt durch Null-Zeichen Trennzeichen. Die Liste ist nach Relevanz sortiert. In den meisten Sprachen werden neutrale Namen verwendet. Für einige, z. b. SR-Cyrl, SR-LATN, zh-Hant und zh-Hans, werden jedoch vollständige Namen verwendet.

## <a name="microsoft-language-detection-operation"></a>Microsoft Sprachenerkennung-Vorgang

Der Microsoft Sprachenerkennung Service überprüft das Unicode-Skript des von der Anwendung bereitgestellten Texts. Er segmentiert den Text basierend auf den erkannten Skripts und bestimmt dann die Sprache, in der die einzelnen Segmente geschrieben werden. Wenn ein Skript eine einzelne Sprache anzeigt, ist die Sprache in der Ausgabeliste der Sprachen garantiert vorhanden. Der Dienst verwendet einen patentierten Algorithmus, um die Relevanz der einzelnen unterstützten Sprachen zu ermitteln.

## <a name="microsoft-language-detection-guid"></a>Microsoft Sprachenerkennung-GUID

Die GUID für den Microsoft Sprachenerkennung-Dienst wird in elssrvc. h deklariert, wie im folgenden Code gezeigt.


```C++
// {CF7E00B1-909B-4d95-A8F4-611F7C377702}
static const GUID ELS_GUID_LANGUAGE_DETECTION =
    { 0xCF7E00B1, 0x909B, 0x4D95, { 0xA8, 0xF4, 0x61, 0x1F, 0x7C, 0x37, 0x77, 0x02 } };
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu erweiterten linguistischen Diensten](about-extended-linguistic-services.md)
</dt> </dl>

 

 



