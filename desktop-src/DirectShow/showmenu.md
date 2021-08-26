---
description: Das ShowMenu-Ereignis wird gesendet, wenn der Datenträger die Anzeige eines Menüs aktiviert oder deaktiviert.
ms.assetid: 78fd0b80-baec-4174-9c55-f061627c3599
title: ShowMenu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56eb6767a8144bab3de832570db63bc4e2cdc012490f776f52b6c8977cce9d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050450"
---
# <a name="showmenu"></a>ShowMenu

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das `ShowMenu` Ereignis wird gesendet, wenn der Datenträger die Anzeige eines Menüs aktiviert oder deaktiviert.

``` syntax
ShowMenu(DVDMenuIDConstants, bEnabled)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="DVDMenuIDConstants"></span><span id="dvdmenuidconstants"></span><span id="DVDMENUIDCONSTANTS"></span>*DVDMenuIDConstants*
</dt> <dd>

Gibt an, welches Menü als Zahlenwert aktiviert oder deaktiviert wurde.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 2     | Titel       |
| 3     | Root        |
| 4     | Subpicture  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Kapitel     |



 

</dd> <dt>

<span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*
</dt> <dd>

Gibt an, ob der Vorgang als boolescher Wert aktiviert oder deaktiviert ist.

</dd> </dl>

 

 



