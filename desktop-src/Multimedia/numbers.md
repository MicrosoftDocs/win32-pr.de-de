---
title: Zahlen (Windows Multimedia)
description: Zahlen
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- Audiomixer, Steuerelemente
- Audiomixer,Zahlen
- Mixer, Steuerelemente
- Mixer, Zahlen
- Zahlensteuerelemente
- MIXERCONTROLDETAILS_SIGNED-Struktur
- MIXERCONTROLDETAILS_UNSIGNED-Struktur
- decbel-Steuerelement
- Prozentsteuerung
- Signiertes Steuerelement
- Steuerelement ohne Vorzeichen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21c9e1bacdea3f52129d78eea2f0bc7134df08b7077c83510bd8de824777e524
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806620"
---
# <a name="numbers-windows-multimedia"></a>Zahlen (Windows Multimedia)

Mit den Zahlensteuerelementen kann der Benutzer numerische Daten eingeben, die einer Zeile zugeordnet sind. Die numerischen Daten werden als ganze Zahlen mit Vorzeichen, ganze Zahlen ohne Vorzeichen oder ganzzahlige Dezibelwerte ausgedrückt. Diese Steuerelemente verwenden die [**STRUKTUREN MIXERCONTROLDETAILS \_ SIGNED und**](/previous-versions//dd757297(v=vs.85)) [**MIXERCONTROLDETAILS \_ UNSIGNED**](/previous-versions//dd757298(v=vs.85)) zum Abrufen und Festlegen von Steuerelementeigenschaften. In der folgenden Tabelle werden die Typen von Zahlensteuerelementen beschrieben.



| Control  | Beschreibung                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Signiert   | Lässt ganzzahlige Werte zu, die im Bereich von – 231 bis (231 –1) eingegeben werden.                                                               |
| Ohne Vorzeichen | Lässt ganzzahlige Werte zu, die im Bereich von 0 bis (232 –1) eingegeben werden.                                                                   |
| Dezibel  | Ermöglicht die Eingabe ganzzahliger Dezibelwerte in Zehnteln von Dezibeln. Der Wertebereich für dieses Steuerelement ist –32.768 bis 32.767. |
| Percent  | Ermöglicht die Eingabe von Werten als Prozentsätze.                                                                                         |



 

 

 
