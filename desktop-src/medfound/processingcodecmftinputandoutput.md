---
description: Verarbeiten von Codec-MFT-Eingabe und -Ausgabe
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Verarbeiten von Codec-MFT-Eingabe und -Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3cbec9b92ae11d8f1f3722f2cb2540a5b5b01bb5d680e448d298a36ec682ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101839"
---
# <a name="processing-codec-mft-input-and-output"></a>Verarbeiten von Codec-MFT-Eingabe und -Ausgabe

Wenn Sie den Eingabe- und Ausgabetyp für eine MFT konfiguriert haben, können Sie mit der Verarbeitung von Datenbeispielen beginnen. Sie übergeben Stichproben zur Verarbeitung an MFT, indem Sie die [**METHODE ZUEgetransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) verwenden, und rufen dann die verarbeitete Stichprobe ab, indem Sie [**DIEBtransform::P rocessOutput aufrufen.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) Sie sollten genaue Zeitstempel und Dauer für alle übergebenen Eingabebeispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, helfen aber bei der Aufrechterhaltung der Audio-/Videosynchronisierung. Wenn Sie nicht über die Zeitstempel für Ihre Stichproben verfügen, ist es besser, sie weg zu lassen, als unsichere Werte zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



