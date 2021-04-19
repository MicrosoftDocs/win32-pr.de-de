---
description: Die anglesavailable-Eigenschaft ruft die Anzahl der derzeit verfügbaren Winkel ab.
ms.assetid: 1e2635d4-63f1-4c3d-a034-437489289bd7
title: Anglesavailable (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b9d27806b314d89c68fcc4d1476a9918cd4446
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346608"
---
# <a name="anglesavailable-property"></a>Anglesavailable (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `AnglesAvailable` Eigenschaft ruft die Anzahl der derzeit verfügbaren Winkel ab.

``` syntax
[ iAngles = ] MSWebDVD.AnglesAvailable
```

## <a name="return-value"></a>Rückgabewert

Gibt einen ganzzahligen Wert zwischen 1 und 9 zurück, der die Anzahl der derzeit verfügbaren Winkel darstellt. Wenn


```
iAngles
```



= 1, an der aktuellen Position ist kein Winkel Block vorhanden.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Ein *Winkel Block* ist ein Video Segment, das aus mehr als einem Kamerawinkel gedreht wurde. Ein Winkel Block kann bis zu neun Winkel aufweisen, nummeriert von 1 bis 9. Wenn der DVD-Navigator zum ersten Mal einen Winkel Block eingibt, sendet er ihrer Anwendung eine \_ \_ Verfügbare Ereignis Benachrichtigung für die EC-DVD-Winkel \_ mit der Anzahl von Winkeln in *lParam1*. Ein Datenträger kann so erstellt werden, dass automatisch ein Menü für verfügbare Winkel angezeigt wird, wenn es in einen Winkel Block wechselt. im Allgemeinen muss eine Anwendung jedoch die Anzahl der verfügbaren Winkel ermitteln und dem Benutzer eine Möglichkeit zur Auswahl bieten.

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Currentangle**](currentangle-property.md)
</dt> </dl>

 

 



