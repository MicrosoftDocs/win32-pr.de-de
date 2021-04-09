---
description: Das showmenu-Ereignis wird gesendet, wenn der Disc die Anzeige eines Menüs aktiviert oder deaktiviert.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: Showmenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53b78c2751a270b56f95bac223ab80b2e2143b04
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103957961"
---
# <a name="showmenu"></a>Showmenu

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das `ShowMenu` Ereignis wird gesendet, wenn der Disc die Anzeige eines Menüs aktiviert oder deaktiviert.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*Dvdmenuidconstants*
</dt> <dd>

Gibt an, welches Menü als Zahlenwert aktiviert oder deaktiviert wurde.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 2     | Titel       |
| 3     | Root        |
| 4     | Untertitel  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Kapitel     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*benabled*
</dt> <dd>

Gibt an, ob der Vorgang als boolescher Wert aktiviert oder deaktiviert ist.

</dd> </dl>

 

 



