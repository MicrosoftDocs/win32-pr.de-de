---
title: Switches
description: Switches
ms.assetid: ab92d30d-97ab-4229-aed8-1080b6e6dc88
keywords:
- Audiomixer, Steuerelemente
- Audiomixer, Switches
- Mixer, Steuerelemente
- Mixer, Switches
- Switch-Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN-Struktur
- Boolesches Steuerelement
- Schaltflächen-Steuerelement
- Ein-/Aus-Steuerelement
- Mono-Steuerelement
- Lautstärkesteuerung
- Erweiterte Stereo-Steuerung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336d2e23c5e6438fbc19208e3366283147462c2451a12e3ccdcae6c13fcd93d2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805080"
---
# <a name="switches"></a>Switches

Die Schaltersteuerelemente sind Schalter mit zwei Zuständen. Diese Steuerelemente verwenden die [**\_ MIXERCONTROLDETAILS BOOLEAN-Struktur,**](/previous-versions//dd757295(v=vs.85)) um Steuerelementeigenschaften abzurufen und festzulegen. In der folgenden Tabelle werden die Typen von Schaltern beschrieben.



| Control         | Beschreibung                                                                                                                                                                                                                           |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolesch         | Der generische Schalter. Sie kann auf **TRUE** oder **FALSE** festgelegt werden.                                                                                                                                                                           |
| Schaltfläche          | Legen Sie für alle Schaltflächen, die der Treiber behandeln soll, auf **TRUE** fest, als ob sie gedrückt worden wären. Wenn der Wert **FALSE** ist, wird keine Aktion ausgeführt.                                                                                         |
| Ein/Aus          | Ein alternativer Schalter, der durch eine andere Grafik als die für den booleschen Schalter dargestellt wird. Sie kann auf ON oder OFF festgelegt werden.                                                                                                    |
| Mute            | Stummschaltt eine Audiozeile (unterdrückt den Datenfluss der Zeile) oder lässt die Wiedergabe der Audiodaten zu. Dieser Schalter wird häufig verwendet, um die Linien zu steuern, die in den Mixer eingespeist werden.                                                        |
| Mono            | Wechselt zwischen Mono- und Stereoausgabe für eine Stereoaudiolinie. Legen Sie diese Einstellung auf OFF fest, um Stereodaten als separate Kanäle wiederzuspielen. Legen Sie diese Einstellung auf ON fest, um Daten aus beiden Kanälen in einer Mono-Audiolinie zu kombinieren.                                            |
| Lautstärke        | Verstärkt low-volume-Sound für eine Audiozeile. Legen Sie diese Einstellung auf ON fest, um die Lautstärke zu erhöhen. Legen Sie diese Einstellung auf OFF fest, um die Lautstärke auf normal festzulegen. Der Umfang der Verstärkung ist hardwarespezifisch. Weitere Informationen finden Sie in der Dokumentation für Ihr Mixergerät. |
| Stereo Enhanced | Erhöht die Stereotrennung. Legen Sie diese Einstellung auf ON fest, um die Stereotrennung zu erhöhen. Legen Sie diese Einstellung ohne Erweiterung auf OFF fest.                                                                                                                                  |



 

 

 