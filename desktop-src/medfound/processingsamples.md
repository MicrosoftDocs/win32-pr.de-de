---
description: Verarbeiten von Codec DMO-Eingaben und-Ausgaben
ms.assetid: fab6244e-a20e-4395-a82c-0905e3225516
title: Verarbeiten von Codec DMO-Eingaben und-Ausgaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05c6781d877f4c863161537fcc5b6a746691cfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344409"
---
# <a name="processing-codec-dmo-input-and-output"></a>Verarbeiten von Codec DMO-Eingaben und-Ausgaben

Wenn Sie den Eingabetyp und den Ausgabetyp für ein DMO konfiguriert haben, können Sie mit der Verarbeitung von Daten Beispielen beginnen. Sie übergeben Beispiele an den DMO zur Verarbeitung mithilfe der **imediaobject::P rocessinput** -Methode, und rufen Sie dann das verarbeitete Beispiel durch Aufrufen von **imediaobject::P rocess Output** ab. Sie sollten genaue Zeitstempel und Dauer für alle bestandenen Eingabe Beispiele festlegen. Zeitstempel sind nicht unbedingt erforderlich, unterstützen jedoch die Verwaltung von Audiodaten und Videos. Wenn Sie nicht über die Zeitstempel für die Beispiele verfügen, ist es besser, Sie zu verlassen, als nicht unsichere Werte zu verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Codec-DMOS](workingwithcodecdmos.md)
</dt> </dl>

 

 



