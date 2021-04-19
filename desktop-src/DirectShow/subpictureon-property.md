---
description: Die subpictureon-Eigenschaft legt den aktuellen Teil Bild Zustand fest oder ruft ihn ab (ein oder aus).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: Subpictureon (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83376793f20468bda88edd8897e8c956094c1a88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369818"
---
# <a name="subpictureon-property"></a>Subpictureon (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SubpictureOn` Eigenschaft legt den aktuellen Teil Bild Zustand fest oder ruft ihn ab (ein oder aus).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob das untergeordnete Bild angezeigt wird.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wirkt sich nicht auf die Anzeige von Untertiteln aus. Untertitel werden in den Videostream eingebettet. DVD-Teilbilder werden in einem separaten Stream transportiert.

Wenn der subbildstream mithilfe von [**currentsubpicturestream**](currentsubpicturestream-property.md)geändert wird, wird die `SubpictureOn` Eigenschaft in **true** geändert.

Diese Eigenschaft ist Lese-/Schreibzugriff und hat den Standardwert false.

 

 



