---
title: Switches
description: Switches
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Switches
- Mischungen, Steuerelemente
- Mixer, Switches
- Switch-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- Boolesches Steuerelement
- Button-Steuerelement
- ein/aus-Steuerelement
- Mono-Steuerelement
- Lautheit-Steuerelement
- Verbessertes Stereo Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1d65bb2a14a0e7dc527fab0e628035839855934
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103858193"
---
# <a name="switches"></a>Switches

Die Switch-Steuerelemente sind Switches mit zwei Zuständen. Diese Steuerelemente verwenden die [**\_ boolesche "mixercontroldetails**](/previous-versions//dd757295(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften. In der folgenden Tabelle werden die Typen von Switches beschrieben.



| Control         | Beschreibung                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolesch         | Der generische Switch. Sie kann auf " **true** " oder " **false**" festgelegt werden.                                                                                                                                                                           |
| Schaltfläche          | Legen Sie für alle Schaltflächen, die vom Treiber behandelt werden sollen, den Wert " **true** " fest. Wenn der Wert **false** ist, wird keine Aktion ausgeführt.                                                                                         |
| Ein/Aus          | Ein alternativer Switch, der durch eine andere Grafik als die für den booleschen Switch verwendet wird. Sie kann auf ein oder aus festgelegt werden.                                                                                                    |
| Mute            | Gibt eine Audiolinie an (unterdrückt den Datenfluss der Zeile) oder ermöglicht die Wiedergabe der Audiodaten. Dieser Schalter wird häufig verwendet, um die Zeilen zu steuern, die in den Mixer eingespeist werden.                                                        |
| Mono            | Schaltet zwischen Mono-und Stereoausgabe für eine Stereo Audiolinie um. Legen Sie diese Einstellung auf OFF fest, um Stereodaten als separate Kanäle wiederzugeben Legen Sie auf ein fest, um Daten aus beiden Kanälen in eine Mono-Audiolinie zu kombinieren.                                            |
| Lautstärke        | Steigert den Bass von niedrigem Volume für eine Audiolinie. Legen Sie auf ein fest, um den Bass von niedrigem Volume zu erhöhen. Legen Sie diese Einstellung auf OFF fest, um die volumeebenen auf normal Der Umfang der Verstärkung ist Hardware spezifisch. Weitere Informationen finden Sie in der Dokumentation für Ihr Mischgerät. |
| Stereo-erweitert | Vergrößert die Stereo Trennung. Legen Sie auf ein fest, um die Trennung von Stereo Auf OFF festgelegt, um keine Erweiterung zu haben.                                                                                                                                  |



 

 

 