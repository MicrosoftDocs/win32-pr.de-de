---
description: Die ShowMenu-Methode zeigt das angegebene Menü auf dem Bildschirm an.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: ShowMenu-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb9135e2999675dc46774f15ee79afd835085b40fe210d0ca1cfd173f8a99fc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050510"
---
# <a name="showmenu-method"></a>ShowMenu-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `ShowMenu` -Methode zeigt das angegebene Menü auf dem Bildschirm an.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*iMenuID*
</dt> <dd>

Gibt die Menü-ID als ganze Zahl an.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 2     | Titel (oben) |
| 3     | Root        |
| 4     | Subpicture  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Kapitel     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Hinweise

DVD-Menünamen können etwas verwirrend sein. Das Titelmenü ist ein weiterer Name für das Video-Manager-Menü, das Hauptmenü für den gesamten Datenträger. In der Regel werden alle Videotitelsätze aufgeführt, die auf dem Datenträger verfügbar sind. Das Stammmenü ist das Menü für einen Videotitelsatz, der einen Titel oder eine Gruppe von Titeln enthalten kann. Alle Titel in einem Titelsatz verwenden die gleichen Menüs für Unterbild, Audio und Winkel.

 

 



