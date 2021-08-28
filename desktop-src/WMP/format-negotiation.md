---
title: Formataushandlung
description: Formataushandlung
ms.assetid: 7847d4e3-1250-4c35-88e1-52d61bf1553f
keywords:
- Windows Media Player Plug-Ins, Formataushandlung
- Plug-Ins, Formataushandlung
- Plug-Ins für die digitale Signalverarbeitung, Formataushandlung
- DSP-Plug-Ins, Formataushandlung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69669bc3af82400ea62d154335d117fef185d0b34184be4101ffa5ae309e6ccb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054968"
---
# <a name="format-negotiation"></a>Formataushandlung

Damit Windows Media Player und ein DSP-Plug-In Daten freigeben können, müssen sich beide Programme auf das Format der daten einigen, die sie verarbeiten. Das DSP-Plug-In implementiert Methoden, die der Player aufruft, um zu bestimmen, welche Formate das Plug-In unterstützt. Das Plug-In implementiert auch Methoden, die der Player aufruft, um das aktuelle Format festzulegen.

Wenn das Plug-In als DirextX-Medienobjekt (DMO) fungiert, ermittelt Windows Media Player Medienformate und legt diese fest, indem methoden der **IMediaObject-Schnittstelle** aufgerufen werden. Beispielsweise ruft der Player wiederholt **IMediaObject::GetInputType** des Plug-Ins auf, um eine Liste aller Eingabeformate abzurufen, die vom Plug-In unterstützt werden. DMO Plug-Ins verwenden die **DMO \_ MEDIA \_ TYPE-Struktur,** um die Informationen zu organisieren, die ein Medienformat angeben. Weitere Informationen dazu, wie DMO Plug-Ins und das Player-Aushandlungsformat verwenden, finden Sie unter [Informationen zu IMediaObject.](about-imediaobject.md)

Wenn das Plug-In als Media Foundation Transform (MFT) fungiert, ermittelt Windows Media Player Medienformate und legt diese fest, indem methoden der **INTERFACESTransform-Schnittstelle** aufgerufen werden. Der Player ruft z. B. wiederholt **DENTRANSFORM::GetInputAvailableType** des Plug-Ins auf, um eine Liste aller Eingabeformate abzurufen, die vom Plug-In unterstützt werden. MFT-Plug-Ins und player verwenden die **SCHNITTSTELLE "FORMATSMediaType",** um Formatinformationen zu organisieren und auszutauschen.

Windows Media Player verwendet nur dann ein DSP-Audio-Plug-In, wenn das Plug-In die gleiche Bittiefe unterstützt wie das wiedergegebene digitale Audio. Wenn die digitale Audiodatei beispielsweise 20 Bit ist, muss das Plug-In geschrieben werden, um 20-Bit-Audio zu verarbeiten. Für CD-Audio müssen DSP-Plug-Ins die 20-Bit-Verarbeitung unterstützen.

Während der Formataushandlung von Mehrkanalinhalten auf einem Computer, der für die Verwendung mit Stereolautmodulen konfiguriert ist, versucht Windows Media Player zunächst, eine Verbindung mit einem Audio-DSP-Plug-In herzustellen, indem das vorhandene Eingabe- und Ausgabeformat verwendet wird, indem **IMediaObject::SetInputType** und **IMediaObject::SetOutputType** aufgerufen werden. Sobald diese erste Aushandlung erfolgt ist, listet der Player die Formate auf, die das Plug-In unterstützt, und versucht, die beste Formatkombination für Player und Plug-In auszuhandeln. Wenn das Plug-In stereo-Audio (definiert durch eine **WAVEFORMATEX-Struktur)** während der ersten Aushandlung als Eingabeformat akzeptiert und anschließend nur Mehrkanalaudio (definiert durch eine **WAVEFORMATEXTENSIBLE-Struktur)** akzeptiert, stellt der Player mehrkanalige Audiodaten als Eingabeformat für das Plug-In bereit. Dieses Verhalten während der Formataushandlung ist für die Verwendung im Betriebssystem Microsoft Windows XP verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Übersicht über DSP-Plug-In-Entwickler**](dsp-plug-in-developer-overview.md)
</dt> </dl>

 

 




