---
description: Die TotalTitleTime-Eigenschaft ruft die Gesamtwiedergabezeit für den aktuellen Titel ab.
ms.assetid: b05bb76b-d4ba-42e6-92ea-8e48f4c8f409
title: TotalTitleTime-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fd809391394dc661745717ce7d173ad548dfd4d01206c07293024dc8e44a478
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119650850"
---
# <a name="totaltitletime-property"></a>TotalTitleTime-Eigenschaft

> [!Note]  
> Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar. Es kann in nachfolgenden Versionen geändert oder entfernt werden.

 

Die `TotalTitleTime` -Eigenschaft ruft die Gesamtwiedergabezeit für den aktuellen Titel ab.

``` syntax
[ sTotalTime = ] MSWebDVD.TotalTitleTime
```

## <a name="return-value"></a>Rückgabewert

Gibt die Gesamtspielzeit des aktuellen Titels als Zeichenfolge im Format "hh:mm:ss:ff" zurück.

## <a name="remarks"></a>Hinweise

Diese Eigenschaft ist schreibgeschützt und hat keinen Standardwert. Die zurückgegebene Zeichenfolge ist 11 Zeichen lang im Format "hh:mm:ss:ff" (Stunden, Minuten, Sekunden, Frames).

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**PlayAtTime**](playattime-method.md)
</dt> <dt>

[**PlayAtTimeInTitle**](playattimeintitle-method.md)
</dt> </dl>

 

 



