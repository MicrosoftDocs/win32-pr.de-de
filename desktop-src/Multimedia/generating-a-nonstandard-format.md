---
title: Generieren eines Nichtstandardformats
description: Generieren eines Nichtstandardformats
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Audiokomprimierungs-Manager (ACM), nicht standardmäßige Formate
- ACM (Audiokomprimierungs-Manager), nicht standardmäßige Formate
- ACM-Beispiele,nicht standardmäßige Formate
- acmFormatSuggest-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 968dafae93cac419a0078989ab8786e02732cbaa942fd185969c5571c2e8237e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119496340"
---
# <a name="generating-a-nonstandard-format"></a>Generieren eines Nichtstandardformats

Manchmal benötigt eine Anwendung ein nicht standardmäßiges Format. Beispielsweise kann eine Anwendung eine ADPCM-Formatdatei mit 16 kHz benötigen. Da 16 kHz nicht dem Standard entspricht, generieren die Enumerationsfunktionen dieses Format nicht. Da die Formatalgorithmen nicht benutzerdefiniert in die Anwendung codiert werden, gibt es keine zuverlässige Möglichkeit, ein nicht standardmäßiges Format zu generieren. Manchmal ist es jedoch möglich, ein analoges Format zu generieren, indem Sie ein gültiges PCM-Format mit allen erforderlichen Informationen einrichten und dann die [**acmFormatSuggest-Funktion**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) verwenden. Da Beiz- und Dekomprimierer versuchen, ein Format zu vorschlagen, das dem gewünschten Format am nächsten ist, werden die Anzahl der Kanäle und die Häufigkeit in der Regel beibehalten.

 

 




