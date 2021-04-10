---
title: Mixarchitektur
description: Mixarchitektur
ms.assetid: 11d650bf-c258-4818-88b7-9fdc71a8d859
keywords:
- Multimedia-Audiodatei, Mixer-Architektur
- Audioarchitektur, Mixer-Architektur
- Audiomixer, Architektur
- Audiomixer, audiolinien
- audiolinien
- Audiomischungen, Steuerelemente
- Multimedia-Audiosteuer Elemente
- Audiodaten, Mixer-Steuerelemente
- Mixer, audiolinien
- Mixer, Architektur
- Mischungen, Steuerelemente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 447b0cdc44a33237aa7e0c726a5eb533b3bc7d0e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309932"
---
# <a name="mixer-architecture"></a>Mixarchitektur

Das grundlegende Element der mixerarchitektur ist eine *Audiolinie*. Eine Audiolinie besteht aus einem oder mehreren Kanälen von Daten, die aus einer einzelnen Quelle oder einer System Ressource stammen. Beispielsweise verfügt eine Stereo audiozeile über zwei Datenkanäle, aber Sie wird als einzelne Audiolinie betrachtet, da Sie aus einer einzelnen Quelle stammt.

Die mixerarchitektur bietet Routing Dienste zum Verwalten von audiolinien auf einem Computer. Sie können die Routing Dienste verwenden, wenn Sie über ausreichend Hardware Geräte und Software Treiber verfügen. Die Mixer-Architektur ermöglicht es, dass mehrere audioquellzeilen einer einzelnen zielaudiozeile zugeordnet werden.

Jeder Audiolinie können Mixer-Steuerelemente zugeordnet sein. Ein Mixer-Steuerelement kann je nach den Merkmalen der zugeordneten Audiolinie eine beliebige Anzahl von Funktionen (z. b. das Steuerelement Volume) ausführen.

 

 




