---
title: Der Volumeskalar
description: Der Volumeskalar
ms.assetid: a9fe2c35-9109-4697-9ffa-a31debbe72c8
keywords:
- Instrument Digital Interface (KEYBOARD), Volumenskalar
- KEYBOARD (Keyboard Instrument Digital Interface), Volumenskalar
- MAPPer, Volumeskalar
- Volumeskalar
- MAPPer, Anpassen von Ausgabeebenen
- Anpassen von Ausgabeebenen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7710e8e3ceb8079f04ac97bfcce8c91c6c74aa60452c220166e358a87939848
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119804945"
---
# <a name="the-volume-scalar"></a>Der Volumeskalar

Der Zweck des Volumeskalars besteht im Zulassen von Anpassungen zwischen den relativen Ausgabeebenen verschiedener Patches auf einem Synthesizer. Wenn das Patchen eines Synthetizers beispielsweise im Vergleich zu seinem Patch zu laut ist, können Sie die Setupzuordnung ändern, um das Volume der Skala herunter- oder hochskalieren zu können.

Der Volumeskalar gibt einen Prozentwert für das Ändern aller NACHRICHTEN des HAUPT-Volumecontrollers an, die auf eine zugeordnete Programmänderungsmeldung folgen. Wenn der Volumeskalarwert z. B. 50 % beträgt, ändert der MAPPer DEST-Mappers DIE Haupt-Volumecontroller-Nachrichten, wie in der folgenden Abbildung dargestellt.

![Abbildung des Mappers "mapper"](images/mmap-a04.gif)

 

 




