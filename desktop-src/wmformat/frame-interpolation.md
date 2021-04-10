---
title: Frame Interpolation
description: Frame Interpolation
ms.assetid: 74dbe855-361c-42ba-b21b-322ccd1c91d0
keywords:
- Windows Media-Format-SDK, Frame Interpolation
- Codecs, Frame Interpolation
- Frame Interpolation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c62f95322920576eec0f10f3e4d61a279fdc4cf
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038558"
---
# <a name="frame-interpolation"></a>Frame Interpolation

Die Frame Interpolation ist der Prozess der Erstellung von zwischen Video Frames auf der Grundlage der Daten in zwei aufeinander folgenden Frames codierter Videos. In der Tat erhöht die Frame Interpolation die [*Framerate*](wmformat-glossary.md) codierter Videos zum Zeitpunkt der Decodierung. Mithilfe von Frame Interpolation können Sie die Glättung von Wiedergabe Möglichkeiten für Videostreams mit niedrigen Frameraten verbessern.

Da es sich hierbei um eine Decodierungs Funktion handelt, sind keine speziellen Codierungsoptionen enthalten, und der Inhalt wird dadurch nicht erhöht. Die Frame Interpolation wird als Ausgabe Einstellung im Reader-Objekt angegeben.

Nur der Windows Media Video 9-Codec unterstützt die Frame Interpolation.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Codec-Features**](codec-features.md)
</dt> <dt>

[**IWMReaderAdvanced2:: setoutputsetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)
</dt> <dt>

[**Ausgabeeinstellungen**](output-settings.md)
</dt> </dl>

 

 




