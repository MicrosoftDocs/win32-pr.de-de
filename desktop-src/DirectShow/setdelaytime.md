---
description: Die setdelta-Time-Methode legt die Verzögerungszeit für die dem mswebdvd-Objekt zugeordnete QuickInfo fest.
ms.assetid: bb1086e1-57e2-495a-9b7b-2d349a516e72
title: Setdelta-Zeit
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c7653777be7e6603494d9ba04a671ed46d3d949
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480587"
---
# <a name="setdelaytime"></a>Setdelta-Zeit

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `SetDelayTime` Methode legt die Verzögerungszeit für die dem **mswebdvd** -Objekt zugeordnete QuickInfo fest.

``` syntax
MSWebDVD.SetDelayTime(iDelayType, iNewVal)
```

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="iDelayType"></span><span id="idelaytype"></span><span id="IDELAYTYPE"></span>*idelta-Type*
</dt> <dd>

Gibt den Typ der Verzögerung als Ganzzahl an.



| Wert | BESCHREIBUNG                                                                                                                                                                                                                                      |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -1    | Um die Zeit für die autopop-Verzögerung auf den Standardwert zurückzusetzen, legen Sie " *inewval* " auf-1 fest.                                                                                                                                                                       |
| 0     | Legen Sie die Zeitspanne fest, die ein QuickInfo-Fenster sichtbar bleibt, wenn der Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär ist.                                                                                                                         |
| 1     | Legen Sie den Zeitraum fest, in dem ein Zeiger innerhalb des umgebenden Rechtecks eines Tools stationär bleiben muss, bevor das QuickInfo-Fenster angezeigt wird.                                                                                                                    |
| 2     | Legen Sie die Zeitspanne fest, die für nachfolgende QuickInfo-Fenster benötigt wird, wenn der Zeiger von einem Tool zu einem anderen verschoben wird.                                                                                                                          |
| 3     | Legen Sie alle Verzögerungszeiten auf Standard Proportionen fest. Die autopop-Zeit ist zehnmal so oft wie die Anfangszeit, und die reshow-Zeit ist ein Fünftel der Anfangszeit. Wenn dieses Flag festgelegt ist, geben Sie mit einem positiven Wert von inewval die anfängliche Zeit in Millisekunden an. |



 

</dd> <dt>

<span id="iNewVal"></span><span id="inewval"></span><span id="INEWVAL"></span>*inewval*
</dt> <dd>

Gibt die Verzögerung (in Millisekunden) als ganze Zahl an.



| Wert                    | BESCHREIBUNG                                                   |
|--------------------------|---------------------------------------------------------------|
| -1                       | Legt die in *idelta Type* angegebene Verzögerung auf den Standardwert fest. |
| ein beliebiger anderer negativer Wert | Legt alle Verzögerungs Typen auf ihren Standardwert fest.                  |



 

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Kein Rückgabewert.

 

 



