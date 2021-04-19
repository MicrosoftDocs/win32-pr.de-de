---
description: Das updateoverlay-Ereignis wird gesendet, wenn die über Lagerungs Oberfläche verschoben oder die Größe geändert wurde oder der Farbschlüssel geändert wurde.
ms.assetid: 692cbd26-b7b3-4fa3-9157-ca96a33e3a1e
title: Updateoverlay (ddraw. h)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2152e1f58ba161dc8dc3e04c908aaf037f1eed2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372497"
---
# <a name="updateoverlay"></a>Updateoverlay

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Das **updateoverlay** -Ereignis wird gesendet, wenn die über Lagerungs Oberfläche verschoben oder die Größe geändert wurde oder der Farbschlüssel geändert wurde.

``` syntax
UpdateOverlay()
```

## <a name="remarks"></a>Bemerkungen

Anwendungen sollten sich nie Gedanken darüber machen, dass die Größe der Überlagerungs Oberfläche geändert oder verschoben wird. Alles wird intern behandelt. Dieses Ereignis wird jedoch auch gesendet, wenn sich der Farbschlüssel ändert. Dies bedeutet Folgendes: Wenn eine Anwendung mswebdvd als fensterloses Steuerelement und unverankerte Schaltflächen oben auf der Video Oberfläche im Vollbildmodus anzeigt, sollte Sie auf dieses Ereignis reagieren, indem der neue Wert der **Colorkey** -Eigenschaft abgerufen wird, damit die Schaltflächen ordnungsgemäß gezeichnet werden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Ddraw. h</dt> </dl> |



 

 




