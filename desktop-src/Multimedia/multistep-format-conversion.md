---
title: Mehrstufige Format Konvertierung
description: Mehrstufige Format Konvertierung
ms.assetid: 21d837e7-d665-461d-9676-68add3829fb0
keywords:
- Audiokomprimierungs-Manager (ACM), Daten werden umgerechnet
- ACM (Audiokomprimierungs-Manager), Daten werden umgerechnet
- ACM-Beispiele, Daten werden umgerechnet
- Konvertieren von Daten
- acmformatvorschlagen-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e81ebd5bef17d6a97cb5735e15219c39d3116b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947772"
---
# <a name="multistep-format-conversion"></a>Mehrstufige Format Konvertierung

Manchmal kann das ACM in einem einzigen Schritt keine Daten von einem Format in ein anderes konvertieren. Beispielsweise muss eine Anwendung möglicherweise 16-Bit-, 44-kHz-Stereodaten in 11-kHz Mono ADPCM konvertieren. Wenn der-Kompressor oder der Dekompressor diese Konvertierung nicht direkt ausführen kann, kann Sie von der Anwendung in zwei Schritten versucht werden. Dies bedeutet in der Regel, dass eine Konvertierung zwischen zwei PCM-Formaten durchführen und dann eine weitere Konvertierung in den endgültigen Formattyp erfolgt.

Um in zwei Schritten zu konvertieren, verwenden Sie die [**acmformatvorschlagen**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest) -Funktion, um ein PCM-Format zu finden, das dem ADPCM-Format entspricht. Verwenden Sie dann zwei Konvertierungsdaten Ströme, um die Konvertierung auszuführen. Führen Sie z. b. eine Konvertierung von 16-Bit-, 44-kHz-Stereo-PCM in 16-Bit, 11-kHz Mono aus, und konvertieren Sie dann von 16-Bit-, 11-kHz Mono in 11-kHz Mono ADPCM.

Die mehrstufige Konvertierung ist auch dann der Fall, wenn das Quell-oder Zielformat nicht PCM ist. Wenn das Quellformat nicht PCM ist, sollte es vor der Konvertierung in ein PCM-Format geändert werden. Wenn das Zielformat nicht PCM ist, muss die Quelle in ein zwischen-PCM-Format konvertiert und dann in das endgültige Zielformat konvertiert werden.

Die einfachsten Konvertierungen treten auf, wenn es sich bei den Quell-und Zielformaten um PCM-Formate handelt. Wenn das Quell-oder Zielformat nicht PCM ist, ist für die Konvertierung möglicherweise ein zusätzlicher Schritt erforderlich. Wenn das Quell-und Zielformat nicht PCM sind, ist für die Konvertierung in der Regel mehr als ein Schritt erforderlich, und in manchen Fällen ist eine Konvertierung möglicherweise nicht möglich.

 

 




