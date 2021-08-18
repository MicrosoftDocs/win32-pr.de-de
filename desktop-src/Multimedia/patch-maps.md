---
title: Patch Karten
description: Patch Karten
ms.assetid: d0c91001-d19d-439c-9773-78d6228a6642
keywords:
- Instruments Instrument Digital Interface (MAPPer)
- KEYBOARD (Instrument Digital Interface), MAPPER
- MAPPer, Patchzuordnungen
- Patchzuordnungen
- PROGRAMMÄNDERUNGSMELDUNGEN
- VOLUMES-Controllernachrichten
- Programmänderungsmeldungen
- Volumecontrollernachrichten
- MAPPer,Programmänderungsmeldungen
- mapper,volume-controller messages
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb32f60ac486d7e8812b5cf71febe3794ae37d650bc795baa4c06ffb48ce5f42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038264"
---
# <a name="patch-maps"></a>Patch Karten

Jedem Kanalzuordnungseintrag kann eine Patchzuordnung zugeordnet sein. Patchzuordnungen wirken sich auf nachrichtenbasierte Programmänderung und Volumecontroller aus. Programmänderungsmeldungen informieren einen Synthesizer, den Instrumentklang (Patch) für einen angegebenen Kanal zu ändern. Volumecontrollernachrichten legen das Volume für einen Kanal fest.

Eine Patchübersicht verfügt über eine Übersetzungstabelle mit einem Eintrag für jeden der 128 Programmänderungswerte. Jede Patch map gibt Folgendes an:

-   Ein Zielprogrammänderungswert.
-   Ein Volumeskalar. (Weitere Informationen finden Sie unter [The Volume Scalar](the-volume-scalar.md).)
-   Eine optionale Schlüsselzuordnung. (Weitere Informationen finden Sie unter [Key Karten](key-maps.md).)

Wenn Programmänderungsmeldungen vom MAPPer des PROGRAMMS empfangen werden, wird der Programmänderungswert des Zielprogramms durch den Programmänderungswert in der Nachricht ersetzt. Wenn der Zielwert für die Programmänderung 16 z. B. 18 ist, ändert der MAPPer des PROGRAMMS die PROGRAMMÄNDERUNGsmeldung des PROGRAMMS, wie in der folgenden Abbildung dargestellt.

![Abbildung des Mappers "mapper"](images/mmap-a03.gif)

 

 




