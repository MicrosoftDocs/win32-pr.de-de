---
description: Die showmenu-Methode zeigt das angegebene Menü auf dem Bildschirm an.
ms.assetid: 971c5bc3-a327-4840-8f3c-9a6573204ffb
title: Showmenu-Methode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c64b2a08c8881001cc47c972ad8cc865af8a174
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746785"
---
# <a name="showmenu-method"></a>Showmenu-Methode

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `ShowMenu` Methode zeigt das angegebene Menü auf dem Bildschirm an.

``` syntax
MSWebDVD.ShowMenu(iMenuID)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iMenuID"></span><span id="imenuid"></span><span id="IMENUID"></span>*imumuid*
</dt> <dd>

Gibt die Menü-ID als Ganzzahl an.



| Wert | BESCHREIBUNG |
|-------|-------------|
| 2     | Titel (oben) |
| 3     | Root        |
| 4     | Untertitel  |
| 5     | Audio       |
| 6     | Angle       |
| 7     | Kapitel     |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

## <a name="remarks"></a>Bemerkungen

DVD-Menü Namen können etwas verwirrend sein. Das Menü Titel ist ein anderer Name für das Menü Video-Manager, das Hauptmenü für die gesamte CD. im Allgemeinen werden alle auf der Festplatte verfügbaren Videotitel Sätze aufgelistet. Das Stamm Menü ist das Menü für einen Videotitel Satz, der einen Titel oder eine Gruppe von Titeln enthalten kann. Alle Titel in einem Titel Satz verwenden dieselben unter Bilder, Audiodateien und Winkel Menüs.

 

 



