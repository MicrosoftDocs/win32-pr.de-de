---
title: Zahlen (Windows Multimedia)
description: Zahlen
ms.assetid: d416c4c2-a3e1-45a2-9ae1-82050a5e471b
keywords:
- Audiomischungen, Steuerelemente
- Audiomixer, Zahlen
- Mischungen, Steuerelemente
- Mixer, Zahlen
- Zahlen Steuerelemente
- MIXERCONTROLDETAILS_SIGNED Struktur
- MIXERCONTROLDETAILS_UNSIGNED Struktur
- Dezibelskala-Steuerelement
- Prozent Steuerelement
- signiertes Steuerelement
- nicht signiertes Steuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02c4ffd40f1058fae51af3798135840394be918
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "104102671"
---
# <a name="numbers-windows-multimedia"></a>Zahlen (Windows Multimedia)

Die Anzahl der Steuerelemente ermöglicht dem Benutzer die Eingabe von numerischen Daten, die einer Zeile zugeordnet sind. Die numerischen Daten werden als ganze Zahlen mit Vorzeichen, ganze Zahlen ohne Vorzeichen oder ganzzahlige Dezimalwerte ausgedrückt. Diese Steuerelemente verwenden die " [**mixercontroldetails \_ Signed**](/previous-versions//dd757297(v=vs.85)) "-und " [**mixercontroldetails \_**](/previous-versions//dd757298(v=vs.85)) "-Struktur ohne Vorzeichen zum Abrufen und Festlegen von Steuerelement Eigenschaften. In der folgenden Tabelle werden die Typen von Zahlen Steuerelementen beschrieben.



| Control  | BESCHREIBUNG                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| Signiert   | Ermöglicht ganzzahlige Werte, die im Bereich von – 231 bis (231 – 1) eingegeben werden.                                                               |
| Ohne Vorzeichen | Ermöglicht ganzzahlige Werte, die im Bereich von 0 bis (232 – 1) eingegeben werden.                                                                   |
| Dezibelskala  | Ermöglicht das Eingeben von ganzzahligen Dezibelskala-Werten in Zehntel Dezimalstellen. Der Wertebereich für dieses Steuerelement ist – 32.768 bis 32.767. |
| Percent  | Ermöglicht die Eingabe von Werten als Prozentsätze.                                                                                         |



 

 

 
