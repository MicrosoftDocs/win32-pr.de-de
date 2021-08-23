---
description: Die CurrentDomain-Eigenschaft ruft die DVD-Domäne ab, in der sich das MSWebDVD-Objekt befindet.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf022d44cc3580a4d5208c5bc96413dfa445b0f2fcbf74eeb938ee77fa0677bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953389"
---
# <a name="currentdomain-property"></a>CurrentDomain-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `CurrentDomain` -Eigenschaft ruft die DVD-Domäne ab, in der sich das MSWebDVD-Objekt befindet.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der die aktuelle Domäne darstellt.

## <a name="remarks"></a>Hinweise

Die möglichen Werte der -Eigenschaft sind:



| Wert | BESCHREIBUNG          |
|-------|----------------------|
| 1     | Erste Wiedergabe           |
| 2     | Video-Manager-Menü   |
| 3     | Menü "Videotitelsatz" |
| 4     | Titel                |
| 5     | Beenden                 |



 

Rufen Sie diese Methode auf, um sicherzustellen, dass sich der DVD-Navigator in einer gültigen Domäne für die Methode befindet, die Sie aufrufen möchten. Überprüfen Sie beispielsweise vor dem Aufrufen von [**PlayTitle**](playtitle-method.md)die `CurrentDomain` -Eigenschaft, um sicherzustellen, dass sich der DVD-Navigator nicht in der Domäne Stop oder First Play befindet.

 

 



