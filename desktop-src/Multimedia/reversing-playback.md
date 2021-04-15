---
title: Umkehren der Wiedergabe
description: Umkehren der Wiedergabe
ms.assetid: cb7c1293-42d7-4c74-b9e6-cc8899ca7c54
keywords:
- Mciwndplayreverse-Makro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a708915679f75bfe478c160d71d35b0bcfa48a23
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388274"
---
# <a name="reversing-playback"></a>Umkehren der Wiedergabe

Einige Geräte unterstützen die Wiedergabe in umgekehrter Richtung. Sie können den Inhalt eines solchen Geräts in umgekehrter Richtung wiedergeben, indem Sie das [**mciwndplayreverse**](/windows/desktop/api/Vfw/nf-vfw-mciwndplayreverse) -Makro verwenden. Dieses Makro definiert den Wiedergabe Bereich von der aktuellen Wiedergabe Position bis zum Anfang des Inhalts. Das Digital-Video-Gerät, mciavi. DRV kann rückwärts abgespielt werden. Geräte, die nicht rückwärts wiedergegeben werden können, z. b. CD-Audiodaten, können eine Fehlermeldung ausgeben, wenn **mciwndplayreverse** aufgerufen wird.

 

 




