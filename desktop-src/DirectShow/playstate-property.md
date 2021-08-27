---
description: Die PlayState-Eigenschaft ruft den aktuellen Zustand des MSWebDVD-Objekts ab.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: PlayState-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b66ae0ddfb1a8ceb296ec647a0149a42de68f635ffd198d6ba6609ff11e4888
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102350"
---
# <a name="playstate-property"></a>PlayState-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `PlayState` -Eigenschaft ruft den aktuellen Zustand des **MSWebDVD-Objekts** ab.

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Rückgabewert

Gibt einen Ganzzahlwert zurück, der den aktuellen Status des DVD-Navigators darstellt.



| Rückgabecode | Beschreibung   |
|-------------|---------------|
| –2          | Nicht definiert     |
| –1          | Uninitialized |
| 0           | Beendet       |
| 1           | Angehalten        |
| 2           | Wird ausgeführt       |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert.

Das **MSWebDVD-Objekt** steuert den Filter DirectShow DVD Navigator, der die eigentliche Arbeit der DVD-Navigation übernimmt. Es handelt sich tatsächlich um den Zustand des DVD-Navigators, auf den diese Eigenschaft verweist. Der DVD-Navigator kann sich in einem der folgenden Zustände wie oben beschrieben in einem von mehreren Zuzuständen befingen. Die -Eigenschaft kann als Diagnosetool nützlich sein, aber im Allgemeinen sollte es keinen Grund für eine Skriptanwendung geben, den Status des `PlayState` DVD-Navigators zu überwachen.

 

 



