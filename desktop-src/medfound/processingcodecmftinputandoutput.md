---
description: Verarbeiten von Codec-MFT-Eingaben und-Ausgaben
ms.assetid: 2d012508-de13-411f-9102-22e47faddffd
title: Verarbeiten von Codec-MFT-Eingaben und-Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1af3a16fa1855574f1b7618bc0d41bf85c15412f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215017"
---
# <a name="processing-codec-mft-input-and-output"></a>Verarbeiten von Codec-MFT-Eingaben und-Ausgaben

Wenn Sie den Eingabetyp und den Ausgabetyp für eine MFT konfiguriert haben, können Sie mit der Verarbeitung von Daten Beispielen beginnen. Zum Verarbeiten von Beispielen an den MFT übergeben Sie die [**imftransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) -Methode, und rufen Sie dann das verarbeitete Beispiel durch Aufrufen von [**imftransform::P rocess Output**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)ab. Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos. Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-MFTs](workingwithcodecmfts.md)
</dt> </dl>

 

 



