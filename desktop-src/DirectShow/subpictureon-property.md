---
description: Die SubpictureOn-Eigenschaft legt den aktuellen Unterbildzustand fest oder ruft den aktuellen Unterbildzustand ab (ein oder aus).
ms.assetid: fa4500bc-48b4-41ed-8b88-0011a0e51c6f
title: SubpictureOn-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 692df6b69bc960562e9acd223a0e4e156fe00de2206146f609ba15d550b7a961
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951769"
---
# <a name="subpictureon-property"></a>SubpictureOn-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SubpictureOn` -Eigenschaft legt den aktuellen Unterbildzustand fest oder ruft sie ab (ein oder aus).

``` syntax
[ bState = ] MSWebDVD.SubpictureOn
```

## <a name="return-value"></a>Rückgabewert

Gibt einen booleschen Wert zurück, der angibt, ob das Unterbild angezeigt wird.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wirkt sich nicht auf die Anzeige von Untertiteln aus. Untertitel werden in den Videostream eingebettet. DVD-Unterbilder werden in einem separaten Stream übertragen.

Wenn der Unterbilddatenstrom mit [**CurrentSubpictureStream**](currentsubpicturestream-property.md)geändert wird, wird die `SubpictureOn` -Eigenschaft auf **True** umgeschaltet.

Diese Eigenschaft ist lese-/schreibgeschützt und hat den Standardwert false.

 

 



