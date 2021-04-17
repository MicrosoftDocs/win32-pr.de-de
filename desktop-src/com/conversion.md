---
title: Konvertierung
description: Wird vom Dialogfeld konvertieren verwendet, um die Formate zu ermitteln, die eine Anwendung lesen und schreiben kann.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- COM für Konvertierungs Registrierungsschlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce7f3a87594513c37a558d21fb7d001fc393763d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104516071"
---
# <a name="conversion"></a>Konvertierung

Wird vom Dialogfeld **konvertieren** verwendet, um die Formate zu ermitteln, die eine Anwendung lesen und schreiben kann.

## <a name="registry-entry"></a>Registrierungseintrag

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Conversion
         Readable
            Main = rformat, ...
         ReadWritable
            Main = rwformat, ...
```

## <a name="remarks"></a>Bemerkungen

Die Konvertierungs Informationen werden im Dialogfeld **konvertieren** verwendet, um zu bestimmen, welche Formate eine Anwendung lesen und schreiben kann. Ein durch Trennzeichen getrenntes Dateiformat wird durch eine Zahl angegeben, wenn es sich um eines der in Windows. h definierten Zwischenablage Formate handelt. Eine Zeichenfolge gibt an, dass das Format in Windows. h (privat) nicht definiert ist. In diesem Fall ist das lesbare und beschreibbare Format CF \_ Umriss (privat).

Der *rformat* -Wert gibt das Dateiformat an, das von einer Anwendung gelesen werden kann (Konvertieren von).

Der Wert *rwformat* gibt das Dateiformat an, das von einer Anwendung gelesen und geschrieben werden kann (aktivieren als).

 

 




