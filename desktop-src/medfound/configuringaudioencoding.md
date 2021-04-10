---
description: Konfigurieren der Audiocodierung
ms.assetid: 40004f07-0b8c-49cd-9e17-1f6ad7604fbb
title: Konfigurieren der Audiocodierung (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47595f440d10ad0d3c5695f117204f357035d4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214334"
---
# <a name="configuring-audio-encoding-microsoft-media-foundation"></a>Konfigurieren der Audiocodierung (Microsoft Media Foundation)

Der Windows Media Audio Encoder listet alle unterstützten Ausgabetypen in seinem vollständigen Formular auf. Rufen Sie den gewünschten Typ durch Aufrufen von **imediaobject:: getoutputtype** oder **imftransform:: getavailableoutputtype** ab, und legen Sie den abgerufenen Typ Unchanged als Ausgabetyp durch Aufrufen von **imediaobject:: setoutputtype** oder **imftransform:: setoutputtype** fest.

Die vom Audioencoder unterstützten Ausgabemedien Typen werden bei der Konfiguration der Codierungs Eigenschaften geändert. Sie müssen alle Codierungs Eigenschaften konfigurieren, die Sie verwenden möchten, bevor Sie den Ausgabetyp auflisten.

Die Modi Two-Pass und VBR werden von den audioencodern unterstützt, sind jedoch anders konfiguriert als für Video. Weitere Informationen finden Sie unter Auflisten [von Audiotypen für bestimmte Codierungs Modi](enumeratingaudiotypesforspecificencodingmodes.md).

Die vom Audioencoder unterstützten Eingabetypen sind erst verfügbar, wenn Sie den Ausgabetyp festgelegt haben. Wenn Sie **imediaobject:: getinputtype** oder **imftransform:: getinputtype** aufrufen, bevor Sie einen Ausgabetyp festlegen, gibt die Methode DMO \_ e \_ ohne \_ Weitere \_ Elemente \_ bzw. MFT e \_ nicht \_ mehr \_ Typen zurück. Nachdem der Ausgabetyp festgelegt wurde, listet der Encoder die Eingabetypen auf, die er für den ausgewählten Ausgabetyp unterstützt.

Vom Windows Media Audio Encoder wird keine audioneu Stichprobe ausgeführt. Dies bedeutet, dass der encoderausgabetyp und der codiereingabetyp die gleiche Anzahl von Kanälen, Bits pro Stichprobe und Stichprobenrate aufweisen müssen. Weitere Informationen finden Sie untersuchen von [Audioencoder-Ausgabetypen](findingaudioencoderoutputtypes.md).

> [!Note]  
>    Jeder vom Audioencoder aufgelistete Ausgabetyp enthält eine **WaveFormatEx** -Struktur (auf die von **am \_ Media \_ Type. pbformat** verwiesen wird), an die erweiterte Daten angehängt wurden. Die Größe der erweiterten Daten wird von **WaveFormatEx. cbSize** angegeben. Diese Daten müssen mit den codierten Inhalten aufbewahrt werden, damit Sie an den Decoder übermittelt werden können. Der Inhalt kann nicht ohne die erweiterten Formatierungsdaten dekomprimiert werden.

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Arbeiten mit Audiodaten](workingwithaudio.md)
</dt> </dl>

 

 



