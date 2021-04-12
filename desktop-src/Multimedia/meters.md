---
title: Meter
description: Meter
ms.assetid: 11a98d2a-7cdd-4249-bba9-7edc51d7f8b0
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Meter
- Mischungen, Steuerelemente
- Mixer, Meter
- Mess Steuerelemente
- MIXERCONTROLDETAILS_BOOLEAN Struktur
- MIXERCONTROLDETAILS_SIGNED Struktur
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Boolesches Steuerelement
- Spitzen Kontrolle
- signiertes Steuerelement
- nicht signiertes Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f36f1bebfca22b963e5c1eb6fede3f2786b35199
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104473116"
---
# <a name="meters"></a>Meter

Die Mess Steuerelemente messen die Daten, die über eine audiozeile übergeben werden. Diese Steuerelemente verwenden den [**mixercontroldetails- \_ booleschen**](/previous-versions//dd757295(v=vs.85))Wert, [**mixercontroldetails \_ signiert**](/previous-versions//dd757297(v=vs.85))und [**mixercontroldetails \_ nicht signierte**](/previous-versions//dd757298(v=vs.85)) Strukturen zum Abrufen und Festlegen von Steuerelement Eigenschaften. In der folgenden Tabelle werden die Typen von Zählern beschrieben.



| Control  | Beschreibung                                                                                                                                            |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Boolesch  | Misst, ob ein ganzzahliger Wert false/Off (null) oder true/on (ungleich null) ist.                                                                            |
| Peak     | Misst die Ablenkung von 0 in der positiven und negativen Richtung. Der Bereich der ganzzahligen Werte für die Spitzen Meter beträgt – 32.768 bis 32.767. |
| Signiert   | Misst ganzzahlige Werte im Bereich von – 231 bis (231 – 1). Der mischertreibers definiert die Grenzwerte dieser Verbrauchseinheit.                                     |
| Ohne Vorzeichen | Misst ganzzahlige Werte im Bereich von 0 bis (232 – 1). Der mischertreibers definiert die Grenzwerte dieser Verbrauchseinheit.                                        |



 

 

 