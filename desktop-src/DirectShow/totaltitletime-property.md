---
description: Die totaltitletime-Eigenschaft ruft die Gesamt Wiedergabezeit für den aktuellen Titel ab.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: Totaltitletime (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a300a2da8de2698a74e0d72362818bd8a2a5ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103865788"
---
# <a name="totaltitletime-property"></a>Totaltitletime (Eigenschaft)

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die- `TotalTitleTime` Eigenschaft ruft die Gesamt Wiedergabezeit für den aktuellen Titel ab.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Rückgabewert

Gibt die Gesamt Wiedergabezeit des aktuellen Titels als Zeichenfolge im Format "hh: mm: SS: FF" zurück.

## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft ist schreibgeschützt und weist keinen Standardwert auf. Die zurückgegebene Zeichenfolge hat eine Länge von 11 Zeichen im Format "hh: mm: SS: FF" (Stunden, Minuten, Sekunden, Rahmen).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Playattime**](playattime-method.md)
</dt> <dt>

[**Playattimeingetitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



