---
title: Konvertierung
description: Wird vom Dialogfeld Konvertieren verwendet, um die Formate zu bestimmen, die eine Anwendung lesen und schreiben kann.
ms.assetid: ff12c4b3-9548-4135-aaf4-d8b49f9aed41
keywords:
- Konvertierungsregistrierungsschlüssel COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272090fb48b214daecd6350e6966350861366341fae055298a2fb2c90c9fb983
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119993482"
---
# <a name="conversion"></a>Konvertierung

Wird vom Dialogfeld **Konvertieren** verwendet, um die Formate zu bestimmen, die eine Anwendung lesen und schreiben kann.

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

## <a name="remarks"></a>Hinweise

Konvertierungsinformationen werden im Dialogfeld **Konvertieren** verwendet, um zu bestimmen, welche Formate eine Anwendung lesen und schreiben kann. Ein durch Trennzeichen getrenntes Dateiformat wird durch eine Zahl angegeben, wenn es eines der in "Windows.h" definierten Zwischenablageformate ist. Eine Zeichenfolge gibt an, dass das Format nicht in Windows.h (privat) definiert ist. In diesem Fall ist das lesbare und schreibbare Format CF \_ OUTLINE (privat).

Der *rformat-Wert* gibt das Dateiformat an, das eine Anwendung lesen kann (aus konvertieren).

Der *rwformat-Wert* gibt das Dateiformat an, das eine Anwendung lesen und schreiben kann (aktivieren als).

 

 




