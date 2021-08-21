---
description: Die SetDelayTime-Methode legt die Verzögerungszeit für die QuickInfo fest, die dem MSWebDVD-Objekt zugeordnet ist.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: SetDelayTime
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26ebd119f20977c98aa2664518dc2125b7b5c157b44ff53c3a37740bf40a1677
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683740"
---
# <a name="setdelaytime"></a>SetDelayTime

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `SetDelayTime` -Methode legt die Verzögerungszeit für die QuickInfo fest, die dem **MSWebDVD-Objekt zugeordnet** ist.

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*iDelayType*
</dt> <dd>

Gibt den Typ der Verzögerung als ganze Zahl an.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Um die Verzögerungszeit für autopop auf den Standardwert zurückzusetzen, legen Sie *iNewVal* auf -1 fest.                                                                                                                                                                       |
| 0     | Legen Sie fest, wie lange ein QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebundenen Rechtecks eines Tools fest ist.                                                                                                                         |
| 1     | Legen Sie fest, wie lange ein Zeiger innerhalb des umgebundenen Rechtecks eines Tools bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.                                                                                                                    |
| 2     | Legen Sie fest, wie lange es dauert, bis nachfolgende QuickInfo-Fenster angezeigt werden, während der Zeiger von einem Tool zu einem anderen wechselt.                                                                                                                          |
| 3     | Legen Sie alle Verzögerungszeiten auf Standardanteile fest. Die autopop-Zeit ist das Zehnfache der Anfangszeit, und die Zeit für die Neupräsentation ist ein Fünftel der Anfangszeit. Wenn dieses Flag festgelegt ist, verwenden Sie den positiven Wert iNewVal, um die Anfangszeit in Millisekunden anzugeben. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*iNewVal*
</dt> <dd>

Gibt die Verzögerung in Millisekunden als ganze Zahl an.



| Wert                    | BESCHREIBUNG                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Legt die in *iDelayType* angegebene Verzögerung auf den Standardwert fest. |
| beliebiger anderer negativer Wert | Legt alle Verzögerungstypen auf ihren Standardwert fest.                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

 

 



