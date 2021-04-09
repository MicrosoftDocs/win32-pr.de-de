---
title: Faders
description: Faders
ms.assetid: 2ca6be9f-9825-44d9-99c1-abcf6f0b42f7
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Faders
- Mischungen, Steuerelemente
- Mixer, Faders
- Faders
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Volume Fade-Steuerelement
- Bass Volume-Fade-Steuerelement
- Steuerelement für Aufblenden von Volumes
- Grafik-Ausgleichs Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd2b560b61a694089b947b0cfda7a54b486f1e3a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948637"
---
# <a name="faders"></a>Faders

Die Fader-Steuerelemente sind in der Regel vertikale Steuerelemente, die nach oben oder unten angepasst werden können. Diese Steuerelemente verfügen über eine lineare Skala und verwenden die " [**mixercontroldetails \_**](/previous-versions//dd757298(v=vs.85)) "-Struktur ohne Vorzeichen zum Abrufen und Festlegen von Steuerelement Details. In der folgenden Tabelle werden die Typen von Faders beschrieben.



| Control   | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Fader     | Allgemeines Fade-Steuerelement. Der Bereich zulässiger Werte ist 0 bis 65.535.                                                                                                                                                                                                                                                                                                                                       |
| Lautstärke    | Allgemeines Volumen-Fade-Steuerelement. Der Bereich zulässiger Werte ist 0 bis 65.535. Informationen zum Ändern dieses Bereichs finden Sie in der Dokumentation für Ihr Mischgerät.                                                                                                                                                                                                                                        |
| Barsch      | Bass Volume-Fade-Steuerelement. Der Bereich zulässiger Werte ist 0 bis 65.535. Die Grenzwerte für das Bass Frequenzband sind Hardware spezifisch. Informationen zu Band Limits finden Sie in der Dokumentation für Ihr Mischgerät.                                                                                                                                                                                      |
| Höhen    | Gespeicherbare volumefade-Steuerelement. Der Bereich zulässiger Werte ist 0 bis 65.535. Die Grenzwerte für das Höhen Frequency-Band sind Hardware spezifisch. Informationen zu den Band Limits finden Sie in der Dokumentation für Ihr Mischgerät.                                                                                                                                                                              |
| Equalizer | Grafik-equalikansteuerelement. Der Bereich der zulässigen Werte für ein Band des Equalizers liegt zwischen 0 und 65.535. Die Anzahl der Ausgleichs Bänder und ihre Grenzwerte sind Hardware spezifisch. Weitere Informationen zum Equalizer finden Sie in der Dokumentation für Ihr Mischgerät. Sie können die [**\_ listtext-Struktur mixercontroldetails**](/previous-versions//dd757296(v=vs.85)) verwenden, um Text Bezeichnungen für den Equalizer abzurufen. |



 

 

 