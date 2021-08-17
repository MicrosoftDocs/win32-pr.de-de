---
title: Audio-Resampling
description: Audio-Resampling
ms.assetid: ec6ad6b2-1d35-4ac4-9a1e-3fc9c053000c
keywords:
- Windows Medienformat-SDK, Audio-Resampling
- Windows Medienformat-SDK, Resampling von Audio
- Advanced Systems Format (ASF), Audioresampling
- ASF (Advanced Systems Format), Audio resampling
- Advanced Systems Format (ASF), Resampling von Audio
- ASF (Advanced Systems Format), Resampling von Audio
- Audio-Resampling
- Resampling von Audiodaten, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a5d95ed50117ac9d0fe7d71a2148314e1b9faf3ba8a26b99bb69083029b991c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118434474"
---
# <a name="audio-resampling"></a>Audio-Resampling

Jedes komprimierte Format eines Audiocodecs hat eine bestimmte Abtastrate und Stichprobengröße. Diese müssen nicht mit den Einstellungen des Eingabe- oder Ausgabeformats übereinstimmen. Wenn ein Eingabeformat über andere Einstellungen als das im Profil beschriebene komprimierte Format verfügt, wird der Writer die Audiodaten während des Codierungsprozesses erneutsammpeln, um dem komprimierten Format zu passen. Nur bestimmte Formate werden vom Writer als Eingabe akzeptiert. Wenn Sie die Eingabeformate für einen komprimierten Audiostream aufzählen, können alle abgerufenen Formate neu erstellt werden, um dem Format im Profil zu passen.

Beim Lesen komprimierter Audiodaten wird der Inhalt vom Reader neu sampelt, um dem Ausgabeformat zu passen. Sie müssen eines der Ausgabeformate verwenden, die vom Reader aufzählt werden, damit Sie garantiert können, dass die Audiodaten für die Ausgabeformateinstellungen neu erstellt werden können.

Jedes Resampling wirkt sich potenziell auf die Qualität des Audios aus. Wenn möglich, sollten Sie Eingabe- und Ausgabeformate mit Einstellungen verwenden, die mit dem komprimierten Format übereinstimmen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Funktionen zum Schreiben von Dateien**](file-writing-features.md)
</dt> <dt>

[**Arbeiten mit Eingaben**](working-with-inputs.md)
</dt> <dt>

[**Arbeiten mit Ausgaben**](working-with-outputs.md)
</dt> </dl>

 

 




