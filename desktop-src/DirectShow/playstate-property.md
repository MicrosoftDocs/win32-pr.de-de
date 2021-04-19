---
description: Die playstate-Eigenschaft ruft den aktuellen Zustand des mswebdvd-Objekts ab.
ms.assetid: ffe71c3f-f8c2-45cc-84bf-e937cfbbe7b9
title: Playstate (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d8c699ce3f232f9afc14472f0308fa65adc6abb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346818"
---
# <a name="playstate-property"></a>Playstate (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `PlayState` Eigenschaft ruft den aktuellen Zustand des **mswebdvd** -Objekts ab.

``` syntax
[ iState = ] MSWebDVD.PlayState
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zurück, der den aktuellen Zustand des DVD-Navigators darstellt.



| Rückgabecode | Beschreibung   |
|-------------|---------------|
| -2          | Nicht definiert     |
| -1          | Uninitialized |
| 0           | Beendet       |
| 1           | Angehalten        |
| 2           | Wird ausgeführt       |



 

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf.

Das **mswebdvd** -Objekt steuert den DirectShow-DVD-Navigator-Filter, der die eigentliche Arbeit der DVD-Navigation übernimmt. Es handelt sich tatsächlich um den Status des DVD-Navigators, auf den diese Eigenschaft verweist. Der DVD-Navigator kann einen von mehreren Zuständen aufweisen, wie oben beschrieben. Die- `PlayState` Eigenschaft kann als Diagnosetool nützlich sein, aber im Allgemeinen sollte es für eine Skript Anwendung keinen Grund geben, den Status des DVD-Navigators zu überwachen.

 

 



