---
title: Erstellen eines nicht standardmäßigen Formats
description: Erstellen eines nicht standardmäßigen Formats
ms.assetid: e9f80aec-d5dc-4c44-aea0-95220542e48d
keywords:
- Audiokomprimierungs-Manager (ACM), nicht dem Standard entsprechende Formate
- ACM (Audiokomprimierungs-Manager), nicht dem Standard entsprechende Formate
- ACM-Beispiele, nicht dem Standard entsprechende Formate
- acmformatvorschlagen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6e775fb09f926e0380b8141101b816b0dcbb221
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856048"
---
# <a name="generating-a-nonstandard-format"></a>Erstellen eines nicht standardmäßigen Formats

Manchmal benötigt eine Anwendung ein nicht standardmäßiges Format. Beispielsweise benötigt eine Anwendung möglicherweise eine Datei mit dem Format "16-kHz ADPCM-Format". Da 16 kHz nicht dem Standard entspricht, wird dieses Format von den Enumerationsfunktionen nicht generiert. In der Tat gibt es keine zuverlässige Möglichkeit, ein nicht standardmäßiges Format zu generieren, wenn Sie die Format Algorithmen nicht in die Anwendung schreiben. Es ist jedoch manchmal möglich, ein entsprechendes Format zu generieren, indem Sie ein gültiges PCM-Format mit allen erforderlichen Informationen einrichten und dann die [**acmformatvorschlagen**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) -Funktion verwenden. Da Kompressoren und Dekompressoren versuchen, ein Format vorzuschlagen, das dem gewünschten Format am nächsten liegt, wird die Anzahl der Kanäle und die Häufigkeit normalerweise beibehalten.

 

 




