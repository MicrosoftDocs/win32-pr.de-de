---
title: Aushandlung formatieren
description: Aushandlung formatieren
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player-Plug-ins, Format Aushandlung
- Plug-ins, Format Aushandlung
- Plug-Ins für die digitale Signalverarbeitung, Format Aushandlung
- DSP-Plug-ins, Format Aushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbc805b18d3e2be081e4f85bcc5ed42aded06853
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337603"
---
# <a name="format-negotiation"></a>Aushandlung formatieren

Bei Windows Media Player und einem DSP-Plug-in für die gemeinsame Nutzung von Daten müssen beide Programme das Format der Daten, die Sie verarbeiten, zustimmen. Das DSP-Plug-in implementiert Methoden, die der Player aufruft, um zu bestimmen, welche Formate das Plug-in unterstützt. Das Plug-in implementiert auch Methoden, die der Player aufruft, um das aktuelle Format festzulegen.

Wenn das Plug-in als "direkmo (direkmo)" fungiert, ermittelt Windows Media Player Medienformate und legt diese fest, indem Methoden der **imediaobject** -Schnittstelle aufgerufen werden. Beispielsweise ruft der Player den **imediaobject:: getinputtype** des Plug-ins wiederholt auf, um eine Liste aller vom Plug-in unterstützten Eingabeformate zu erhalten. DMO-Plug-Ins verwenden die **DMO- \_ \_ Medientyp** Struktur zum Organisieren der Informationen, die ein Medienformat angeben. Weitere Informationen zur Verwendung von DMO-Plug-ins und des playeraushandlungs-Formats finden Sie unter [Informationen zu imediaobject](about-imediaobject.md).

Wenn das Plug-in als Media Foundation Transformation (MFT) fungiert, erkennt Windows Media Player Medienformate durch Aufrufen von Methoden der **imftransform** -Schnittstelle und legt diese fest. Beispielsweise ruft der Player den **imftransform:: getinputavailabletype** des Plug-ins wiederholt auf, um eine Liste aller vom Plug-in unterstützten Eingabeformate zu erhalten. MFT-Plug-ins und der Player verwenden die **imfmediatype** -Schnittstelle zum organisieren und Austauschen von Formatinformationen.

Windows Media Player verwendet ein audiodsp-Plug-in nur dann, wenn das Plug-in dieselbe bidirektiontiefe wie die wiedergegebene digitale Audiodatei unterstützt. Wenn die digitale Audiodatei beispielsweise 20-Bit ist, muss das Plug-in für die Verarbeitung von 20-Bit-Audiodaten geschrieben werden. Bei CD-Audiodaten müssen DSP-Plug-ins 20-Bit-Verarbeitung unterstützen.

Bei der formataushandlung von Multi-Channel-Inhalten auf einem Computer, der für die Verwendung mit Stereo Referenten konfiguriert ist, versucht Windows Media Player zuerst, mithilfe des vorhandenen Eingabe-und Ausgabeformats eine Verbindung zu einem audiodsp-Plug-in herzustellen, indem **imediaobject:: setinputtype** und **imediaobject:: setoutputtype** aufgerufen werden. Nach dieser anfänglichen Aushandlung listet der Spieler die Formate auf, die das Plug-in unterstützt, und versucht, die beste Format Kombination für den Player und das Plug-in auszuhandeln. Wenn das Plug-in bei der anfänglichen Aushandlung Stereo-Audiodaten (definiert durch eine **WaveFormatEx** -Struktur) als Eingabeformat annimmt und anschließend nur multikanalaudiodaten akzeptiert (definiert durch eine **WAVEFORMATEXTENSIBLE** -Struktur), stellt der Spieler multikanalaudiodaten als Eingabeformat für das Plug-in bereit. Dieses Verhalten während der formataushandlung ist für die Verwendung im Microsoft Windows XP-Betriebssystem verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über den DSP-Plug-in-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




