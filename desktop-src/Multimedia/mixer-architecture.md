---
title: Mixer Architektur
description: Mixer Architektur
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- Multimediaaudio, Mixerarchitektur
- Audio, Mixerarchitektur
- Audiomixer,Architektur
- Audiomixer, Audiolinien
- Audiozeilen
- Audiomixer, Steuerelemente
- Multimediaaudio, Mixersteuerelemente
- Audio,Mixer-Steuerelemente
- Mixer, Audiolinien
- Mixer, Architektur
- Mixer, Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3f435396dd2a8d5983f596628711dfd01afe7111e75af1dc2060f5c6c4ef0a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065610"
---
# <a name="mixer-architecture"></a>Mixer Architektur

Das grundlegende Element der Mixerarchitektur ist eine *Audiolinie.* Eine Audiozeile besteht aus einem oder mehreren Datenkanälen, die aus einer einzelnen Quelle oder einer Systemressource stammen. Beispielsweise verfügt eine Stereo-Audiolinie über zwei Datenkanäle, wird aber als einzelne Audiolinie betrachtet, da sie aus einer einzelnen Quelle stammt.

Die Mixerarchitektur bietet Routingdienste zum Verwalten von Audioleitungen auf einem Computer. Sie können die Routingdienste verwenden, wenn sie über geeignete Hardwaregeräte und Softwaretreiber verfügen. Die Mixerarchitektur ermöglicht die Zuordnung mehrerer Audioquellenlinien zu einer einzelnen Zielaudiolinie.

Jeder Audiozeile können Mixer-Steuerelemente zugeordnet sein. Ein Mixer-Steuerelement kann abhängig von den Merkmalen der zugeordneten Audiolinie eine beliebige Anzahl von Funktionen (z. B. Die Lautstärke des Steuerelements) ausführen.

 

 




