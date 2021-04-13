---
title: Schieberegler (Windows Multimedia)
description: Schieberegler
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Schieberegler
- Mischungen, Steuerelemente
- Mixer, Schieberegler
- Schieberegler-Steuerelemente
- MIXERCONTROLDETAILS_SIGNED Struktur
- Pan-Steuerelement
- QSound Pan-Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1d7644255e2fa9ee6384cbb5102df81c2a1eb0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104391398"
---
# <a name="sliders-windows-multimedia"></a>Schieberegler (Windows Multimedia)

Die Schieberegler-Steuerelemente sind in der Regel horizontale Steuerelemente, die nach links oder rechts angepasst werden können. Diese Steuerelemente verwenden die [**\_ signierte "mixercontroldetails**](/previous-versions//dd757297(v=vs.85)) "-Struktur zum Abrufen und Festlegen von Steuerelement Eigenschaften. In der folgenden Tabelle werden die Typen von Schiebereglern beschrieben.



| Control    | BESCHREIBUNG                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Schieberegler     | Hat einen Bereich von – 32.768 bis 32.767. Der mischertreibers definiert die Begrenzungen dieses Steuer Elements.                               |
| Schwenken        | Hat einen Bereich von – 32.768 bis 32.767. Der mischertreibers definiert die Begrenzungen dieses Steuer Elements mit 0 als Wert für Midrange. |
| QSound schwenken | Bietet erweiterte Soundsteuerung durch QSound. Dieses Steuerelement hat einen Bereich von – 15 bis 15.                               |



 

 

 
