---
description: Verarbeiten von Codec DMO Eingabe und Ausgabe
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Verarbeiten von Codec DMO Eingabe und Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e3b159ea9e8a323a8e980b9dbba227aa2a62d76316b90e09f45592044091f81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035088"
---
# <a name="processing-codec-dmo-input-and-output"></a>Verarbeiten von Codec DMO Eingabe und Ausgabe

Wenn Sie den Eingabetyp und den Ausgabetyp für eine DMO konfiguriert haben, können Sie mit der Verarbeitung von Datenstichproben beginnen. Sie übergeben Beispiele zur Verarbeitung mithilfe der **IMediaObject::P rocessInput-Methode** an den DMO und rufen dann das verarbeitete Beispiel ab, indem **Sie IMediaObject::P rocessOutput** aufrufen. Sie sollten genaue Zeitstempel und Daueren für alle übergebenen Eingabebeispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, unterstützen aber die Aufrechterhaltung der Audio-/Videosynchronisierung. Wenn Sie nicht über die Zeitstempel für Ihre Stichproben verfügen, sollten Sie sie besser weglassen, als unsichere Werte zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOs](workingwithcodecdmos.md)
</dt> </dl>

 

 



