---
title: Audiomixer in Windows Vista
description: Audiomixer in Windows Vista
ms.assetid: 541cb5f3-b5ca-436f-88dd-6ef8459c6157
keywords:
- Multimedia-Audiodaten, Windows Vista-Audiomixer
- Audiodaten, Windows Vista-Audiomixer
- Audiomixer, Windows Vista
- Mixer, Windows Vista
- Windows Vista-Audiomixer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0610e9f16e13c19a253fbd9f6fac5ef452fa68ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104561274"
---
# <a name="audio-mixers-in-windows-vista"></a>Audiomixer in Windows Vista

Ab Windows Vista werden einige Mixer-Steuerelemente in Software anstelle von Hardware implementiert. Beispielsweise werden die volumesteuerelemente mithilfe der Windows-audiositzungs-API (WASAPI) implementiert. Diese Steuerelemente wirken sich nicht direkt auf die Hardware Einstellungen aus. Außerdem sind Sie einer prozessspezifischen Audiositzung zugeordnet, sodass sich die Änderungen auf die aufrufenden Anwendungen auswirken, sich aber nicht auf andere Anwendungen auswirken.

Jedes audioendpunktgerät verfügt über ein Standard-Mischungs Layout, das in Software implementiert ist.

-   Jeder audiorenderingendpunkt enthält eine Zielzeile, die Folgendes enthält:
    -   Volumesteuerung
    -   Steuerelement stumm schalten
    -   Quellzeile: Waveform-Audioausgabe.
    -   Quellzeile: AudioCD.
-   Jeder audioerfassungs-Endpunkt enthält eine Zielzeile, die Folgendes enthält:
    -   Volumesteuerung
    -   Steuerelement stumm schalten
    -   Quellzeile: Waveform-Audioeingabe. Der Komponententyp ist abhängig vom Eingabegerät – z. b. einem Mikrofon.

Jede Quellzeile enthält ein volumensteuerelement und ein stumm Steuerelement. Das folgende Diagramm zeigt die Komponenten der Rendering-Endpunkte und Aufzeichnungs Endpunkte.

![standardmischlayouts](images/mixer1.gif)

Alle-Steuerelemente für einen Endpunkt manipulieren das gleiche zugrunde liegende Software Steuerelement. Wenn Sie die Einstellungen für ein Steuerelement ändern, erhalten Sie daher eine Benachrichtigung zum Ändern des Steuer Elements für die anderen Steuerelemente. (Siehe [**mm- \_ mixm- \_ Steuerelement \_ Änderung**](mm-mixm-control-change.md).)

Dieses Standardlayout wird für die Kompatibilität mit vorhandenen Anwendungen bereitgestellt, die die Audiomixer-Funktionen verwenden. Neue Anwendungen sollten diese Funktionen nicht verwenden.

 

 




