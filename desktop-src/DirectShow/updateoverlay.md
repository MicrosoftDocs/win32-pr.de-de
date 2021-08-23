---
description: Das UpdateOverlay-Ereignis wird gesendet, wenn die Überlagerungsoberfläche verschoben oder die Größe geändert oder der Farbschlüssel geändert wurde.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: UpdateOverlay (Ddraw.h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 205b4ca002ec06862b006dc3e3b6facec2f5cb7f0ffb92f3e5a65bc2bb0a161c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650824"
---
# <a name="updateoverlay"></a>UpdateOverlay

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das **UpdateOverlay-Ereignis** wird gesendet, wenn die Überlagerungsoberfläche verschoben oder ihre Größe geändert wurde oder der Farbschlüssel geändert wurde.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Hinweise

Anwendungen sollten sich keine Gedanken darüber machen, dass die Größe der Überlagerungsoberfläche geändert oder verschoben wird. Dies alles wird intern behandelt. Dieses Ereignis wird jedoch auch gesendet, wenn sich der Farbschlüssel ändert. Das bedeutet: Wenn eine Anwendung MSWebDVD als fensterloses Steuerelement hostet und unverankerte Schaltflächen auf der Videooberfläche im Vollbildmodus anzeigt, sollte sie auf dieses Ereignis reagieren, indem sie den neuen Wert der **ColorKey-Eigenschaft** erhält, damit sie die Schaltflächen ordnungsgemäß zeichnen kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ddraw.h</dt> </dl> |



 

 




