---
title: Schieberegler (Windows Multimedia)
description: Schieberegler
ms.assetid: cfd82672-5b22-4b59-82b5-15ca68a451fc
keywords:
- Audiomixer, Steuerelemente
- Audiomixer, Schieberegler
- Mixer, Steuerelemente
- Mixer, Schieberegler
- Schieberegler-Steuerelemente
- MIXERCONTROLDETAILS_SIGNED Struktur
- Schwenken-Steuerelement
- QSound-Schwenksteuerelement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e902e3ead0416cb4b2a7d56d289f91779563109cb9494784635affc75069dfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805350"
---
# <a name="sliders-windows-multimedia"></a>Schieberegler (Windows Multimedia)

Die Schieberegler-Steuerelemente sind in der Regel horizontale Steuerelemente, die nach links oder rechts angepasst werden können. Diese Steuerelemente verwenden die [**MIXERCONTROLDETAILS \_ SIGNED-Struktur,**](/previous-versions//dd757297(v=vs.85)) um Steuerelementeigenschaften abzurufen und festzulegen. In der folgenden Tabelle werden die Typen von Schiebereglern beschrieben.



| Control    | Beschreibung                                                                                                               |
|------------|---------------------------------------------------------------------------------------------------------------------------|
| Schieberegler     | Hat einen Bereich von –32.768 bis 32.767. Der Mixertreiber definiert die Grenzwerte dieses Steuerelements.                               |
| Schwenken        | Hat einen Bereich von –32.768 bis 32.767. Der Mixertreiber definiert die Grenzwerte dieses Steuerelements, wobei 0 als Mittelbereichswert festgelegt ist. |
| QSound Pan | Stellt erweitertes Soundsteuerelement über QSound bereit. Dieses Steuerelement hat einen Bereich von –15 bis 15.                               |



 

 

 
