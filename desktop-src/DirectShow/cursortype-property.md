---
description: Die CursorType-Eigenschaft legt den aktuellen Cursortyp fest oder ruft ihn ab.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Cursor Type (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860286"
---
# <a name="cursortype-property"></a>Cursor Type (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `CursorType` Eigenschaft legt den aktuellen Cursortyp fest oder ruft ihn ab.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Integer-Wert zurück, der den Cursortyp darstellt.

## <a name="remarks"></a>Bemerkungen

Folgende Werte sind für diese Eigenschaft möglich:



| Wert | BESCHREIBUNG |
|-------|-------------|
| 0     | Pfeil       |
| 1     | Vergrößern     |
| 2     | Verkleinern    |
| 3     | Linken        |
| -1    | Keine        |



 

Diese Eigenschaft ist Lese-/Schreibzugriff mit dem Standardwert 0 (null). Wenn das Bild vergrößert wird, wird die Anwendung durch die Festlegung `CursorType` auf **Hand** (0x3) in den Zieh Modus versetzt, sodass der Benutzer das Bild innerhalb des Videoanzeige Bereichs verschieben kann.

 

 



